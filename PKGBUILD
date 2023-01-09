# Maintainer: Paulo Corrêa Creto <pcreto2020@gmail.com>

pkgbasename=PauloBCreto-wallpapers
pkgname=${pkgbasename}-git
pkgver=r1
pkgrel=1
pkgdesc="Wallpapers by PauloBCreto"
url="https://github.com/PauloBCreto/wallpapers.git"
license=('GNU General Public License v3.0')
arch=('any')
source=("$pkgbasename::git+https://github.com/PauloBCreto/wallpapers.git")
sha256sums=('SKIP')

pkgver() {
  cd "$pkgbasename"
  echo "r$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

package() {
  cd "$pkgbasename"

  install -d "${pkgdir}"/usr/share/backgrounds/"${pkgbasename}"

  cp -dr --no-preserve=ownership "${pkgdir}"/usr/share/backgrounds/"${pkgbasename}"

  install -Dm644 LICENSE -t "$pkgdir"/usr/share/licenses/"$pkgbasename"/
}
