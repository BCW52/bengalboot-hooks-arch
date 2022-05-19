pkgname=bengalboot-hooks
pkgver=1
pkgrel=1
pkgdesc='Bengalboot pacman hooks'
arch=('any')
license=('GPL3')
url=https://github.com/BCW52
depends=(libnotify)

source=(https://github.com/BCW52/bengalboot-hooks/archive/refs/heads/main.zip)
sha512sums=('f1ff92434699e7d044728e2da59bae6b3b347e56c0bbb55295d4a0f0809efa0acb8acee6ec3deff1b571d4c16b2919c42ed1506b069d1bc2961f72cb0e33e95f')

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
