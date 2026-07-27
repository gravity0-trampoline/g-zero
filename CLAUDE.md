# g-zero

## Important: this repo is not the production app

The app that students actually use is hosted from a **different** repository:

```
https://gravity0-trampoline.github.io/Claude-code/
```

(GitHub repo: `gravity0-trampoline/Claude-code`)

This `g-zero` repo's `index.html`/`manifest.json` are not the ones deployed
in production, as far as we've confirmed. Before debugging reports of slow
check-ins, communication errors, or missing home-screen icons, confirm
which URL/repo the report is actually about — don't assume it's this one.

## Shared backend

Both the production app and this repo's `index.html` call the same Google
Apps Script backend (`Code.gs`, bound to a Google Sheet named `生徒名簿`),
via a hardcoded `GAS_URL` in the frontend JS. Apps Script code changes are
not live until a deployment is explicitly updated ("デプロイを管理" →
edit the existing deployment → new version → デプロイ) — editing/saving the
script alone does not affect any already-deployed exec URL. Multiple
deployments can exist with different exec URLs; make sure the one being
edited matches the URL actually in use.
