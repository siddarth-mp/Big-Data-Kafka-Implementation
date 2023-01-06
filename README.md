# Big-Data-Kafka-Implementation

In the above mentioned project , we as a team have implemented the actual working of Kafka environment, without actually making use of built-in available modules of kafka , but have developed inturn some of modules like zookeeper, broker, and simulated the environment of kafka working which is a producer-consumer messaging system
Repo created programmatically. Project Title: Yet another Kafka (YaK)

First run Zookeeper.py where it will allocate and run a leader broker.

Messages and topic sent through producer.html (multiple producers can be made to run).

From the appropriate leader broker messages sent to RabbitMQ

Topic directory is created for each topic within the respective leader broker directory to store message

If a leader breaks down , Zookeeper allocates a new leader by round robin algorithm

Every broker maintains a log where the leader broker updates the log which is replicated in all broker logs

Finally consumer.py is run with topic name as first argument and if flag --from-beginning is used then fetches all messages of that topic from log and if flag --from-producer is used then only fetches messages from the time of running the consumer.
