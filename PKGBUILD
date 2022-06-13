pkgname=svlogger
pkgver=1.0.2
pkgrel=1
pkgdesc="A generic svlogd wrapper for runit services"
license=("MIT")
arch=("x86_64")
provides=("svlogger")

package() {
    cd ..
    usrdir="$pkgdir/usr"
    mkdir -p $usrdir
    localddir="$pkgdir/etc/local.d"
    mkdir -p $localddir
    hookdir="$pkgdir/usr/share/libalpm/hooks"
    mkdir -p "$hookdir"
    install -Dm 755 "${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
    install -Dm 755 "${pkgname}.start" "${localddir}/${pkgname}.start"
    install -Dm 644 "99-configure-svlogger.hook" "${hookdir}/99-configure-svlogger.hook"
}
