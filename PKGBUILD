# Maintainer: Caspar Friedrich <c.s.w.friedrich@gmail.com>

pkgname=python-pylink-square
pkgdesc="Python interface for SEGGER J-Link"
pkgver=0.3.0
pkgrel=1
arch=("any")
license=("Apache-2.0")
depends=("python"
         "jlink-software-and-documentation>=6.0b"
         "python-psutil")
makedepends=("python-setuptools")
_pypiname=${pkgname#python-}
url="https://pypi.org/project/${_pypiname}"
source=(${_pypiname}-${pkgver}.tar.gz::"https://files.pythonhosted.org/packages/source/${_pypiname::1}/${_pypiname}/${_pypiname}-${pkgver}.tar.gz")
sha256sums=("ee3208e9a78e7fb81d8bc0b9e81d03ead3cce96a1a6b46caa3b82aad7d2747a8")

package() {
	cd "${srcdir}/${_pypiname}-${pkgver}"
	python setup.py install --root="${pkgdir}/" --optimize=1
}
