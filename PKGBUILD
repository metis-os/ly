# Maintainer: whoisYoges <helloyogesh@tuta.io>
pkgname=metis-ly
pkgver=r3.b0bcf72
pkgrel=1
pkgdesc="TUI display manager for metis linux"
arch=('any')
url="https://github.com/whoisYoges/metis-ly"
license=('MIT')
makedepends=('git')
depends=('pam' 'xorg-xauth')
conflicts=('ly' 'ly-git' 'python-ly-git')
backup=('etc/ly/config.ini')
source=(${pkgname}::"git+${url}")
sha256sums=('SKIP')

build() {
	cd "$srcdir/$pkgname"
	make
}

package() {
	cd "$srcdir/$pkgname" 
	make DESTDIR="$pkgdir" install
}

pkgver() {
  cd "${srcdir}/$pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}
