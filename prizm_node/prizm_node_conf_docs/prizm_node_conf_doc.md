### Prizm Node Configuration
[Location directory](../../prizm_node/conf)

 1. [prizm.default.properties](../../prizm_node/conf/prizm.default.properties)
  - `line 61`
  ```yml
  myAddress=[External IP or Hostname with/without port]
  ```

  - `line 256`
  ```yml
  prizm.adminPassword=[Generate an admin password for executing protected API Requests]
  ```

 2. [logging-default.properties](.././prizm_node/conf/logging-default.properties)
  - Not necessary
