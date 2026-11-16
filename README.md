# polylint/scoop-bucket

[Scoop](https://scoop.sh) manifests for the [polylint](https://github.com/polylint) tools on Windows, mirroring the
[Homebrew tap](https://github.com/polylint/homebrew-tap).

```powershell
scoop bucket add polylint https://github.com/polylint/scoop-bucket
scoop install polylint/<app>
```

| App                                                            | Commands           | Description                                                                   |
| -------------------------------------------------------------- | ------------------ | ----------------------------------------------------------------------------- |
| [polylint](https://github.com/polylint/polylint) (also `poly`) | `poly`, `polylint` | One linter and formatter for every language in a repository                   |
| [skif](https://github.com/polylint/skif)                       | `skif`             | Dependency and package-manager linter for JavaScript and TypeScript monorepos |
| [adrlint](https://github.com/polylint/adrlint)                 | `adrlint`          | Linter and formatter for MADR architecture decision records                   |

## How manifests are updated

Each manifest points at a project's prebuilt Windows archive and takes its SHA-256 from that release's published
checksums. Each project's release workflow renders its own manifest with
[`xberg-io/actions/publish-scoop-manifests`](https://github.com/xberg-io/actions/tree/main/publish-scoop-manifests)
and pushes it here through the organization's GitHub App.
