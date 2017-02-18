# SonarQube #
====

## Introducción ##
===

Sonarqube es una plataforma Open Source de administración de calidad de código.


## [Documentación](http://docs.sonarqube.org/display/SONAR/Documentation)
## [Analizar Código fuente](http://docs.sonarqube.org/display/SONAR/Analyzing+Source+Code)

##Docker Test##

1.- Obtener contenedor oficial.

docker pull somarqube

2.- Iniciar el contenedor

docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 sonarqube
docker run -it -p 9000:9000 sonarqube


##Vagrant Sonarqube environment##

```java
vagrant box add ubuntu-14.04 https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box
cyberlaptop:sonarqube rvaldes$ vagrant box add ubuntu-14.04 https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box
==> box: Box file was not detected as metadata. Adding it directly...
==> box: Adding box 'ubuntu-14.04' (v0) for provider:
    box: Downloading: https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box
==> box: Successfully added box 'ubuntu-14.04' (v0) for 'virtualbox'!

.......


cyberlaptop:sonarqube rvaldes$ vagrant init ubuntu-14<.04
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
```
https://github.com/bastien03/sonarqube


Intento 2 Vagrant
========



https://packages.chef.io/files/stable/chefdk/1.2.22/mac_os_x/10.12/chefdk-1.2.22-1.dmg
https://downloads.chef.io/chefdk

Instalación Chefdk

Alternativa 1: Mac DMG packagging system. 

Mac Os XMac OS X/macOS
Mac OS X/macOS 10.12
License Information

Architecture: x86_64
SHA256: 5c435de289e90da45938a0f1a1f7e472e73a84f9b6bbe93e50342e11cc935458
URL: https://packages.chef.io/files/stable/chefdk/1.2.22/mac_os_x/10.12/chefdk-1.2.22-1.dmg

Alternativa 2: Mac brew install 
```java
cyberlaptop:vagrant-sonarqube rvaldes$ brew install Caskroom/cask/chefdk
To install it, run:
  brew install Caskroom/cask/chefdk
cyberlaptop:vagrant-sonarqube rvaldes$ brew install Caskroom/cask/chefdk
Updating Homebrew...
==> Auto-updated Homebrew!
Updated 1 tap (homebrew/core).
==> New Formulae
knot-resolver

==> brew cask install Caskroom/cask/chefdk
==> Downloading https://packages.chef.io/stable/mac_os_x/10.11/chefdk-0.18.26-1.dmg
######################################################################## 100.0%
==> Verifying checksum for Cask chefdk
==> Running installer for chefdk; your password may be necessary.
==> Package installers may write to any location; options such as --appdir are ignored.
Password:
^[[D==> installer: Package name is Chef Development Kit
==> installer: Upgrading at base path /
==> installer: The upgrade was successful.
🍺  chefdk was successfully installed!
```

### Videos Referencias
===

* https://www.youtube.com/watch?v=pxRBDMPmEuo&index=3&list=PLRRgDQV61kJ7O6eNBio9slXWnVvJw9j3u
