## Building a customer facing analytics platform - Laura Kirbu

App with massive data generation. Every second they have more data.

Exploring solutions for organization and storage:
- Redis and MySQL
- Redis is key value store and requires several queries to get the data that you want.
- MySQL. Tables will get really big and queries will time out.

Solution: Kafka.

- Separates data by topic
- Allows pararell processing


Spark allows to stream and modify data and then they send it to Kafka.

Tables built on specific queries.

Partition tables based on timestamp to make queries faster.


Ruby Kafka

Cassandra                                       


Tech stack:

Spark, Rails, Kafka, Fenix and Elexir.