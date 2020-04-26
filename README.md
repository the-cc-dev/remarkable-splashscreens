<h1 align="center">Splash screens for the reMarkable tablet</h1>

## Contents
- [Info](#info)

## Info <a name = "info"></a>
This repository contains a bunch of `png` files with the correct ratio to be used as backgrounds or splash screens in the [reMarkable paper tablet](https://remarkable.com/).

## About <a name = "about"></a>
Some of the original files can be found in this repository, in the folder [originals](originals).

## Log in
To log in to the reMarkable, `SSH` into the address given on the bottom of the section _General information_ in the _Copyrights and licenses_ file. E.g.
```
ssh root@10.0.1.17
```
and type in the password, given in the same file as the address, e.g. `pswrd123`.

## Adding new splash screens
To copy the original files from reMarkable to your computer (for backup) use
```
scp root@10.0.1.17:/usr/share/remarkable/filename.png /path/to/filename.png
```
You then want to log in to the tablet and delete all files you want to replace, using
```
rm -f filename.png
```
You can now copy a new file from your computer to the same place in the reMarkable by doing
```
scp /path/to/filename.png root@10.0.1.17:/usr/share/remarkable/filename.png
```
