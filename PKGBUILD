# Maintainer: ThunderMikey

pkgname=lifxlan-git
_pkgname="lifxlan"
pkgver=386.ba51118
pkgrel=1
pkgdesc="Python library for accessing LIFX devices locally using the official LIFX LAN protocol"
arch=(any)
url="https://github.com/mclarkk/lifxlan"
provides=('lifxlan')
license=('MIT')
depends=(
  'python'
  'python-requests'
  'python-setuptools'
	'python-bitstring'
	'python-netifaces'
)
conflicts=()
source=("${_pkgname}::git+${url}.git")
md5sums=('SKIP')

src_git_dir="$srcdir/${_pkgname}"

pkgver() {
  cd "$srcdir/${_pkgname}"
	echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd "$srcdir/${_pkgname}"
  python setup.py install --root="$pkgdir/"
}
