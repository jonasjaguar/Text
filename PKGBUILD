# Maintainer: Jonas Jaguar <jonasjaguar@jagudev.net>
pkgname=jagudev-commander
pkgver=1.2
pkgrel=1
pkgdesc="A terminal. Very barebones, but functional."
arch=('x86_64')
url="https://jagudev.net"
license=('GPL3')
depends=(qt5-base qtermwidget)
makedepends=(gcc make)
options=()
source=("https://github.com/jonasjaguar/Commander/archive/$pkgver.tar.gz")
md5sums=('449919ff4debf8b14f8d3bf73a58566b')
validpgpkeys=()


build() {
	cd "$srcdir/Commander-$pkgver/Commander"
	qmake ./Commander.pro -spec linux-g++ && /usr/bin/make qmake_all
	make
}

package() {
	cd "$srcdir/Commander-$pkgver/Commander"
	make INSTALL_ROOT="$pkgdir" install
}
