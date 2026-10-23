# go-symbolic.github.io

The go-symbolic landing page (Hugo), served at <https://go-symbolic.github.io/>.
The documentation is at <https://go-symbolic.github.io/docs/> (repository
[go-symbolic/docs](https://github.com/go-symbolic/docs)).

go-symbolic is **planned, wave 4** of the go-scikit roadmap
([PLAN.md](https://github.com/go-scikit/roadmap/blob/main/PLAN.md), [STATUS.md](https://github.com/go-scikit/roadmap/blob/main/STATUS.md)): computer algebra. It has no
library and no release yet, so the page says what will be covered and where it
is in the plan; there is no playground and no figure.

The layout is the go-* family template: `layouts/index.html` and the shared
design (stylesheet, theme toggle, fork ribbon, icons), imported as the Hugo
module `github.com/go-fleettools/landingkit` pinned in `go.mod`. `[params.brand]`
in `hugo.toml` is read from the logo's gradient:

```sh
go run github.com/go-fleettools/landingkit/cmd/landingkit brand static/img/logo.svg
hugo server
```

| Workflow | What |
| --- | --- |
| `hugo.yml` | builds on pull requests; builds and deploys to Pages on `main` |
| `ci.yml` | the site builds and names every repository; `go mod tidy` keeps the landingkit requirement |
| `links.yml` | every link and image of the built site resolves |

BSD-3-Clause.
