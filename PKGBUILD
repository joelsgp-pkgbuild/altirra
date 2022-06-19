# Maintainer: jmcb <joelsgp@protonmail.com>
pkgname=altirra
pkgver=4.01
pkgrel=1
pkgdesc="Altirra emulator for Atari 8-bit computers, on Wine"
arch=('x86_64')
url="https://www.virtualdub.org/altirra.html"
license=('GPL2')
depends=('wine'
		'wine-mono')
provides=('altirra')
install=altirra.install
source=("https://www.virtualdub.org/downloads/Altirra-$pkgver.zip"
		"http://www.emulators.com/freefile/pcxf380.zip"
		"https://atariage.com/5200/roms/5200.zip"
		"altirra.desktop"
		"altirra.png")
md5sums=("fd513ed987711433cdfd4d836fd2241e"
		"0225dc8bcf2e69fd30c12a226822222a"
		"481cc24c9500c887eca14bef9e203f24"
		"9ad9b26c45020dce1c638a92cda6fe5f"
		"3b6db414cd1df3f383270fb02b45ec72")
validpgpkeys=()

package() {
	dest=$pkgdir/opt/altirra
	mkdir -p $dest
	cp -t $dest Additions.atr Altirra.chm Altirra.exe Altirra64.exe
	cp -r extras/ $dest
	romsdir=$dest/roms
	mkdir -p $romsdir
	cp -t $romsdir 5200.rom ATARIBAS.ROM ATARIOSB.ROM ATARIXL.ROM
	share=$pkgdir/usr/share
	mkdir -p $share/applications
	cp altirra.desktop $share/applications
	mkdir -p $share/icons
	cp altirra.png $share/icons
}
