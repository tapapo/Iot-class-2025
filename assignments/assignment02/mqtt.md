# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
Enter QoS level (0, 1, 2): 2
[15:33:32] DEBUG | Sending PUBLISH (d0, q2, r0, m2), 'b'test/qos/6510301002/temperature'' (NULL payload)
[15:33:32] PUBLISH REQUESTED | QoS=2 | Message='' | msgid=2
Enter message to publish: [15:33:32] DEBUG | Received PUBREC (Mid: 2)
[15:33:32] DEBUG | Sending PUBREL (Mid: 2)
[15:33:32] DEBUG | Received PUBCOMP (Mid: 2)
[15:33:32] PUBLISHED | msgid=2
```

## Subscriber_qos.py Output

```
pop@MacBook-Air-khxng-Tosapat app % python3 subscriber_qos.py 
/Users/pop/Desktop/iot2025/Iot-class-2025-gateway/app/subscriber_qos.py:25: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[15:34:21] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[15:34:21] DEBUG | Received CONNACK (0, 0)
[15:34:21] Connected with result code 0
[15:34:21] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6510301002', 2)]
[15:34:21] DEBUG | Received SUBACK
```