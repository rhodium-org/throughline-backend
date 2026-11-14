# Twelve-Factor App backend methodology — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates it in CI. The prose headings are hand-owned — everything between `tl:*` markers is injected from the YAML items, so the published spec can never drift from the graph.

This source re-expresses the **Twelve-Factor App** methodology as a grounded IDD graph: each of the twelve factors is a `user_requirement`, and every individual rule is a `system_requirement` that `implements` its factor. The methodology reference lives in `attrs.source_ref`; the throughline UIDs are this source's own and immutable — a consumer cites a rule as `backend:SR-0001`, never by factor name.

It carries
<!-- tl:count type == 'user_requirement' -->
12
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
46
<!-- tl:end --> methodology rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — A backend service is portable, scalable and disposable in the cloud** — `intent`, status `proposed`

> The Twelve-Factor App methodology exists so that a backend service can be built for the modern cloud: with a clean contract to the operating system for maximum portability across execution environments, suitable for deployment on modern cloud platforms without the need for servers or systems administration, minimising divergence between development and production to enable continuous deployment, and able to scale up without significant changes to tooling, architecture or development practices.

**source_ref**: Twelve-Factor App
<!-- tl:end -->

## I. Codebase

<!-- tl:item UR-0001 -->
**UR-0001 — I. Codebase** — `user_requirement`, status `proposed`

> One codebase tracked in revision control, many deploys.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: I. Codebase
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: I. Codebase') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | proposed | Track the app in one codebase under revision control |
| SR-0002 | system_requirement | proposed | Keep a one-to-one correlation between codebase and app |
| SR-0003 | system_requirement | proposed | Do not share code between apps by sharing a codebase |
| SR-0004 | system_requirement | proposed | Run many deploys from the one codebase |
<!-- tl:end -->

## II. Dependencies

<!-- tl:item UR-0002 -->
**UR-0002 — II. Dependencies** — `user_requirement`, status `proposed`

> Explicitly declare and isolate dependencies.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: II. Dependencies
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: II. Dependencies') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0005 | system_requirement | proposed | Declare all dependencies in a manifest |
| SR-0006 | system_requirement | proposed | Isolate dependencies at execution time |
| SR-0007 | system_requirement | proposed | Do not rely on implicit system tools |
| SR-0008 | system_requirement | proposed | Let a new developer build with only the runtime and manager |
<!-- tl:end -->

## III. Config

<!-- tl:item UR-0003 -->
**UR-0003 — III. Config** — `user_requirement`, status `proposed`

> Store config in the environment.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: III. Config
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: III. Config') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0009 | system_requirement | proposed | Store config that varies per deploy in the environment |
| SR-0010 | system_requirement | proposed | Keep a strict separation of config from code |
| SR-0011 | system_requirement | proposed | Never check credentials into revision control |
| SR-0012 | system_requirement | proposed | Use granular, orthogonal environment variables |
<!-- tl:end -->

## IV. Backing services

<!-- tl:item UR-0004 -->
**UR-0004 — IV. Backing services** — `user_requirement`, status `proposed`

> Treat backing services as attached resources.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: IV. Backing services
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: IV. Backing services') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0013 | system_requirement | proposed | Treat every backing service as an attached resource |
| SR-0014 | system_requirement | proposed | Make no code distinction between local and third-party services |
| SR-0015 | system_requirement | proposed | Allow resources to be attached and detached at will |
| SR-0016 | system_requirement | proposed | Count each distinct backing service as a separate resource |
<!-- tl:end -->

## V. Build, release, run

<!-- tl:item UR-0005 -->
**UR-0005 — V. Build, release, run** — `user_requirement`, status `proposed`

> Strictly separate build and run stages.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: V. Build, release, run
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: V. Build, release, run') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0017 | system_requirement | proposed | Strictly separate the build, release and run stages |
| SR-0018 | system_requirement | proposed | Produce a build by fetching dependencies and compiling |
| SR-0019 | system_requirement | proposed | Form a release by combining the build with the deploy's config |
| SR-0020 | system_requirement | proposed | Give every release a unique ID and never mutate it |
| SR-0021 | system_requirement | proposed | Keep the run stage to as few moving parts as possible |
<!-- tl:end -->

