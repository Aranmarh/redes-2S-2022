# <center>TOPOLOGIA 1 </center>

La topologia dos es la que se muestra a continuación. 
<div id="MENU">

![topologia1](/proyecto1/documentacion/imagenes/topo1.png)

1. [**ESW1**](#CLIENTE1)
1. [**ESW2**](#CLIENTE2)
1. [**ESW3**](#CLIENTE3)

[TOPOLOGIAS](/proyecto1/README.md)

<div id="CLIENTE1">

**EWS1**

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
exit

#VISUALIZACION INTERFACES
sh int tr
```
[**MENU**](#MENU)

<div id="CLIENTE2">

**EWS2**

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
int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

#VISUALIZACION INTERFACES TRUNK
sh int tr

#CONFIGURACION INTERFACES ACCESS
conf t
int f1/1
switchport mode access
switchport trunk access vlan 10
exit
int f1/2
switchport mode access
switchport trunk access vlan 30
exit
int f1/3
switchport mode access
switchport trunk access vlan 10
exit
exit
```
[**MENU**](#MENU)

<div id="CLIENTE3">

**EWS3**

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
int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

#VISUALIZACION INTERFACES TRUNK
sh int tr

#CONFIGURACION INTERFACES ACCESS
conf t
int f1/1
switchport mode access
switchport trunk access vlan 20
exit
int f1/2
switchport mode access
switchport trunk access vlan 40
exit
int f1/3
switchport mode access
switchport trunk access vlan 30
exit
exit
```
[**MENU**](#MENU)