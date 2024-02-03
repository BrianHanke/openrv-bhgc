32-core+ vCPU VM - 30 minute build time
Open a MSYS2 MINGW64 console  and run:
  
```
cd /c/Source  
git clone --recursive https://github.com/AcademySoftwareFoundation/OpenRV.git  
cd OpenRV
source rvcmds.sh  
rvbootstrap  
cd /c/Source/OpenRV/_build/stage  
find . -name "*.pdb" -type f -delete
mv app openrv-bhgc  
7z a openrv-bhgc.zip openrv-bhgc
```
