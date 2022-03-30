# MYD-C8MMX
```
sudo nano /etc/apt/sources.list
apt-cache search exfat
sudo apt install exfat-utils
exit
ll /media
mkdir -p ~/MYD-C8MMX-devel
export DEV_ROOT=~/MYD-C8MMX-devel
cd MYD-C8MMX-devel/
ll
cd 03-Tools/
ls
cd ToolsChain/
chmod +x myir-imx-xwayland-glibc-x86_64-meta-toolchain-aarch64-toolchain-4.14-sumo.sh
./myir-imx-xwayland-glibc-x86_64-meta-toolchain-aarch64-toolchain-4.14-sumo.sh
source /media/hufan/myir-imx-xwayland/4.14-sumo/environment-setup-aarch64-poky-linux
source /media/hufan/environment-setup-aarch64-poky-linux 
echo $CC
ll
cd ..
;;
ll
cd repo
cd Repo/
ls
cat repo 
chmod +x repo
./repo
cd $DEV_ROOT
ls
cd 04-Sources/
ls
tar -xvf MYIR-i.MX8MM-Uboot.tar.gz 
cd MYIR-i.MX8MM-Uboot/
make distclean
make myd_imx8mm_ddr4_evk_defconfig
make -j16
ls
wget http://www.nxp.com/lgfiles/NMG/MAD/YOCTO/firmware-imx-8.1.bin
chmod +x firmware-imx-8.1.bin 
./firmware-imx-8.1.bin --auto-accept
tree -L 2 firmware-imx-8.1
cd ..
tar xvf imx8mm-atf.tar.gz 
cd imx8mm-atf/
make clean PLAT=imx8mm
LDFLAGS="" make PLAT=imx8mm
cd ..
tar xvf imx-mkimage.tar.gz 
cd imx-mkimage/
cp ../MYIR-i.MX8MM-Uboot/tools/mkimage ./iMX8M/mkimage_uboot
cp ../MYIR-i.MX8MM-Uboot/arch/arm/dts/myb-fsl-imx8mm-ddr4-evk.dtb ./iMX8M/
cp ../MYIR-i.MX8MM-Uboot/spl/u-boot-spl.bin ./iMX8M/
cp ../MYIR-i.MX8MM-Uboot/u-boot-nodtb.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_dmem_1d.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_dmem_2d.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_imem_1d.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_imem_2d.bin ./iMX8M/
cp ../imx8mm-atf/build/imx8mm/release/bl31.bin ./iMX8M/
makeSOC=iMX8MMclean
make SOC=iMX8MMclean
make SOC=iMX8MM clean
make SOC=iMX8MM flash_ddr4_evk
ls ./iMX8M
cd ..
tar -xvf MYIR-i.MX8MM-Linux.tar.gz 
cd MYIR-i.MX8MM-Linux
make distclean
make defconfig
LDFLAGS=""
LDFLAGS="" CC="$CC"
make Image dtbs modules -j16
cd ..
tar xvf 04-Sources/MYIR-Yocto-i.MX8MM.tar.gz
tar xvf 04-Source/MYIR-i.MX8MM-Uboot.tar.gz -C ~/
tar xvf 04-Sources/MYIR-i.MX8MM-Uboot.tar.gz -C ~/
tar xvf 04-Sources/MYIR-i.MX8MM-Linux.tar.gz -C ~/
cd MYIR-Yocto-i.MX8MM
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
ls
./setup-environment 
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source setup-environment
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source setup-environment build
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
exit
sudo apt purge unattended-upgrades 
sudo apt update
sudo apt install gawk wget git-core diffstat unzip texinfo gcc-multilib build-essential chrpath socat libsdl1.2-dev u-boot-tools
sudo apt-get install libsdl1.2-dev xterm sed cvs subversion coreutils texi2html docbook-utils python-pysqlite2 help2man make gcc g++ desktop-file-utils libgl1-mesa-dev libglu1-mesa-dev mercurial autoconf automake groff curl lzop asciidoc
cat ~/.bash_history
cd MYD-C8MMX-devel/
ls
cd 04-Sources/
ls
git clone git://git.yoctoproject.org/poky
cd ..
cd MYIR-Yocto-i.MX8MM\
cd MYIR-Yocto-i.MX8MM
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbakecore-image-base
bitbake core-image-base
export GIT_SSL_NO_VERIFY=1
bitbake core-image-base
bitbake core-image-base -c fetch
cd ..
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
cd ..
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake meta-toolchain
exit
cd ~/Downloads/
ls
sudo dpkg -i baidunetdisk_4.3.0_amd64.deb 
/opt/baidunetdisk/baidunetdisk 
/opt/baidunetdisk/baidunetdisk --help
apt-cache search baidu
sudo apt purge baidunetdisk
sudo add-apt-repository ppa:flatpak/stable
sudo apt update
sudo apt install flatpak
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
sudo update-ca-certificates
flatpak remote-add --user --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install flathub us.zoom.Zoom
git clone git://git.freescale.com/imx/imx-firmware.git
ls
cd MYD-C8MMX-ISO-20200401/03-Tools/
ls
cd Repo/
ls
pwd
cd ..
mkdir yocto
cd yocto/
/home/hufan/Downloads/MYD-C8MMX-ISO-20200401/03-Tools/Repo/repo init -u git://source.codeaurora.org/external/imx/imx-manifest.git -b imx-linux-sumo -m imx-4.14.98-2.3.3.xml
which python
python --version
python3 /home/hufan/Downloads/MYD-C8MMX-ISO-20200401/03-Tools/Repo/repo init -u git://source.codeaurora.org/external/imx/imx-manifest.git -b imx-linux-sumo -m imx-4.14.98-2.3.3.xml
/home/hufan/Downloads/MYD-C8MMX-ISO-20200401/03-Tools/Repo/repo init -u git://source.codeaurora.org/external/imx/imx-manifest.git -b imx-linux-sumo -m imx-4.14.98-2.3.3.xml
nano /home/hufan/Downloads/MYD-C8MMX-ISO-20200401/yocto/.repo/repo/main.py
cd ..
ls
cd 04-Sources/
ls
cd ~/MYD-C8MMX-devel/
ls
cd 04-Sources/
ls
cd poky
ls
git checkout krogoth
cd /media
ls
cd hufan/
ls
cd ~/
ls
cd MYIR-i.MX8MM-Linux
ls
ll
git st
git status
git branch
sudo apt-get build-dep qemu
exit
cd ~/MYD-C8MMX-devel/
ls
cd 03-Tools/
ls
cd ToolsChain/
ls
./myir-imx-xwayland-glibc-x86_64-fsl-image-qt5-validation-imx-aarch64-toolchain-4.14-sumo.sh
source /media/hufan/myir-imx-xwayland/4.14-sumo/environment-setup-aarch64-poky-linux
source /media/hufan/environment-setup-aarch64-poky-linux 
ls
cd ..
ls
cd ..
ls
cd MYIR-Yocto-i.MX8MM/
ls
git st
git rev-parse --short HEAD
git rev-parse HEAD
cat /home/hufan/MYD-C8MMX-devel/MYIR-Yocto-i.MX8MM/build_8m_mini/tmp/work/myd_imx8mm-poky-linux/linux-imx/4.14.98-r0/temp/log.do_fetch.21032
ls
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
exit
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake fsl-image-qt5-validation-imx
bitbake bitbake-cookerdaemon.log core-image-base
bitbake core-image-base
bitbake fsl-image-qt5-validation-imx
bitbake fsl-image-qt5-validation-imx -c fetch
bitbake fsl-image-qt5-validation-imx
cd ..
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake core-image-minimal
cd ..
cd ../
ls
cd ..
ls
md5 custom-MYIR-i.MX8MM-Linux.tar.gz 
md5sum custom-MYIR-i.MX8MM-Linux.tar.gz 
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake fsl-image-qt5-validation-imx
exit
history
source /media/hufan/environment-setup-aarch64-poky-linux
cd MYD-C8MMX-devel/
ls
cd MYIR-Yocto-i.MX8MM/
exit
flatpak install flathub com.microsoft.Teams
flatpak run com.microsoft.Teams
exit
source /media/hufan/environment-setup-aarch64-poky-linux 
ll /media/hufan/sysroots/
cd /media/hufan
ls
cd /media/hufan
ls
ll
cd ~/MYD-C8MMX-devel/
ls
cd MYIR-Yocto-i.MX8MM/
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake fsl-image-qt5-validation-imx
cd ..
exit
cd /media/hufan/
ls
rm -Rf *
sudo rm -Rf *
export DEV_ROOT=~/MYD-C8MMX-devel/
export DEV_ROOT=~/MYD-C8MMX-devel
cd $DEV_ROOT
ls
cd 03-Tools/\
cd 03-Tools/
ls
cd ToolsChain/
ls
sudo ./myir-imx-xwayland-glibc-x86_64-fsl-image-qt5-validation-imx-aarch64-toolchain-4.14-sumo.sh
source /media/hufan/environment-setup-aarch64-poky-linux
echo $cc
echo $CC
cd $DEV_ROOT
ls
cd 04-Sources/
ls
tar -xvf MYIR-i.MX8MM-Uboot.tar.gz 
cd MYIR-i.MX8MM-Uboot/
make distclean
make myd_imx8mm_ddr4_evk_defconfig
make -j16
cd ..
ls
./firmware-imx-8.1.bin 
./firmware-imx-8.1.bin --auto-accept
tar -xvf imx8mm-atf.tar.gz 
cd imx8mm-atf/
make clean PLAT=imx8mm
LDFLAGS="" make PLAT=imx8mm
cd ..
tar -xvf imx-mkimage.tar.gz 
cd imx-mkimage/
history
cp ../MYIR-i.MX8MM-Uboot/tools/mkimage ./iMX8M/mkimage_uboot
cp ../MYIR-i.MX8MM-Uboot/arch/arm/dts/myb-fsl-imx8mm-ddr4-evk.dtb ./iMX8M/
cp ../MYIR-i.MX8MM-Uboot/spl/u-boot-spl.bin ./iMX8M/
cp ../MYIR-i.MX8MM-Uboot/u-boot-nodtb.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_dmem_1d.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_dmem_2d.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_imem_1d.bin ./iMX8M/
cp ../firmware-imx-8.1/firmware/ddr/synopsys/ddr4_imem_2d.bin ./iMX8M/
cp ../imx8mm-atf/build/imx8mm/release/bl31.bin ./iMX8M/
make SOC=iMX8MM clean
make SOC=iMX8MM flash_ddr4_evk
ls ./iMX8M/
cd $DEV_ROOT
ls
cd 04-Sources/
ls
tar -xvf MYIR-i.MX8MM-Linux.tar.gz 
cd MYIR-i.MX8MM-Linux
ls
make distclean
make defconfig
LDFLAGS="" CC="$CC"
make Image dtbs modules -j16
cd $DEV_ROOT
ls
tar xvf 04-Sources/MYIR-Yocto-i.MX8MM.tar.gz 
cd MYIR-Yocto-i.MX8MM/
mv -v ../bak_MYIR-Yocto-i.MX8MM/downloads/ .
ls
exit
cd ~/
l
ls
cd MYIR-i.MX8MM-Linux/
git st
history
git branch
git rev-parse HEAD
exit
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake fsl-image-qt5-validation-imx
bitbake core-image-base
cd MYD-C8MMX-devel/
ls
cd MYIR-Yocto-i.MX8MM/
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake core-image-base
history
cd MYD-C8MMX-devel/
ls
cd MYIR-Yocto-i.MX8MM/
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake core-image-base
exit
cd MYD-C8MMX-devel/
ls
cd MYIR-Yocto-i.MX8MM/
ls
tar -cvf downloads.tar downloads
ll
tar -cvf build_8m_mini.tar build_8m_mini
cd ..
exit
sudo apt-get remove update-manager
sudo apt purge update-manager
ll /etc/apt/apt.conf.d
nano /etc/apt/apt.conf.d/99update-notifier 
sudo nano /etc/apt/apt.conf.d/99update-notifier 
pkill update-notifier
ps aux
ps aux | grep -i update
sudo nano /etc/apt/apt.conf.d/10periodic
cat /etc/update-manager/release-upgrades
sudo /etc/update-manager/release-upgrades
sudo nano /etc/update-manager/release-upgrades
history | grep -i teams
flatpak run com.microsoft.Teams
exit
cd MYD-C8MMX-devel/
ls
mv -v stable_MYIR-Yocto-i.MX8MM/downloads/ .
ls
tar xvf 04-Sources/MYIR-Yocto-i.MX8MM.tar.gz 
ls
cd MYIR-Yocto-i.MX8MM/
ll
ll -Ah
ls
exit
cd ~/
ls
cd MYIR-i.MX8MM-Linux/
ls
cd ..
tar xvf MYIR-i.MX8MM-Linux.tar.gz 
source /media/hufan/environment-setup-aarch64-poky-linux 
echo $CC
make distclean
cd MYIR-i.MX8MM-Linux
make distclean
make defconfig
LDFLAGS="" CC="$CC"
make Image dtbs modules -j16
git branch
history
git rev-parse HEAD
exit
ls
cd ~/MYD-C8MMX-devel/MYIR-Yocto-i.MX8MM/
bitbake -c menuconfig virtual/kernel
history
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake -c menuconfig virtual/kernel
bitbake -c savedefconfig virtual/kernel
exit
apt-cache search 7zip
apt-cache search 7-zip
apt-cache search 7z
sudo apt install p7zip-full
exit
cd MYD-C8MMX-devel/
cd MYIR-Yocto-i.MX8MM/
history
bitbake -c menuconfig linux-imx
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake -c menuconfig linux-imx
exit
grep bindings
grep -iR bindings .
grep -iR dts .
cd ../
ls
cd MYIR-i.MX8MM-Uboot/
grep -iR dts .
exit
cd /home/hufan/MYIR-i.MX8MM-Uboot/configs
grep -iR usb .
cd ..
grep -iR tree .
exit
source /media/hufan/environment-setup-aarch64-poky-linux 
cd ~/
ls
cd MYIR-i.MX8MM-Linux
make distclean
cd ..
cd MYIR-i.MX8MM-Uboot/
ls
cd ~/MYD-C8MMX-devel/
cd 04-Sources/
ls
cd imx8mm-atf/
make clean PLAT=imx8mm
LDFLAGS=""
LDFLAGS="" make PLAT=imx8mm
make clean PLAT=imx8mm
LDFLAGS="" make PLAT=imx8mm
make clean PLAT=imx8mm
LDFLAGS="" make PLAT=imx8mm
cd ..
cd ~/MYIR-i.MX8MM-Uboot/
make distclean
make myd_imx8mm_ddr4_evk_defconfig
make distclean
grep -iR myd_imx8mm_ddr4_evk_defconfig .
grep -iR myd_imx8mm_ddr4_evk .
grep -iR ddr4_evk .
make distclean
make myd_imx8mm_ddr4_evk_defconfig
cd ../MYIR-i.MX8MM-Linux/
make distclean
make defconfig
LDFLAGS="" CC="$CC"
make Image dtbs modules -j16
exit
cd ~/MYIR-i.MX8MM-Linux/
grep -iR CONFIG_OF_ALL_DTBS .
exit
ll arch/arm/boot/dts/
arch/arm/boot/dts/
ll
pwd
make dtbs
exit
pwd
exit
ll /home/hufan/MYD-C8MMX-devel/MYIR-Yocto-i.MX8MM/build_8m_mini/tmp/deploy/images/myd-imx8mm
cd /home/hufan/MYD-C8MMX-devel/MYIR-Yocto-i.MX8MM/build_8m_mini/tmp/deploy/images/myd-imx8mm
ll
exit
cd ..
cd MYD-C8MMX-devel/
ls
cd MYIR-Yocto-i.MX8MM/
grep -iR dts .
DISTRO=myir-imx-xwaylandMACHINE=myd-imx8mmsourcefsl-setup-release.sh-bbuild_8m_mini
history
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake -e virtual/kernel | grep '^FILE='
bitbake -c devshell virtual/kernel
history
bitbake -c menuconfig linux-imx
bitbake -c savedefconfig linux-imx
bitbake -c devshell virtual/kernel 
history
bitbake core-image-minimal
exit
cd ~/
apt-cache search bluefish
sudo apt install bluefish
exit
history
pwd
grep -iR usb@32e40000 .
pwd
make dtbs
make
exit
cd /tmp
cd devtree1/
ll
history
dtc -I dtb -O dts -f Image--4.14.98-r0-myb-fsl-imx8mm-lcdif-20220310195236.dtb -o devicetree_file_name.dts
exit
cd /tmp/devtree1/
sudo apt install device-tree-compiler
ls
dtc -I dtb -O dts -f Image--4.14.98-r0-myb-fsl-imx8mm-ddr4-evk-m4-20220310051010.dtb -o devicetree_file_name.dts
cd ~/MYD-C8MMX-devel/
ls
cd MYIR-Yocto-i.MX8MM/
history
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake -c devshell virtual/kernel
history
bitbake -c menuconfig linux-imx
bitbake -c savedefconfig linux-imx
history
bitbake core-image-minimal
exit
pwd
make dtbs
exit
cd /tmp/newdevtree/
ll
dtc -I dtb -O dts -f myb-fsl-imx8mm-lcdif.dtb -o devicetree_file_name.dts
exit
history
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
cd ~/MYD-C8MMX-devel/MYIR-Yocto-i.MX8MM/
DISTRO=myir-imx-xwayland MACHINE=myd-imx8mm source fsl-setup-release.sh -b build_8m_mini
bitbake -c devshell virtual/kernel
history
bitbake -c menuconfig linux-imx
bitbake -c savedefconfig linux-imx
history
bitbake core-image-minimal
exit
sudo apt install memtester
sudo memtester 10G 1
sudo systemctl stop packagekit
sudo systemctl status packagekit
sudo systemctl status PackageKit
sudo systemctl status Packagekit
cd ~/Documents/Projects/
ls
cat README.md 
git st
cd MYD-C8MMX/
git st
git status
ls
cd ..
ls
git status
rm -Rf MYD-C8MMX/
split -b 10M /home/hufan/MYD-C8MMX-devel/MYIR-Yocto-downloads.tar MYIR-Yocto-downloads.tar.
ls
ls -l
exit
cd /tmp
mkdir myd
cd myd
split -b 1G ~/MYD-C8MMX-devel/MYIR-Yocto-downloads.tar MYIR-Yocto-downloads.tar. 
ls
ll
mkdir aa
cd aa
split -b 10M ../MYIR-Yocto-downloads.tar.aa MYIR-Yocto-downloads.tar.aa.
ll
cd ..
mv -v aa ~/Documents/Projects/MYD-C8MMX/MYIR-Yocto-downloads/
cd ..
mv -v myd ~/Documents/Projects/
exit
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
ssh -T git@github.com
cd Documents/
ll
mkdir Projects
cd Projects/
echo "# MYD-C8MMX" >> README.md
git init
git add README.md
git commit -m "first commit"
git commit -m "first commit"
git branch
git push -u origin master
cd /home/hufan/MYD-C8MMX-devel/MYIR-Yocto-i.MX8MM
ls -lA
cd downloads
ls
cd ..
ls -lA
cd ..
cd downloads/
ls
cd ..
ll
tar cvf MYIR-Yocto-downloads.tar downloads
pwd
ll
htop
top
cd ~/Documents/Projects/
git st
ls
git add .
git status
git commit -m "MYIR-Yocto"
git push
git config core.compression 0
git config core.loosecompression 0
git push
vim ~/.ssh/config
sudo apt install vim
AddKeysToAgent  yes
TCPKeepAlive yes
ServerAliveInterval 15
ServerAliveCountMax 6
Compression yes
ControlMaster auto
ControlPath /tmp/%r@%h:%p
vim ~/.ssh/config
history
ssh -T git@github.com
ll /tmp
git config --global pack.window 0
git config --global core.compression 0
git config --global core.loosecompression 0
echo '*.tar.* -delta' > .gitattributes
git gc
git st
git status
git add .
git ci -m "attributes"
git commit -m "attributes"
git push
cd ..
rm -Rf Projects/
mkdir Projects
cd Projects/
cd MYD-C8MMX/
history | grep -i split
echo '*.tar.* -delta' > .gitattributes
git st
git status
git add .
git commit -m "attributes"
git push
mkdir MYIR-Yocto-downloads
cd MYIR-Yocto-downloads
cd ..
git status
git ls
cd MYIR-Yocto-downloads/
git ls-files . --exclude-standard --others
git ls-files . --exclude-standard --others | head
git ls-files . --exclude-standard --others | head -1
git push && git ls-files . --exclude-standard --others | head -1
git config --global push.default simple
git push && git ls-files . --exclude-standard --others | head -1
git push -q
git push -q && git ls-files . --exclude-standard --others | head -1
git push -q && git ls-files . --exclude-standard --others | head -1 | xargs git add | git commit -m "updates" | git push
git status
git reset aa/MYIR-Yocto-downloads.tar.aa.aa
git status
git push -q && git ls-files . --exclude-standard --others | head -1 | xargs -t git add | git commit -m "updates" | git push
git reset aa/MYIR-Yocto-downloads.tar.aa.aa
git push -q && git ls-files . --exclude-standard --others | head -1 | xargs -t git add && git commit -m "updates" | git push
git reset aa/MYIR-Yocto-downloads.tar.aa.aa
git push -q && git ls-files . --exclude-standard --others | head -1 | xargs -t {git add ;git commit -m "updates"} | git push
git push -q && git ls-files . --exclude-standard --others | head -1 | xargs -t {git add ;git commit -m "updates"} | git push -v
git push -q && git ls-files . --exclude-standard --others | head -1
git push -q && git ls-files . --exclude-standard --others | head -1 | xargs -t -d $'\n' sh -c 'git add "$arg";git commit -m "updates"' | git push -v
git push -q && git ls-files . --exclude-standard --others | head -1 | xargs -t -d $'\n' sh -c 'git add "$arg" && git commit -m "updates" && git push -v'
```
