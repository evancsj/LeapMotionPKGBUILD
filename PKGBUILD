#intainer: Helge Rausch <helge@rausch.io>
# This script is licensed under the MIT license.
# https://gist.github.com/tsujigiri/5476281
#
# Fork Maintainer: DoveDev
# https://gist.github.com/DoveDev/
#
## Installation
# prerequisite: set up the INTEGRITY_CHECK option in /etc/makepkg.conf for sha256.
#
# To install the Leap software, you first need to download the Public .tgz for Linux
# from https://www.leapmotion.com/setup Unpack it, place the included .deb files in the same
# directory as this PKGBUILD and run `makepkg`. If all goes well this will
# create a package file, which can be installed by running:
#
# yaourt -U leap-2.1.5+22699-x86_64.pkg.tar.xz
#
# or
#
# yaourt -U leap-2.1.5+22699-i686.pkg.tar.xz
#
# depending on your architecture.
#
## Running Leap Motion
# Use the following commands to run the Leap Motion deamon and LeapMotion Control Panel
# 
# sudo leapd
# 
# LeapControlPanel
#
pkgname=leap
pkgver=2.3.1+31549
pkgrel=1
pkgdesc="Installs the Debian package from the Leap public to Arch Linux"
arch=('i686' 'x86_64')
url="https://www.leapmotion.com/setup"
depends=('mesa' 'libxxf86vm')
license=('unknown')
options=(debug !strip)
_arch='x86' 		
sha256sums=('9c88f9d99bd84227b1d6a7fa4434e951c1f4f3d34a1f07ca587cf419c623032c')
 
source=("Leap-${pkgver}-${_arch}.deb")
 
package() {
export LD_PRELOAD=/lib/libfakeroot/libfakeroot.so
tar -Jxvf data.tar.xz -C "${pkgdir}"
}


