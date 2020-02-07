# Maintainer: Mircea Dan Gheorghe <mirceadan@gmail.com>
# Contributor: Mircea Dan Gheorghe <mirceadan@gmail.com>


# inspired from
#https://wiki.archlinux.org/index.php/creating_packages
#https://aur.archlinux.org/cgit/aur.git/tree/PKGBUILD?h=tclxml
#https://bbs.archlinux.org/viewtopic.php?id=243517

pkgname=mpexpr
pkgver=1.2
pkgrel=1
pkgdesc="Mpexpr is a multiple precision math package for Tcl. Mpexpr adds two new commands to Tcl: mpexpr and mpformat. mpexpr is used just like Tcl's expr command, except it allows you to calculate with ridiculously large numbers. Or ordinary average size numbers, without the binary floating point to decimal floating point conversion problems that expr sometimes experiences."
url="http://mpexpr.sourceforge.net/"
arch=('any')
license=('BSD')
depends=('tcl')
optdepends=(
    'tcllib: technically not needed, but you want it if you want this package'
)
source=("https://sourceforge.net/projects/mpexpr/files/mpexpr/1.2/mpexpr-1.2.tar.gz")
md5sums=('a6d89c7490a699e03f4246a3a080c210')

build() {
  cd $srcdir/$pkgname-$pkgver/unix
  bash ./configure --prefix=/usr/share  --exec-prefix=/usr
  make
  make test
  make install
}

