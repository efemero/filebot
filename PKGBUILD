# Maintainer: Roman Vasilev <2rvasilev@live.ru>
# Maintainer: max.bra <max dot bra at alice dot it>
# Contributor: nadolph
# Contributor: dcelasun
# Contributor: said
# Contributor: Kaurin <milos dot kaurin at gmail>
# Contributor: Nathan Owe <ndowens04 at gmail>
# Contributor: Bernhard Bermeitinger <bernhard.bermeitinger at gmail.com>
# Contributor: François Bastien <fmrbastien at gmail dot com>

pkgname=filebot
pkgver=5.1.2
pkgrel=1
pkgdesc="The ultimate TV and Movie Renamer"
arch=('i686' 'x86_64' 'aarch64' 'armv7l' 'armv7h')
url="https://www.filebot.net/"
license=('Commercial')
depends=('jre17-openjdk' 'fontconfig' 'chromaprint')
makedepends=()
checkdepends=()

optdepends=('libzen: Required by libmediainfo'
            'libmediainfo: Read media info such as video codec, resolution or duration'
            'gvfs: Drag-n-Drop from GVFS remote filesystems')

provides=('filebot')

conflicts=('filebot47' 'filebot-git')
install=$pkgname.install
source=(
    "https://get.filebot.net/filebot/FileBot_${pkgver}/FileBot_${pkgver}-aur.tar.xz"
    "https://get.filebot.net/filebot/FileBot_${pkgver}/FileBot_${pkgver}-aur.tar.xz.asc"
    "filebot.sh"
)

sha256sums=('f8acf7af5d6aa992b6aed1d41caf484cae967ed6cb0d501656ba82d3f22c736a'
            'SKIP'
            '7876c203315d8f6f59ed4c71ef22594fad19cb0bff7044d0cf724a25ce137d7c')
validpgpkeys=('B0976E51E5C047AD0FD051294E402EBF7C3C6A71')

package() {
  mkdir -p "${pkgdir}/usr/bin"
  mkdir -p "${pkgdir}/usr/share/${pkgname}"
 
  install -Dm755 "${pkgname}.sh" "${pkgdir}/usr/bin/${pkgname}"

  cp -dpr --no-preserve=ownership "${srcdir}/etc" "${srcdir}/usr" "${pkgdir}"
}
