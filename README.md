# nice-code

**Public issue tracker & discussion hub for [nice-code](https://nicecode.io).**

The nice-code source lives in a private repository. This repo exists so that users of the
published packages have a public place to **report bugs, request features, ask questions, and
discuss the project**. There is no source code here — just the tracker.

- 🌐 **Website / docs:** https://nicecode.io
- 🐛 **Report a bug or request a feature:** [open an issue](../../issues/new/choose)

---

## 🤖 For AI coding assistants (`llms.txt`)

Point your AI coding assistant at these files for accurate, up-to-date context on the
libraries. Each is a plain-text concatenation of the relevant documentation.

- **[llms.txt](https://nicecode.io/llms.txt)** — full documentation, every package in one file. Best when you're using several packages or want the complete API surface.

Using only one package? Point your agent at the per-module file instead:

- **[llms-action.txt](https://nicecode.io/llms-action.txt)** — `@nice-code/action`
- **[llms-error.txt](https://nicecode.io/llms-error.txt)** — `@nice-code/error`
- **[llms-state.txt](https://nicecode.io/llms-state.txt)** — `@nice-code/state`
- **[llms-util.txt](https://nicecode.io/llms-util.txt)** — `@nice-code/util`
- **[llms-common-errors.txt](https://nicecode.io/llms-common-errors.txt)** — `@nice-code/common-errors`
- **[llms-realm.txt](https://nicecode.io/llms-realm.txt)** — `@nice-code/realm`

---

## What is nice-code?

A collection of TypeScript libraries for building reliable, type-safe applications. The
packages are published on npm under the [`@nice-code`](https://www.npmjs.com/org/nice-code)
scope and remain **freely available** — only the source repository has been closed for now.

### Core libraries

| Package | What it does |
| --- | --- |
| [`@nice-code/error`](https://www.npmjs.com/package/@nice-code/error) | Typed, serializable errors with domain hierarchies, pattern matching, and safe transport across API boundaries. |
| [`@nice-code/action`](https://www.npmjs.com/package/@nice-code/action) | Typed, transport-agnostic action system for calling functions across client/server boundaries — including bi-directional calls over a single WebSocket, with first-class Cloudflare Worker → Durable Object routing. |
| [`@nice-code/realm`](https://www.npmjs.com/package/@nice-code/realm) | Schema-defined, authoritative shared-state engine — many clients observe (and optimistically write) one server-owned state tree over a binary patch protocol, riding your app's single secure connection. |
| [`@nice-code/state`](https://www.npmjs.com/package/@nice-code/state) | Framework-agnostic, Immer-backed state container with fine-grained selector subscriptions, derived reactions, patch streams, and a React adapter + devtools. |
| [`@nice-code/wire`](https://www.npmjs.com/package/@nice-code/wire) | The connectivity backbone of the stack: dialing + transport fallback, the authenticated/encrypted handshake, secure sessions, reconnection, hibernation, keepalive, and the frame-protocol multiplex that lets several protocols share one connection. |
| [`@nice-code/util`](https://www.npmjs.com/package/@nice-code/util) | Typed storage adapters (browser, Cloudflare Durable Objects, in-memory) and WebCrypto utilities (Ed25519 signing, X25519 key exchange, AES-GCM encryption). |
| [`@nice-code/common-errors`](https://www.npmjs.com/package/@nice-code/common-errors) | Shared validation error domain and Hono middleware for Standard Schema validation. |

### Devtools

| Package | What it does |
| --- | --- |
| [`@nice-code/devtools`](https://www.npmjs.com/package/@nice-code/devtools) | One-call devtools for nice-code — actions, state, realms, wire traffic, and a live topology of your frontends and backends, in a standalone window, from one function call per runtime (browser, server, or Durable Object). |
| [`@nice-code/devtools-vite`](https://www.npmjs.com/package/@nice-code/devtools-vite) | Vite dev-server plugin that makes opening the devtools the entire setup — the local relay starts itself on first use and every client of the app joins the same devtools window. |
| [`@nice-code/devtools-relay`](https://www.npmjs.com/package/@nice-code/devtools-relay) | A tiny, reusable WebSocket relay that lets the devtools span browser storage partitions — a private window, another profile, another browser, even another device. |
| [`@nice-code/devtools-core`](https://www.npmjs.com/package/@nice-code/devtools-core) | The framework-agnostic core the devtools panels, relay, and producers all build on, so a backend can stream telemetry to a devtools window without pulling in React. |

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
[private vulnerability reporting](../../security/advisories/new)

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
