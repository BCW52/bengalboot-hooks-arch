pkgname=bengalboot-hooks
pkgver=1.4.20
pkgrel=1
pkgdesc='Bengalboot pacman hooks'
arch=('any')
license=('GPL3')
url=https://github.com/BCW52
depends=(libnotify)

source=(https://github.com/BCW52/bengalboot-hooks/archive/refs/heads/main.zip)
sha512sums=('8870a4376d824415a58558e6cfb5c5136d5c3d8215d223dddcd9c6154966b107bad656fb95eb761e6d1f7d5a3e95e8ad68402de8aac9a91fc3c4c1c02742a202')

package() {
  local hooks=$pkgdir/usr/share/libalpm/hooks
  local bin=$pkgdir/usr/bin

  install -Dm644 bengalboot-hooks-main/bengal-lsb-release.hook      $hooks/bengal-lsb-release.hook
  install -Dm644 bengalboot-hooks-main/bengal-os-release.hook       $hooks/bengal-os-release.hook
  install -Dm644 bengalboot-hooks-main/bengal-hooks.hook            $hooks/bengal-hooks.hook
  install -Dm644 bengalboot-hooks-main/bengal-reboot-required.hook  $hooks/bengal-reboot-required.hook

  install -Dm755 bengalboot-hooks-main/bengal-reboot-required       $bin/bengal-reboot-required
  install -Dm755 bengalboot-hooks-main/bengal-reboot-required2      $bin/bengal-reboot-required2
  install -Dm755 bengalboot-hooks-main/bengal-hooks-runner          $bin/bengal-hooks-runner
}
