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

...

rvaldes@ubuntu:~/github/blog-tecnico$ git push
warning: push.default is unset; its implicit value is changing in
Git 2.0 from 'matching' to 'simple'. To squelch this message
and maintain the current behavior after the default changes, use:

  git config --global push.default matching

To squelch this message and adopt the new behavior now, use:

  git config --global push.default simple

When push.default is set to 'matching', git will push local branches
to the remote branches that already exist with the same name.

In Git 2.0, Git will default to the more conservative 'simple'
behavior, which only pushes the current branch to the corresponding
remote branch that 'git pull' uses to update the current branch.

See 'git help config' and search for 'push.default' for further information.
(the 'simple' mode was introduced in Git 1.7.11. Use the similar mode
'current' instead of 'simple' if you sometimes use older versions of Git)

The authenticity of host 'github.com (192.30.253.113)' can't be established.
RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
Counting objects: 23, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (12/12), done.
Writing objects: 100% (13/13), 2.08 KiB | 0 bytes/s, done.
Total 13 (delta 7), reused 0 (delta 0)
remote: Resolving deltas: 100% (7/7), completed with 4 local objects.
To git@github.com:roxtrongo/blog-tecnico.git
   c490f6b..f5603b7  gh-pages -> gh-pages
rvaldes@ubuntu:~/github/blog-tecnico$ 
rvaldes@ubuntu:~/github/blog-tecnico$ 


```
[Agregar llave ssh al repo local](https://confluence.atlassian.com/bitbucket/set-up-ssh-for-git-728138079.html)



