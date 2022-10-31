><img src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Usac_logo.png" alt="drawing" width="75">
>
> Universidad San Carlos de Guatemala
>
>Facultad de Ingeniería 
>Escuela de Ciencias y Sistemas 
>Segundo Semestre, 2022
>
>Laboratorio de Redes de Computadoras 1

### Grupo No.1

Integrantes:


## <center> DATOS DE LOS ESTUDIANTES </center>
| Nombre                               | Carnet     |  
| ------------------------------------ | ---------  | 
| José Ignacio Martinez Hernandez      |  201408507 | 
| Luis Roberto Boror Yoc               |  201403517 | 
| Erick Javier Bernal Orellana         |  201480017 | 
| Claudia Iovana Miranda Alvarez       |  201700387 | 
---
<br>


 <h1 align="center" > PROYECTO 2</h1>



<div id='content'/>

## CONTENIDO

1. [DESCRIPCION](#id1)
2. [RED FISICA](#id2)
3. [TOPOLOGIA 1](#id3)
4. [TOPOLOGIA 2](#id4)
5. [TOPOLOGIA 3](#id5)
6. [CONFIGURACIONES](#id6)

<div id='id1'/>

## 1. DESCRIPCION  [ ⇧](#content)
<div class=''text-justify''>
La empresa “Libros Real S.A”, nos ha contratado para la siguiente configuración que les servirá para organizar de manera segura y eficiente los diferentes departamentos con los que cuenta la empresa, en dos distintos lugares de trabajo; uno de esos lugares es el centro de datos y el otro es la oficina central la cual está próxima a inaugurarse.

Para este caso el centro de datos consta con 4 servidores, el servidor web de ventas, de contabilidad, de recursos humanos e informática, los cuales se encuentran
en subredes diferentes como se muestra en la topología del centro de datos.

La empresa quiere implementar una topología de red para comunicarse desde la
oficina central con el centro de datos.

Los administradores, la base de datos y los servidores web deben de estar en
VLAN diferentes cada uno.

Se debe de proveer la siguiente configuración en la red para cumplir con las
expectativas y requerimientos que la empresa necesita:

- Garantizar que el servidor de contabilidad sea solo accedido por usuarios del departamento de contabilidad y el servidor de recursos humanos sea solo accedido por usuarios del departamento de recursos humanos.

- Garantizar que el servidor web de e-commerce sea accedido solo por los usuarios de ventas.

- Garantizar que el servidor de informática sea accedido únicamente por usuarios del departamento de desarrollo.

- Garantizar la comunicación de los administradores con todos los servidores web.
 </div>
<div id='id2'/>

## 2. RED FISICA [ ⇧](#content)
Para el Proyecto 2, nos hemos apoyado de las herramientas:

<p align="center">
  <img src="https://www.gstatic.com/devrel-devsite/prod/v3d59008e544647a0ef15b3aa6144afaaec4bb33821f37d7fece1fe7311821ed6/cloud/images/favicons/onecloud/apple-icon.png" alt="drawing" width="100" height= "100">  <img src="https://es.vpnmentor.com/wp-content/uploads/2017/08/Openvpn20Logo.png" alt="drawing" width="200"> 
</p>




Para darle solucion a este problema, conectaron 3 computadoras fisicas por medio de la VPN formando una pequeña red donde estas tienen conexión y acceso a propiedades de red tradicionales como archivos compartidos, y muchas cosas mas por defecto. A continuacion se muestra el grafico que describe nuestra Red Fisica:

<p align="center">
  <img src="recursos/redfisica.png" alt="drawing" width="600">
</p>

# TOPOLOGIA GENERAL
en esta parte se encuentra la funcionalidad general.
<p align="center">
  <img src="recursos/topologias/general.png" alt="drawing" width="600">
</p>


<div id='id3'/>

## 3. TOPOLOGIA 1  [ ⇧](#content)
Se realizo el cálculo de subredes de la red 10.1.0.0/16, y se obtuvieron las subredes necesarias para conectar toda la red.
- Se asignaron las direcciones IP a cada uno de los router.
- Se configuraron las rutas estáticas necesarias en los routers para que sea posible establecer la comunicación del centro de datos y la oficina central.
- Se configuro el protocolo de redundancia GLBP.
- Se configuro protocolo de redundancia HSRP.

### Red WAN (Interconexión de centro de datos y oficina central)
```sh
Imagen descriptiva de la Topologia 1
```
<p align="center">
  <img src="recursos/topologias/topologia_1.png" alt="drawing">
</p>

```sh
Para esta red se realizo el calculo FLSM que se describe en la siguiente tabla: 
```
<p align="left">
  <img src="recursos/topologias/tabla_1.png" alt="drawing" width="620" height="400">
</p>



<div id='id4'/>

## 4. TOPOLOGIA 2  [ ⇧](#content)

### Oficina Central

Dentro de la oficina central se encuentran cuatro departamentos:
  - Recursos Humanos
  - Contabilidad
  - Ventas
  - Bases de datos.


El departamento de recursos humanos cuenta con: 
  - 1 Gerente
  - 15 Reclutadores
  - 5 Analistas de recursos humanos.


El departamento de contabilidad es el más pequeño y actualmente cuenta con:
  - 1 Gerente
  - 5 asistentes de contabilidad 
  - 1 contador en general 
  - 1 auditor

El departamento ventas es el departamento más grande, la empresa prevé un crecimiento de hasta un 32%, cuenta con:
  - 76 Operadores de ventas
  - 4 Encargados de cuentas
  - 12 Managers
  - 1 gerente

  
En el departamento de informática se prevee un crecimiento hasta un 18% por lo que se considero el crecimiento de la Red, cuenta con:
  - 15 Programadores
  - 5 Gestores de proyectos
  - 1 Administrador de la base de datos
  - 3 Analistas de infraestructura
  - 6 Testers
  - 1 Gerente


```sh
Imagen descriptiva de la Topologia 2
```
<p align="center">
  <img src="recursos/topologias/topologia_2.png" alt="drawing">
</p>



```sh
Para esta red se realizo el calculo VLSM que se describe en la siguiente tabla: 
```
<p align="left">
  <img src="recursos/topologias/tabla_2.png" alt="drawing" >
</p>

<div id='id5'/>

##  TOPOLOGIA3 [ ⇧](#content)


### Centro de Datos
Para esta topologia ise utilizo la red 192.168.51.0/24 la cual se administro en subredes para los departamentos que se mensionaron anteriormente.


 
  - Se crearon las VLANs correspondientes para realizar la configuración de los puertos, asignando el modo y VLAN correspondientes.
  - Se configuraron las rutas estáticas necesarias en R1 para que sea posible establecer comunicación entre el centro de datos y la oficina central
```sh
Imagen descriptiva de la Topologia 3
```
<p align="center">
  <img src="recursos/topologias/topologia_3.png" alt="drawing">
</p>

```sh
Para esta red se realizo el calculo que se describe a continuacion: 
192.168.51.0/24
```
<p align="left">
  <img src="recursos/topologias/tabla_3.png" alt="drawing" >
</p>
<div id='id6'/>

##  CONFIGURACIONES [ ⇧](#content)


```bat
CONFIGURACIONES ESW1
REM ESW1
    REM CONFIGURACIÓN VTP
    conf t
    vtp domain redes1gp1
    vtp password redes1gp1
    vtp mode server
    vtp version 2
    #comprobar la configuración
        sh vtp st

  REM configuración de VLAN
	conf t
	vlan 10
	name RHUMANOS
	vlan 20 
	name CONTABILIDAD
	vlan 30
	name VENTAS
	vlan 40
	name INFORMATICA
```

```bat
REM CONFIGURACION DE ESW1 F1/10 EN MODO TRUNK
    conf t
    int f1/0
    switchport mode trunk
    switchport trunk allowed vlan 1,10,20,30,40,1002-1005
    sh int tr
```

```sh
  # configuración de port channel en cada bloque de conexiones.
# consejos:
	# repetir la configuración, para cada bloque de port channel
	#en simultáneo para evitar que falle
	# Solo falta cambiar para cada configuración la interfaz(f1/ 3 - 4) correspondiente
# Para “channel-group # mode on”, el número indica el número del texto en rojo

 ```
<p align="center">
  <img src="recursos/topologias/config_portChanel.png" alt="drawing" width="320" height="200">
</p>

```bat
REM ESW1
    REM configuración de port channel 
        conf t
        interface range fastEthernet 1/3 - 4
        channel-group 2 mode on

REM  ESW3
    REM configuración de port channel ESW3
        conf t
        interface range fastEthernet 1/3 - 4
        channel-group 2 mode on


```

```bat
REM  ESW1
    REM configuración acceso a vlan mode trunk y port channel
        conf t
        interface port-channel 2
        switchport mode trunk
        switchport trunk allowed vlan 1,10,20,30,40,1002-1005

REM ESW3
    REM configuración acceso a vlan mode trunk y port channel
        conf t
        interface port-channel 2
        switchport mode trunk
        switchport trunk allowed vlan 1,10,20,30,40,1002-1005



```


```bat
REM  configuración modo acceso para ESW5, ESW6 y ESW7

    REM ESW5
	conf t
	int f1/2
	switchport mode access
	switchport access vlan 20
	exit
	int f1/1
	switchport mode access
	switchport access vlan 40

	REM ESW6
	conf t
	int f1/2
	switchport mode access
	switchport access vlan 30
	exit
	int f1/1
	switchport mode access
	switchport access vlan 40

	REM ESW7
	conf t
	int f1/11
	switchport mode access
	switchport access vlan 30
	exit
	int f1/12
	switchport mode access
	switchport access vlan 10

```

```bat
REM configuración para VPCS
	REM asignar la ip correspondiente
    ip 192.168.10.10 255.255.255.0 192.168.10.1
    save
    sh ip
```

configuración de puertos en slot1 : “NM-1FE-TX” en R5
<p align="left">
  <img src="recursos/topologias/R5.png" alt="drawing" >
</p>

```bat
REM configuración de las inter-Vlan en R5
	conf t
    int f1/0
    no shutdown
    int f 1/0.10
    int f 1/0.20
    int f 1/0.30
    int f 1/0.40
    do sh run

    REM VLAN 10 = RHUMANOS
    int f1/0.10
    encapsulation dot1Q 10
    ip address 192.168.41.193 255.255.255.224

    REM VLAN 20 = CONTABILIDAD
    int f1/0.20
    encapsulation dot1Q 20
    ip address 192.168.41.225 255.255.255.240

    REM VLAN 30 = VENTAS
    int f1/0.30
    encapsulation dot1Q 30
    ip address 192.168.41.1 255.255.255.128

    REM VLAN 40 = VENTAS
    int f1/0.40
    encapsulation dot1Q 40
    ip address 192.168.41.129 255.255.255.192

sh ip ro
sh ip int br
RUTEO RIP

```

## PRUEBAS RUTEO ESTATICO

<table>
  <tr>
    <th style="background-color:gray">R1</th>
   
  </tr>
<tr style="background-color:yellow; color:black">
    <td>
    <li>ip route 192.168.41.0 255.255.255.128 10.1.0.1</li>
    <li>ip route 192.168.41.128 255.255.255.192 10.1.0.1</li>
    <li>ip route 192.168.41.192 255.255.255.224 10.1.0.1</li>
    <li>ip route 192.168.41.224 255.255.255.240 10.1.0.1</li>
    </td>  
</tr>
  <tr style="background-color:blue;" >
    <td>
    <li>ip route 192.168.51.0 255.255.255.192 10.1.64.2</li>
    <li>ip route 192.168.51.64 255.255.255.192 10.1.64.2</li>
    <li>ip route 192.168.51.128 255.255.255.192 10.1.64.2</li>
    <li>ip route 192.168.51.192 255.255.255.192 10.1.64.2</li>
</td>
   
  </tr>
  <tr style="background-color:black">
    <td><li>ip route 10.1.64.0 255.255.224.0 10.1.32.2 </li>
    </td>
   
  </tr>
</table>

<br/>
<br/>
<table>
  <tr>
    <th style="background-color:gray">R2</th>
   
  </tr>
<tr style="background-color:yellow; color:black">
     <td>
    <li>ip route 192.168.41.0 255.255.255.128 10.1.96.1   </li>
    <li>ip route 192.168.41.128 255.255.255.192 10.1.96.1 </li>
    <li>ip route 192.168.41.192 255.255.255.224 10.1.96.1 </li>
    <li>ip route 192.168.41.224 255.255.255.240 10.1.96.1</li>
    </td>
</tr>
  <tr style="background-color:blue;" >
    <td>
    <li>ip route 192.168.51.0 255.255.255.192 10.1.160.2</li>
    <li>ip route 192.168.51.64 255.255.255.192 10.1.160.2</li>
    <li>ip route 192.168.51.128 255.255.255.192 10.1.160.2</li>
    <li>ip route 192.168.51.192 255.255.255.192 10.1.160.2</li>
</li>
    </td>
   
  </tr>
  <tr style="background-color:black">
    <td><li>ip route 10.1.160.0 255.255.224.0 10.1.128.2  </li>
    </td>
   
  </tr>
</table>
<br/>
<br/>

<table>
  <tr>
    <th style="background-color:gray">R3</th>
   
  </tr>
<tr style="background-color:yellow; color:black">
    <td>
    <li>ip route 192.168.41.0 255.255.255.128 10.1.96.1</li>
    <li>ip route 192.168.41.128 255.255.255.192 10.1.96.1</li>
    <li>ip route 192.168.41.192 255.255.255.224 10.1.96.1</li>
    <li>ip route 192.168.41.224 255.255.255.240 10.1.96.1</li>

</tr>
  <tr style="background-color:blue;" >
    <td>
    <li>ip route 192.168.51.0 255.255.255.192 10.1.160.2</li>
    <li>ip route 192.168.51.64 255.255.255.192 10.1.160.2</li>
    <li>ip route 192.168.51.128 255.255.255.192 10.1.160.2</li>
    <li>ip route 192.168.51.192 255.255.255.192 10.1.160.2</li>
</td>
   
  </tr>
  <tr style="background-color:black">
    <td><li>ip route 10.1.96.0 255.255.224.0 10.1.128.1 </li>
    </td>
   
  </tr>
</table>

<br/>
<br/>


<table>
  <tr>
    <th style="background-color:gray">R4</th>
   
  </tr>
<tr style="background-color:yellow; color:black">
    <td>
    <li>ip route 192.168.41.0 255.255.255.128 10.1.0.1</li>
    <li>ip route 192.168.41.128 255.255.255.192 10.1.0.1</li>
    <li>ip route 192.168.41.192 255.255.255.224 10.1.0.1</li>
    <li>ip route 192.168.41.224 255.255.255.240 10.1.0.1</li>
    </td>  
</tr>
  <tr style="background-color:blue;" >
    <td>
    <li>ip route 192.168.51.0 255.255.255.192 10.1.64.2</li>
    <li>ip route 192.168.51.64 255.255.255.192 10.1.64.2</li>
    <li>ip route 192.168.51.128 255.255.255.192 10.1.64.2</li>
    <li>ip route 192.168.51.192 255.255.255.192 10.1.64.2</li>
</td>
   
  </tr>
  <tr style="background-color:black">
    <td>
    <li>ip route 10.1.64.0 255.255.224.0 10.1.32.1 </li>
    </td>
  </tr>
</table>

<br/>

<br/>

<table>
  <tr>
    <th style="background-color:gray">R5</th>
   
  </tr>
<tr style="background-color:blue;">
    <td>
    <li>ip route 192.168.51.0 255.255.255.192 10.1.0.2</li>
    <li>ip route 192.168.51.64 255.255.255.192 10.1.0.2</li>
    <li>ip route 192.168.51.128 255.255.255.192 10.1.0.2</li>
    <li>ip route 192.168.51.192 255.255.255.192 10.1.0.2</li>
    <li>ip route 192.168.51.0 255.255.255.192 10.1.96.2</li>
    <li>ip route 192.168.51.64 255.255.255.192 10.1.96.2</li>
    <li>ip route 192.168.51.128 255.255.255.192 10.1.96.2</li>
    <li>ip route 192.168.51.192 255.255.255.192 10.1.96.2</li>
    </td>


  </tr>
  <tr style="background-color:black">
    <td>
    <li>ip route 10.1.32.0 255.255.224.0 10.1.0.2 </li>
    <li>ip route 10.1.64.0 255.255.224.0 10.1.0.2 </li>
    <li>ip route 10.1.128.0 255.255.224.0 10.1.96.2 </li>
    <li>ip route 10.1.160.0 255.255.224.0 10.1.96.2 </li>
 </li>
    </td>
   
  </tr>
</table>

<br/>
<br/>

<table>
  <tr>
    <th style="background-color:gray">R6</th>
   
  </tr>
<tr style="background-color:yellow; color:black">
    <td>
    <li>ip route 192.168.41.0 255.255.255.128 10.1.64.1</li>
    <li>ip route 192.168.41.128 255.255.255.192 10.1.64.1</li>
    <li>ip route 192.168.41.192 255.255.255.224 10.1.64.1</li>
    <li>ip route 192.168.41.224 255.255.255.240 10.1.64.1</li>
    <li>ip route 192.168.41.0 255.255.255.128 10.1.160.1</li>
    <li>ip route 192.168.41.128 255.255.255.192 10.1.160.1</li>
    <li>ip route 192.168.41.192 255.255.255.224 10.1.160.1</li>
    <li>ip route 192.168.41.224 255.255.255.240 10.1.160.1</li>
</li>
    </td>  
</tr>
</tr>
  <tr style="background-color:black">
    <td>
    <li>ip route 10.1.0.0 255.255.224.0 10.1.64.1 </li>
<li>ip route 10.1.32.0 255.255.224.0 10.1.64.1 </li>
<li>ip route 10.1.96.0 255.255.224.0 10.1.160.1 </li>
<li>ip route 10.1.128.0 255.255.224.0 10.1.160.1 </li>
</li>
    </td>
   
  </tr>
</table>
