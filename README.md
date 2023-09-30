# CreateShortcut

Create a desktop shortcut.

## Download

[x86]

[x64]

[x86]: build/CreateShortcut-x86.exe
[x64]: build/CreateShortcut-x64.exe

## Usage

CreateShortcut.exe [options] <source> <destination>

### options

+ `--work-dir`
+ `--arguments`
+ `--show-cmd`
+ `--icon-file`
+ `--description`
+ `--desktop-shortcut`

## Build

```Bash
pacman -S mingw-w64-gcc
mkdir build

i686-w64-mingw32-windres CreateShortcut.rc -o build/CreateShortcut-x86.res -O coff
i686-w64-mingw32-gcc CreateShortcut.c build/CreateShortcut-x86.res -o build/CreateShortcut-x86.exe -luuid -lole32
i686-w64-mingw32-strip build/CreateShortcut-x86.exe

x86_64-w64-mingw32-windres CreateShortcut.rc -o build/CreateShortcut-x64.res -O coff
x86_64-w64-mingw32-gcc CreateShortcut.c build/CreateShortcut-x64.res -o build/CreateShortcut-x64.exe -luuid -lole32
x86_64-w64-mingw32-strip build/CreateShortcut-x64.exe
```

## LICENSE

[GPL v2]

[GPL v2]: LICENSE
