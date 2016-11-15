# vagrant-aws-helper
Helper for setting up AWS EC2 instances with vagrant using vagrant-aws, see https://github.com/mitchellh/vagrant-aws.

# Prerequisites

* Install vagrant, for details see https://www.vagrantup.com.
* Install `vagrant-aws`: 

```shell
vagrant plugin install vagrant-aws
```
* Add your AWS credentials to `~/.aws/aws.credentials`, see [this example file](../master/examples/aws.credentials).
 * On Windows, use `mkdir ~/.aws` from your command prompt to create the `.aws` directory.


## Extra steps for Windows
Support for Windows is a bit limited. No synced file systems possible.

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

You need to run vagrant up as

```shell
vagrant up --no-provision
```
