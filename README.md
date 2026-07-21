# 26H2 host

Static GitHub Pages host. The only deployable is `index.html` — an encrypted,
password-gated single file.

Maintenance rules:

- Never commit unencrypted builds or the access code (see `.gitignore`).
- All edits happen in the offline source kit; rebuild there and replace
  `index.html` with the freshly built protected file only.
- `index.html` must keep its `noindex,nofollow` meta and make no external
  requests beyond the youtube-nocookie embed.
- After every rebuild: decrypt round-trip, plaintext-leak grep, and a local
  gate test before pushing.
