# <center>TOPOLOGIA 2 </center>

La topologia dos es la que se muestra a continuación. 
<div id="MENU">

![topologia2](/proyecto1/documentacion/imagenes/topo2.png)

Se tiene 4 switchs y una vpc. El ESW es configurado como servidor en donde se encuentran las VLANS.

1. [**ESW4**](#SERVER)
1. [**ESW5**](#CLIENTE1)
1. [**ESW6**](#CLIENTE2)
1. [**ESW7**](#CLIENTE3)

[TOPOLOGIAS](/proyecto1/README.md)

<div id="SERVER">

**EWS4**

```shell
#CREACION VLANS
conf t
vlan 10
name RRHH
exit
vlan 20
name INFORMATICA
exit
vlan 30
name CONTABILIDAD
exit
vlan 40
name VENTAS
exit
exit

#VISUALIZAR VLANS
sh vlan-sw

#CONFIGURACION VTP SERVER
conf t
vtp domain GRUPO1
vtp password grupo1
vtp mode server
vtp version 2
exit 
exit

#VISUALIZAR VTP
sh vtp st

#CREACION DEL SPANNING-TREE
spanning-tree vlan 10 root primary
spanning-tree vlan 20 root primary
spanning-tree vlan 30 root primary
spanning-tree vlan 40 root primary

#CONFIGURACION INTERFACES
conf t
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/1
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
```
[**MENU**](#MENU)


<div id="CLIENTE1">

**EWS5**

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
int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

#VISUALIZACION INTERFACES
sh int tr
```
[**MENU**](#MENU)

<div id="CLIENTE2">

**EWS6**

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
int f1/1
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
```
[**MENU**](#MENU)

<div id="CLIENTE3">

**EWS7**

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
int f1/0
switchport mode access
switchport trunk access vlan 20
exit
exit

#VISUALIZACION INTERFACES
sh vlan-sw
```
[**MENU**](#MENU)