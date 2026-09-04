# Presence client changelog

## Unreleased

## 0.1.2 - 2026-09-04

- Improved the concise product description around visual awareness,
  interruptibility, asynchronous tools, and authorized retained outcomes.
- Added the required local HTTP-serving step so a `file://` test does not
  appear as a blank broken embed.
- Documented the required `Idempotency-Key` on explicit Session end and the
  deployed typed HTTP error envelope.
- Made the zero-authoring path explicit: omitting `presence_id` selects
  Bohita's camera-required visual demo, while authored Presences retain their
  published camera policy.
- Reduced the first Session request to `external_id` and `surface`; managed
  startup remains the default.
- Clarified reusable Presence authoring and the opaque, Think-only knowledge
  retrieval boundary.
- Documented compiled cross-surface retention policy and the authorized
  Session output manifest.

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
