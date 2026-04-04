Tech stack:
- Scala: https://docs.scala-lang.org/
- Redis: https://redis.io/docs/latest/
- PostgreSQL: https://www.postgresql.org/docs/
- snabbdom: https://github.com/snabbdom/snabbdom
- Typescript: https://www.typescriptlang.org/docs/
- Sass: https://sass-lang.com/documentation/

Scala:
- Strongly typed
- Decent support for functional programming
- Scales in complexity
- Runs on the JVM and benefits from the Java ecosystem
- Play Framework SHOULD be replaced with smaller idependent libraries that we can swap as needed.

PostgreSQL:
- Serves tens of thousand of queries per second
- Fast, compresses the data
- Replicates seamlessly for redundancy and data safety
- Released under open-source license

Redis:
- Communicates between services
- WebSocket servers saves events into a Redis cache

Typescript:
- Easy refactoring and maintenance
- Compiler do heavy lifting

Snabbdom:
- Focuses on simplicity
- Comes with only Virtual DOM and nothing else
- Extra functionalities can be opted into by adding modules

Architecture
- Can be described as a monolith with satellites
- Main server is a massive monolith service
- Smaller services are split into separate servers
- Main server is a monolith because all the state is in one place, and can be cached in-heap for all modules of the site to use. Which makes it very efficient and quick at runtime. Everything compiles as a single unit, which ensures the entire site is coherent and free of incompatibilities