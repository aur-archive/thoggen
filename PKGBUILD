# Maintainer: Mateusz Herych <heniekk@gmail.com>
# Contributor: Robert Emil Berge <filoktetes@linuxophic.org>

pkgname=thoggen
pkgver=0.7.1
pkgrel=6
pkgdesc="A DVD ripper based on GStreamer and GTK+"
arch=('i686' 'x86_64')
url="http://thoggen.net/"
license=('GPL')
depends=('libofa' 'perlxml' 'gstreamer0.10-base-plugins' 'gstreamer0.10-good-plugins'
	 'gstreamer0.10-ugly-plugins' 'gstreamer0.10-bad-plugins' 'gstreamer0.10-ffmpeg'
	 'libdvdread' 'libglade' 'hal')
source=("http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz")
md5sums=('e36c1ceb098f8ed51ca6c0d1e7ae8279')

build() {
  cd $srcdir/$pkgname-$pkgver
  ./configure --prefix=/usr
  make
}

package() {
  cd $srcdir/$pkgname-$pkgver
  make DESTDIR=$pkgdir install
}
