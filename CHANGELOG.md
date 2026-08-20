# Presence client changelog

## Unreleased

- The hosted web client is deployed. Web sessions return an opaque
  `embed_url` that loads the complete Presence-owned runtime.

## 0.1.0 - 2026-08-19

- Added the hosted iframe integration contract.
- Added `bohita.embed.v1` application-readiness guidance.
- Added agent-readable web, voice, meeting, phone, tools, events, privacy, and
  compatibility guidance.
- Clarified that recording preference does not itself authorize retention.
- Clarified that Bohita stores tool and lifecycle webhook destinations
  server-side; the live Presence runtime does not receive their URLs or secrets.
- Defined shared terminal Session states across web, voice, meeting, and phone.
