REACHDESK CLIENT SOFTWARE FOR WINDOWS
Pre-requisite:
Build C++ environment.
Install Visual studio
Install Rustup 
Install vcpkg
Download sciter.dll
Install llvm
Download & Install Gitbash
Download & Install Python
Setup the Environment:
Download msvc and install.
Download rustup-init.exe and run it as administrator to install rust.
open Gitbash to clone the vcpkg & Download it by using below commands.
git clone https://github.com/microsoft/vcpkg
cd vcpkg
git checkout 2023.01.09
cd ..
vcpkg/bootstrap-vcpkg.bat
export VCPKG_ROOT=$PWD/vcpkg
vcpkg/vcpkg install libvpx:x64-windows-static libyuv:x64-windows-static opus:x64-windows-static
Add System environment variable VCPKG_ROOT=<path>\vcpkg
Download llvm and install. Also add system environment variable
LIBCLANG_PATH=<llvm_install_dir>/bin
Build - ReachDesk Client:
Pre-requisite: Add the wget.exe, python.exe file in Git installed directory ( GIt\Mingw64\bin).
Enter the below commands in gitbash
git clone https://github.com/kirishree/reachdesk
cd reachdesk
mkdir –p target/release
wget https://raw.githubusercontent.com/c-smile/sciter-sdk/master/bin.win/x64/sciter.dll
cp sciter.dll target/release
python3 build.py
Our ReachDesk.exe file is available in reachdesk/target/release/
