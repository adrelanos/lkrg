# Linux Kernel Runtime Guard (LKRG) #

Linux Kernel Runtime Integrity Checking and Exploit Detection.

LKRG provides security through diversity.
Similar to running an uncommon operating system (kernel) would.

This is a lightweight software fork [4] of LKRG, with a focus on easy
installation, added user documentation, and integration with Whonix [5],
Kicksecure [6], Debian [7], and other distributions.
The LKRG Debian Package Website can be found here. [8]
No changes to or review of the core source code of LKRG.
The software fork source code can be found here. [9]
Original LKRG upstream can be found here. [10]

* [4] https://en.wikipedia.org/wiki/Fork_(software_development)
* [5] https://www.whonix.org
* [6] https://www.whonix.org/wiki/Kicksecure
* [7] https://www.debian.org
* [8] https://www.whonix.org/wiki/Linux_Kernel_Runtime_Guard_LKRG
* [9] https://github.com/Whonix/lkrg
* [10] https://www.openwall.com/lkrg/

This metapackage depends lkrg-dkms.
## How to install `lkrg` using apt-get ##

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
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

See instructions. (Replace `generic-package` with the actual name of this package `lkrg`.)

* **A)** [easy](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.whonix.org/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)
