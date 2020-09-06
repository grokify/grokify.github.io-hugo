+++
author = "John Wang"
title = "Litecoin Mining with Ubuntu"
date = "2014-01-12"
tags = [
    "cryptocoin",
]
url = "/litecoin/mining-with-ubuntu/"
+++

This is a quick how-to on getting started with Litecoin mining on Ubuntu.

## Install AMD Catalyst Display Driver

To use the AMD card for video, download and install the AMD Catalyst Display Driver for Linux.

```
$ unzip amd-catalyst-13.12-linux-x86.x86_64.zip
$ chmod +x amd-catalyst-13.12-linux-x86.x86_64.run
$ ./amd-catalyst-13.12-linux-x86.x86_64.run
```

## Install AMD OpenCL

## Install CGminer

To install CGminer for GPU mining we will need header files from the AMD Display Library (ADL) SDK so download it from the AMD ADL page. You can download CGminer from either Con Koliva’s personal website or Github. Github is used below.

Install CGminer with ADL:

```
$ unzip ADL_SDK_6.0.zip -d ADL_SDK_6.0
$ wget https://github.com/ckolivas/cgminer/archive/v3.7.2.tar.gz -O cgminer-3.7.2.tgz
$ tar xvfz cgminer-3.7.2.tgz
$ cp -p ADL_SDK_6.0/include/*.* cgminer-3.7.2/ADL_SDK/
$ cd cgminer-3.7.2
$ ./autogen.sh --enable-scrypt --enable-opencl
$ sudo make install
```

After autogen, you should see something like the following:

CGminer `autogen.sh` results

```
------------------------------------------------------------------------
cgminer 3.7.2
------------------------------------------------------------------------

Configuration Options Summary:

  libcurl(GBT+getwork).: Enabled: -lcurl  
  curses.TUI...........: FOUND: -lncurses
  OpenCL...............: FOUND. GPU mining support enabled
  scrypt...............: Enabled
  ADL..................: SDK found, GPU monitoring support enabled

  Avalon.ASICs.........: Disabled
  BFL.ASICs............: Disabled
  KnC.ASICs............: Disabled
  BitForce.FPGAs.......: Disabled
  BitFury.ASICs........: Disabled
  Hashfast.ASICs.......: Disabled
  Icarus.ASICs/FPGAs...: Disabled
  Klondike.ASICs.......: Disabled
  ModMiner.FPGAs.......: Disabled

Compilation............: make (or gmake)
  CPPFLAGS.............: 
  CFLAGS...............: -g -O2
  LDFLAGS..............:  -lpthread
  LDADD................: -ldl -lcurl   compat/jansson-2.5/src/.libs/libjansson.a -lpthread -L/opt/AMDAPP/lib/x86_64 -lOpenCL    -lm  -lrt

Installation...........: make install (as root if needed, with 'su' or 'sudo')
  prefix...............: /usr/local
```

## Create the Shell Script

Create `cgminer.sh` to set `ENV`.

```
#!/bin/sh
export DISPLAY=:0
export GPU_MAX_ALLOC_PERCENT=100
export GPU_USE_SYNC_OBJECTS=1
/path/to/cgminer --scrypt --url=stratum+tcp://<fqdn1>:<port1> --userpass=<user1>:<pass1> --url=stratum+tcp://<fqdn2>:<port2> --userpass=<user2>:<pass2> --failover-only --thread-concurrency=22400 --intensity=20 --temp-target 80 --temp-cutoff 85 --gpu-po
wertune 20 --thread-concurrency 24000 --gpu-engine 1100
```

## Happy Mining!

That’s all there is to it. Happy mining!
