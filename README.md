# vagrant-aws-helper
Helper for setting up AWS EC2 instances with vagrant using vagrant-aws, see https://github.com/mitchellh/vagrant-aws.

# Prerequisites

* Install vagrant, for details see https://www.vagrantup.com.
* Install `vagrant-aws`: 

```bash
 vagrant plugin install vagrant-aws
```

## Extra steps for Windows

Install git bash, see https://git-scm.com/downloads.

On Windows you need to install rsync locally. To do that, follow these steps:

* Install mingw: http://sourceforge.net/projects/mingw/files/Installer/
* Using mingw, install the bin package `msys-rsync`.
* From `C:\MinGW\msys\1.0\bin`, copy the following files to ~/bin:
  * rsync.exe
  * msys-1.0.dll
  * msys-iconv-2.dll
  * msys-intl-8.dll
  * msys-popt-0.dll
