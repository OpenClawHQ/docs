# Publishing effectorHQ packages

Canonical checklist for maintainers also lives alongside the monorepo workspace as `DEPLOY_CHECKLIST.md` (section **7**). Summary:

## npm (primary registry)

- Scoped packages: `npm publish --access public` from each repo after tests pass.
- `@effectorhq/types` runs `npm run build` via `prepublishOnly` (generates `dist/`).

## GitHub Releases + tags

- Tag `vX.Y.Z` must match `package.json` and npm version.
- Create a **Release** on GitHub for changelog visibility.

## GitHub Actions (not npm)

- **skill-lint:** `uses: effectorHQ/skill-lint-action@v1`
- **effector.toml validation:** `uses: effectorHQ/effector-action@v1`

## GitHub Packages

- Not required for public `@effectorhq/*`; npmjs is the default install path.

## User install

- `npx @effectorhq/<package>` for CLIs; `npm install @effectorhq/<package>` for dependencies.
