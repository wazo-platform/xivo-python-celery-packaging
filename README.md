# xivo-python-celery-packaging

Debian packaging for [Celery](http://www.celeryproject.org) used in Wazo.

## Upgrading

To upgrade Celery:

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version
* Push the changes

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
make -f debian/rules get-orig-source
tar -xvf ../xivo-python-celery-packaging_*.orig.tar.gz  --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.
