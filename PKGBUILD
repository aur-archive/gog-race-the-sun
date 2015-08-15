# Maintainer : TimorLee

pkgname=gog-race-the-sun
pkgver=1.1.0.3
pkgrel=1
pkgdesc="You are a solar powered craft, racing against the sunset at insane speeds. GOG linux game package required"
arch=("i686" "x86_64")
url="http://www.gog.com/game/race_the_sun"
license=("custom")
groups=("games")
source=("gog_race_the_sun_${pkgver}.tar.gz" "gog-race-the-sun")
md5sums=('401a3a9a23009de19e838b1ddbaec26a'
         'b1d8be9f1d33bd6066e2834febfb2687')
depends=(libgl libx11 libxext desktop-file-utils)
#options=('!strip')
PKGEXT=.pkg.tar

package() {
  mkdir -p "${pkgdir}"/opt/gog/race-the-sun
  cp -r "${srcdir}"/Race\ The\ Sun/* "${pkgdir}"/opt/gog/race-the-sun
  install -Dm644 "${srcdir}"/Race\ The\ Sun/support/gog-race-the-sun-primary.desktop "${pkgdir}"/usr/share/applications/gog-race-the-sun.desktop
  install -Dm644 "${srcdir}"/Race\ The\ Sun/support/gog-race-the-sun.png "${pkgdir}"/usr/share/pixmaps/gog-race-the-sun.png
  install -Dm644 "${srcdir}"/Race\ The\ Sun/docs/End\ User\ License\ Agreement.txt "${pkgdir}"/usr/share/licenses/$pkgname/LICENSE
  install -Dm755 "${srcdir}/gog-race-the-sun" "${pkgdir}/usr/bin/gog-race-the-sun"
}
