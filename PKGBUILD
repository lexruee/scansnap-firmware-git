
_pkgname=scansnap-firmware
pkgname="${_pkgname}-git" 
pkgver=r12.8b31a6a
pkgrel=1
pkgdesc="Firmware for the Scansnap S1300 scanner" 
arch=('x86_64')
url="https://github.com/lexruee/scansnap-firmware"
license=('Unknown')
groups=()
depends=()
makedepends=('git' 'make') 
options=()
install=
source=("${pkgname}::git+https://github.com/lexruee/scansnap-firmware.git")
noextract=()
md5sums=('SKIP')

pkgver() {
	cd "$srcdir/${pkgname}"
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$srcdir/${pkgname}"
	make install DESTDIR="$pkgdir/"
}
