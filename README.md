<div align="center">
  <img loading="lazy" src="https://raw.githubusercontent.com/StardustMod/build/refs/heads/main/assets/banner.png"/>
</div>

<h4 align="center">StardustKernel 💫 for Exynos 7870 devices.</h4>

# Features

- Kernel Based on SIMPLE-KERNEL V1.0 (Enforcing) by [***@Astrako***](https://github.com/Astrako) ***(A600FNXXU5CTB9)***
- Only Support OneUI ROM (It may have some issues depending on OneUI version)
- KernelSU by [***@backslashxx***](https://github.com/backslashxx)
- A little overclock for GPU (WIP)
- Overclock for Little, Mid and Big CPU (WIP)
- CPU Input Boost (WIP)
- HZ Tick Set at 25Hz (WIP)
- WireGuard (WIP)
- Boeffla Wakelock Blocker (WIP)
- ThunderTweaks Support (You can get ThunderTweaks [here](https://github.com/StardustMod/build/raw/refs/heads/main/ThunderTweaks_v1.1.1.5.apk) to customize kernel features)

# How to Install

- Flash kernel zip file via `TWRP` recovery based
- Install `Kernel Addons` on `/sdcard/StardustKernel-Addons-Exynos7870-[version].zip` via KernelSU
- Install `KernelSU` from [Here](https://github.com/backslashxx/KernelSU/releases)

# Supported Devices

|         Name         |  Codename  |    Model   |
|:--------------------:|:----------:|:----------:|
|  Galaxy A3 (2017)    |  a3y17lte  |  SM-A320x  |
|  Galaxy A6 (2018)    |  a6lte     |  SM-A600x  |
|  Galaxy J5 (2017)    |  j5y17lte  |  SM-J530x  |
|  Galaxy J6 (2018)    |  j6lte     |  SM-J600x  |
|  Galaxy J7 Core      |  j7velte   |  SM-J701x  |
|  Galaxy J7 (2016)    |  j7xelte   |  SM-J710x  |
|  Galaxy J7 (2017)/Pro|  j7y17lte  |  SM-J730x  |
|  Galaxy J7 Prime     |  on7xelte  |  SM-G610x  |

# How to Build

1. Copy command below and paste on your terminal to install all necessary dependencies

```
sudo apt update && sudo apt upgrade -y && sudo apt install --no-install-recommends -y bc build-essential ccache cpio && wget http://security.ubuntu.com/ubuntu/pool/universe/p/python2.7/python2.7_2.7.18-13ubuntu1.5_amd64.deb http://security.ubuntu.com/ubuntu/pool/universe/p/python2.7/libpython2.7-stdlib_2.7.18-13ubuntu1.5_amd64.deb http://security.ubuntu.com/ubuntu/pool/universe/p/python2.7/python2.7-minimal_2.7.18-13ubuntu1.5_amd64.deb http://security.ubuntu.com/ubuntu/pool/universe/p/python2.7/libpython2.7-minimal_2.7.18-13ubuntu1.5_amd64.deb && sudo apt install -y ./libpython2.7-minimal_2.7.18-13ubuntu1.5_amd64.deb ./libpython2.7-stdlib_2.7.18-13ubuntu1.5_amd64.deb ./python2.7-minimal_2.7.18-13ubuntu1.5_amd64.deb ./python2.7_2.7.18-13ubuntu1.5_amd64.deb && rm -rf *.deb && sudo ln -sf /usr/bin/python2.7 /usr/bin/python2
```

2. Clone repository

```
git clone https://github.com/StardustMod/android_kernel_samsung_exynos7870
```

3. Build for your device (To list all build script command run `./build.sh -h`)

```
./build.sh -m [device_codename]
```

> **Example:** Build for Galaxy J7 (2016) [j7xelte]
> 
> ```
> ./build.sh -m j7xelte
> ```

4. After build you can find the kernel zip file at the location below

```
build/export/StardustKernel-Unofficial-[yyyyMMdd]-[device_model]-[device_codename].zip
```

5. Flash using TWRP based recovery

6. Test it and enjoy!

# Credits

- [`Astrako`](https://github.com/Astrako) for [Kernel Source](https://github.com/samsungexynos7870/android_kernel_samsung_exynos7870)
- [`backslashxx`](https://github.com/backslashxx) for [KernelSU](https://github.com/backslashxx/KernelSU) and [Backport Guide](https://github.com/backslashxx/KernelSU/issues/20)
