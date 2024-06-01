FROM multiarch/qemu-user-static:x86_64-arm as qemu
FROM arm32v7/node:18
COPY --from=qemu /usr/bin/qemu-arm-static /usr/bin

WORKDIR /app

COPY . .

RUN chmod +x query-engine
RUN chmod +x libquery_engine.so.node
RUN chmod +x schema-engine

ENV PRISMA_ENGINES_CHECKSUM_IGNORE_MISSING=1
ENV PRISMA_QUERY_ENGINE_BINARY=query-engine
ENV PRISMA_QUERY_ENGINE_LIBRARY=libquery_engine.so.node
ENV PRISMA_SCHEMA_ENGINE_BINARY=schema-engine

RUN --mount=type=cache,target=/root/.npm \
    npm install -g prisma

CMD uname -a && npx prisma -v