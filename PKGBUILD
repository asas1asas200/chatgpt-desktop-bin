# Maintainer: asas1asas200 <asas1asas200@gmail.com>
pkgname="chatgpt-desktop-bin"
pkgver="0.11.1"
pkgrel=1
pkgdesc="ChatGPT Desktop Application (Mac, Windows and Linux)"
arch=("x86_64")
url="https://github.com/lencx/ChatGPT"
makedepends=("binutils"
             "tar")
depends=("openssl-1.1"
         "webkit2gtk"
         "libayatana-appindicator")
provides=("chatgpt-desktop=${pkgver}")
conflicts=('chatgpt-desktop')
license=("Apache")
source=("https://github.com/lencx/ChatGPT/releases/download/v${pkgver}/ChatGPT_${pkgver}_linux_${arch}.deb")
sha256sums=('07c9ec6aaf7f6555687b3c3624d320dfa58f591e4af3b4d932a85933e26bc779')
noextract=("chat-gpt_${pkgver}_amd64.deb")

prepare() {
	ar p ChatGPT_${pkgver}_linux_${arch}.deb data.tar.gz | tar zx
}

package() {
	cd $srcdir
	cp -R usr ${pkgdir}
}

