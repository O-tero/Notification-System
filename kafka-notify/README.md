# Kafka

- Kafka is an “event broker” — a system that controls and handles events or messages between various applications or services.
  It can handle massive daily event volumes as a distributed event streaming platform, guaranteeing that data is seamlessly transported and analyzed in real time.

Kafka’s core components ⚙️
Now that you’ve been acquainted with Kafka, let’s dive into the main elements that make up its architecture:

*Events*
An event records the fact that “something happened”. It can be thought of as a message or a piece of data representing a change or an action. In the context of our real-time notification system, you could consider an event as follows:

Event key: “1” (representing the user ID for Emma)
Event value: “Bruno started following you.”

*Brokers*
A Kafka broker is a server that runs the Kafka software and stores data. While large-scale production setups often involve multiple brokers across several machines, you’ll use a single broker setup for this tutorial.

*Topics*
Topics in Kafka are similar to folders in a filesystem. They represent categories under which data or events are stored. For instance, an example topic name could be "notifications".

*Producers*
Producers are entities that publish (write) or send messages to Kafka, such as a Go program or a service. When a producer has an event to send, it chooses a topic to address the event to.

*Consumers*
Consumers read and process events or messages from Kafka. After producers send messages to topics, consumers can subscribe to one or more topics to receive the messages.

*Partitions*
Each topic in Kafka can be further divided into partitions. Think of partitions as segments within a topic that enable Kafka to manage data more efficiently, especially in setups with multiple brokers.


*Consumer groups*
A consumer group consists of multiple consumers collaboratively processing messages from different partitions of a topic. This ensures that each message from a partition is processed by just one consumer in the group, allowing for efficient and scalable consumption.

*Replicas*
Replication ensures data safety. In larger Kafka deployments, storing multiple data replicas is common to help recover from unexpected failures.

