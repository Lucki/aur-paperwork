# Maintainer: Fabien Dubosson <fabien.dubosson@gmail.com>
# Contributor: Francois Boulogne <fboulogne@april.org>

pkgname=paperwork
pkgver=0.3.2
pkgrel=2
pkgdesc='A tool to make papers searchable - scan & forget'
arch=('any')
url='https://github.com/jflesch/paperwork'
license=('GPL3')
depends=('pygobject2-devel' 'pygtk' 'python2-pycountry'
         'python2-poppler' 'python2-pyinsane<2' 'python2-pyocr'
         'python2-levenshtein' 'python2-whoosh' 'python2-pyenchant'
         'python2-joblib' 'python2-numpy' 'python2-scipy' 'python2-scikit-learn'
         'python2-scikit-image' 'python2-gobject' 'python2-nltk'
         'python2-termcolor' 'python2-simplebayes' 'glade'
         'gnome-icon-theme-symbolic' 'gnome-icon-theme')
makedepends=('python2' 'python2-setuptools')
optdeps=('cuneiform: alternativer OCR')
source=("https://github.com/jflesch/paperwork/archive/${pkgver}.zip")
md5sums=('52986efafb82a5c34382c7d483a7afeb')
install=paperwork.install

build() {
  cd "${pkgname}-${pkgver}"
  python2 setup.py build
}

package() {
  cd "${pkgname}-${pkgver}"
  python2 setup.py install --prefix=/usr --root="${pkgdir}" --optimize=1
  install -D -m644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
