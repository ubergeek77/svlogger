pkgname=svlogger
pkgver=1.0.0
pkgrel=1
pkgdesc="A generic svlogd wrapper for runit services"
url="https://github.com/ubergeek77/svlogger"
license=("MIT")
source=("git+$url")
md5sums=('SKIP')
arch=("x86_64")
provides=("svlogger")

package() {
    cd $pkgname
    usrdir="$pkgdir/usr"
    mkdir -p $usrdir
    localddir="$pkgdir/etc/local.d"
    mkdir -p $localddir
    install -Dm 755 "${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
    install -Dm 755 "${pkgname}.start" "${localddir}/${pkgname}.start"
}
