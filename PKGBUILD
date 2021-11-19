# Maintainer: Fabien POLETTE <fabien.polette@protonmail.com>
pkgname=containerlab
pkgver=0.20.1
pkgrel=1
pkgdesc="Provides a CLI for orchestrating and managing container-based networking labs."
arch=('x86_64')
url="https://containerlab.srlinux.dev/"
license=('BSD')
groups=()
depends=('docker')
changelog=
source=("https://github.com/srl-labs/${pkgname}/releases/download/v${pkgver}/${pkgname}_${pkgver}_Linux_amd64.tar.gz")
sha256sums=('f5d50b6ade5ba2f54510e1887c8cc5a6212c51ba62df8e16e7afcaf17a6f4203')

package() {
  # Install Configurations examples
  mkdir -p $pkgdir/etc/$pkgname
  cp -r $srcdir/lab-examples $pkgdir/etc/$pkgname

  # Install Binary
  install -Dm755 $srcdir/containerlab $pkgdir/usr/bin/containerlab
}
