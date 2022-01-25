# Maintainer: Michal Krenek (Mikos) <m.krenek@gmail.com>
pkgname=cryptboot
pkgver=1.1.0
pkgrel=1
pkgdesc="Encrypted boot partition manager with UEFI Secure Boot support"
arch=('any')
url="https://github.com/xmikos/cryptboot"
license=('GPL3')
depends=('cryptsetup' 'grub' 'efibootmgr' 'efitools' 'sbsigntools')
source=(https://github.com/xmikos/cryptboot/archive/v$pkgver.tar.gz)

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm755 cryptboot "$pkgdir/usr/bin/cryptboot"
  install -Dm755 cryptboot-efikeys "$pkgdir/usr/bin/cryptboot-efikeys"
  install -Dm755 grub-install "$pkgdir/usr/local/bin/grub-install"
  install -Dm644 cryptboot.conf "$pkgdir/etc/cryptboot.conf"
}

# vim:set ts=2 sw=2 et:
