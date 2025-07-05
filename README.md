# xosview-el9-rpm

This repository contains the xosview 1.23 source RPM rebuilt from Fedora 34 for use on AlmaLinux 9 / RHEL 9 / EL9 systems. The spec file and dependencies have been reviewed and updated to ensure compatibility with modern EL9 environments.

## Source

Original Fedora 34 SRPM:

```
xosview-1.23-2.fc34.src.rpm
```

Rebuilt for EL9:

```
xosview-1.23-2.el9.src.rpm
```

## How to extract the spec file

To extract the spec file and sources:

```
rpm2cpio xosview-1.23-2.el9.src.rpm | cpio -idmv
```

This will extract:

- `xosview.spec`
- `xosview-1.23.tar.gz` (or similar source files)

## How to build RPM

To build the RPM from the SRPM on AlmaLinux 9 / EL9:

```
dnf install -y rpm-build gcc make libXt-devel libXaw-devel
rpmbuild --rebuild xosview-1.23-2.el9.src.rpm
```

The resulting RPMs will be located in:

```
~/rpmbuild/RPMS/
```

## License

GPLv2+

## Maintainer

Fedora EPEL Maintainer (FAS: redadmin)

