# lo-bin-build: Build files for Gentoo's libreoffice-bin

These files are used to generate app-office/libreoffice-bin. 
Warning - continuous work in progress...

## Installation of a build chroot

- Use a DEDICATED chroot, i.e. the chroot should be used for NOTHING ELSE. Only for this build system.
- Clone this repository as /root/lo-bin-build
- remove /etc/portage/make.conf and symlink /root/lo-bin-build/config/make.conf.${ARCH} there
- symlink /root/lo-bin-build/config/keywords to /etc/portage/package.keywords/automatic
- symlink /root/lo-bin-build/config/useflags to /etc/portage/package.use/automatic
- symlink /root/lo-bin-build/config/environment to /etc/portage/package.env/automatic
- symlink /root/lo-bin-build/config/env to /etc/portage/env
- set the profile to be the main desktop profile

You should be able to figure out the rest for yourself.

## Trivial bump (for a stable request)

- Update config/keywords with all versions going stable together
- Update VERSION and BINVERSION (usually the same) in generate
- Run build / ask tamiko to run build
- ...
