# Maintainer: Bartłomiej Piotrowski <barthalion@gmail.com>

_pkgname=pentadactyl
pkgname=pentadactyl-nightly
pkgver=20130604
pkgrel=1
pkgdesc="Firefox for Vim and Links addicts. The next generation of Vimperator by its primary developers."
arch=('any')
url="http://dactyl.sourceforge.net/"
license=('MIT')
depends=('firefox>=3.5')
conflicts=('pentadactyl')
provides=('pentadactyl')
source=(http://dactyl.googlecode.com/files/$_pkgname-$pkgver.xpi)

package() {
    local _fxver=$(firefox -v | cut -d' ' -f3 | cut -f1-2 -d.)
    local _emid=pentadactyl@dactyl.googlecode.com #TODO: Extract from install.rdf
    local dstdir="$pkgdir/usr/lib/firefox/extensions/$_emid"

    cd "$srcdir"
    install -d "$dstdir"
    cp -R * "$dstdir"
    rm "$dstdir/$_pkgname-$pkgver.xpi"
}
md5sums=('1552571776c3bf1f02a369a885c20b76')
