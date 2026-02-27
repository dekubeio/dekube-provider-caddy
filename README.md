# dekube-provider-caddy

Caddy reverse proxy provider for [dekube](https://dekube.io) — converts Ingress manifests into a Caddy compose service and generates a Caddyfile.

**The Gatekeeper** — one of the Eight Monks, the founding extensions of the helmfile2compose distribution.

> Heresy level: 3/10 — conjures an entire service from thin air and writes its own config file. Moderate apostasy.

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

## Install

Via [dekube-manager](https://github.com/dekubeio/dekube-manager):

```sh
python3 dekube-manager.py caddy
```

Or listed in `distribution.json` — installed automatically when building a distribution.
