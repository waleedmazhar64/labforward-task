# Lab procedure workflow generator

A historical Angular 6.1 and Node.js/Express application for composing lab-procedure workflows.

## Code map

- [Angular components](src/app): workflow canvas, conditions, controls, properties and connectors.
- [Express entry point](server.js): serves the compiled client and mounts `/workflows`.
- [Backend workflow code](server): workflow handling.
- [Package scripts](package.json): build and server commands.

## Local evaluation

The project uses a historical Angular toolchain. Choose compatible Node/npm versions and review the lockfile before installing.

```bash
npm ci
npm run build
npm start
```

The package's `postinstall` also triggers a production build. The Express server uses `PORT` or port 8080 and expects client assets in `dist/ch-ui`.

The current manifest has no `test` script, so the old README's generic `ng test` guidance is not a verified test procedure. Build, backend behaviour and browser interactions were not executed in this documentation review.

## Scope and attribution

This is a historical workflow-editor exercise. The checked-in [LICENSE](LICENSE) remains authoritative. Production scalability, deployment status and current test coverage are not claimed.
