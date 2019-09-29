## Cache is king - Molly Struve

tw - @molly_struve

Decrease # of datastore hits

Kenna security
- MySQL source of Truth, the index on elastic search. Then serialization.

Were using active model serializing (rails)
Less db calls. Gropu little calls into a bigger one. Bulk serialization. 

Bulk serialization decreased significantly db calls and CPU usage. Process in bulk is more efficient.

They transferred load from MySQL to Redis

- Redis.
Hash cache in Ruby is faster than Redis, try to reduce Redis get requests with it.

Tried

Active record Base.Connection
Talk to local active record connection. Prefer local cache.

- Avoid db hits

.none method, scopes

Logging for debug. Read logs. Check if libraries are hitting data store. 


- resque workers

They limited number of workers per db. 
Workers requests were overwhelming Redis.
They removed throttling.

**Remove datastore hits you don't need.**