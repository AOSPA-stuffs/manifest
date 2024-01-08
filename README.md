# Paranoid Android #

### Creating workspace folder ###

```bash
mkdir AOSPA
cd AOSPA
```

### Initializing repo ###

```bash
repo init -u https://github.com/AOSPA-stuffs/manifest -b topaz
```

### Initializing depth repo ###

```bash
repo init --depth=1 -u https://github.com/AOSPA-stuffs/manifest -b topaz
```

### Downloading the source tree ###

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

## Building ##

```bash
./rom-build.sh DEVICE -j$(nproc --all)
```
