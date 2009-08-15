# Contributor: Slash <demodevil5[at]yahoo[dot]com>

pkgname=quake3-defrag
pkgver=1.92.01
pkgrel=1
pkgdesc='DeFRaG is a Quake3 modification made specifically for speedruns and trickjumps.'
url='http://defrag.planetquake.gamespy.com/'
license=('GPL')
arch=('i686' 'x86_64')
depends=('quake3')
makedepends=('unzip')
install=
source=("http://q3defrag.org/files/defrag/defrag_${pkgver}.zip" \
'http://www.german-defrag.de/files/defrag/defragpak1.zip' \
'http://www.german-defrag.de/files/defrag/defragpak2.zip' \
'http://www.german-defrag.de/files/defrag/defragpak3.zip' \
'http://www.german-defrag.de/files/defrag/defragpak4.zip' \
'http://www.german-defrag.de/files/defrag/defragpak5.zip' \
'http://www.german-defrag.de/files/defrag/defragcpmpak01.zip' \
'http://www.german-defrag.de/files/defrag/defragpak7.zip' \
'http://www.german-defrag.de/files/defrag/defragpak8.zip' \
'http://www.german-defrag.de/files/defrag/defragpak9.zip' \
'http://www.german-defrag.de/files/defrag/defragpak10.zip' \
'http://www.german-defrag.de/files/defrag/defragpak11.zip')
noextract=("defrag_${pkgver}.zip" 'defragpack1.zip' 'defragpack2.zip' \
'defragpack3.zip' 'defragpack4.zip' 'defragpack5.zip' 'defragcpmpak01.zip' \
'defragpack7.zip' 'defragpack8.zip' 'defragpack9.zip' 'defragpack10.zip' \
'defragpack11.zip')
md5sums=('94f2491b40cbed4e38273c802be2c5e4'
         'a3f16d49be8db65b57fb061cbef42a82'
         '18526ac48731eecf3d7c690e20814302'
         'a166584ff79e0d1d76094b085c02fe5f'
         'd970eb150fccd1c09b3cadc6d4acb421'
         '4a818919a1e06b1173722ffe65cc0b41'
         'ee2d4820b2bd8f615e7be542affe1e1b'
         'f4c7dbc856c20f9a90702d341d6335c4'
         '9dec1f8497a386f9afa2e101d74d8883'
         '0afbcffa260d6c1c83dd467a01b86131'
         '363edf0eae93de429a4577307ffec0fd'
         'fdb9687cbbb5507259c089dfbb3349f0')

build() {
	cd ${srcdir}

	# Base DeFRaG Files
	install -d ${pkgdir}/opt/quake3/
	/usr/bin/unzip defrag_${pkgver}.zip -d ${pkgdir}/opt/quake3/

    # Rename Defrag Directory
    mv ${pkgdir}/opt/quake3/defrag_192 \
        ${pkgdir}/opt/quake3/defrag

	# Install Map Packs
	for i in $(ls defrag{pak,cpmpak}*.zip); do
		/usr/bin/unzip -j $i -d ${pkgdir}/opt/quake3/defrag/
	done
}
