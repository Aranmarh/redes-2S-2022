><img src="https://upload.wikimedia.org/wikipedia/commons/4/4a/Usac_logo.png" alt="drawing" width="75">
>
>Universidad San Carlos de Guatemala
>
>Facultad de Ingeniería 
>
>Escuela de Ciencias y Sistemas 
>
>Segundo Semestre, 2022
>
>Laboratorio de Redes de Computadoras 1 Sección 

### Grupo No.1

Integrantes:

| Nombre                               | Carnet     | Cliente* | 
| ------------------------------------ | ---------  | -------- |
| José Ignacio Martinez Hernandez      |  201408507 |  1       |
| Luis Roberto Boror Yoc               |  201403517 |  2       |
| Erick Javier Bernal Orellana         |  201480017 |  3       |
| Claudia Iovana Miranda Alvarez       |  201700387 |  4       |
 


# Practica 1

<div id='content'/>

## Contenido

1. [Configuración de las VPC](#id1)
2. [Configuración de las Nubes](#id2)
3. [Pings entre los hosts ](#id3)


<div id='id1'/>

## 1. Configuración de las VPC  [ ⇧](#content)

Configuración de las  ***VPC*** en instancia de máquina virtual.

### Para poder crear un Máquina virtual,  se selecciona en el mennu un VPCS
![ConfiguracionVPN](/practica1/recursos/vpc_1.png "Seleccionar VPC")

### cuando se cra una VPC se muestra el siguiente icono
![ConfiguracionVPN](/practica1/recursos/vpc_2.png "Instancia de VPC")

luego se conecta la vpc al switch a la red local.

### luego de que la VPC este creada dar click derecho sobre la VPCS creada y presionar “Start”, esto iniciara la máquina 		virtual
![ConfiguracionVPN](/practica1/recursos/vpc_3.png "inicio de una VPC")

### luego de iniciar la máquina virtual, tendremos que asignar una ip valida, para ellos 		ejecutamos la consola, dando click derecho sobre la VPCS y seleccionando Console
![ConfiguracionVPN](/practica1/recursos/vpc_4.png "inicio de una VPC")

Ingresamos la configuracion de ip que necesitamos.
```
•	Ip:
	    192.168.11.10
•	Mascara de Sub Red:
    		255.255.255.0
•	Getawey:
    		192.168.11.1
•	Comando completo, a ingresar
    		ip 192.168.11.10 255.255.255.0 192.168.11.1

```
![ConfiguracionVPN](/practica1/recursos/vpc_5.png "configuracion VPC")

Al presionar enter, retorna el siguiente mensaje, el cual indica que la ip ha sido asignada correctamente
![ConfiguracionVPN](/practica1/recursos/vpc_6.png "configuracion VPC")

<div id='id2'/>


## 2. Configuración de las Nubes  [ ⇧](#content)

Luego de estar configuradas las ***VPC*** se configuran las nubes a ;as cual se van a ingresar 

### Para poder crear una nube,  se selecciona en el mennu un cloud 
![ConfiguracionVPN](/practica1/recursos/vpc_1.png "Seleccionar Cloud")

### Se selecciona la congfigurscion en la nube, parfa poder aplicar la configuracion
![ConfiguracionVPN](/practica1/recursos/cloud_1.png "configuracion Cloud")

se selecciona UDP tunnels y se asigna el numero del puerto que esta a la escucha con ***local port*** y en ***remote port*** se asigna el numero de puerto al que se va a hacer la coneccion

![ConfiguracionVPN](/practica1/recursos/cloud_2.png "configuracion Cloud")


<div id='id3'/>

## 3. Pings entre los hosts  [ ⇧](#content)
luego que esten configuradas las nubes con sus respectivos puertos se procede a hacer los pings entre todos los integrantes
### Cliente 1
```sh
IP: 10.8.0.20
```
![ConfiguracionVPN](/practica1/recursos/Jose_pin.jpeg "configuracion VPC")

### Cliente 2
```sh
IP: 10.8.0.20
```
![ConfiguracionVPN](/practica1/recursos/luis_pin.jpeg "configuracion VPC")

### Cliente 3
```sh
IP: 10.8.0.30
```

![ConfiguracionVPN](/practica1/recursos/eric_pin.jpeg "configuracion VPC")

### Cliente 4
```sh
IP: 10.8.0.40
```
![ConfiguracionVPN](/practica1/recursos/iovana_ping.jpeg "configuracion VPC")



