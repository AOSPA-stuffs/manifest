### Paranoid Android ###

## Create a directory for the source files ##

```bash
repo init --depth=1 -u https://github.com/AOSPA-stuffs/manifest.git -b uvite-rd
```

## Downloading the source tree ##

This is what you will run each time you want to pull in upstream changes. Keep in mind that on your
first run, it is expected to take a while as it will download all the required Android source files
and their change histories.

```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

## Syncing specific projects ##

In case you are not interested in syncing all the projects, you can specify what projects you do
want to sync. This can help if, for example, you want to make a quick change and quickly push it
back for review. You should note that this can sometimes cause issues when building if there is
a large change that spans across multiple projects.

```bash
# Specify one or more projects by either name or path

# For example, enter AOSPA/android_frameworks_base or
# frameworks/base to sync the frameworks/base repository

$ repo sync PROJECT
```

## Building ##

The bundled builder tool `./rom-build.sh` handles all the building steps for the specified device
automatically. As the device value, you just feed it with the device codename (for example,
'beryllium' for the Pocophone F1).

```bash
# Go to the root of the source tree...
$ cd WORKSPACE
# ...and run the builder tool.
./rom-build.sh DEVICE
```

## Code ##

Our codebase is licensed under Apache License, Version 2.0 unless otherwise specified. Apache
License 2.0 allows a variety of actions on the content as long as licensing and copyright
notices are retained and included with the code and your changes to the codebase are stated.

You can read the full license text at http://www.apache.org/licenses/LICENSE-2.0
