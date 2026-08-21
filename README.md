# Spctre schema registry

Published schema artifacts for [Spctre](https://github.com/getspctre/spctre): versioned JSON Schema documents and the OpenAPI 3.1 specification for the public API.

> **Status: live.** The registry is published at [`https://schema.spctre.dev`](https://schema.spctre.dev). Consumers may use its versioned artifacts and root [`manifest.json`](https://schema.spctre.dev/manifest.json).

## This content is generated

Every document here is emitted from source in [`getspctre/spctre`](https://github.com/getspctre/spctre) under `packages/api-contracts`, and published from there by an automated workflow.

**Do not edit these files by hand.** Hand edits are overwritten on the next publish, and they break the SHA-256 digests recorded in `manifest.json`. To change a schema, change its source in the upstream repository.

## Layout

Artifacts are addressed by domain, name, and version:

```
/<domain>/<name>/<version>.json
```

`manifest.json` at the root is the index: it lists every published artifact with its id, title, description, URL, and SHA-256 digest.

## Versioning and immutability

A published version is intended to be immutable. A breaking change to a contract is published as a **new version** rather than as an edit to an existing document, so a consumer that pins a version keeps getting the bytes it validated against.

Immutability here is procedural — enforced by the publishing pipeline and by this repository's history — rather than by write-once storage.

## Licence

Apache-2.0. See [LICENSE](./LICENSE).
