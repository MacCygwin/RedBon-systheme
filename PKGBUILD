pkgname=redbon-catppuccin
pkgver=2026.02.11
pkgrel=1
pkgdesc="Install catppuccin themes with ease on RedBon"
arch=('x86_64')
license=('MIT')
options=('!strip')
install=redbon-catppuccin.install

package() {
    install -d "$pkgdir/usr/share/themes"
    cp -r "$srcdir/themes/Catppuccin-Dark-Macchiato" "$pkgdir/usr/share/themes/"


    install -d "$pkgdir/usr/share/icons"
    cp -r "$srcdir/icons/Catppuccin-Macchiato" "$pkgdir/usr/share/icons/"

    install -d "$pkgdir/usr/share/redbon-qt"
    cp -r "$srcdir/redbon-qt/." "$pkgdir/usr/share/redbon-qt"
}

