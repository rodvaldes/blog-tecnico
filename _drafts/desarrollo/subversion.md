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