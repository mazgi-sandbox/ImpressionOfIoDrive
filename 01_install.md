```shellsession
[root@Gottfried] # uname -a
Linux Gottfried 3.12.20-gentoo #1 SMP Mon Jun 2 01:07:15 JST 2014 x86_64 Intel(R) Xeon(R) CPU E5-2420 0 @ 1.90GHz GenuineIntel GNU/Linux
```

## Install < kernel 3.6

```shellsession
[root@Gottfried] # emerge -pv \=gentoo-sources-3.4.99

These are the packages that would be merged, in order:

Calculating dependencies... done!
[ebuild   R   ~] sys-kernel/gentoo-sources-3.4.99:3.4.99  USE="-build -deblob -symlink" 0 kB

Total: 1 package (1 reinstall), Size of downloads: 0 kB
```

```shellsession
[root@Gottfried] # genkernel --makeopts=-j28 --kerneldir=/usr/src/linux-3.4.99-gentoo --menuconfig all
```

