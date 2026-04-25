# dev-sec-bug 📦🔐♾️
## A repo for applying to the Agile SDLC method on A DevSecOps project

### dev branch for developers 📦
### sec branch for security engineers 🔐
### bug branch or test branch for code testers or test engineers ♾️

## Branch Strategy

| Branch | Purpose |
|--------|---------|
| `main` | Stable, production-ready code |
| `dev`  | Active feature development and bug fixes |
| `sec`  | Security patches and vulnerability remediation |
| `test` | Test suites, QA automation, and test tooling |

## Workflow

```
dev  ──┐
sec  ──┼──► main
test ──┘
```

1. Work is done on the relevant branch (`dev`, `sec`, or `test`).
2. A Pull Request is opened targeting `main`.
3. The PR is reviewed and all CI checks must pass.
4. After approval, the branch is merged into `main`.

## Branch Initialization

The `.github/workflows/setup-branches.yml` workflow automatically creates the `dev`, `sec`, and `test` branches (if they do not already exist) whenever a push is made to `main`, or when triggered manually via **Actions → Setup dev, sec, and test branches → Run workflow**.
