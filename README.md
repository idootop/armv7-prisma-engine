# armv7-prisma-engine

Building Prisma Engine for ARMv7

# Usage

1. Require `prisma >= 5.0.0`
1. Download engine files from the [release](https://github.com/idootop/armv7-prisma-engine) page
1. Update the environment variables for your projects

```shell
PRISMA_QUERY_ENGINE_BINARY=path/to/query-engine
PRISMA_SCHEMA_ENGINE_BINARY=path/to/schema-engine
```

Test your environment variable:

```shell
npx prisma -v
```

Learn more: https://www.prisma.io/docs/orm/more/under-the-hood/engines

# Reference

- https://github.com/prisma/prisma-engines
- https://github.com/ImBIOS/prisma-armv7-builds
