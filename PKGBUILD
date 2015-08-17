# Contributor : Daniel Neve <the.mephit@googlemail.com>
pkgname=pynzb
pkgver=0.1.0
pkgrel=4
pkgdesc="A unified API for parsing NZB files"
arch=('any')
url="http://pypi.python.org/pypi/pynzb/"
license=('BSD')
depends=('python' 'expat')
makedepends=('setuptools')
optdepends=('python-lxml: Use lxml instead of expat')
source=(http://pypi.python.org/packages/source/p/$pkgname/$pkgname-$pkgver.tar.gz
        https://github.com/ericflo/$pkgname/raw/master/LICENSE.txt)
md5sums=('63c74a36348ac28aa99732dcb8be8c59'
         '87d87599921bae943f981b28ecfc3cc1')

build() {
  cd $srcdir/$pkgname-$pkgver
  python2 setup.py install --root=$pkgdir/ --optimize=1 || return 1
  install -D -m644 $srcdir/LICENSE.txt $pkgdir/usr/share/licenses/$pkgname/LICENSE.txt
}

