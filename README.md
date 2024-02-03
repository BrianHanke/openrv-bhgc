1. 32-core+ vCPU VM - 30 minute build time  
2. Download OpenRV-BHGC as a ZIP file  
3. Open a MSYS2 MINGW64 console and run:
  
```
cd /c/Source  
git clone --recursive https://github.com/AcademySoftwareFoundation/OpenRV.git
```
4. Merge the contents of openrv-bhgc.zip with the main source code, then run:
```
cd OpenRV
source rvcmds.sh  
rvbootstrap  
cd /c/Source/OpenRV/_build/stage  
find . -name "*.pdb" -type f -delete
mv app openrv-bhgc  
7z a openrv-bhgc.zip openrv-bhgc
```
