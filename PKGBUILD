# Contributor: Anonymous
# Generator  : CPANPLUS::Dist::Arch 1.28

pkgname='perl-web-query'
pkgver='0.26'
pkgrel='1'
pkgdesc="Yet another scraping library like jQuery"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-html-parser>=0' 'perl-html-selector-xpath>=0.06' 'perl-html-treebuilder-xpath>=0.12' 'perl-libwww>=0' 'perl>=5.8.5')
makedepends=()
url='http://search.cpan.org/dist/Web-Query'
source=('http://search.cpan.org/CPAN/authors/id/C/CA/CAFEGRATZ/Web-Query-0.23.tar.gz')
md5sums=('d9cd85762efe971536616e36ea950ca4')
sha512sums=('412d2c6d825c11ba54e6df99d06772447f05c1a5df187bfcda3622aea96a4f8d9abad968915eb5d1cedd731697306c6e41b3022961c20674ba784056b30bfb3a')
_distdir="Web-Query-0.23"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Build.PL
    /usr/bin/perl Build
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    /usr/bin/perl Build test
  )
}

package() {
  cd "$srcdir/$_distdir"
  /usr/bin/perl Build install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:

