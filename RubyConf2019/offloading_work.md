## High availability by offloading work - background jobs, message queues or kafka - Kerstin Puschke
tw - @titanoboa42

Works at Shopify

Approaches to offload work
- High availability. 
    
    Meaningful interactions with community of users. Available whenever needed.

- Background jobs

    - Resque, sidekiq
    - Work to be done later
    - Message queue for asynchronous communication (broker)
    - Paralelization
    - Retries
    - Idempotent jobs and at least one delivery
    - Transactional queueing
    - SAGA pattern

    github.com/shopify/job-iteration 

- Message oriented

    Is in middleware
    - Commands and events: propagating updates
    - No single source of truth
    - Decoupling microservices

- Event log
    - Kafka
    - Stateless broker
    - Based on shared log
    - Single source of Truth
    - For high throughput apps