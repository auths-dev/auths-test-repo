# Auths Test Repo

[![Verified with Auths](https://img.shields.io/badge/verified-auths-brightgreen)](https://auths.dev)

This repository demonstrates [Auths](https://github.com/auths-dev/auths) — decentralized commit signing and artifact verification.

## What's here

- **Signed commits** — Every commit is signed with an Auths cryptographic identity
- **Artifact attestation** — `hello.tar.gz` is signed with `hello.tar.gz.auths.json`
- **CI verification** — GitHub Action verifies signatures on every push

## Verify locally

```bash
# Install Auths
brew install auths-dev/tap/auths

# Clone and verify
git clone https://github.com/auths-dev/auths-test-repo.git
cd auths-test-repo
auths verify HEAD
```

## Verify the artifact

```bash
auths artifact verify hello.tar.gz
```

## Inline verification widget

Add this to any HTML page:

```html
<script type="module" src="https://unpkg.com/@auths-dev/verify@0.3.0/dist/auths-verify.mjs"></script>
<auths-verify repo="https://github.com/auths-dev/auths-test-repo"></auths-verify>
```

## Learn more

- [Auths CLI](https://github.com/auths-dev/auths) — The CLI tool
- [Quickstart](https://auths.dev/docs/quickstart) — Get started in 5 minutes
- [GitHub Action](https://github.com/marketplace/actions/auths-verify) — CI verification
