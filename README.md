# SDM120_Homeassistant
SDM120 WEMOS_D1_MINI NODEMCU RS485

See wiki https://github.com/jarcikw/SDM120_Homeassistant/wiki/SDM120-&-nodemcu-&-RS485-wiring

example Home Assistant sensor configuration

  - platform: mqtt
    name: "PIEKARNIK_VOLTAGE"
    state_topic: "tele/SDM120_PIEKARNIK/SENSOR"
    value_template: "{{ value_json['ENERGY'].Voltage }}"
    unit_of_measurement: 'V'
  - platform: mqtt
    name: "PIEKARNIK_CURRENT"
    state_topic: "tele/SDM120_PIEKARNIK/SENSOR"
    value_template: "{{ value_json['ENERGY'].Current }}"
    unit_of_measurement: 'A'
  - platform: mqtt
    name: "PIEKARNIK_FREQ"
    state_topic: "tele/SDM120_PIEKARNIK/SENSOR"
    value_template: "{{ value_json['ENERGY'].Frequency }}"
    unit_of_measurement: 'Hz'
  - platform: mqtt
    name: "PIEKARNIK_FACTOR"
    state_topic: "tele/SDM120_PIEKARNIK/SENSOR"
    value_template: "{{ value_json['ENERGY'].Factor }}"
  - platform: mqtt
    name: "PIEKARNIK_TOTAL_POW"
    state_topic: "tele/SDM120_PIEKARNIK/SENSOR"
    value_template: "{{ value_json['ENERGY'].Total }}"
    unit_of_measurement: 'kWh'
  - platform: mqtt
    name: "PIEKARNIK_ACTIVE_POW"
    state_topic: "tele/SDM120_PIEKARNIK/SENSOR"
    value_template: "{{ value_json['ENERGY'].ActivePower }}"
    unit_of_measurement: 'W'
  - platform: mqtt
    name: "PIEKARNIK_APPARENT_POW"
    state_topic: "tele/SDM120_PIEKARNIK/SENSOR"
    value_template: "{{ value_json['ENERGY'].ApparentPower }}"
    unit_of_measurement: 'W'
