# h2c-provider-caddy

Caddy reverse proxy provider for [helmfile2compose](https://github.com/helmfile2compose/helmfile2compose) — converts Ingress manifests into a Caddy compose service and generates a Caddyfile.

**The Gatekeeper** — one of the Seven Bishops, the founding extensions of the helmfile2compose distribution.

## Type

`IngressProvider` (priority 900)

## Kinds

- `Ingress` (inherited from IngressProvider)

## Configuration

Extension config in `helmfile2compose.yaml`:

```yaml
extensions:
  caddy:
    email: admin@example.com      # Caddy automatic HTTPS
    tls_internal: true            # force internal CA for all domains
```

## Note

This is a **build-time only** extension, designed to be concatenated by `build-distribution.py` into a single-file distribution. It uses internal core imports that are resolved at build time. It is **not** designed for runtime loading via `--extensions-dir`.

## Install

Listed in `distribution.json` — installed automatically when building a distribution via `h2c-manager`.
