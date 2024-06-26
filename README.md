# libao for Visual Studio

Building [libao](https://www.xiph.org/ao/)(libao.lib & libao.dll) with Visual Stduio.(Output: WMM or NULL only.)

## Requirement

- Visual Studio(tested on VS2022)
- Git for Windows(bash/curl/find/patch/etc...)


## Build


download & patch files.

```.text
 $ git clone https://github.com/stkchp/libao-windows.git
 $ cd libao-windows
 $ ./prepare.sh
```


### build x86

open `windows/VS20XX/libao.sln` with Visual Stduio & build.

OR 

open `x64 native tool command prompt` 

```powershell
MSBuild .\windows\VS20xx\libao.vcxproj -t:Rebuild /property:Configuration=Release
```


lib & dll files.

```
.\windows\VS20xx\[Debug/Release]\libao.dll
.\windows\VS20xx\[Debug/Release]\libao.lib
```

###  build x64

open `x64 native tool command prompt` 

```powershell
MSBuild .\windows\VS20xx\libao_x64.vcxproj -t:Rebuild /property:Configuration=Release /property:Platform=x64
```


lib & dll files.

```
.\windows\VS20xx\x64\[Debug/Release]\libao.dll
.\windows\VS20xx\x64\[Debug/Release]\libao.lib
```



## Usage

header files.

```.text
build/ao/ao.h
build/ao/ao_private.h
build/ao/os_types.h
```
