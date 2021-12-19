# Maintainer: Fabien POLETTE <fabien.polette@protonmail.com>
pkgname=containerlab
pkgver=0.21.0
pkgrel=1
pkgdesc="Provides a CLI for orchestrating and managing container-based networking labs."
arch=('x86_64')
url="https://containerlab.srlinux.dev/"
license=('BSD')
groups=()
depends=('docker')
changelog=
source=("https://github.com/srl-labs/${pkgname}/releases/download/v${pkgver}/${pkgname}_${pkgver}_Linux_amd64.tar.gz")
sha256sums=('161dd88c6bf06d46aac4a69e1a3ea4dab7caed5a01502d93fbcd254e4a2b25b4')

package() {
  # Install Configurations examples
  mkdir -p $pkgdir/etc/$pkgname
  cp -r $srcdir/lab-examples $pkgdir/etc/$pkgname

  # Install Binary
  install -Dm755 $srcdir/containerlab $pkgdir/usr/bin/containerlab
}
