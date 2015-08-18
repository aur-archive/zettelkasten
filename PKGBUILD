# Maintainer: Johann Gruendl <johann.gruendl@gmail.com>
pkgname=zettelkasten
pkgver=3.2.4.3
pkgrel=3
pkgdesc="A java-based tool for managing scientific work with articles or texts following Niklas Luhmann's Zettelkasten"
arch=('any')
url="http://zettelkasten.danielluedecke.de"
# Zettelkasten is now licensed under GPL3, the custom LICENSE has been removed. For further information (in German): http://zettelkasten.danielluedecke.de/wiki/doku.php?id=opensource
license=('GPL3')
install="${pkgname}.install"
depends=('java-runtime' 'x-server' 'xdg-utils')
source=(http://zettelkasten.danielluedecke.de/download/Zettelkasten3_linux.zip
        ${pkgname}16.png
	${pkgname}32.png
        ${pkgname}256.png
        ${pkgname}.sh
        ${pkgname}.desktop
)
package() {
  cd ${srcdir}
  install -D -m755 Zettelkasten.jar ${pkgdir}/usr/share/java/${pkgname}/Zettelkasten.jar

  install -D -m755 ${pkgname}.sh ${pkgdir}/usr/bin/${pkgname}
  install -D -m644 ${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop

  # Installing the icons
  for _i in 16 32 256; do
    install -D -m644 ${pkgname}${_i}.png ${pkgdir}/usr/share/icons/hicolor/${_i}x${_i}/apps/${pkgname}.png
  done
}
md5sums=('03eeab27adcca422e2b53b1fd90997c2'
	 '77538ae0bcde69094be7d4b6228bdf37'
         '8df248cb97efd82415a53dd1ea76fffb'
         'd3ff6ee63d4f614a3e5b999c305530b0'
         '4f9a0427f48a693b38f81c093d55837d'
         '43e3558d7bafad0593f0f5e42b692e20')
