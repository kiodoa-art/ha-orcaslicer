# OrcaSlicer Web (experimental)

Home Assistant app using `lscr.io/linuxserver/orcaslicer:latest` and the Supervisor Ingress proxy on internal HTTP port 3000.

**Experimental:** LinuxServer Selkies may not support Home Assistant's dynamic Ingress subpath; a blank screen, broken assets, or broken WebSockets are possible. Verify before relying on remote use.

No direct host port is exposed. Authentication comes from Home Assistant Ingress. Do not expose a raw port to the internet. The LinuxServer web desktop contains a terminal with elevated permissions **inside its container**.

The old local add-on `local_orcaslicer` and this repository-managed add-on are distinct installations. Do not remove the local add-on until persistent settings have been backed up and the new installation is tested. They may both use the slug `orcaslicer` within different repositories.

This initial configuration intentionally omits hard-coded usernames/passwords. Avoid committing real credentials to GitHub.

The LinuxServer image recommends 1GB shared memory for graphical stability, which is not configured in this minimum viable Home Assistant wrapper. GPU acceleration and connection to a specific printer also remain untested.

Upstream: https://docs.linuxserver.io/images/docker-orcaslicer/
