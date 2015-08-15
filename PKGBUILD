# Maintainer: Zom <zom[at]eevul[dot]org>
#Contributor: <thomas.luebking@gmail.com>

pkgname=bempc
pkgver=0.11
pkgrel=2
pkgdesc="BE::MPC is a client for MPD with some UI experiments"
arch=('i686' 'x86_64')
url="http://qt-apps.org/content/show.php/BE::MPC?content=137091"
license=('GPL')
depends=('qt4' 'libmpdclient')
makedepends=()
install='bempc.install'
source=('http://qt-apps.org/CONTENT/content-files/137091-bempc-'${pkgver}.txz)
md5sums=('95d7bd6cf4418dad7a7c018fe2d5592d')

build() {
  cd ${srcdir}/bempc-${pkgver}

  qmake-qt4
  make
}

package() {
  cd ${srcdir}/bempc-${pkgver}
  sed -ie 's/update-desktop-database//g' Makefile
  make INSTALL_ROOT=${pkgdir} install
}
