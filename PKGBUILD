# Maintainer: Jan Boelsche <jan@lagomorph.de>

pkgname='persist-ssh-host-keys'
pkgver=1.0
pkgrel=4
pkgdesc="stores ssh host keys under /var/ssh/host-keys instead of /etc/ssh"
packager='Jan Boelsche'
arch=('any')
license=('GPL')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
install=${pkgname}.install
source=(
  "${pkgname}.service"
  "${pkgname}"
)

sha256sums=('d5d802e091c8dbc65047c57137824f50007be2d4a751c0bc66d4e42e351d9e1c'
            '83eb699516dd68732e060b12f0d11aabf21978065197aff144de6999f77e408f')

package() {
  mkdir -p "${pkgdir}/usr/lib/systemd/system"
  install -Dm 644 "${pkgname}.service" "${pkgdir}/usr/lib/systemd/system"
  install -Dm 744 -t "${pkgdir}/usr/bin" "${pkgname}" 
}
