# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dmraid-s6rcserv
pkgver=0.1
pkgrel=3
pkgdesc="dmraid service for s6"
arch=(x86_64)
license=('beerware')
depends=('dmraid' 's6' 's6-rc' 's6-boot')
conflicts=()
install=dmraid-s6rcserv.install
source=('dmraid.prepare.dependencies.s6'
		'dmraid.prepare.type.s6'
		'dmraid.prepare.up.s6'
		
		'dmraid.daemon.dependencies.s6'
		'dmraid.daemon.type.s6'
		'dmraid.daemon.up.s6'		
		
		'bundle.dmraid.contents.s6'
		'bundle.dmraid.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '85bceea1fb94d4166f24496dc40a35e6'
         'b8b36a55438c545b50241c4f1d565ad0'
         'ff36e89238db3549a2153da9b8a5ee35'
         '85bceea1fb94d4166f24496dc40a35e6'
         'aef728bd7f03a5a42dda823d89393350'
         'a04094373200f62ae73b1d43cb55cf2c'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dmraid need a maj at dmraid e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dmraid.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dmraid/contents"
	install -Dm 0644 "$srcdir/bundle.dmraid.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dmraid/type"
	
	#prepare
	install -Dm 0644 "$srcdir/dmraid.prepare.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dmraid-prepare/dependencies"
	install -Dm 0644 "$srcdir/dmraid.prepare.type.s6" "$pkgdir/etc/s6-serv/available/rc/dmraid-prepare/type"
	install -Dm 0644 "$srcdir/dmraid.prepare.up.s6" "$pkgdir/etc/s6-serv/available/rc/dmraid-prepare/up"
	
	# daemon
	install -Dm 0644 "$srcdir/dmraid.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dmraid-daemon/dependencies"
	install -Dm 0644 "$srcdir/dmraid.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/dmraid-daemon/type"
	install -Dm 0644 "$srcdir/dmraid.daemon.up.s6" "$pkgdir/etc/s6-serv/available/rc/dmraid-daemon/up"
	
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dmraid-s6rcserv/LICENSE"
}
