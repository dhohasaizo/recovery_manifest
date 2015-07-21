#Setting up a minimal tree for building TWRP
##Android 4.4 branch
This repo is ~2.6GB
###To initialize the main repository:

````
repo init -u https://github.com/dhohasaizo/recovery_manifest.git -b android-4.4
````
Then add anyrecovery/device trees/kernels you need to a file (one XML for each device) and add them to the .repo/local_manifests folder of your initialized repo folder.

Once added:
````
repo sync
````
Done

To build recovery:
````
. build/envsetup.sh
lunch (devicename)
make installclean
time make recoveryimage
````


Devices tested:

````
ACER V370
````
