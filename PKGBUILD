pkgname=vim-unite
pkgver=6.1
pkgrel=1
pkgdesc="Unite and create user interfaces"
arch=('any')
url="https://github.com/Shougo/unite.vim"
license=('MIT')
depends=('vim>=7.0' 'vim-vital-git')
optdepends=('vim-vimproc: for various unite sources')
groups=('vim-plugins')
install=vimdoc.install
source=($pkgname-$pkgver.tar.gz::"https://github.com/Shougo/unite.vim/archive/ver.$pkgver.tar.gz")
sha1sums=('49d9e5443dbd89d4050ac9da3d8c26d92023415a')

package() {
	cd "$srcdir/unite.vim-ver.$pkgver"

	installpath="${pkgdir}/usr/share/vim/vimfiles"

	install -d $installpath/{autoload/unite,plugin/unite}
	install -d $installpath/autoload/unite/{filters,kinds,sources/buffer}
	install -d $installpath/autoload/vital/_unite/{Data,System,Vim}
	install -Dm644 autoload/unite.vim $installpath/autoload/
	install -Dm644 autoload/unite/*.vim $installpath/autoload/unite/
	install -Dm644 autoload/unite/filters/* $installpath/autoload/unite/filters/
	install -Dm644 autoload/unite/kinds/* $installpath/autoload/unite/kinds/
	install -Dm644 autoload/unite/sources/*.vim $installpath/autoload/unite/sources/
	install -Dm644 autoload/unite/sources/buffer/* $installpath/autoload/unite/sources/buffer/
	install -Dm644 autoload/vital/*.vi* $installpath/autoload/vital/
	install -Dm644 autoload/vital/_unite/*.vim $installpath/autoload/vital/_unite/
	install -Dm644 autoload/vital/_unite/Data/* $installpath/autoload/vital/_unite/Data/
	install -Dm644 autoload/vital/_unite/System/* $installpath/autoload/vital/_unite/System/
	install -Dm644 autoload/vital/_unite/Vim/* $installpath/autoload/vital/_unite/Vim/
	install -Dm644 doc/unite.txt $installpath/doc/unite.txt
	install -Dm644 plugin/unite.vim $installpath/plugin/unite.vim
	install -Dm644 plugin/unite/* $installpath/plugin/unite/
	install -Dm644 syntax/unite.vim $installpath/syntax/unite.vim
}
