# Maintainer: Andrew Lubawy <dlubawy@gmail.com>

pkgname="datadraw-git"
pkgver=0.1.0
pkgrel=1
pkgdesc="A database generator"
arch=("x86_64")
url="https://github.com/waywardgeek/datadraw"
license=("GPL2")

_commit="2d94a19ff6e65ba58f49e937c151d325a2017de7"
source=("https://github.com/waywardgeek/datadraw/archive/$_commit/master.zip")
md5sums=("2a3e1cb7ded86ea613e783e06d05615d")

build() {
    cd "${pkgname/-git/}-$_commit"
    ./autogen.sh
    ./configure --prefix=/usr
    make
}

package() {
    cd "${pkgname/-git/}-$_commit"
    make DESTDIR="$pkgdir/" install
}
