# Contributor: SubNeX, iVendor

pkgname=scangearmp-x86_64
pkgver=1.60
pkgrel=2
pkgdesc="Canon IJ Scanner Driver (Common package) x86_64"
url="http://www.canon.dk/Support/Consumer_Products/products/Fax__Multifunctionals/InkJet/PIXMA_MP_series/MP495.aspx?type=download&page=1"
arch=('x86_64')
license=('custom')
depends=('sane' 'gtk2>=2.4.0' 'gimp>=2.0.0' 'libpng>=1.2.8' 'libusb>=0.1.12')
conflicts=('scangearmp')
makedepends=('rpmextract')
source=(http://files.canon-europe.com/files/soft40270/Software/MP495series-scanner_driver.tar)
md5sums=('9217ca25d62677ce2b24d0e95da35f4c')

build() {
  cd $srcdir
  tar -xvf MP495series-scanner_driver.tar 
  tar -xvf scangearmp-mp495series-$pkgver-1-rpm.tar.gz -C $pkgdir scangearmp-mp495series-$pkgver-1-rpm/packages/scangearmp-common-$pkgver-1.x86_64.rpm
  cd $pkgdir
  rpmextract.sh scangearmp-mp495series-$pkgver-1-rpm/packages/scangearmp-common-$pkgver-1.x86_64.rpm
  rm -Rf scangearmp-mp495series-$pkgver-1-rpm
  chmod -R a+rX usr/
}
