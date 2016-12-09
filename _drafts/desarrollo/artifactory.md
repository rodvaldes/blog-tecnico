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

[root@centos65 ~]# wget https://bintray.com/jfrog/artifactory-rpms/rpm -O bintray-jfrog-artifactory-rpms.repo
--2016-12-08 22:18:06--  https://bintray.com/jfrog/artifactory-rpms/rpm
Resolviendo bintray.com... 108.168.194.93
Connecting to bintray.com|108.168.194.93|:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: no especificado [text/plain]
Saving to: `bintray-jfrog-artifactory-rpms.repo'

    [ <=>                                                                  ] 219         --.-K/s   in 0s      

2016-12-08 22:18:07 (17,8 MB/s) - `bintray-jfrog-artifactory-rpms.repo' saved [219]

[root@centos65 ~]# sudo mv bintray-jfrog-artifactory-rpms.repo /etc/yum.repos.d/
[root@centos65 ~]# sudo yum install jfrog-artifactory-oss
Complementos cargados:fastestmirror, refresh-packagekit, security
Configurando el proceso de instalación
Loading mirror speeds from cached hostfile
 * base: mirror.gtdinternet.com
 * extras: mirror.gtdinternet.com
 * updates: mirror.gtdinternet.com
bintray--jfrog-artifactory-rpms                                                         | 1.3 kB     00:00     
bintray--jfrog-artifactory-rpms/primary                                                 |  13 kB     00:00     
bintray--jfrog-artifactory-rpms                                                                          89/89
Resolviendo dependencias
--> Ejecutando prueba de transacción
---> Package jfrog-artifactory-oss.noarch 0:4.14.3-40328 will be instalado
--> Resolución de dependencias finalizada

Dependencias resueltas

===============================================================================================================
 Paquete                      Arquitectura  Versión               Repositorio                            Tamaño
===============================================================================================================
Instalando:
 jfrog-artifactory-oss        noarch        4.14.3-40328          bintray--jfrog-artifactory-rpms         39 M

Resumen de la transacción
===============================================================================================================
Instalar       1 Paquete(s)

Tamaño total de la descarga: 39 M
Tamaño instalado: 40 M
Está de acuerdo [s/N]:s
Descargando paquetes:
jfrog-artifactory-oss-4.14.3.rpm                                                        |  39 MB     00:34     
Ejecutando el rpm_check_debug
Ejecutando prueba de transacción
La prueba de transacción ha sido exitosa
Ejecutando transacción
Checking if group artifactory exists...
Group artifactory doesn't exist. Creating ...
Checking if ARTIFACTORY_HOME exists
Checking if user artifactory exists...
User artifactory doesn't exist. Creating ...
useradd: aviso: el directorio personal ya existe.
No se va a copiar ningún fichero del directorio «skel» en él.
Removing tomcat work directory
  Instalando    : jfrog-artifactory-oss-4.14.3-40328.noarch                                                1/1 
Adding the artifactory service to auto-start

The installation of Artifactory has completed successfully.

PLEASE NOTE: It is highly recommended to use Artifactory in conjunction with MySQL. You can easily configure this setup using '/opt/jfrog/artifactory/bin/configure.mysql.sh'.

Checking if group artifactory exists...
Group artifactory exists.
Checking if ARTIFACTORY_HOME exists
Checking if user artifactory exists...
User artifactory exists.
  Verifying     : jfrog-artifactory-oss-4.14.3-40328.noarch                                                1/1 

Instalado:
  jfrog-artifactory-oss.noarch 0:4.14.3-40328                                                                  

¡Listo!
[root@centos65 ~]# service artifactory status
Artifactory Tomcat stopped
[root@centos65 ~]# service artifactory start
/usr/bin/java
Starting Artifactory tomcat as user artifactory...
Max number of open files: 32000
Using ARTIFACTORY_HOME: /var/opt/jfrog/artifactory
Using ARTIFACTORY_PID: /var/opt/jfrog/run/artifactory.pid
Creating directory /var/opt/jfrog/artifactory/logs
Creating directory /var/opt/jfrog/artifactory/logs/catalina
Creating directory /var/opt/jfrog/artifactory/temp
Creating directory /var/opt/jfrog/artifactory/work
Using CATALINA_BASE:   /opt/jfrog/artifactory/tomcat
Using CATALINA_HOME:   /opt/jfrog/artifactory/tomcat
Using CATALINA_TMPDIR: /opt/jfrog/artifactory/tomcat/temp
Using JRE_HOME:        /usr
Using CLASSPATH:       /opt/jfrog/artifactory/tomcat/bin/bootstrap.jar:/opt/jfrog/artifactory/tomcat/bin/tomcat-juli.jar
Using CATALINA_PID:    /var/opt/jfrog/run/artifactory.pid
Tomcat started.
Artifactory Tomcat started in normal mode














 
