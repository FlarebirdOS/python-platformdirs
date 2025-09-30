pkgname=python-platformdirs
pkgver=4.4.0
pkgrel=1
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
sha256sums=(1a8b4ecad7df48f3b68c77709f6b2c3c951f8705fe9b1f2a83b9c8e5dc11b733)

build() {
    cd ${pkgname#*-}

    python3 -m build --wheel --no-isolation
}

package() {
    cd ${pkgname#*-}

    python3 -m installer -d ${pkgdir} dist/*.whl
}
