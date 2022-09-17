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
<br>

# <center>[REDES1] PROYECTO1 </center>

## <center> DATOS DE LOS ESTUDIANTES </center>
| Nombre                               | Carnet     | Cliente* | 
| ------------------------------------ | ---------  | -------- |
| José Ignacio Martinez Hernandez      |  201408507 |  1       |
| Luis Roberto Boror Yoc               |  201403517 |  2       |
| Erick Javier Bernal Orellana         |  201480017 |  3       |
| Claudia Iovana Miranda Alvarez       |  201700387 |  4       |
---
<br>

## <center> REQUERIMIENTOS DEL SISTEMA </center>
#### SISTEMA OPERATIVO COMPATIBLE:
* Windows 
    * 10,11
* GNU/LINUX
    * Ubuntu 22.04
#### MEMORIA RAM:
* Minimo 12GB de RAM
#### SOFTWARE UTILIZADO:
* EMULACION DE REDES
    * [GNS3](https://www.gns3.com/software/download)
* RED PRIVADA VIRTUAL [VPN]
    * [OpenVPN](https://openvpn.net/)
* VIRTUALIZACIÓN
    * [VirtualBox](https://www.virtualbox.org/)
#### IMAGENES UTILIZADAS:
* [Ethernet o Switch de Capa 3](https://drive.google.com/file/d/10810USuKu7M6s-_u6cIxek-6czPIt7XH/view)
------
<br>

## <center> OBJETIVOS DEL PROYECTO</center>
* Implementar y desarrollar una topología de red que utiliza protocolos de capa1 y capa2 del modelo OSI.
* Practicar la creación de VLAN.
* Determinar cuando utilizar un puerto de modo acceso y modo troncal.
* Configurar y administrar los protocolos VTP y STP.

## <center> DESCRIPCIÓN DEL PROYECTO </center>
<p style='text-align: justify;'>Se debe configurar y administrar el cableado estructurado para una empresa de venta, se les proporciona el diseño de la topología de red que será utilizado como infraestructura de red para dicha compañía, pero deberán de configurarla para proveer comunicación de acuerdo con las necesidades que se indican. 
La compañía cuenta con 4 departamentos: recursos humanos, informática, contabilidad y ventas. Se debe proveer comunicación entre los usuarios del mismo departamento y con su servidor web si tuvieran uno, por ejemplo, los usuarios del departamento de ventas no se podrán comunicar con ningún otro departamento solamente con host de su mismo departamento. 
</p>

## <center> RED VIRTUALIZADA </center>
<p style='text-align: justify;'>La topologia a configurar de la empresa es la siguiente:
</p>

![topologiaCompleta](/proyecto1/documentacion/imagenes/topologia.png)

En la siguiente tabla se puede observar la distribución de direcciones IP correspondientes a cada departamento de la empresa.

<center>
<table border="1" cellpadding="0" cellspacing="0"  width="80%">
<tr>
<td ><p style="color:#FFF">VLAN</p></td>
<td ><p style="color:#FFF">#VLAN</p></td>
<td ><p style="color:#FFF">DIRECCION IP</p></td>
<td><p style="color:#FFF">GATEWAY</p></td>
</tr>
<tr>
<td bgcolor="green"><p style="color:#FFF">RRHH</p>
</td>
<td bgcolor="green"><p style="color:#FFF">10</p></td>
<td bgcolor="green"><p style="color:#FFF">192.168.11.0/24</p></td>
<td bgcolor="green"><p style="color:#FFF">192.168.11.1</p></td>
</tr>
<tr>
<td bgcolor="yellow"><p style="color:#000">INFORMATICA</p></td>
<td bgcolor="yellow"><p style="color:#000">20</p></td>
<td bgcolor="yellow"><p style="color:#000">192.168.12.0/24</p></td>
<td bgcolor="yellow"><p style="color:#000">192.168.12.1</p></td>
</tr>
<tr>
<td bgcolor="red"><p style="color:#FFF">CONTABILIDAD</p></td>
<td bgcolor="red"><p style="color:#FFF">30</p></td>
<td bgcolor="red"><p style="color:#FFF">192.168.13.0/24</p></td>
<td bgcolor="red"><p style="color:#FFF">192.168.13.1</p></td>
</tr>
<tr>
<td bgcolor="blue"><p style="color:#FFF">VENTAS</p></td>
<td bgcolor="blue"><p style="color:#FFF">40</p></td>
<td bgcolor="blue"><p style="color:#FFF">192.168.14.0/24</p></td>
<td bgcolor="blue"><p style="color:#FFF">192.168.14.1</p></td>
</tr>
</table>
</center>

CONFIGURACION DE CADA TOPOLOGIA
* [Topologia1](/proyecto1/documentacion/topo1.md)
* [Topologia2](/proyecto1/documentacion/topo2.md)
* [Topologia3](/proyecto1/documentacion/topo3.md)