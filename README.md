
![](https://i.postimg.cc/T2V0gWyb/cisco.png)

### Création 3 pool adresse IP:
> ServerPool - 192.168.1.1/24 (192.168.1.50 -> 192.168.1.100

> Pool2 - 192.168.2.1/24 (192.168.2.50 -> 192.168.2.100)

> Pool3 - 192.168.3.1/24 (192.168.3.50 -> 192.168.3.100)


### Configuration routeur:
`int fa0/0`

`ip address 192.168.1.1 255.255.255.0`

`no shutdown`

`exit `


`int fa1/0`

`ip address 192.168.2.1 255.255.255.0`

`ip helper-add 192.168.1.2`

`no shutdown`

`exit `


`int fa2/0`

`ip address 192.168.3.1 255.255.255.0`

`ip helper-add 192.168.1.2`

`no shutdown`

`exit `


`exit`