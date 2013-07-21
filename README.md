Vagrant Drupal
==============

Drupal specific vagrant configured virtual box. The single command line installation script will take care
of everything, and when finished http://local.drupal.org should be accessable for review. This repo makes
use of the submodule [Vagrant](https://github.com/delphian/vagrant) which contains all the actual vagrant
configuration and puppet scripts.

Installation script will:

 * Create a virtual box on 33.33.33.36
 * Modify hosts file mapping local.drupal.org to 33.33.33.36
 * Create the drupal database.
 * Install drupal.
 * Install and enable modules: devel.
 * Disable modules: overlay.

#### Prerequisites ####

1. Download and install install virtualbox for [Windows](http://download.virtualbox.org/virtualbox/4.2.6/VirtualBox-4.2.6-82870-Win.exe) or [Mac](http://download.virtualbox.org/virtualbox/4.2.6/VirtualBox-4.2.6-82870-OSX.dmg).
2. Download and install vagrant for [Windows](http://files.vagrantup.com/packages/476b19a9e5f499b5d0b9d4aba5c0b16ebe434311/Vagrant.msi) or [Mac](http://files.vagrantup.com/packages/476b19a9e5f499b5d0b9d4aba5c0b16ebe434311/Vagrant.dmg)
3. If you are on windows please download and install [Cygwin](http://cygwin.com/setup.exe). See [Cygwin Setup](http://cygwin.com/cygwin-ug-net/setup-net.html#setup-packages) for help. Make sure to install ssh and git packages.

#### Installation ####

Copy and paste this [installation script](https://gist.github.com/delphian/6048720) into your shell to install everything.

```
curl -s https://raw.github.com/delphian/vagrant-drupal-7/master/scripts/bootstrap.sh | bash
```

#### Usage ####

After installation script is finished open a browser and navigate to http://local.drupal.org