# Traefik and MQTT Broker

This is a playground to test how [traefik](https://containo.us/traefik/) on different versions can be successfully configured to:

- Redirect MQTT connection over TCP to a [Mosquitto MQTT Broker](https://mosquitto.org/)
- Redirect MQTT connection over websocket to a [Mosquitto MQTT Broker](https://mosquitto.org/)

## Manual Test

- TCP connection tested using [MQTT.fx](https://mqttfx.jensd.de/) by connecting to port **HOSTIP**:1883
- Websocket connection test using [HIVEMQ Websocket Client](http://www.hivemq.com/demos/websocket-client/) by connecting to port **HOSTIP**:80

## Result

| Traefik Version  | TCP | Websocket |
|------------------|-----|-----------|
| 1.7.14 | Unsupported | Successful  |
| 2.1.6  | Successful | [Failed](https://community.containo.us/t/traefik-v2-and-mqtt-broker-tcp-and-websocket-connections-error-502-bad-gateway-caused-by-eof/4865) |

## Future

- SSL support by Let's encrypt
