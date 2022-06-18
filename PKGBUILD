pkgname='zsh-prompt-simple'
pkgver='1.0.0'
pkgrel=1
pkgdesc='zsh prompt displaying the present working directory'
arch=('any')
url="https://github.com/atanvarno69/${pkgname}"
license=('MIT')
depends=('zsh')
makedepends=('git')
source=("${pkgname}-${pkgver}.tar.gz::https://api.github.com/repos/atanvarno69/${pkgname}/tarball/${pkgver}")
sha256sums=('SKIP')

pkgver() {
    curl -s "https://api.github.com/repos/atanvarno69/${pkgname}/releases/latest" | grep '"name":' | sed 's/\s*"name":\s"\([a-zA-Z0-9_\.]*\)",/\1/'
}

package() {
    cd "${pkgname}-${pkgver}"
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    cp -f LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/"
    cp -f prompt_simple_setup "${pkgdir}/usr/share/zsh/Prompts/"
}
