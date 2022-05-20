# Linux Kernel Runtime Guard (LKRG) #

LKRG performs runtime integrity checking of the Linux kernel and detection of
security vulnerability exploits against the kernel.

LKRG is a kernel module (not a kernel patch), so it can be built for and loaded
on top of a wide range of mainline and distros' kernels, without needing to
patch those.

That is only a dependency package to install the LKRG kernel module and also
some systemd service in order to help to manage loading/unloading the module at
system boot/shutdown.

## How to install `lkrg` using apt-get ##

1\. Download the APT Signing Key.

```
wget https://www.kicksecure.com/derivative.asc
```

Users can [check the Signing Key](https://www.kicksecure.com/wiki/Signing_Key) for better security.

2\. Add the APT Signing Key..

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.kicksecure.com bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `lkrg`.

```
sudo apt-get install lkrg
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions.

NOTE: Replace `generic-package` with the actual name of this package `lkrg`.

* **A)** [easy](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.kicksecure.com)
* [Professional Support](https://www.kicksecure.com/wiki/Professional_Support)

## Donate ##

`lkrg` requires [donations](https://www.kicksecure.com/wiki/Donate) to stay alive!
