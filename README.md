This is the repository of the distribution specific Yocto layer for the Stromer Medusa hardware.

Patches:
- [CVE-2017-1000251 (BlueBorne)](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=e860d2c904d1a9f38a24eb44c9f34b8f915a6ea3)
- [Barebox with GCC 6.3 or newer](http://lists.infradead.org/pipermail/barebox/2017-May/030156.html)
- [JTAG with running Linux Kernel](https://community.nxp.com/thread/376786)
- [systemd /etc/localtime symlinks chasing](https://github.com/tramseyer/meta-medusa-dist/tree/master/recipes-core/systemd/systemd/chase_symlinks_etc_localtime.patch)

Backports:
- [linux-common: adapt to poky updates](https://github.com/PHYTEC-Messtechnik-GmbH/meta-phytec/commit/9c7f4e1e366f8f0b936bdf7eb0a91ebe130bd279)
- [linux-mainline_4.12.4-phy4.bb](https://github.com/PHYTEC-Messtechnik-GmbH/meta-phytec/blob/morty/recipes-kernel/linux/linux-mainline_4.12.4-phy4.bb)
- [nano](https://github.com/openembedded/meta-openembedded/commit/100a00a32dae355aba6bfb49e72d6546b3cba81b)

Ideas and todo's for reducing boot time:
- Strip down Qt to a bare minimum via QT_CONFIG_FLAGS in qtbase_%.bbappend.
- Compile driver for BMP280 as Kernel module and load it after drive.target.
- Set GPIO's to desired direction and possibly value already in device tree.
