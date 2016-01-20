pkgname=perl-www-robotrules
pkgver=6.02
pkgrel=1
pkgdesc="Database of robots.txt-derived permissions"
arch=('x86_64')
url="https://metacpan.org/release/WWW-RobotRules"
license=('PerlArtistic' 'GPL')
depends=('perl' 'perl-uri')
options=('!emptydirs')
source=(http://search.cpan.org/CPAN/authors/id/G/GA/GAAS/WWW-RobotRules-${pkgver}.tar.gz)
sha1sums=('e158e6559307878b32d8e4c241bf257c2bc88ebb')

build() {
  cd "${srcdir}/WWW-RobotRules-${pkgver}"
  perl Makefile.PL INSTALLDIRS=vendor
  make
}

check() {
  cd "${srcdir}/WWW-RobotRules-${pkgver}"
  make test
}

package() {
  cd "${srcdir}/WWW-RobotRules-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
