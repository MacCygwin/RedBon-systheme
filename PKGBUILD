pkgname=redbon-systheme
pkgver=2026.06.11
pkgrel=1
pkgdesc="Overall Theme/Icons(Qt, GTK) for RedBon Desktop"
arch=('x86_64')
license=('MIT')
options=('!strip')
depends=('nwg-look' 'qt5ct' 'qt6ct' 'papirus-icon-theme')

package() {
  local theme="$srcdir/themes/Catppuccin-Dark-Macchiato"
  [ -d "$theme" ] || { echo "src/themes/Catppuccin-Dark-Macchiato is missing"; return 1; }

  install -d "$pkgdir/usr/share/themes"
  cp -a "$theme" "$pkgdir/usr/share/themes/"

  find "$pkgdir/usr/share/themes" -type d -exec chmod 755 {} +
  find "$pkgdir/usr/share/themes" -type f -exec chmod 644 {} +

  # system-wide Qt colour schemes: qt5ct and qt6ct list these in their own settings
  install -Dm644 "$srcdir/redbon-qt/qt5ct/colors/Catppuccin-Macchiato.conf" \
    "$pkgdir/usr/share/qt5ct/colors/Catppuccin-Macchiato.conf"
  install -Dm644 "$srcdir/redbon-qt/qt6ct/colors/Catppuccin-Macchiato.conf" \
    "$pkgdir/usr/share/qt6ct/colors/Catppuccin-Macchiato.conf"
}

