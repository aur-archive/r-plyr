# Contributor: Nick B <Shirakawasuna at gmail _dot_com>

pkgname=r-plyr
pkgver=1.7.1
pkgrel=2
pkgdesc="An R package providing a set of tools to break a problem down into pieces, operate on each piece, then put it all back together."
arch=('i686' 'x86_64')
url="http://cran.r-project.org/web/packages/plyr/index.html"
license=('MIT')
depends=('r' 'r-itertools')
source=(http://cran.r-project.org/src/contrib/Archive/plyr/plyr_$pkgver.tar.gz)
md5sums=('072e6a80e81b85059fb24d833e4df475')

build() {
 mkdir -p $pkgdir/usr/lib/R/library
 cd $srcdir
 R CMD INSTALL -l $pkgdir/usr/lib/R/library ./plyr

 #plyr doesn't come with a license spelled out in its entirety, it just says 'MIT'
 install -D -m644 $srcdir/plyr/DESCRIPTION $pkgdir/usr/share/licenses/r-plyr/DESCRIPTION
}
