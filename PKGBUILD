# Maintainer: Caspar Friedrich <c.s.w.friedrich@gmail.com>

pkgname=python-pylink-square
pkgdesc="Python interface for SEGGER J-Link"
pkgver=0.4.0
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
sha256sums=("88e2bef11c33955f7eb74b362454cbbe56210f26035ce9e1c0a6d44ab77f9761")

package() {
	cd "${srcdir}/${_pypiname}-${pkgver}"
	python setup.py install --root="${pkgdir}/" --optimize=1
}
