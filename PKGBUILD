# Maintainer: evr <evanroman @ gmail>
# Contributer: fnord0
pkgname=metagoofil
pkgver=1.4b
pkgrel=1
pkgdesc="An information gathering tool designed for extracting metadata of public documents"
url="http://www.edge-security.com/metagoofil.php"
arch=('i686' 'x86_64')
license=('GPLv2')
depends=('libextractor' 'python')
source=("http://www.edge-security.com/soft/${pkgname}-${pkgver}.tar")
md5sums=('ef1cd2a73338d69faaf2acad57c02fa0')
sha1sums=('be6e96ce2d2cd01829f5544591b5d309277ac625')

build() {
    cd ${srcdir}/${pkgname}
    install -d ${pkgdir}/usr/bin || return 1
    install -d ${pkgdir}/usr/share/${pkgname}/doc || return 1
    install -d ${pkgdir}/usr/share/licenses/${pkgname} || return 1
    install -Dm755 ${srcdir}/${pkgname}/${pkgname}.py ${pkgdir}/usr/share/${pkgname}/${pkgname}.py || return 1
    install -Dm644 README ${pkgdir}/usr/share/${pkgname}/doc/README || return 1
    install -Dm644 COPYING ${pkgdir}/usr/share/licenses/${pkgname}/COPYING || return 1
    install -Dm644 LICENSES ${pkgdir}/usr/share/licenses/${pkgname}/LICENSES || return 1
    ln -sf /usr/share/${pkgname}/${pkgname}.py ${pkgdir}/usr/bin/${pkgname}.py || return 1
}


