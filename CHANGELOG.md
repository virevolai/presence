# Presence client changelog

## Unreleased

## 0.1.1 - 2026-09-02

- The hosted web client is deployed. Web sessions return an opaque
  `embed_url` that loads the complete Presence-owned runtime.
- Documented the public Session creation metadata: real idempotent `replayed`
  state, optional host-facing recording consent metadata, and no public
  `session_ref`.
- Clarified that callers use the admitted `max_seconds` returned for each
  Session; paid and demo policies may differ.
- Clarified that camera behavior belongs to the published Presence rather than
  adding another launch-time option.
- Synced bounded `restart_required` recovery guidance with the deployed hosted
  client.
- Separated the website's `llms-fragment.txt` publishing workflow from Bohita
  Infra's API/runtime implementation handoff.

## 0.1.0 - 2026-08-19

- Added the hosted iframe integration contract.
- Added `bohita.embed.v1` application-readiness guidance.
- Added agent-readable web, voice, meeting, phone, tools, events, privacy, and
  compatibility guidance.
- Clarified that recording preference does not itself authorize retention.
- Clarified that Bohita stores tool and lifecycle webhook destinations
  server-side; the live Presence runtime does not receive their URLs or secrets.
- Defined shared terminal Session states across web, voice, meeting, and phone.
