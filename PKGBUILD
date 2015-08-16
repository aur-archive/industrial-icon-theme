# Maintainer: Limao Luo <luolimao+AUR@gmail.com>

pkgname=industrial-icon-theme
pkgver=11.0.5.0
pkgrel=1
pkgdesc="Ximian Industrial icon theme for GNOME"
arch=(any)
url=https://launchpad.net/ubuntu/+source/$pkgname
license=(CCPL:by-sa-3.0)
makedepends=(gtk2 'icon-naming-utils>=0.7.0')
options=(!emptydirs)
source=(https://launchpad.net/ubuntu/jaunty/+source/$pkgname/$pkgver-1/+files/${pkgname}_$pkgver.orig.tar.gz)
sha256sums=('de7ab7d24d090c1bda018db78f8a0383c38e4d4051ee0f9e80aa276f75cf869c')
sha512sums=('32f8adba5bb280c43a13f46012377986231ec6d4ae8700c1faf33cc23509a6005a0e073ff06290d8fc687d516224e66208a788c2eae9d47f01e18f074ac2524e')

build() {
    cd $pkgname-${pkgver%.*}/
    ./configure --prefix=/usr
    make
}

package() {
    make -C $pkgname-${pkgver%.*} DESTDIR="$pkgdir" install
}
