# tags-pub Helm Chart

This chart deploys `ghcr.io/social-web-foundation/tags.pub`.

## Required values

- `env.DATABASE_URL`: Sequelize URL (`postgres`, `sqlite`, or `mysql`)
- `env.ORIGIN`: Public origin URL, e.g. `https://example.com`

## Defaults

- `env.PORT`: `"9000"`
- `env.LOG_LEVEL`: `"info"`

## Install

```bash
helm install tags-pub . \
  --set env.DATABASE_URL='postgres://user:pass@db:5432/tags' \
  --set env.ORIGIN='https://example.com'
```

## Upgrade

```bash
helm upgrade tags-pub . --install \
  --set env.DATABASE_URL='postgres://user:pass@db:5432/tags' \
  --set env.ORIGIN='https://example.com'
```
