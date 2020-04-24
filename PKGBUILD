pkgname=dmenu-kirito
gitname=dmenu
pkgver=4.9
pkgrel=1
pkgdesc='Menu for X11'
arch=('x86_64')
source=('git+https://github.com/SearyBlue/dmenu')
sha1sums=('SKIP')
provides=('dmenu')
conflicts=('dmenu' 'dmenu-git')
build() 
{
	cd "$srcdir/$gitname"
	cat ~/.config/dmenu/config.h > config.h
        make
}

package() 
{
  	cd "$srcdir/$gitname"
  	make PREFIX=/usr DESTDIR="${pkgdir}" install
}
