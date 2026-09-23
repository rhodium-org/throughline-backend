# throughline-backend

The **Twelve-Factor App** methodology expressed as a
[throughline](https://pypi.org/project/throughline/) **source** — a standalone,
grounded requirements graph that a consuming project composes with
`tl` from [throughline](https://pypi.org/project/throughline/) 3.11.0 or later.

This repository holds no code. It is a directory of small YAML items with permanent
UIDs, validated by `tl check`. Consumers import it under a namespace and reference
its rules as `backend:SR-0001`.

It is a backend **concern** source. Compose it **orthogonally** alongside a language
source (e.g. `throughline-go` or `throughline-java`) so a backend service is grounded
in both its language style **and** its cloud-native methodology at once: the language
source governs how the code is written, this source governs how the service is
structured, configured, built and run.

## Status

<!-- tl:count type == 'user_requirement' -->
12
<!-- tl:end --> factors and
<!-- tl:count type == 'system_requirement' -->
46
<!-- tl:end --> methodology rules, published to [`docs/spec.md`](docs/spec.md):

- `INT-0001` — the root intent (why the methodology exists), `normative: false`.
- Each of the twelve factors as a `user_requirement` that `derives_from` the intent.
- Every individual rule as a `system_requirement` that `implements` its factor,
  carrying the methodology reference in `attrs.source_ref`.

The counts above are rendered from the live graph by the `tl:count` directive, so
they cannot drift.

## Editions — dated tags

The methodology is a living document. A material revision is cut as a dated tag on
this repo (e.g. `v2026-08`); a consumer pins the ref it wants.

## Composing it

```toml
[[sources]]
namespace = "backend"
url = "https://github.com/rhodium-org/throughline-backend"
ref = "v2026-08"
```

Then reference a rule from your own items:

```yaml
links:
- target: backend:SR-0011      # Twelve-Factor App: never check credentials into revision control
  type: satisfies
```

`tl check` in the consuming project composes this source and resolves the reference.
A `tl` older than 3.11.0 reports it as `namespace-unresolved`.

## Local checks

```sh
pip install throughline
tl check --strict     # the graph must stay sound
tl docs --check       # docs/spec.md must match the graph
```

## Provenance

The Twelve-Factor App is by Adam Wiggins and contributors, licensed CC BY-SA 3.0. See
[NOTICE](NOTICE) and https://12factor.net/. This repository is Apache-2.0 for its
structure and tooling; the reproduced rule text remains the work of its authors.
