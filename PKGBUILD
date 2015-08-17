# Contributor: neosam <neosam@posteo.de>
pkgname=ocaml-dolog-git
pkgver=1.0.0
pkgrel=2
pkgdesc="Logging for Ocaml"
arch=('i686' 'x86_64' 'mips64el' 'armv6h' 'armv7h' 'arm')
url="https://github.com/UnixJunkie/dolog"
license=('BSD 3')
depends=('ocaml')
makedeps=('git' 'ocaml' 'ocaml-findlib')
source=()
md5sums=()

build() {
  cd $srcdir
  git clone https://github.com/UnixJunkie/dolog.git
  cd dolog
  ./configure --exec-prefix $pkgdir/usr/ --destdir $pkgdir --prefix $pkgdir/usr/
  make all
}

package ()
{
  cd "$srcdir/dolog"
  mkdir -p $pkgdir/usr/lib/ocaml/
  ocamlfind install -destdir "$pkgdir/usr/lib/ocaml/" dolog lib/META _build/lib/*
}

# vim:set ts=2 sw=2 et:
