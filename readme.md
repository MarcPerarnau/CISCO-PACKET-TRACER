Añadir un router inalambrico, ordenador portatil, smarphone.
configurar el portatil 

Configurar router: <br>
1- Configurar IP <br>
2- DHCP ON o OFF <br>
3- Wirles->SSID (Poner un nombre) <br>
4- Standad channel 1, 6 o 11 <br>
5- SSID Broadcast Visible o Invisible <br>
6- Wirles->Wirles Security. <br>
8- Security mode WPA2 y configuara contraseña. <br>


Configurar laptop: <br>
1- Cambiar SSID al nombre del SSID del router <br>
2. Poner la autencication en la escogida al router y la contraseña. <br>
3. Esperar hasta que se conecte con el router. <br>

Configurar smarphone:
Seguimos los mismos pasos que con el laptop <br>

Que necesitamos: <br>
- Router <br>
- Switch <br>
- 3 PC <br>
- Access Point <br>
- Portatil <br>
- Tablet <br>
- Smarphone

Connectamos el router con el switch y el switch con el access point, donde se conectaran el portatil, la tablet y el smarphone, <br>
en el switch conectamos los PC.

## Crear Vlan
- Dentro del SWITCH:<br>
```
enable
configure terminal
vlan 10
name "el nombre que quieras"
int range fa0/1-20 
switchport mode acess
switchport access vlan 10
```
```
vlan 20
name 'nombre'
int range fa0/20-24
switchport mode access
switchport access vlan 20
show vlan (muestra las vlna's y sus puertos)
```
```
int fa0/1
switchport mode trunk 
Some basic Git commands are:
```
- Dentro del Router: <br>
```
enable 
conf terminal 
int gig0/0/0.10 
encapsulation dotlq 10 
ip add 192.168.1.1 255.255.255.0 
ip dhcp pool 'nombre vlan' 
network 192.168.1.0 255.255.255.0 
default-router 192.168.1.1 
exit
no sh
```
- Dentro del Access Point:  <br>
- Configurar como el router del principio.
## Verificar :
Para verificar los que hemos hecho con anterioridad tenemos que entrar en un PC y hacer un ping. 
```
ping 192.168.1.56
```
## Resoluciones
En caso de que el access point no de la IP esperada verificad en que puertos estan conectados los puertos y hacer un renew de IP.
