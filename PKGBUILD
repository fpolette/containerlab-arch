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
sha256sums=('dbe4629474a01ec67952b0a176d5766941c3a5dc615f806679e6a0ebf37ea979')

package() {
  # Install Configurations examples
  mkdir -p $pkgdir/etc/$pkgname
  cp -r $srcdir/lab-examples $pkgdir/etc/$pkgname

  # Install Binary
  install -Dm755 $srcdir/containerlab $pkgdir/usr/bin/containerlab
}
