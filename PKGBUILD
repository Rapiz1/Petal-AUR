# Maintainer:
# g1eny0ung <g1eny0ung@gmail.com>
# rapiz <contact@rapiz.me>
# lxs137 <lxs137@hotmail.com>
pkgname=petal-bin
pkgver=2.20.0
pkgrel=1
epoch=
pkgdesc="A Douban.FM Client With Extra"
arch=('x86_64')
url="https://ilime.github.io/Petal/"
license=('MIT')
groups=()
depends=('gtk3' 'nss' 'libxss')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/ilime/Petal/releases/download/v$pkgver/Petal-$pkgver.tar.gz"
        'https://raw.githubusercontent.com/ilime/Petal/dev/LICENSE'
        'petal.svg'
        'Petal.desktop'
        'petal.sh'
)
noextract=()
validpgpkeys=()
md5sums=('41c8c259ff57c36749f6615105c33937'
         'cebd0dda9b913e6254f5e09a257955bb'
         'a4f3cb91573bbc3fce9466350ddfb4d2'
         'e946f427355b1a85454b74e7ca918072'
         '5c3aace4646132860b8084cbbb55ad55')

package() {
    mkdir -p "$pkgdir/usr/lib"
    cp -r "$srcdir/Petal-$pkgver" "$pkgdir/usr/lib/petal"
    
    install -Dm755 "$srcdir/petal.sh" "$pkgdir/usr/bin/petal"
    install -Dm644 "$srcdir/Petal.desktop" -t "$pkgdir/usr/share/applications/"

    ICON="$srcdir/petal.svg"
    install -Dm644 "$ICON" "$pkgdir/usr/share/icons/hicolor/scalable/apps/petal.svg"

    install -Dm644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/petal/LICENSE"
}
