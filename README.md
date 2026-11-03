# just-enough.jp apps info (shared static site)

One Render static site (service `stc-info`) serves every NEF product's Privacy/Support pages.

- Legacy STC (unchanged): `/privacy.html`, `/support.html` (+ `/privacy`, `/support`) on stc.just-enough.jp
- Shared host: `apps.just-enough.jp/<product>/privacy.html` and `/<product>/support.html`
  - `dojo/` = 土壌汚染調査技術管理者 過去問
  - `sogo/` = 工事担任者 総合通信 過去問

## Adding a product (no DNS / Render changes)
1. Add `<product>/privacy.html` and `<product>/support.html` (copy `dojo/`, edit title/body/nav links).
2. Commit to main, then manual deploy on Render (autoDeploy is off).
3. Put `https://apps.just-enough.jp/<product>/privacy.html` and `/support.html` into App Store Connect.

Build copies every top-level entry except `dist`, `render.yaml`, `README.md` into `dist/`.
