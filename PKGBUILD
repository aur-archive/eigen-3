# Maintainer: Wilhelm
# This PKGBUILD is a modified version of extra/eigen that provides eigen 2.x

pkgname=eigen-3
pkgver=3.0.1
pkgrel=4
pkgdesc="Eigen 3 :: Eigen is a lightweight C++ template library for vector and matrix math, a.k.a. linear algebra."
arch=('any')
url='http://eigen.tuxfamily.org'
license=('GPL' 'LGPL')
makedepends=('cmake' 'pkgconfig')
provides=('eigen3')
source=("http://bitbucket.org/eigen/eigen/get/${pkgver}.tar.bz2")

build() {
	cd $srcdir
	if [ ! -d build ]; then
		mkdir build
	fi
	cd build
	cmake ../eigen-eigen-$pkgver \
		-DCMAKE_BUILD_TYPE=Release \
		-DCMAKE_INSTALL_PREFIX=/usr
	make
	make DESTDIR=$pkgdir install
}
md5sums=('69004f4d04fa6e49bf9fbeb957cfb97e')

