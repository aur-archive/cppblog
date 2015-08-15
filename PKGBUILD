# Maintainer: Paolo Bolzoni <paolo.bolzoni.brown@gmail.com>
pkgname=cppblog
pkgver=0.1.0
pkgrel=1
epoch=
pkgdesc="A high performance blog engine based on CppCMS technology"
arch=(i686 x86_64)
url="http://cppcms.com/wikipp/en/page/install_cppblog"
license=('GPL')
groups=()
depends=(cppcms cppdb discount graphicsmagick gsfonts)
makedepends=()
checkdepends=()
optdepends=(
    'texlive-bin: embed LaTeX formulae in blog posts'
)
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=('cppblog_0.1.0.tar.bz2::http://sourceforge.net/projects/cppcms/files/cppblog/cppblog_0.1.0.tar.bz2/download')
noextract=()
md5sums=('d964b04feecbb9a432ce69568a0749b1')

build() {
	cd "$srcdir/$pkgname""_$pkgver"
	mkdir build
	cd build
	cmake -DCMAKE_INSTALL_PREFIX=/usr ..
	make
}

package() {
	cd "$srcdir/$pkgname""_$pkgver/build"
	make DESTDIR="$pkgdir/" install
}

