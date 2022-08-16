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
| Erick Javier Bernal Orellana         |  201480017 |  2       |
| Luis Roberto Boror Yoc               |  201403517 |  3       |
|  Claudia Iovana Miranda Alvarez      |  201700387 |  4       |
 

> \* ***Nota:*** El apartado ***Cliente***, en la tabla anterior, identifica a cada miembro del grupo en la sección ***Conexión entre miembros del grupo*** presentada más adelante.

# Tarea No. 3

<div id='content'/>

## Contenido

1. [Configuración de la red privada](#id1)
2. [Conexión entre miembros del grupo](#id2)
3. [Configuración de _openVPN_ ](#id3)
4. [Grupo IAM](#id4)
5. [Máquina Virtual](#id5)

<div id='id1'/>

## 1. Configuración de la red privada  [ ⇧](#content)

Configuración de red ***VPN*** en instancia de máquina virtual.

Comandos utilizados: 

```sh
sudo wget https://git.io/vpn -O openvpn-install.sh

sudo bash openvpn-install.sh
```
- Configuración de ***IP***.

![ConfiguracionVPN](/tarea%203/images/config1.jpg "Configuración IP")

- Configuración de puerto y protocolo.

![ConfiguracionVPN](/tarea%203/images/config2.jpg "Configuración Puerto y Protocolo")

- Configuración de ***DNS***.

![ConfiguracionVPN](/tarea%203/images/config3.jpg "Configuración DNS")

- Generación de archivos ***.ovpn*** para conexión con clientes.

//pendiente
![ConfiguracionVPN]( "Generación de archivos OVPN")

<div id='id2'/>

## 2. Conexión entre miembros del grupo [ ⇧](#content)

Conexión de cada uno de los miembros del equipo con el resto de integrantes. 

### Cliente 1
```sh
IP: 10.8.0.6
```
![InstalacionOpenVPN](/tarea%203/images/Jose.png "Descarga openVPN")

### Cliente 2
```sh
IP: 10.8.0.5
```
![InstalacionOpenVPN](/tarea%203/images/Eric.png "Descarga openVPN")

### Cliente 3
```sh
IP: 10.8.0.4
```

![InstalacionOpenVPN](/tarea%203/images/luis.png "Descarga openVPN")

### Cliente 4
```sh
IP: 10.8.0.3
```
![InstalacionOpenVPN](/tarea%203/images/iova.png "Descarga openVPN")
<div id='id3'/>

## 3. Configuración de _openVPN_  [ ⇧](#content)

- Descarga de software ***openVPN*** desde su sitio oficial.

```sh
https://openvpn.net/vpn-client/
```

![InstalacionOpenVPN](/tarea%203/images/open1.png "Descarga openVPN")

![InstalacionOpenVPN](/tarea%203/images/open2.png "Archivo openVPN")

- Ejecución del asistente de instalación

![InstalacionOpenVPN](/tarea%203/images/open3.png "Asistente")

![InstalacionOpenVPN](/tarea%203/images/open4.png "Asistente")

![InstalacionOpenVPN](/tarea%203/images/open5.png "Asistente")

![InstalacionOpenVPN](/tarea%203/images/open6.png "Asistente")

![InstalacionOpenVPN](/tarea%203/images/open7.png "Asistente")


- Ejecución del software instalado

![InstalacionOpenVPN](/tarea%203/images/open8.png "Ejecución")

- Conexión a servidor por medio de archivo generado

![InstalacionOpenVPN](/tarea%203/images/open9.png "Conexión")

![InstalacionOpenVPN](/tarea%203/images/open11.png "Conexión")

![InstalacionOpenVPN](/tarea%203/images/open10.png "Conexión")

![InstalacionOpenVPN](/tarea%203/images/open12.png "Conexión")

> \* ***Nota:*** El firewall debe estar desactivado para poder llevar a cabo la comunicación.
> 
> ![Firewall](/images/firewall.png "Firewall")

<div id='id4'/>

## 4. Grupo IAM [ ⇧](#content)
Grupo de ***IAM*** con todos los miembros del grupo.

![GrupoIAM](/tarea%203/images/iam.jpg "Grupo IAM")

<div id='id5'/>

## 5. Máquina virtual [ ⇧](#content)

Creación de instancia de máquina virtual en ***Google Cloud Platform***

![Virtual](/tarea%203/images/mv1.png "Maquina Virtual")

![Virtual](/tarea%203/images/mv2.png "Maquina Virtual")

![Virtual](/tarea%203/images/mv3.png "Maquina Virtual")

![Virtual](/tarea%203/images/instanciaVM.jpg "Maquina Virtual")

Resumen de características:
|Característica|Valor|
|--|--|
|**Plataforma**| <img src="https://cloud.google.com/_static/cloud/images/social-icon-google-cloud-1200-630.png?hl=es-es" alt="drawing" width="150"><br>Google Cloud Platform |
|**Tipo de instancia**|e2-small|
|**Sistema operativo**|<img src="https://anthoncode.com/wp-content/uploads/2019/01/ubuntu-logo-png.png" alt="drawing" width="135"><br>Ubuntu|
|**Versión**| 18.04 LTS|
|**Espacio en disco**| 10 GB|
|**Memoria RAM**| 2 GB|

> Adicionalmente se crearon dos reglas de ***firewall***, una de entrada y una de salida como se observa a continuación.
> 
> **Regla de entrada:**
> ![FirewallRules](/tarea%203/images/firewallvmin.png "Regla de Firewall - Entrada")
> **Regla de salida:**
> ![FirewallRules](/tarea%203/images/firewallvmout.png "Regla de Firewall - Salida")
