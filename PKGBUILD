# Contributor: damir <damir@archlinux.org>

pkgname=libmusepack
pkgver=1.1.1
pkgrel=1
pkgdesc="Musepack decoding library"
arch=('i686' 'x86_64')
url="http://musepack.net/"
license=('BSD')
depends=('glibc')
options=('!libtool')
source=(http://www.saunalahti.fi/grimmel/musepack.net-files/source/libmusepack-$pkgver.tar.bz2)
md5sums=('480033dea2fff03afcfa17dfb60c7527')

build() {
  cd $srcdir/$pkgname-$pkgver
  ./configure --prefix=/usr || return 1
  make || return 1
  make DESTDIR=$pkgdir install || return 1
  install -Dm644 COPYING $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
