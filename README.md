# Lazurite-patches
Patches for Lazurite driver sources.

# Installation

1. Install Lazurite driver sources</br>
Follow the instructions of [here](https://github.com/LAPIS-Lazurite/LazuriteInstaller.git) for the installation.

2. Patch and Re-build
```bash
pushd driver/liblazurite
patch -p1 < diff.patch
make
sudo cp lib/liblazurite.so /lib/modules/`uname -r`/kernel/Your preffered directory
sudo depmod /lib/modules/`uname -r`/kernel/Installed directory

popd
pushd driver/LazuriteJava
make
make install
popd
```
