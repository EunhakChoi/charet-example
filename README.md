# charet example

A small React + shadcn app worked on in [charet](https://github.com/EunhakChoi/charet), used to try the
whole loop: changes made and merged in charet come here as pull requests, and changes made here go
back to charet.

- `src/`: the app. `.charet/`: its screens, mocks and stories for charet (charet-only).
- `vendor/charet-sdk-0.0.0.tgz`: `@charet/sdk` packed from the charet repo until it is on npm.

```bash
pnpm install
pnpm dev        # the app
pnpm typecheck
pnpm test       # a preview build with the screen manifest
```

## With charet

```bash
charet import --key example                     # once
charet handoff -p example                       # what to hand off, and this repo's own changes
charet handoff export -p example --out p.patch  # on a work branch: git apply p.patch, then a PR
charet handoff mark vN -p example               # after the PR is merged (HEAD of main)
charet import --update -p example               # bring this repo's own changes back
```
