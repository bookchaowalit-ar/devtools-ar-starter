# bookchaowalit-ar-starter

Starter repository for the `bookchaowalit-ar` organization.

## Purpose

This repository is an intentionally thin baseline for AR/MR interfaces
and shared conventions under the Book Dev owner model. It contains no product
features yet.

## Repository boundary

- **Owner:** `bookchaowalit-ar`
- **Surface:** AR/MR
- **Book Dev category:** `book-apps/ar`
- **Default branch:** `main`
- **Status:** starter / skeleton

## CI

GitHub Actions runs [`scripts/check-starter.sh`](./scripts/check-starter.sh)
on pushes to `main` and on every pull request. It checks that:

- the baseline files exist (`README.md`, MIT `LICENSE`, `.gitignore`,
  `.editorconfig`, `docs/UPGRADE-PLAN.md`, CI workflow);
- this README keeps its owner-model sections;
- relative Markdown links resolve;
- no secret-bearing files (`.env`, keys, credentials) are tracked;
- while **Status** says `starter`, no implementation files have been added
  (update the Status line when the first product lands).

The shared security workflow from
[`bookchaowalit/platform-ci-workflows`](https://github.com/bookchaowalit/platform-ci-workflows)
(v1.1.1: gitleaks, Semgrep, OSV-Scanner, Trivy) runs in the same CI. The shared
language CIs (`ci-node.yml`, `ci-python.yml`) are added with the first product
scaffold, once there is a stack to lint, type check and test.

## Local development

There is no runtime or dependency setup yet. The only local check is:

```bash
bash scripts/check-starter.sh
```

Add implementation only when a concrete AR/MR product is approved. The
candidate stacks and the first-scaffold checklist are in
[`docs/UPGRADE-PLAN.md`](./docs/UPGRADE-PLAN.md).

## License

MIT. See [`LICENSE`](./LICENSE).
