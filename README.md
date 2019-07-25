# ioquake3-Mac
Tip to run ioquake3 on Mac, versions like Sierra, Mojave and others. 

## Problem: ioquake doesn't launch
If your ioquake3 doesn't launch, follow the steps bellow to solve it

## Solutions
1. Verify if exist file `pak0.pk3` in folder `baseq3`, i.e: `/Applications/ioquake3/baseq3`. in folder `baseq3` 
2. If file exist, it's possible this `ioquake3` are in **quarentine** from **App Translocation Security** Resource

## How can I check if `ioquake3` are in quarentine?

```
$ sudo xattr /Applications/ioquake3/ioquake3-1.36.app
# Command return
$ com.apple.quarantine
```

## How can I disable **App Translocation Security**?

```
$ sudo xattr -d -r com.apple.quarantine /Applications/ioquake3/ioquake3-1.36.app
$ sudo reboot
```
