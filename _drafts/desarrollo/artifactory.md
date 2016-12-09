# Instalación de Artifactory en CentOS 6.5

## Overview

EL desarrollo del pipeline de xxxxxxx requiere un sistema de almacenamiento de artefactos.
Los artefactos son los resultados del proceso de building de software y al igual que en 
la industria de manufactura, estos productos deben estar clasificados. almacenados y 
disponibles en cuanto sea necesario utilizarlos ya sea para deployment o inclusión como
librerías en el caso de los proyectos de este tipo.

## Componentes de Instalación 

1.- Hardware con capacidades de virtualización. 
2.- Software Hipervisor(VirtualBox, VMware, ).
3.- Linux CentOS 6.5.

## Creación de la máquina virtual

1.- Descarga de software CentOS 6.5.
2.- Creación máquina virtualbox CentOS 6.5.
3.- Inicio Máquina.


## Instalación de Sistema Operativo 

1.- Arrancar la máquina booteando desde el controlador IDE que está apuntando a la imagen
ISO de instalación.

2.- Setear configuración de instalación.

## Instalación de middleware

1.- Se instala Oracle JDK8. 
https://www.digitalocean.com/community/tutorials/how-to-install-java-on-centos-and-fedora 

2.- Snapshot de máquina virtual. 

3.- 

## Instalación de Artifactory

1.- Descarga de Artifactory

a) Instalación vía RPM

wget https://bintray.com/jfrog/artifactory-rpms/rpm -O bintray-jfrog-artifactory-rpms.repo
sudo mv bintray-jfrog-artifactory-rpms.repo /etc/yum.repos.d/
sudo yum install jfrog-artifactory-oss













 
