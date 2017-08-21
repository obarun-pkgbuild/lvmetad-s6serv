# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=lvmetad-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="lvmetad service for s6"
arch=(x86_64)
license=('beerware')
depends=('lvm2' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('lvmetad.daemon.run.s6'
		'lvmetad.log.run.s6'
		'lvmetad.logd'
		'LICENSE')
md5sums=('6453edb17839c10895e4d6bf1d147e95'
         '97b51885b7a846aaa36838ca1917ba2e'
         '49db630b6713c1257a20cc208835569e'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/lvmetad.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/lvmetad/run"
	
	# log
	install -Dm 0755 "$srcdir/lvmetad.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/lvmetad/log/run"
	install -Dm 0644 "$srcdir/lvmetad.logd" "$pkgdir/etc/s6-serv/log.d/lvmetad"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/lvmetad-s6serv/LICENSE"
}
