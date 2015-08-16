# Contributor: Dany Martineau <dany.luc.martineau@gmail.com>
# Maintainer: Mcder3 <mcder3[at]gmail[dot]com>

pkgname=kmediafactory
pkgver=0.8.1
pkgrel=2
pkgdesc="An easy to use template based dvd authoring tool."
url="http://code.google.com/p/kmediafactory/"
license="GPL"
arch=('i686' 'x86_64')
depends=('dvdauthor' 'imagemagick' 'mjpegtools' 'zip' 'dvd-slideshow' 'libdvdread' 'xine-lib' 'kdelibs' 'libdv' 'ffmpeg')
makedepends=('cmake' 'automoc4')
optdepends=('k3b' 'kaffeine')
source=(http://kmediafactory.googlecode.com/files/$pkgname-$pkgver.tar.bz2)
md5sums=('e13e4682c78d6f49647551aeab7a1235')


build() {
	  cd ${srcdir}/$pkgname-$pkgver
	  cmake . -DCMAKE_INSTALL_PREFIX=/usr
	  make || return 1
	  make DESTDIR=${pkgdir} install || return 1
	}
