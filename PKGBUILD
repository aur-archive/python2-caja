# Maintainer : Martin Wimpress <code@flexion.org>
# Contributor: Xpander <xpander0@gmail.com>

pkgname=python2-caja
_pkgname=python-caja
pkgver=1.6.0
pkgrel=6
pkgdesc="Python binding for Caja, to allow Caja property page and menu item extensions to be written in Python."
url="http://mate-desktop.org"
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
license=('GPL')
depends=('mate-file-manager' 'python2' 'python2-gobject')
makedepends=('mate-common')
options=('!emptydirs')
replaces=('python-caja')
provides=('python-caja')
source=("http://pub.mate-desktop.org/releases/1.6/${_pkgname}-${pkgver}.tar.xz")
sha1sums=('a7dbcff03b9dbdf2f33dbea96946426097eb9e56')

build() {
    cd "${srcdir}/${_pkgname}-${pkgver}"
    PYTHON=/usr/bin/python2 ./autogen.sh \
        --prefix=/usr \
        --disable-static
    make
}

package() {
    cd "${srcdir}/${_pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
