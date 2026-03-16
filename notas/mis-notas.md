# Lab 2

## Equipo
- c2960 Cisco Switch
- 4321 Cisco Router

## Switch
- Password enable: admin
- Password enable secret: secret
- Password line console 0: console0
- Password line vty 0 15: vty015

## Procedimiento

### Initial configuration
´´´
SWITCH-A> ena
SWITCH-A# configure terminal
SWITCH-A( config)# hostname SW-A # Change device name
SW-A( config)# enable password admin # Change admin password
SW-A( config)# banner motd $
Este es el el switch A, por favor no romper.
$
SW-A( config)# enable secret secret # Create secret
SW-A( config)# line console 0
SW-A(config-line)# password console0
SW-A(config-line)# exit
SW-A( config)# line vty 0 15
SW-A(config-line)# password vty015
SW-A(config-line)# exit
SW-A( config)# exit
SWITCH-A#
´´´
### IP configuration
´´´
SWITCH-A> ena
SWITCH-A# configure terminal
SWITCH-A( config)# interface vlan 1
SWITCH-A(config-if)# no shutdown
SWITCH-A(config-if)# ip address 10.0.0.4 255.0.0.0
SWITCH-A(config-if)# exit
SWITCH-A( config)# exit
´´´

Finalmente 

´´´
SWITCH-A# copy running-config startup-config
´´´


