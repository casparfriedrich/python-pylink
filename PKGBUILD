# Maintainer: Caspar Friedrich <c.s.w.friedrich@gmail.com>

pkgname=python-pylink-square
pkgdesc="Python interface for SEGGER J-Link"
pkgver=0.6.0
pkgrel=1
arch=("any")
license=("Apache-2.0")
depends=("python"
         "jlink-software-and-documentation"
         "python-psutil")
makedepends=("python-setuptools")
_pypiname=${pkgname#python-}
url="https://pypi.org/project/pylink-square/"
source=(${_pypiname}-${pkgver}.tar.gz::"https://files.pythonhosted.org/packages/source/${_pypiname::1}/${_pypiname}/${_pypiname}-${pkgver}.tar.gz")
sha256sums=("6b5c2f24c1cbbc0d71e9eb77d1c75d29dfe10b065916ad7320a93e39996cf2b6")

package() {
	cd "${srcdir}/${_pypiname}-${pkgver}"
	python setup.py install --root="${pkgdir}/" --optimize=1
}
