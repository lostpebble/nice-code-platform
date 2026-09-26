# nice-code

**Public issue tracker & discussion hub for [nice-code](https://nicecode.io).**

The nice-code source lives in a private repository. This repo exists so that users of the
published packages have a public place to **report bugs, request features, ask questions, and
discuss the project**. There is no source code here — just the tracker.

- 🌐 **Website / docs:** https://nicecode.io
- 🎮 **Live demos:** [Tank Shooter](https://demo-tank-shooter.nicecode.io) · [Pixel Plaza](https://demo-pixel-plaza.nicecode.io) · [Playground](https://nice-code-demo.nicecode.io)
- 📜 **What changed in each release:** [changelog](https://nicecode.io/production/changelog/)
- 🐛 **Report a bug or request a feature:** [open an issue](../../issues/new/choose)

---

## 🤖 For AI coding assistants (`llms.txt`)

Point your AI coding assistant at these files for accurate, up-to-date context on the
libraries. Each is a plain-text concatenation of the relevant documentation, regenerated on
every docs build.

- **[llms.txt](https://nicecode.io/llms.txt)** — full documentation, every package in one file. Best when you're using several packages or want the complete API surface.

Using only one package? Point your agent at the per-module file instead:

- **[llms-wire.txt](https://nicecode.io/llms-wire.txt)** — `@nice-code/wire`
- **[llms-action.txt](https://nicecode.io/llms-action.txt)** — `@nice-code/action`
- **[llms-realm.txt](https://nicecode.io/llms-realm.txt)** — `@nice-code/realm`
- **[llms-error.txt](https://nicecode.io/llms-error.txt)** — `@nice-code/error`
- **[llms-state.txt](https://nicecode.io/llms-state.txt)** — `@nice-code/state`
- **[llms-util.txt](https://nicecode.io/llms-util.txt)** — `@nice-code/util`
- **[llms-common-errors.txt](https://nicecode.io/llms-common-errors.txt)** — `@nice-code/common-errors`
- **[llms-process.txt](https://nicecode.io/llms-process.txt)** — `@nice-code/process`
- **[llms-commander.txt](https://nicecode.io/llms-commander.txt)** — `@nice-code/commander`
- **[llms-devtools.txt](https://nicecode.io/llms-devtools.txt)** — `@nice-code/devtools` and the rest of the devtools suite (`-cli`, `-vite`, `-relay`)

---

## What is nice-code?

**One secure connection for your whole app.** nice-code is a set of TypeScript libraries: call
server functions with typed **actions**, share live, server-owned state with **realms**, and keep
errors typed from throw to catch. Actions and realms share one connection that reconnects itself,
and devtools are included.

The packages are published on npm under the [`@nice-code`](https://www.npmjs.com/org/nice-code)
scope and remain **freely available** — only the source repository has been closed for now.
Every package releases **in lockstep at one version**, so upgrade them together — see
[Stability & Versioning](https://nicecode.io/production/stability/).

Not sure which packages you need? Start at
[**What are you building?**](https://nicecode.io/getting-started/choosing/)

### Core libraries

| Package | What it does |
| --- | --- |
| [`@nice-code/wire`](https://www.npmjs.com/package/@nice-code/wire) | The connectivity backbone of the stack: dialing + transport fallback, the authenticated/encrypted handshake, secure sessions, reconnection, hibernation, keepalive, and the frame-protocol multiplex that lets several protocols share one connection. |
| [`@nice-code/action`](https://www.npmjs.com/package/@nice-code/action) | Typed, transport-agnostic action system for calling functions across client/server boundaries — including bi-directional calls over a single WebSocket, with first-class Cloudflare Worker → Durable Object routing. |
| [`@nice-code/realm`](https://www.npmjs.com/package/@nice-code/realm) | Schema-defined, authoritative shared-state engine — many clients observe (and optimistically write) one server-owned state tree over a binary patch protocol, riding your app's single secure connection. |
| [`@nice-code/error`](https://www.npmjs.com/package/@nice-code/error) | Typed, serializable errors with domain hierarchies, pattern matching, and safe transport across API boundaries. |
| [`@nice-code/state`](https://www.npmjs.com/package/@nice-code/state) | Framework-agnostic, Immer-backed state container with fine-grained selector subscriptions, derived reactions, patch streams, and a React adapter + devtools. |
| [`@nice-code/common-errors`](https://www.npmjs.com/package/@nice-code/common-errors) | Shared validation error domain and Hono middleware for Standard Schema validation. |
| [`@nice-code/util`](https://www.npmjs.com/package/@nice-code/util) | Typed storage adapters (browser, Cloudflare Durable Objects, in-memory) and WebCrypto utilities (Ed25519 signing, X25519 key exchange, AES-GCM encryption). |

### Devtools

| Package | What it does |
| --- | --- |
| [`@nice-code/devtools`](https://www.npmjs.com/package/@nice-code/devtools) | One-call devtools for nice-code — actions, state, realms, wire traffic, and a live topology of your frontends and backends, in a standalone window, from one function call per runtime (browser, server, or Durable Object). Inert in production. |
| [`@nice-code/devtools-cli`](https://www.npmjs.com/package/@nice-code/devtools-cli) | The devtools window without an app server: open it standalone, manage deployed relay sessions, and get the URL a staging deployment uses to join one — so you can inspect it live. |
| [`@nice-code/devtools-vite`](https://www.npmjs.com/package/@nice-code/devtools-vite) | Vite dev-server plugin — the zero-config path while developing locally. The relay starts itself on first use, and every client of the app joins the same devtools window. |
| [`@nice-code/devtools-relay`](https://www.npmjs.com/package/@nice-code/devtools-relay) | A tiny, reusable WebSocket relay that lets the devtools span browser storage partitions — a private window, another profile, another browser, even another device — plus token-authenticated sessions for inspecting deployed environments. |
| [`@nice-code/devtools-core`](https://www.npmjs.com/package/@nice-code/devtools-core) | The framework-agnostic core the devtools panels, relay, and producers all build on, so a backend can stream telemetry to a devtools window without pulling in React. |

### Dev environment

For the environment your app runs in, rather than the app itself.

| Package | What it does |
| --- | --- |
| [`@nice-code/commander`](https://www.npmjs.com/package/@nice-code/commander) | Your dev environment as one typed config — long-running processes, one-shot checks, dependency ordering, and declared env knobs — run by a local daemon with a CLI and a live web UI. |
| [`@nice-code/process`](https://www.npmjs.com/package/@nice-code/process) | One child process, fully managed — spawn, readiness you can await, restart backoff, log capture, and whole-tree teardown, with the same semantics on Windows, Linux, WSL, and macOS. The supervisor commander is built on. |

Full documentation for every package is at **https://nicecode.io**.

---

## Reporting an issue

Good bug reports get fixed faster. Please include:

1. **Which package** and the **version** you're on (e.g. `@nice-code/action@0.107.0`). All
   packages share one version — if yours are mixed, say so.
2. **What you expected** to happen vs. **what actually happened**.
3. A **minimal reproduction** — the smallest snippet, repo, or steps that trigger it.
4. Your **environment**: runtime (Node / Bun / browser / React Native / Cloudflare Workers),
   OS (say if it's WSL), and relevant tooling versions (TypeScript, bundler, etc.).
5. Any **error output**, stack traces, or logs.

Before opening a new issue, please **search existing issues** — someone may have already
reported it, and adding a 👍 or a comment with your details helps us prioritize. It's also worth
checking the [changelog](https://nicecode.io/production/changelog/): the fix may already be out.

## Feature requests

Feature requests are welcome. Describe the **use case** and the problem you're trying to solve,
not just the proposed solution — it helps us find the best fit across the libraries.

## Security

**Please do not report security vulnerabilities in public issues.** Instead, disclose them
privately by emailing the maintainer or using GitHub's
[private vulnerability reporting](../../security/advisories/new).

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
