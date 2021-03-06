mkinitcpio-ykfde
================

**Full disk encryption with Yubikey (Yubico key)**

This allows to automatically unlock a LUKS encrypted hard disk from `systemd`-
enabled initramfs.

Requirements, building, installing and usage
--------------------------------------------

Most of this is generic, but it still differs in detail for
distributions. Please look at what matches best for you.

* [mkinitcpio based initramfs (Arch Linux, ...)](README-mkinitcpio.md)
* [dracut based initramfs (Fedora, ...)](README-dracut.md)

Limitation / TODO
-----------------

* [systemd password agents](http://www.freedesktop.org/wiki/Software/systemd/PasswordAgents/)
  do not support nested queries. That is why we can not ask for a
  password ourselfs, breaking two factor authentication (2FA).
* When using your additional initramfs `grub-mkconfig` does not know
  about that. Regenerating `grub` configuration file `grub.cfg` will
  overwrite our changes.

### Upstream

URL: [GitHub.com](https://github.com/eworm-de/mkinitcpio-ykfde)  
Mirror: [eworm.de](http://git.eworm.de/cgit.cgi/mkinitcpio-ykfde/)
