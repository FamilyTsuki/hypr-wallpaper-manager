# Maintainer: FamilyTsuki
pkgname=hypr-wallpaper-manager-git
pkgver=r1.123456
pkgrel=1
pkgdesc="A wallpaper manager scripts suite for linux-wallpaperengine on Hyprland"
arch=('any')
url="https://github.com/FamilyTsuki/hypr-wallpaper-manager"
license=('GPL3')
depends=('bash' 'jq')
optdepends=(
    'fzf: interactive wallpaper selection'
    'libnotify: desktop notifications'
    'linux-wallpaperengine-git: engine to render wallpapers'
)
provides=('hypr-wallpaper-manager')
conflicts=('hypr-wallpaper-manager')
source=("git+https://github.com/FamilyTsuki/hypr-wallpaper-manager.git")
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/hypr-wallpaper-manager" 2>/dev/null || cd "$srcdir/${pkgname%-git}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/hypr-wallpaper-manager" 2>/dev/null || cd "$srcdir/${pkgname%-git}"
  install -Dm755 src/set-wallpaper "$pkgdir/usr/bin/set-wallpaper"
  install -Dm755 src/wallpaper-daemon "$pkgdir/usr/bin/wallpaper-daemon"
  install -Dm755 src/wallpaper-add "$pkgdir/usr/bin/wallpaper-add"
}
