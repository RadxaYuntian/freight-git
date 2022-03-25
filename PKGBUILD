# Maintainer: Yuntian Zhang <yt at radxa dot com>

pkgname=freight-git
_pkgname=${pkgname%-git}
pkgver=0.3.13.r30.gdb53121
pkgrel=1
pkgdesc="A modern take on the Debian archive"
arch=('any')
url="https://github.com/freight-team/freight"
license=('BSD')
depends=('dpkg')
makedepends=('git')
source=("git+https://github.com/freight-team/freight.git")
md5sums=('SKIP')

pkgver() {
    cd "$_pkgname"
    git describe --long | sed 's/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
    cd "$srcdir/$_pkgname"
    DESTDIR="$pkgdir" make install prefix=/usr 
}
