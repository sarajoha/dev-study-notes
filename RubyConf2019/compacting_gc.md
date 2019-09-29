## Compacting GC for MRI - Aaron Patterson

|> Pipeline operator, was reverted

Typed Ruby? 

Compact heap

- Ruby's heap
Copy on Write (CoW) 

Eliminating fragmentation

Malloc heap: jemalloc

Ruby's object heap: gc.compact

- compaction algorithm

Two finger compaction

- implementation details