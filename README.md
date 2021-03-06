# mqttFleet
Home automation using MQTT

## Requirements
1. MQTT Broker
2. ESP866 boards

## MQTT Broker Options
* MQTT Lense MQTTLens Chrome extension allows you to run a local MQTT broker. Runs on port 1883 (Default port used by the broker).
* [Mosquitto Broker](https://mosquitto.org/download/)

If running brew on Mac OS
```
brew install mosquitoo
ln -sfv /usr/local/opt/mosquitto/*.plist ~/Library/LaunchAgents
launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mosquitto.plist
```

#### Subscribe to a topic
```
mosquitto_sub -t topic/state
```

##### Publish to a topic
```
mosquitto_pub -t topic/state -m "Hello World"
```
#### Check you IP on terminal
For Mac OS
```
ifconfig | grep "inet " | grep -Fv 127.0.0.1 | awk '{print $2}'
```

## Devices
1. IoT Button, trigger actions on the go.
