Contracts in Clojure - The Best-Yet Compromise Between Types and Tests

Prismatic Schema - https://github.com/Prismatic/schema

How do we know our code works?
 - Informal Reasoning
   * Does not scale outside our heads
 - Formal Proofs
   * Type systems are proofs by the compiler
 - Experimental Evidence
   * Tests
   
Experiments and Formal Proofs remove bagage so that we can free up more of our mind for informal reasoning.
Types are like a skeleton. Clojure data being all hash maps make it hard to know what the shape of the data is.

Schema
```clojure
(def Event {:when DateTime
            :what Incident
            :who Customer})
            
(s/defn fetch-events :- [Event]
  [params]
  ...)
```

What do we know from Schema?
 - Data shape
 - Data value bounderies
 - Relationships within values
 

