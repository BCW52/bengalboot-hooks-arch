pkgname=bengalboot-hooks
pkgver=1
pkgrel=2
pkgdesc='Bengalboot pacman hooks'
arch=('any')
license=('GPL3')
url=https://github.com/BCW52
depends=(libnotify)

source=(https://github.com/BCW52/bengalboot-hooks/archive/refs/heads/main.zip)
sha512sums=('7f2d3f2b5f2f41976acadf7e92b4a99d61f826c0e66a962353be435900cef544b04646a6662301d54def06ff9aac42b309edcdabf272eaf9cc08db8c579de6c8')

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
