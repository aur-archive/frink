pkgname=frink
pkgver=latest
pkgrel=1
pkgdesc="Calculating tool and programming language with support for units of measure."
arch=('any')
url="http://futureboy.us/frinkdocs/"
license=('unknown')
depends=(java-runtime)
source=("http://futureboy.us/frinkjar/frink.jar" "frink.desktop")
md5sums=(SKIP 'e75a88d2bca81bd054d47c3f121e4d5f')

package() {
	cd $srcdir

	install -m755 -D frink.jar "$pkgdir/usr/share/java/frink.jar"
	install -m644 -D frink.desktop "$pkgdir/usr/share/applications/frink.desktop"

	mkdir $pkgdir/usr/bin

	echo '#!/bin/sh
	"$JAVA_HOME/bin/java" -jar /usr/share/java/frink.jar $@' > "$pkgdir/usr/bin/frink"
	chmod +x "$pkgdir/usr/bin/frink"
}
