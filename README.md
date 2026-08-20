# Presence clients

This repository is the public integration boundary for Bohita Presence. It
contains the public contract today and may contain optional client helpers in
the future; the hosted iframe and private execution service live elsewhere.

## Available now

- **Hosted web client:** create a `surface.type: "web"` Session on a trusted
  server and assign its opaque `embed_url` directly to an iframe. The hosted
  document owns media, rendering, captions, expressions, artifacts, and
  reconnect behavior. No npm package is required.
- **Agent-readable integration fragment:**
  [`llms-fragment.txt`](./llms-fragment.txt) is the Presence portion Bohita
  publishes inside its canonical `llms.txt` after filling its release and
  support placeholders.

## Public contract

[`llms-fragment.txt`](./llms-fragment.txt) documents the current HTTP, hosted
embed, realtime voice, tools, events, artifact, privacy, and compatibility
contracts. Bohita publishes it with concrete API, release, changelog, status,
and support URLs. The hosted iframe implementation, private FastAPI adapters,
and infrastructure handoffs are not part of this repository.

Do not add private runtime URLs, implementation/model names, controller
credentials, or account secrets here. An account API key belongs on a server
or in a local development secret store, never in browser JavaScript.

Future JavaScript, Swift, and Android clients belong in separate subdirectories
here only when their public contracts and implementations are real. They may
wrap the hosted client or implement supported native lanes, but they should
not copy the remotely managed character renderer into application bundles.

## Releases and pinning

[`VERSION`](./VERSION) identifies the public contract release prepared by this
checkout. Stable releases use annotated Git tags such as `v0.1.0`; tags are
immutable by policy. Pin a tag for a human-readable dependency and its exact
commit SHA when a build must be reproducible.

The repository release is distinct from `/v1` HTTP compatibility, the
`bohita.embed.v1` and `bohita.realtime.v1` protocols, and an authored
Presence's integer version. The hosted iframe remains centrally managed and is
not pinned by customer applications.
