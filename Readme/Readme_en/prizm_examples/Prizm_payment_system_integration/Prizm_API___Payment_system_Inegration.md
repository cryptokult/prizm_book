### Prizm API - Payment system Inegration into your project

[Original source](https://pzm.space/en/pzm-integration/)

#### Prizm payment system integration

PRIZM payment system is the easiest way to receive and send crypto payments.

- Description
- PHP implementation example
- The basic principle of work
- Function Example


To begin working with PRIZM you will need to launch the [network node (Node)](https://github.com/prizmspace/PrizmCore#prizmcore-wallet-download-v11044-windows-osx-linux) and [API_Servlet](https://github.com/prizmspace/PrizmCore#easy-api-gateway-prizmapiservlet-1104).

#### Guidelines:
- [Prizm Core on Linux](https://pzm.space/en/prizm-forging)
- [Prizm Core Windows | MacOSX](https://pzm.space/en/prizm-forging)

##### Network node
- [Prizm Core](https://github.com/prizmspace/PrizmCore#prizmcore-wallet-download-v11044-windows-osx-linux)
- [Easy API Gateway](https://github.com/prizmspace/PrizmCore#easy-api-gateway-prizmapiservlet-1104)
- [Prizm API Doc](http://blockchain.prizm.space/api-doc/PRIZM_API.html)

The software can run on one server as well as on different servers. However it's better to launch it on the one for your convenience.


Firstly, you should launch the node and wait while it syncs. The next step is configuration of the PrizmAPIServlet module.


Inside the archive there is a file called PrizmAPIServlet.properties


in the line passphrase: NONE

instead of NONE you should write the private key of the wallet that will be used by your project.

in the line sendkey: NONE

instead of NONE you should write the password (it will be used by the function of coin sending as an additional protection from unauthorized transactions).


After you have filled in the fields, you should launch the servlet through
run-servlet.sh

#### The example of implementation in PHP

The description of work with receiving and sending coins, with examples of ready-made functions and description of the principles of work. The Mysql database is used to store the transaction list, there is a dump of the storage table below, along with examples of code to work with the table (if you apply QueryBuilder, it won't be a problem).

##### The main principle of work:

There is a script in the Cron-task that makes a request to the servlet every 2-5 minutes so it could receive new transactions on the wallet of the store. Having received the list of transactions, you should save them to the local database. If there are no operations in the database, you should run the command without any parameter. However if you wish to receive new transactions, you should send the number of the last transaction that you have as a parameter.


##### The example of the function:
```php
<?php
function historyPZM($last_id = 0)
{
	if ($last_id) {
		$url = 'http://localhost:8888/history?fromid=' . $last_id;
	} else {
		$url = 'http://localhost:8888/history';
	}
	$page = '';
	$result = get_web_page($url);
	if (($result['errno'] != 0) || ($result['http_code'] != 200)) {
		$error = $result['errmsg'];
	} else {
		$page = $result['content'];
	}
	$array_new = array();
	$xcmorewrite = explode("\n", str_replace("\r", '', $page));
	foreach ($xcmorewrite as $value) {
		if ($value) {
			$array_new[] = explode(";", $value);
		}
	}
	return $array_new;
}

?>
```

##### The function for retrieving page content:
```php
<?php

function get_web_page($url)
{
	$uagent = "Opera/9.80 (Windows NT 6.1; WOW64) Presto/2.12.388 Version/12.14";
	$ch = curl_init($url);
	curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1); // recovers the web page         
           curl_setopt($ch, CURLOPT_HEADER, 0); // doesn’t recover headers   
           curl_setopt($ch, CURLOPT_FOLLOWLOCATION, 1); // follows redirects
           curl_setopt($ch, CURLOPT_ENCODING, ""); // handles all encodings
          curl_setopt($ch, CURLOPT_USERAGENT, $uagent); // useragent
          curl_setopt($ch, CURLOPT_CONNECTTIMEOUT, 20); // time-out of the connection   
          curl_setopt($ch, CURLOPT_TIMEOUT, 20); // time-out of the answer
          curl_setopt($ch, CURLOPT_MAXREDIRS, 2); // stops after the 10th redirect

           $content = curl_exec($ch);
	$err = curl_errno($ch);
	$errmsg = curl_error($ch);
	$header = curl_getinfo($ch);
	curl_close($ch);

	$header['errno'] = $err;
	$header['errmsg'] = $errmsg;
	$header['content'] = $content;
	return $header;
}

?>

You can test it through the console, for example: curl http://localhost:8888/history

The example of the Cron-task handler script for receiving new transactions and the table structure

CREATE TABLE `pzm_history` (
  `id` bigint(20) NOT NULL,
  `tarif_id` int(1) NOT NULL,
  `tr_id` varchar(255) NOT NULL,
  `tr_date` varchar(255) NOT NULL,
  `tr_timestamp` int(11) NOT NULL,
  `pzm` varchar(50) NOT NULL,
  `summa` decimal(16,2) NOT NULL,
  `mess` varchar(255) NOT NULL,
  `status` int(1) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;


* All necessary keys and autoincrement for ID should be added to the table

Handler:

<?php

$nomer = getLastPrmHistory();
$historys = historyPZM($nomer);

foreach ($historys as $item) {
    if ($item['0'] != "No transactions!") {


// this line adds data to the ‘pzm_history’ table using INSERT IGNORE


PzmHistory::find()->insertIgnore([
            'tr_id' => $item['0'],
            'tr_date' => $item['1'],
            'tr_timestamp' => $item['2'],
            'pzm' => $item['3'],
            'summa' => $item['4'],
            'mess' => $item['5'],
            'status' => 0
        ]);
    }
}


function getLastPrmHistory()
{

// this line searches for the last row in the table to get the last ID of the transactions which are in the table

if (!empty($pzmHistory = PzmHistory::find()->orderBy('id', "DESC")->first())) {
		return $pzmHistory->tr_id;            
	};
	return 0;
}

?>
```

In this example you receive the list of new transactions that should be saved to the local database.


Therefore, you keep a history of all transactions on the wallet and in the future you will search for them in our local database using key data.


Your project must work with the same Prizm Wallet, that is why all clients will be given the same requisites to replenish the internal account and the same hash ID of the operation. Be sure to inform the client that he must make a transaction strictly on the requisites indicating the hash identifier in the payment comment.

Thus, there should be another process that will analyze new incoming transactions and deposit coins to the internal account if the payment comment has a hash identifier of the client. Also you need to make a separate "I PAID" button for the client which could search and record new transactions for this user after making click on it.

##### Secondary functions and functions of coin sending
Getting public key for the wallet (works only for activated wallets having balance).

```php
<?php

	function destinationPZM($pzm)
    {
        $url = 'http://localhost:8888/publickey?destination=' . $pzm;
        $page = '';
        $result = get_web_page($url);
        if (($result['errno'] != 0) || ($result['http_code'] != 200)) {
            $error = $result['errmsg'];
            return '';
        } else {
            $page = $result['content'];
            $haystack = "Public key absent";
            $haystack2 = "Send error!";
            $pos = strripos($page, $haystack);
            $pos2 = strripos($page, $haystack2);
            if ($pos === false AND $pos2 === false) {
                $xcmorewrite = explode(' ', $page);
                $page = trim($xcmorewrite[0]);
                return $page;
            } else {
                return '';
            }
        }
        return $page;
    }

?>
```

##### Receiving current balance of the wallet:

```php
<?php

	function getBalancePZM($pzm)
    {
        $ip = '*******';  // пример 192.168.1.1:9976  with port
		$url = 'http://'.$ip.'/prizm?requestType=getAccount&account=' . $pzm;
        $page = '';
        $result = get_web_page($url);
		//print_r($result); die;
        if (($result['errno'] != 0) || ($result['http_code'] != 200)) {
            $error = $result['errmsg'];
            return '';
        } else {
            $page = $result['content'];
            $page = json_decode($page, true);
            if ( isset($page['balanceNQT']) ) {
              return $page['balanceNQT'] / 100;
            } else {
              return 0;
            }
        }
    }

?>
```

##### Method of coin sending:

```php
<?php

public function payPZM($summa, $pzm, $public_key, $text)
{
	$p2 = SENDKEY;   //  this is the password that you specified during setup
	$return = false;
	$url = 'http://localhost:8888/send?sendkey=' . $p2 . '&amount=' . $summa . '&comment=' . urlencode($text) . '&destination=' . $pzm . '&publickey=' . $public_key;
	$page = '';
	$result = get_web_page($url);

	if (($result['errno'] != 0) || ($result['http_code'] != 200)) {
		$error = $result['errmsg'];
	} else {
		$page = $result['content'];
	}

	if (preg_match('/^\+?\d+$/', $page)) {
		$return = true;
	} else {
		$return = false;
	}
	return $return;
}

?>
```
