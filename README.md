This repo contains source code patch files to build OpenRV-BHGC. Improvements include:  
  
- Updated interface style  
- New icons  
- Streamlined menus  
  
Build time is around 45 minutes on a 32 vCPU VM. VM software configuration should follow the official OpenRV [build guide](https://github.com/AcademySoftwareFoundation/OpenRV/blob/main/docs/build_system/config_windows.md): Visual Studio 2022, Strawberry Perl, MSYS2, etc.  
  
OpenRV-BHGC build steps:  
  
1. Download OpenRV-BHGC as a ZIP file  
2. Open a MSYS2 MINGW64 console and run:  
```
cd /c/Source  
git clone --recursive https://github.com/AcademySoftwareFoundation/OpenRV.git
```
3. Merge the contents of openrv-bhgc.zip with the main source code, then run:
```
cd OpenRV
source rvcmds.sh  
rvbootstrap
```
```
cd /c/Source/OpenRV/_build/stage  
find . -name "*.pdb" -type f -delete
mv app openrv-bhgc
rm -d openrv-bhgc/src
7z a openrv-bhgc.zip openrv-bhgc
```
