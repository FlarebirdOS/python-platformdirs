pkgname=python-platformdirs
pkgver=4.5.0
pkgrel=2
pkgdesc="A library to determine platform-specific system directories"
arch=('x86_64')
url="https://github.com/tox-dev/platformdirs"
license=('MIT')
depends=('python')
makedepends=(
    'git'
    'python-build'
    'python-installer'
    'python-hatchling'
    'python-hatch-vcs'
)
source=(git+ssh://git@github.com/tox-dev/platformdirs#tag=${pkgver})
sha256sums=(9cc50d3842ebb08103c6fb9bba26e55653455a1a902d8bbeb57659950b39ba65)

build() {
    cd ${pkgname#*-}

    python3 -m build --wheel --no-isolation
}

package() {
    cd ${pkgname#*-}

    python3 -m installer -d ${pkgdir} dist/*.whl
}
