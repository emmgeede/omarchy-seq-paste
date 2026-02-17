# Maintainer: emmgee
pkgname=omarchy-seq-paste
pkgver=1.0.0
pkgrel=1
pkgdesc="Sequential copy/paste (FIFO clipboard) for Hyprland, inspired by macOS Pastebot"
arch=(any)
url="https://aur.archlinux.org/packages/omarchy-seq-paste"
license=(MIT)
depends=(wl-clipboard inotify-tools ghostty libnotify hyprland)
source=(
  "omarchy-seq-paste"
  "hyprland-bindings.conf"
  "hyprland-rules.conf"
  "LICENSE"
)
sha256sums=(
  '3a681374032904154dbcc2b72d04586874d654d4cc75d200ce2ba2a52495a578'
  'b13f5dc79123566c9496c8fe70495235f6e1854d71642e5e7c54972fc837c260'
  '6962999cc4e6bef579fd927539d4f83d673a05a69ff58d05bafcbd056ce3506a'
  '3c13098a9c569d1e158a80125981f3023092f6e69755743d90aa19b22e506a28'
)

package() {
  install -Dm755 "$srcdir/omarchy-seq-paste" "$pkgdir/usr/bin/omarchy-seq-paste"
  install -Dm644 "$srcdir/hyprland-bindings.conf" "$pkgdir/usr/share/omarchy-seq-paste/hyprland-bindings.conf"
  install -Dm644 "$srcdir/hyprland-rules.conf" "$pkgdir/usr/share/omarchy-seq-paste/hyprland-rules.conf"
  install -Dm644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/omarchy-seq-paste/LICENSE"
}
