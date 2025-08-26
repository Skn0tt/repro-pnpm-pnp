```sh
$ pnpm i
$ pnpm exec playwright

/Users/skn0tt/dev/tmp/repro-pnpm-pnp/.pnp.cjs:5653
    throw firstError;
    ^

Error: Your application tried to access playwright, but it isn't declared in your dependencies; this makes the require call ambiguous and unsound.

Required package: playwright (via "playwright/lib/program")
Required by: /Users/skn0tt/dev/tmp/repro-pnpm-pnp/node_modules/.pnpm/@playwright+test@1.55.0/node_modules/@playwright/test/

Require stack:
- /Users/skn0tt/dev/tmp/repro-pnpm-pnp/node_modules/.pnpm/@playwright+test@1.55.0/node_modules/@playwright/test/cli.js
    at require$$0.Module._resolveFilename (/Users/skn0tt/dev/tmp/repro-pnpm-pnp/.pnp.cjs:5652:13)
    at defaultResolveImpl (node:internal/modules/cjs/loader:1061:19)
    at resolveForCJSWithHooks (node:internal/modules/cjs/loader:1066:22)
    at Function.<anonymous> (node:internal/modules/cjs/loader:1215:37)
    at require$$0.Module._load (/Users/skn0tt/dev/tmp/repro-pnpm-pnp/.pnp.cjs:5543:31)
    at TracingChannel.traceSync (node:diagnostics_channel:322:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:235:24)
    at Module.require (node:internal/modules/cjs/loader:1491:12)
    at require (node:internal/modules/helpers:135:16)
    at Object.<anonymous> (/Users/skn0tt/dev/tmp/repro-pnpm-pnp/node_modules/.pnpm/@playwright+test@1.55.0/node_modules/@playwright/test/cli.js:18:21)

Node.js v23.11.0
```