## Overview

Subversion es una herramienta de control de version de archivos centralizada. 
Es uno de los sistemas de versionamiento de código con muchos usuarios en Chile
y en CoreDevX se me ha mencionado la necesidad de comprender su funcionamiento 
a nivel de usuario.

## Prueba de Concepto

OS: Ubuntu 14.04 (Trusty Tahr)

### Instalación

#### Opciones Linux

-[wandisco](https://www.wandisco.com/subversion/download#ubuntu)

```bash
sudo apt-get install -y subversion
sudo apt-get install -y libapache2-svn
...
rvaldes@cyberlaptop-vbox-ubuntu14:~$ svn --version
svn, version 1.8.8 (r1568071)
   compiled Aug 20 2015, 12:51:30 on x86_64-pc-linux-gnu

Copyright (C) 2013 The Apache Software Foundation.
This software consists of contributions made by many people;
see the NOTICE file for more information.
Subversion is open source software, see http://subversion.apache.org/

The following repository access (RA) modules are available:

* ra_svn : Module for accessing a repository using the svn network protocol.
  - with Cyrus SASL authentication
  - handles 'svn' scheme
* ra_local : Module for accessing a repository on local disk.
  - handles 'file' scheme
* ra_serf : Module for accessing a repository via WebDAV protocol using serf.
  - using serf 1.3.3
  - handles 'http' scheme
  - handles 'https' scheme

rvaldes@cyberlaptop-vbox-ubuntu14:~$ 
```


## [Inicialización de Repositorio](https://subversion.apache.org/quick-start)



```bash
$ mkdir -p $HOME/.svnrepos/
$ svnadmin create ~/.svnrepos/my-repos
$ svn mkdir -m "Crear estructura de directorios." file://$HOME/.svnrepos/my-repos/trunk file://$HOME/.svnrepos/my-repos/branches file://$HOME/.svnrepos/my-repos/tags
$ cd my-directory
$ svn checkout file://$HOME/.svnrepos/my-repos/trunk ./
$ svn add --force ./
$ svn commit -m "Initial import"
$ svn up
```


# Subversion Source Control 

https://subversion.apache.org/

# Overview

From Subversion Apache Website:

## Subversion

"Enterprise-class centralized version control for the masses."

## Documentación

https://subversion.apache.org/docs/

## Instalación Subversion en Ubuntu 14.04

## Apache Subversion: Quick Start

https://subversion.apache.org/quick-start

$ mkdir -p $HOME/.svnrepos/
$ svnadmin create ~/.svnrepos/my-repos
$ svn mkdir -m "Create directory structure." file://$HOME/.svnrepos/my-repos/trunk file://$HOME/.svnrepos/my-repos/branches file://$HOME/.svnrepos/my-repos/tags
$ cd my-directory
$ svn checkout file://$HOME/.svnrepos/my-repos/trunk ./
$ svn add --force ./
$ svn commit -m "Initial import"
$ svn up


[Desde el Libro](http://svnbook.red-bean.com/nightly/en/svn.intro.quickstart.html)

## Configuración


## Version Control Basics 
### [Fundamental Concepts](http://svnbook.red-bean.com/en/1.7/svn.basic.version-control-basics.html)




### [Eclipse Subversive Plug-In](https://eclipse.org/subversive/installation-instructions.php)

### Bamboo - Subversion
---


### Puppet

https://forge.puppet.com/puppetlabs/vcsrepo
Nota: este módulo no instala el software VCS.

### Saltstack
