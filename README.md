# LEGO Snap

LEGO is a Let's Encrypt client and ACME library written in Go. For more information, read the [official documentation](https://go-acme.github.io/lego/usage/).

The LEGO snap makes it easy to install and use LEGO on any Linux distribution that supports snaps.

## Usage

```bash
sudo snap install lego
sudo snap connect lego:dot-lego
sudo lego \
  --email="you@example.com" \
  --domains="example.com" \
  --server=https://acme-staging-v02.api.letsencrypt.org/directory \
  --http \
  --http.port :8080 \
  run
```

Note: The LEGO snap can only write to the `/var/snap/lego/common/.lego` directory.
