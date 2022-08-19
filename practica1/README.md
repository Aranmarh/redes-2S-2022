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
![ConfiguracionVPN](practica1/recursos/vpc_1.png "Seleccionar VPC")

### cuando se cra una VPC se muestra el siguiente icono
![ConfiguracionVPN](/recursos/vpc_2.png "Instancia de VPC")

### luego de que la VPC este creada dar click derecho sobre la VPCS creada y presionar “Start”, esto iniciara la máquina 		virtual
![ConfiguracionVPN](/recursos/vpc_3.png "inicio de una VPC")

### luego de iniciar la máquina virtual, tendremos que asignar una ip valida, para ellos 		ejecutamos la consola, dando click derecho sobre la VPCS y seleccionando Console
![ConfiguracionVPN](/recursos/vpc_4.png "inicio de una VPC")

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
![ConfiguracionVPN](/recursos/vpc_5.png "configuracion VPC")

Al presionar enter, retorna el siguiente mensaje, el cual indica que la ip ha sido asignada correctamente
![ConfiguracionVPN](/recursos/vpc_6.png "configuracion VPC")

<div id='id2'/>


## 2. Configuración de las Nubes  [ ⇧](#content)

Luego de estar configuradas las ***VPC*** se configuran las nubes a ;as cual se van a ingresar 

### Para poder crear una nube,  se selecciona en el mennu un cloud 
![ConfiguracionVPN](/recursos/vpc_1.png "Seleccionar VPC")


![InstalacionOpenVPN](/images/open1.png "Descarga openVPN")

![InstalacionOpenVPN](/images/open2.png "Archivo openVPN")

- Ejecución del asistente de instalación

![InstalacionOpenVPN](/images/open3.png "Asistente")

![InstalacionOpenVPN](/images/open4.png "Asistente")

![InstalacionOpenVPN](/images/open5.png "Asistente")

![InstalacionOpenVPN](/images/open6.png "Asistente")

![InstalacionOpenVPN](/images/open7.png "Asistente")


- Ejecución del software instalado

![InstalacionOpenVPN](/images/open8.png "Ejecución")

- Conexión a servidor por medio de archivo generado

![InstalacionOpenVPN](/images/open9.png "Conexión")

![InstalacionOpenVPN](/images/open11.png "Conexión")

![InstalacionOpenVPN](/images/open10.png "Conexión")

![InstalacionOpenVPN](/images/open12.png "Conexión")

> \* ***Nota:*** El VPC y el VPN deben estar encendidos para la comunicación.


<div id='id3'/>

## 3. Pings entre los hosts  [ ⇧](#content)
luego que esten configuradas las nubes con sus respectivos puertos se procede a hacer los pings entre todos los integrantes
### Cliente 1
```sh
IP: 10.8.0.20
```
![ConfiguracionVPN](/recursos/Jose_pin.jpeg "configuracion VPC")

### Cliente 2
```sh
IP: 10.8.0.20
```
![ConfiguracionVPN](/recursos/luis_pin.jpeg "configuracion VPC")

### Cliente 3
```sh
IP: 10.8.0.30
```

![ConfiguracionVPN](/recursos/eric_pin.jpeg "configuracion VPC")

### Cliente 4
```sh
IP: 10.8.0.40
```
![ConfiguracionVPN](/recursos/iovana_ping.jpeg "configuracion VPC")



