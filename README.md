# Docker for Tableau Server for Linux - Single node

That is the fork of the original project created by [@tfoldi](https://twitter.com/tfoldi).

### Prerequisites

- Docker has be installed. Run `docker version` to verify.
- Since Tableau Server itself has some requirements to the host machine, you need to change [the advanced settings](https://docs.docker.com/docker-for-windows/#advanced) for docker to grant it at least 8Gb of memory and 8 cores of CPU.

### Build

```bash
  docker build -t tfoldi/tableau-server:release .
```

### Run

```bash
  docker run -ti --privileged -v /sys/fs/cgroup:/sys/fs/cgroup -v /run -p 80 tfoldi/tableau-server:release
```

### Tableau docs

- [Introducing Tableau Server on Linux](https://onlinehelp.tableau.com/current/server-linux/en-us/release_notes_linux.htm)

- [Whitepaper Tableau for the enterprise](https://www.tableau.com/sites/default/files/whitepapers/whitepaper_tableau-for-the-enterprise_0.pdf)

- [Online Help](http://onlinehelp.tableau.com/v10.5/pro/desktop/en-us/help.htm)
