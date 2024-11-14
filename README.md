# home-assistant-node-red-km200

This node-red flow will read all data available from the original Buderus/Bosch API.
All enties read are then build in Home Assistant using MQTT discovery.

Aditionally energy consumption data for last 12 months can be loaded into the statistic database when MariaDb DB is used.
Energy consumption for heating and warm water consumption is then available with the energy dashboard.


Node-Red Config: Add 4 npm packages: rijndael-js, crypto, axios, mysql2
![alt text](image.png)



Node-red settings:  /addon_configs/a0d7b954_nodered/settings.js
add :
  functionGlobalContext: {
    rijndael:require("rijndael-js"),
    crypto:require("crypto"),
    axios:require("axios"),
    mysql2:require("mysql2/promise"),
    // os:require('os'),
  },