## VI. Processes

<!-- tl:item UR-0006 -->
**UR-0006 — VI. Processes** — `user_requirement`, status `proposed`

> Execute the app as one or more stateless processes.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: VI. Processes
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: VI. Processes') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0022 | system_requirement | proposed | Execute the app as stateless, share-nothing processes |
| SR-0023 | system_requirement | proposed | Never assume in-memory or on-disk state survives a request |
| SR-0024 | system_requirement | proposed | Do not use sticky sessions |
| SR-0025 | system_requirement | proposed | Compile assets during the build stage, not at run time |
<!-- tl:end -->

## VII. Port binding

<!-- tl:item UR-0007 -->
**UR-0007 — VII. Port binding** — `user_requirement`, status `proposed`

> Export services via port binding.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: VII. Port binding
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: VII. Port binding') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0026 | system_requirement | proposed | Be completely self-contained and bind to a port |
| SR-0027 | system_requirement | proposed | Add the webserver as a declared dependency in user space |
| SR-0028 | system_requirement | proposed | Let a routing layer map public requests to the bound port |
| SR-0029 | system_requirement | proposed | Allow one app to become another app's backing service |
<!-- tl:end -->

## VIII. Concurrency

<!-- tl:item UR-0008 -->
**UR-0008 — VIII. Concurrency** — `user_requirement`, status `proposed`

> Scale out via the process model.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: VIII. Concurrency
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: VIII. Concurrency') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0030 | system_requirement | proposed | Treat processes as first-class citizens |
| SR-0031 | system_requirement | proposed | Assign different work to different process types |
| SR-0032 | system_requirement | proposed | Scale out horizontally by adding more processes |
| SR-0033 | system_requirement | proposed | Never daemonize or write PID files |
<!-- tl:end -->

## IX. Disposability

<!-- tl:item UR-0009 -->
**UR-0009 — IX. Disposability** — `user_requirement`, status `proposed`

> Maximise robustness with fast startup and graceful shutdown.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: IX. Disposability
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: IX. Disposability') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0034 | system_requirement | proposed | Make processes disposable, startable and stoppable at will |
| SR-0035 | system_requirement | proposed | Minimise startup time |
| SR-0036 | system_requirement | proposed | Shut down gracefully on SIGTERM |
| SR-0037 | system_requirement | proposed | Make jobs reentrant and robust against sudden death |
<!-- tl:end -->

## X. Dev/prod parity

<!-- tl:item UR-0010 -->
**UR-0010 — X. Dev/prod parity** — `user_requirement`, status `proposed`

> Keep development, staging and production as similar as possible.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: X. Dev/prod parity
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: X. Dev/prod parity') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0038 | system_requirement | proposed | Keep dev, staging and production as similar as possible |
| SR-0039 | system_requirement | proposed | Deploy in hours and keep developers close to production |
| SR-0040 | system_requirement | proposed | Use the same type and version of each backing service everywhere |
<!-- tl:end -->

## XI. Logs

<!-- tl:item UR-0011 -->
**UR-0011 — XI. Logs** — `user_requirement`, status `proposed`

> Treat logs as event streams.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: XI. Logs
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: XI. Logs') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0041 | system_requirement | proposed | Write each process's event stream unbuffered to stdout |
| SR-0042 | system_requirement | proposed | Never route or manage the app's own logfiles |
| SR-0043 | system_requirement | proposed | Let the execution environment capture and route the stream |
<!-- tl:end -->

## XII. Admin processes

<!-- tl:item UR-0012 -->
**UR-0012 — XII. Admin processes** — `user_requirement`, status `proposed`

> Run admin/management tasks as one-off processes.

*Derives from:* INT-0001

**source_ref**: Twelve-Factor App: XII. Admin processes
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('Twelve-Factor App: XII. Admin processes') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0044 | system_requirement | proposed | Run admin and management tasks as one-off processes |
| SR-0045 | system_requirement | proposed | Run one-off processes in an identical environment |
| SR-0046 | system_requirement | proposed | Ship admin code with the application code |
<!-- tl:end -->

