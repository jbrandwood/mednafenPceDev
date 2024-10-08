# Mednafen

## Compiling this Repository on Linux

### Dependencies

Mednafen is built upon a number of external libraries which are required in order to compile.

Assuming that you already have a working install of gcc/make and other basic developer tools,
the following command(s) may still be needed:

```
sudo apt-get install build-essential pkg-config libasound2-dev libcdio-dev libsdl1.2-dev libsdl-net1.2-dev libsndfile1-dev zlib1g-dev  
```

#### Raspberry Pi Additional Dependencies

```
sudo apt-get install libsdl2-2.0-0 libsdl2-dev
```

### Compile Commands

Mednafen's build process makes use of 'configure' in order to set up environment-specific options in preparation
for the compile; the procedure is as follows:

```
./configure

make
```

At this point, the Mednafen binary can be found in the mednafen/src/ folder; you may manually copy/move it
from there, or use the prescribed:
```
sudo make install
```

## Common Problems:

It is possible that the sound device may not be properly identified by Mednafen; if this is the case, the original
Mednafen documentation has some hints here:
[https://mednafen.github.io/documentation/#Section_troubleshooting_nosoundlinux](https://mednafen.github.io/documentation/#Section_troubleshooting_nosoundlinux)

On Raspberry Pi, you will almost certainly need to update the sound.device in the Mednafen settings as specified in
https://mednafen.github.io/releases/ :
```
sound.device sexyal-literal-default
```
