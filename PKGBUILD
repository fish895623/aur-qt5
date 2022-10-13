# Maintainer: fish895623 <dan990429@gmail.com>

pkgname=qt5
pkgver=v5.15.6
pkgrel=0
arch=(x86_64)
depends=(
    libxcb
    xcb-proto
    xcb-util
    xcb-util-image
    xcb-util-wm
    libxi
)
makedepends=(
    git
)

build() {
    git clone --recurse-submodules --jobs=$(nproc) --branch v5.15.6-lts-lgpl https://code.qt.io/qt/qt5.git
}

package() {
    ./configure -opensource -confirm-license -nomake examples -nomake tests
    make -j$(nproc)
}
