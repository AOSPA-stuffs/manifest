# Paranoid Android #

### Creating workspace folder ###

```bash
mkdir AOSPA
cd AOSPA
```

### Initializing repo ###

```bash
repo init -u https://github.com/AOSPA-stuffs/manifest -b topaz-rd
```

### Initializing depth repo ###

```bash
repo init --depth=1 -u https://github.com/AOSPA-stuffs/manifest -b topaz-rd
```

### Downloading the source tree ###

```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

## Building ##

```bash
./rom-build.sh DEVICE -j$(nproc --all)
```
