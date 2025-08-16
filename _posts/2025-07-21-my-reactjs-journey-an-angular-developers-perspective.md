---
layout: post
title: "How to install v2ray on Fedora 42"
---

## Introduction
Installing **V2Ray** on `Fedora 42` took me a whole day and caused lots of headaches! So I decided to share this post to help others facing the same problem and hopefully save them some time.

In this post, I’m going to show you how to install and configure **V2Ray** on **Fedora 42** in the easiest way possible. By the end, you should be able to set it up without any issues.

## Installation

To run `v2ray` on Fedora 42, we need to install both the **V2Ray Core** and **Qv2ray (GUI)**. Let’s get started.

### V2Ray Core

Download the latest release of the core from the following URL:

```
https://github.com/XTLS/Xray-core/releases/tag/v1.6.2
```

Download the file `Xray-linux-64.zip`, then unzip it. After that, make the `xray` file executable by running:

```bash
sudo chmod +x xray
```

### Qv2ray (GUI)

Download the GUI from the following URL:

```
https://github.com/Qv2ray/Qv2ray/releases
```

Get the file `Qv2ray-v2.7.0-linux-x64.AppImage` and make it executable:

```bash
sudo chmod +x Qv2ray-v2.7.0-linux-x64.AppImage
```

Now you can run it:

```bash
./Qv2ray-v2.7.0-linux-x64.AppImage
```

**Note:** If you see the following error:

```
qv2ray: error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```

you need to install the `libxcrypt-compat` package:

```bash
sudo dnf install libxcrypt-compat
```

## Configuration

![Qv2ray Preferences](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/22f2xr2kz0qwiycttx3k.png)

Run `Qv2ray-v2.7.0-linux-x64.AppImage`, then go to:
**Preferences → Kernel Setting**

* In the **V2Ray Core Executable Path** tab, select the path where you unzipped the V2Ray core and choose the `xray` file.
* In the **V2Ray Assets Directory** tab, select the same directory as the **V2Ray Core Executable Path**.

Finally, click **Check V2Ray Core Settings**. If you see the following message, everything is configured correctly:

```
V2Ray path configuration check passed.
```
![image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/66tetzr53xe2g9t7fq42.png)




## Conclusion

In this post, we walked through installing and configuring `V2Ray` on `Fedora 42` in the simplest way possible. I hope this guide helps others save time and avoid the headaches I experienced.




