# Installation on FreeBSD

This small guide is an addendum for installing XO on FreeBSD 10

## Packages and Pre-requisites

Just install those packages:

```
pkg install gmake rubygem-sass rubygem-compass ruby redis python git npm node
```

Because FreeBSD is shipped with CLANG and not GCC, you need to do this:

```
ln -s /usr/bin/clang++ /usr/local/bin/g++
```

You can update `npm` itself right now with a `npm update -g`

To enable redis on boot, add this in your `/etc/rc.conf`:

```
redis_enable="YES"
```

Don't forget to start redis if you don't reboot:

```
service redis start
```

You can now follow the rest of the procedure, starting at "[Fetching the code](https://github.com/vatesfr/xo/blob/master/installation.md#fetching-the-code)"
