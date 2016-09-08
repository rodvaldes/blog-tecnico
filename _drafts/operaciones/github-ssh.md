# Configuración llaves SSH para acceso a github.

## Overview

Acceso y autenticación automática vía llaves y tunel ssh.

## Documentación

[Generando llaves ssh](https://help.github.com/articles/generating-an-ssh-key/)

### Verificar llaves actuales

```bash
rvaldes@ubuntu:~/github/blog-tecnico$ cd
rvaldes@ubuntu:~$ ls -al ~/.ssh
ls: cannot access /home/rvaldes/.ssh: No such file or directory
rvaldes@ubuntu:~$
```

### [Generar claves SSH](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
ssh-keygen -t rsa -b 4096 -C "rodrigovaldes@gmail.com"
...
rvaldes@ubuntu:~/github/blog-tecnico$ 
rvaldes@ubuntu:~/github/blog-tecnico$ cd
rvaldes@ubuntu:~$ ls -al ~/.ssh
ls: cannot access /home/rvaldes/.ssh: No such file or directory
rvaldes@ubuntu:~$ ssh-keygen -t rsa -b 4096 -C "rodrigovaldes@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/home/rvaldes/.ssh/id_rsa): 
Created directory '/home/rvaldes/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/rvaldes/.ssh/id_rsa.
Your public key has been saved in /home/rvaldes/.ssh/id_rsa.pub.
The key fingerprint is:
32:35:91:27:7b:d8:b1:ed:da:67:99:ae:ed:3f:08:bb rodrigovaldes@gmail.com
The key's randomart image is:
+--[ RSA 4096]----+
|        ..       |
|        o.o      |
|        o* +     |
|       .o.+ .    |
|      o S. .     |
|       o   ..    |
|           oo .o |
|          ...o=. |
|           Eo*+.o|
+-----------------+
.....
rvaldes@ubuntu:~$ eval "$(ssh-agent -s)"
Agent pid 6040
rvaldes@ubuntu:~$ ssh-add ~/.ssh/id_rsa
Enter passphrase for /home/rvaldes/.ssh/id_rsa: 
Identity added: /home/rvaldes/.ssh/id_rsa (/home/rvaldes/.ssh/id_rsa)
```

### [Agregar la llave SSH a la cuenta GitHub.](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/#platform-linux)

```bash
sudo apt-get install xclip
$ sudo apt-get install xclip
# Downloads and installs xclip. If you don't have `apt-get`, you might need to use another installer (like `yum`)
$ xclip -sel clip < ~/.ssh/id_rsa.pub
# Copies the contents of the id_rsa.pub file to your clipboard

rvaldes@ubuntu:~$ xclip -sel clip < ~/.ssh/id_rsa.pub
rvaldes@ubuntu:~$ 

git@github.com:roxtrongo/blog-tecnico.git
```
https://confluence.atlassian.com/bitbucket/set-up-ssh-for-git-728138079.html



