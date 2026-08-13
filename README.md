# Alpine-minirootfs-latest-stable (AARCH64) | active ssh with root permitted

_general info:_

- Alpine-minirootfs-stable (linux/aarch64) from locally, downloaded from:
```
https://dl-cdn.alpinelinux.org/alpine/latest-stable/releases/aarch64/alpine-minirootfs-3.23.0-aarch64.tar.gz
```
- Active SSH
- Expose ssh 22 (8222:22)
- Built and tested on ARM64 device (ZTE B860H v.2) with Armbian Community v25.11 running:
```
https://github.com/armbian/community/releases/download/25.11.0-trunk.472/Armbian_community_25.11.0-trunk.472_Aml-s9xx-box_trixie_current_6.12.57_minimal.img.xz
```

---

## Quick Start

### Pull Image
```bash
docker pull ftoweren/alpine-minirootfs-stable-aarch64:latest
```

### Run Container
```bash
docker run -itd \
	--name alpine-mrfs-stable-arm64 \
	-p 8222:22 \
    --restart always \
	ftoweren/alpine-minirootfs-stable-aarch64:latest
```

### Post-Installation Management
Change Container Root Password (if needed):
```bash
docker exec -it alpine-mrfs-stable-arm64 passwd
```
---

## Build from Source

### Build Docker Image
```
docker build --no-cache -f path/Dockerfile -t image_name:tag .
```
