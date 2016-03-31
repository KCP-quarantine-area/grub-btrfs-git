pkgname=grub-btrfs-git
_pkgname=grub-btrfs
pkgrel=1
pkgver=1.7.2.r4.g6ae56db
pkgdesc="grub-btrfs, add support for btrfs snapshots into grub menu"
arch=('x86_64')
url="https://github.com/Antynea/grub-btrfs"
license=('GPL3')
depends=('btrfs-progs' 'bash' 'grub')
backup=('etc/grub.d/41_snapshots-btrfs')
source=(${_pkgname}'::git+https://github.com/Antynea/grub-btrfs.git')
sha512sums=('SKIP')

pkgver() {
  cd "${srcdir}/${_pkgname}"
  git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
	install -Dm 755 "${srcdir}/${_pkgname}/41_snapshots-btrfs" "${pkgdir}/etc/grub.d/41_snapshots-btrfs"
}
