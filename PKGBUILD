pkgname=udptunnel-mptcp
pkgver=1.1
pkgrel=1
pkgdesc="Tunnel UDP packets over a TCP connection."
provides=(udptunnel)
conflicts=(udptunnel udptunnel-mptcp)
arch=(aarch64 x86_64)
license=(BSD)
makedepends=(gcc)

build() {
  ./configure --prefix=/usr
  make
}

package() {
  make DESTDIR="$pkgdir" install
  install -D -m 0644 COPYRIGHT "$pkgdir/usr/share/licenses/$_pkgname/COPYRIGHT"
}
