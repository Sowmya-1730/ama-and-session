# AMA Questions and Answers

## 1. What is the main purpose of exchange in RabbitMQ?

**Answer:** An Exchange receives messages from producers and routes them
to one or more queues based on routing rules. Producers never send
messages directly to queues.

## 2. What is persistent messages?

**Answer:** Persistent messages are messages marked to survive broker
restarts. They should be sent to durable queues to maximize durability.

## 3. What are the data types in Python?

**Answer:** Common built-in data types are:
- int
- float
- complex
- bool
- str
- list
- tuple
- set
- dict
- range
- bytes
- bytearray
- frozenset
- NoneType

## 4. How are we seeing the real time update of delivery man in any app?

**Answer:** Delivery apps use the driver's GPS to collect location data.
The mobile app sends coordinates to the server periodically, and
technologies like WebSockets or push updates deliver the latest location
to customers, which is displayed on map services such as Google Maps.
