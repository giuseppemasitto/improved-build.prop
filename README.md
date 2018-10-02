# improved-build.prop
Tweaks for build.prop configuration

## Getting Started
These instructions will get you a pull of the build.prop file up and ready to edit on your local machine for development and testing purposes. After that you are able to push back and see changes.
> HARDWRE & SOFTWARE
>>When I was writing I am able to test theese edits in a Custom ROM based on MIUI Global stable running Android 8.1 over a Xiaomi Redmi 5 (rosy)

So you have to take care about your infos and backup things!

>We are looking for a great configuration to set up a smooth device as possible, (I'm looking) so do it at your own risk. Is also possible that theese configurations can not override the kernel ones, so does not works at all (I'm trying). 

### Prerequisites
We only need platform tools from Android Google suite (not required to download the entire Android studio (thanks!), Google update theese things so the setup is much easier right now).
>Of course we need at least a **ROOT ACCESS** on device or you will not able to write this confiuration file.

```
Visit https://developer.android.com/studio/releases/platform-tools for more informations
```

## Getting the informations
We are ready to pull build.prop. This file will be saved onto the current adb.exe folder.
```
adb pull /system/build.prop .
```
If you want to save the file in a specific path replace ```.``` with ```<path\to\save>``` in your machine.

### Break down into file
Let's start to edit and follow this style so is more easy to help each others reading and maintaining the configuration file.
```sh
# category_name
prop_name=prop_value
```

### Uploading the result
Upload back the edited file
```
adb push <path\to\your\file> /system/build.prop
```
and set right permission or system overwrite changes
```
adb shell
chmod 644 /system/build.prop
```
And you're done
Reboot your phone and see the changes


## Deployment
If you want to deploy this one, link to https://github.com/mazinthebox/improved-build.prop

## Built With
* [npp++](https://notepad-plus-plus.org/download/v7.5.8.html) - The editor used
* [adb](https://developer.android.com/studio/releases/platform-tools) - From the platform tools


## Authors
* **Giuseppe Masitto** - *Author* - [mazinthebox](https://github.com/mazinthebox)


## License
This project is licensed under the Apache License 2.0 - see the [LICENSE.md](LICENSE.md) file for details
