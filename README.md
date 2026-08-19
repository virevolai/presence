# Presence clients

This repository is the public-client boundary for Bohita Presence. It contains
only public integration contracts and client-side helpers; the private
execution service lives elsewhere.

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
