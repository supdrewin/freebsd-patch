# FreeBSD Patch

Only **14-CURRENT** available because I working with this version FreeBSD
*(which has iwlwifi support)*.

### Which modified

- [x] Add Device ID for **Tenda U12** *(rtl8812au)*

### How to

For `/path/to/xxx.patch`,
simply do below:

``` shell
$ cd /usr/src
$ patch -Np1 < /path/to/xxx.patch
```

Then rebuild your kernel with:

``` shell
$ make -jN -C /usr/src buildkernel
$ make -C /usr/src installkernel
$ reboot
```

The `N` of `-j` should be the threads you prefered to build the kernel,
and then install and reboot to your new kernel.

Also see official handbook for details of wireless.

### Bugs

Feel free to open a issues if you have some problem
*(but not for kernel itself)*.
