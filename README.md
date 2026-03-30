# Arch Linux ARM - Pre-built Packages for LX2160A

Pre-built Arch Linux ARM packages and container images for NXP LX2160A based boards.

Packages: `restool`, `linux-aarch64-lx2160`, `zfs-dkms`, `zfs-utils`

## Pacman Repository

```bash
curl -s https://archlinux-lx2160.yxio.net/lx2160.gpg | sudo pacman-key --add -
sudo pacman-key --lsign-key 612143A8503BD71E08A6976768E73A1FE6A4783B
```

Add to `/etc/pacman.conf`:

```ini
[lx2160]
Server = https://archlinux-lx2160.yxio.net
```

## Incus Image

```bash
incus remote add archlinux-aarch64 https://archlinux-lx2160.yxio.net/incus --protocol simplestreams
incus launch archlinux-aarch64:archlinux mycontainer
```

## More Info

See https://archlinux-lx2160.yxio.net/