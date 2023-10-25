pkgname=ksysguardd-powercap
pkgver=1
pkgrel=1
pkgdesc="Program for exposing device power data available in Linux kernel's powercap API to ksysguard"
arch=('any')
license=('MIT')
url="https://github.com/sandy-8925/ksysguardd-powercap/"
source=("git+https://github.com/sandy-8925/ksysguardd-powercap.git")
makedepends=(git cmake)
sha512sums=(SKIP)

build() {
    cmake -B build -S $pkgname \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr
  cmake --build build
}

package() {
    DESTDIR="$pkgdir" cmake --install build
}
