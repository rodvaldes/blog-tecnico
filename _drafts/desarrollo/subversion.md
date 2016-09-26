
## Subversion

## Overview

Subversion es una herramienta de control de version de archivos centralizada. 
Es uno de los sistemas de versionamiento de código con muchos usuarios en Chile
y en CoreDevX se me ha mencionado la necesidad de comprender su funcionamiento 
a nivel de usuario.


## From Subversion Apache Website:

"Enterprise-class centralized version control for the masses."


## Prueba de Concepto

OS: Ubuntu 14.04 (Trusty Tahr)

### Instalación

#### Software

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


## Documentación

https://subversion.apache.org/docs/

## Instalación Subversion en Ubuntu 14.04
## Configuración
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


## Importar archivos y directorios no versionados al repositorio subversion


```bash
$ svn import /path/to/mytree \
             http://svn.example.com/svn/repo/some/project \
             -m "Initial import"
Adding         mytree/foo.c
Adding         mytree/bar.c
Adding         mytree/subdir
Adding         mytree/subdir/quux.h

Committed revision 1.
$
```

## Como hacer checkout "git clone" en Subversion

```bash
rvaldes@cyberlaptop-vbox-ubuntu14:~$ mkdir svntest2
rvaldes@cyberlaptop-vbox-ubuntu14:~$ cd svntest2/
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2$ ls
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2$ svn checkout file:///home/rvaldes/.svnrepos/my-repos/
A    my-repos/tags
A    my-repos/trunk
A    my-repos/trunk/newfolder
A    my-repos/trunk/newfolder/README.md
A    my-repos/trunk/newfolder/newfile.md
A    my-repos/branches
Checked out revision 5.
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2$ ls
my-repos
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2$ cd my-repos/
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos$ ls
branches  tags  trunk
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos$ cd trunk/
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ ls
newfolder
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ nano newfile
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ 
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ 
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ 
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ 
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ svn status
?       newfile
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ svn add newfile 
A         newfile
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ git status
fatal: Not a git repository (or any of the parent directories): .git
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ svn status
A       newfile
rvaldes@cyberlaptop-vbox-ubuntu14:~/svntest2/my-repos/trunk$ svn commit -m "Agrega archivo desde otro folder"
Adding         newfile
Transmitting file data .
Committed revision 6.
```

<<<<<<< HEAD
=======
## [Ciclo básico de trabajo](http://svnbook.red-bean.com/en/1.7/svn.tour.cycle.html)



## Revisar la historia

svn diff
Shows line-level details of a particular change

svn log
Shows you broad information: log messages with date and author information attached to revisions and which paths changed in each revision

svn cat
Retrieves a file as it existed in a particular revision number and displays it on your screen

svn annotate
Retrieves a human-readable file as it existed in a particular revision number, displaying its contents in a tabular form with last-changed information attributed to each line of the file.

svn list
Displays the files in a directory for any given revision

>>>>>>> 12fdfe2ea3088040bdd7a90b0f077bde463fab63
## Version Control Basics 
### [Fundamental Concepts](http://svnbook.red-bean.com/en/1.7/svn.basic.version-control-basics.html)




### [Eclipse Subversive Plug-In](https://eclipse.org/subversive/installation-instructions.php)

### Bamboo - Subversion
---







### Puppet

https://forge.puppet.com/puppetlabs/vcsrepo
Nota: este módulo no instala el software VCS.

### Saltstack
