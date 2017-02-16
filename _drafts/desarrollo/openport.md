#Abrir puerto 8081 para acceder a aplicación web


[root@centos65 ~]#
[root@centos65 ~]# iptables -I INPUT -p tcp -m tcp --dport 8081 -j ACCEPT
[root@centos65 ~]# service iptables save
iptables: Guardando las reglas del cortafuegos en /etc/sysc[  OK  ]tables:
