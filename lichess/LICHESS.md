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

Developer mindset:
- With each new line of code, we're adding maintenance burden for the years to come. Compatibility with the rest of the site, with things like mobile apps. Migrations through new libraries and language versions. Refactoring of the code itself. Redesigning the UI it is a part of.

- The new line of code will need to be revisited many times, adding time and risk to every code modification that affects it.

- Adding new feature is quick and fun. Maintaining it over the years is the real work.

- Lines of code are not valuable. They are a cost, that is not paid while writing them, but while maintaining them. Sometimes years later. And they pile up.

- Adding lines of code to a program is like adding weight to a plane. It better be worth it.

- I didn't shy away from changing the parts of the stack that I didn't like.

- Even when it took weeks or months. It's one of the props of a project led by its developer. There was no-one to tell me that something is more important than clearing the tech debt.