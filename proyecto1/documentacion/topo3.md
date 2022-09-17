# <center>TOPOLOGIA 3 </center>

La topologia tres es la que se muestra a continuación. 
<div id="MENU">

![topologia3](/proyecto1/documentacion/imagenes/topo3.png)

1. [**ESW8**](#CLIENTE1)
1. [**ESW9**](#CLIENTE2)
1. [**ESW10**](#CLIENTE3)
1. [**ESW11**](#TRANSPARENT)

[TOPOLOGIAS](/proyecto1/README.md)

<div id="CLIENTE1">

**EWS8**
```shell
#CONFIGURACION VTP CLIENT
conf t
vtp domain GRUPO1
vtp password grupo1
vtp mode client
exit 
exit

#VISUALIZAR VTP
sh vtp st

#CONFIGURACION INTERFACES TRUNK
conf t
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

#VISUALIZACION INTERFACES
sh int tr

#CONFIGURACION INTERFACES ACCESS
conf t
int f1/2
switchport mode access
switchport trunk access vlan 40
exit
int f1/3
switchport mode access
switchport trunk access vlan 40
exit
exit

#VISUALIZACION INTERFACES
sh vlan-sw
```
[**MENU**](#MENU)

<div id="CLIENTE2">

**EWS9**
```shell
#CONFIGURACION VTP CLIENT
conf t
vtp domain GRUPO1
vtp password grupo1
vtp mode client
exit 
exit

#VISUALIZAR VTP
sh vtp st

#CONFIGURACION INTERFACES
conf t
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

#VISUALIZACION INTERFACES
sh int tr

#CONFIGURACION INTERFACES ACCESS
conf t
int f1/1
switchport mode access
switchport trunk access vlan 30
exit
int f1/4
switchport mode access
switchport trunk access vlan 30
exit
exit
```
[**MENU**](#MENU)

<div id="CLIENTE3">

**EWS10**
```shell
#CONFIGURACION VTP CLIENT
conf t
vtp domain GRUPO1
vtp password grupo1
vtp mode client
exit 
exit

#VISUALIZAR VTP
sh vtp st

#CONFIGURACION INTERFACES
conf t
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

#VISUALIZACION INTERFACES
sh int tr

#CONFIGURACION INTERFACES ACCESS
conf t
int f1/1
switchport mode access
switchport trunk access vlan 30
exit
int f1/4
switchport mode access
switchport trunk access vlan 30
exit
exit
```
[**MENU**](#MENU)

<div id="TRANSPARENT">

**EWS11**
```shell
#CONFIGURACION VTP TRANSPARENT
conf t
vtp domain GRUPO1
vtp password grupo1
vtp mode transparent
vtp version 2
exit 
exit

#VISUALIZAR VTP
sh vtp st

#CONFIGURACION INTERFACES
conf t
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

#VISUALIZACION INTERFACES
sh int tr

#CONFIGURACION INTERFACES ACCESS
conf t
int f1/1
switchport mode access
switchport trunk access vlan 20
exit
exit
```
[**MENU**](#MENU)