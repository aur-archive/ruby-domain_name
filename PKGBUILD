# Contributor: Emiliano Vavassori <syntaxerrormmm@gmail.com>
# Maintainer: Emiliano Vavassori <syntaxerrormmm@gmail.com>
pkgname=ruby-domain_name
_gemname=domain_name
pkgver=0.5.24
pkgrel=1
pkgdesc="Domain Name manipulation library for Ruby."
arch=('any')
url="https://github.com/knu/ruby-domain_name"
license=('MIT')
depends=('ruby' 'ruby-unf>=0.0.5' 'ruby-unf<1')
makedepends=('ruby')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('e0dd8cf5599148233aebf08869328df2')

package() {
  cd "${srcdir}"
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  
  gem install --ignore-dependencies --no-user-install -f -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem
}
