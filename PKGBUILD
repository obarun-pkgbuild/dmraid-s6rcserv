# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dmraid-s6rcserv
pkgver=0.1
pkgrel=4
pkgdesc="dmraid service for"
arch=(x86_64)
license=('beerware')
depends=('dmraid' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('dmraid.prepare.dependencies'
		'dmraid.prepare.type'
		'dmraid.prepare.up'
		
		'dmraid.oneshot.dependencies'
		'dmraid.oneshot.type'
		'dmraid.oneshot.up'		
		
		'bundle.dmraid.contents'
		'bundle.dmraid.type'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '85bceea1fb94d4166f24496dc40a35e6'
         'b8b36a55438c545b50241c4f1d565ad0'
         'ff36e89238db3549a2153da9b8a5ee35'
         '85bceea1fb94d4166f24496dc40a35e6'
         'aef728bd7f03a5a42dda823d89393350'
         '92a303bf4ce0db59086a8b5577debd49'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dmraid need a maj at dmraid e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dmraid.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Dmraid/contents"
	install -Dm 0644 "$srcdir/bundle.dmraid.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Dmraid/type"
	
	#prepare
	install -Dm 0644 "$srcdir/dmraid.prepare.dependencies" "$pkgdir/etc/s6-serv/available/rc/dmraid-prepare/dependencies"
	install -Dm 0644 "$srcdir/dmraid.prepare.type" "$pkgdir/etc/s6-serv/available/rc/dmraid-prepare/type"
	install -Dm 0644 "$srcdir/dmraid.prepare.up" "$pkgdir/etc/s6-serv/available/rc/dmraid-prepare/up"
	
	# oneshot
	install -Dm 0644 "$srcdir/dmraid.oneshot.dependencies" "$pkgdir/etc/s6-serv/available/rc/dmraid-oneshot/dependencies"
	install -Dm 0644 "$srcdir/dmraid.oneshot.type" "$pkgdir/etc/s6-serv/available/rc/dmraid-oneshot/type"
	install -Dm 0644 "$srcdir/dmraid.oneshot.up" "$pkgdir/etc/s6-serv/available/rc/dmraid-oneshot/up"
	
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dmraid-s6rcserv/LICENSE"
}
