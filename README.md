# clowder APT repository

Debian packages of [clowder](https://github.com/webcodingcat/clowder) for Debian 13 (trixie),
amd64, served by GitHub Pages. The release workflow of clowder writes this repository; do
not change it by hand.

```bash
curl -fsSL https://webcodingcat.github.io/clowder-apt/clowder.asc \
  -o /usr/share/keyrings/clowder.asc
echo "deb [signed-by=/usr/share/keyrings/clowder.asc] https://webcodingcat.github.io/clowder-apt trixie main" \
  > /etc/apt/sources.list.d/clowder.list
apt-get update && apt-get install clowderd   # on a host; the CLI is the package clowder
```

`clowderd` also needs LINBIT's public repository for `drbd-dkms` and `drbd-utils`
(`http://packages.linbit.com/public proxmox-9 drbd-9`).
