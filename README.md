# nice-code

**Public issue tracker & discussion hub for [nice-code](https://nicecode.io).**

The nice-code source lives in a private repository. This repo exists so that users of the
published packages have a public place to **report bugs, request features, ask questions, and
discuss the project**. There is no source code here — just the tracker.

- 🌐 **Website / docs:** https://nicecode.io
- 🐛 **Report a bug or request a feature:** [open an issue](../../issues/new/choose)
- 💬 **Ask a question or start a discussion:** [Discussions](../../discussions) *(if enabled)*

---

## What is nice-code?

A collection of TypeScript libraries for building reliable, type-safe applications. The
packages are published on npm under the [`@nice-code`](https://www.npmjs.com/org/nice-code)
scope and remain **freely available** — only the source repository has been closed for now.

| Package | What it does |
| --- | --- |
| [`@nice-code/error`](https://www.npmjs.com/package/@nice-code/error) | Typed, serializable errors with domain hierarchies, pattern matching, and safe transport across API boundaries. |
| [`@nice-code/action`](https://www.npmjs.com/package/@nice-code/action) | Typed, transport-agnostic action system for calling functions across client/server boundaries — including bi-directional calls over a single WebSocket, with first-class Cloudflare Worker → Durable Object routing. |
| [`@nice-code/state`](https://www.npmjs.com/package/@nice-code/state) | Framework-agnostic, Immer-backed state container with fine-grained selector subscriptions, derived reactions, patch streams, and a React adapter + devtools. |
| [`@nice-code/common-errors`](https://www.npmjs.com/package/@nice-code/common-errors) | Shared validation error domain and Hono middleware for Standard Schema validation. |
| [`@nice-code/util`](https://www.npmjs.com/package/@nice-code/util) | Typed storage adapters (browser, Cloudflare Durable Objects, in-memory) and WebCrypto utilities (Ed25519 signing, X25519 key exchange, AES-GCM encryption). |

Full documentation for every package is at **https://nicecode.io**.

---

## Reporting an issue

Good bug reports get fixed faster. Please include:

1. **Which package** and the **version** you're on (e.g. `@nice-code/action@0.55.0`).
2. **What you expected** to happen vs. **what actually happened**.
3. A **minimal reproduction** — the smallest snippet, repo, or steps that trigger it.
4. Your **environment**: runtime (Node / Bun / browser / React Native / Cloudflare Workers),
   OS, and relevant tooling versions (TypeScript, bundler, etc.).
5. Any **error output**, stack traces, or logs.

Before opening a new issue, please **search existing issues** — someone may have already
reported it, and adding a 👍 or a comment with your details helps us prioritize.

## Feature requests

Feature requests are welcome. Describe the **use case** and the problem you're trying to solve,
not just the proposed solution — it helps us find the best fit across the libraries.

## Security

**Please do not report security vulnerabilities in public issues.** Instead, disclose them
privately by emailing the maintainer or using GitHub's
[private vulnerability reporting](../../security/advisories/new) *(if enabled)*.

---

## FAQ

**Is nice-code still maintained?**
Yes. The published packages are actively maintained; only the source repository has been made
private for now. This repo is how we stay in touch with users.

**Can I still use the packages?**
Absolutely — they're published on npm and free to install and use as before.

**Will the source be reopened?**
Possibly in the future. There are no guarantees at this stage.

---

Maintained by [@lostpebble](https://github.com/lostpebble). Thanks for using nice-code! 🙂
