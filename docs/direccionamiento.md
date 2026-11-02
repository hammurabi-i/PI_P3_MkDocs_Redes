# Direccionamiento IP

## Que es una direccion IP

Una direccion IP identifica de forma logica una interfaz dentro de una red que utiliza el protocolo IP. En IPv4 esta formada por 32 bits, que normalmente se escriben como cuatro numeros separados por puntos.

Ejemplo: `192.168.1.25`

## Direccion, mascara y puerta de enlace

- **Direccion IP:** identifica al dispositivo dentro de la red.
- **Mascara de subred:** permite distinguir la parte de red y la parte de host.
- **Puerta de enlace:** direccion del router al que se envian los paquetes destinados a otras redes.

!!! info "Ejemplo de configuracion"
    - IP: `192.168.1.25`
    - Mascara: `255.255.255.0`
    - Puerta de enlace: `192.168.1.1`

## Direcciones privadas IPv4

| Rango privado | Uso habitual |
|---|---|
| `10.0.0.0/8` | Redes privadas grandes |
| `172.16.0.0/12` | Redes privadas medianas |
| `192.168.0.0/16` | Redes domesticas y pequenas |

## Comprobar la configuracion

En Windows puedes ejecutar:

```powershell
ipconfig
```

En Linux puedes utilizar:

```bash
ip addr
ip route
```

!!! tip "Consejo"
    Dos dispositivos de una misma subred necesitan direcciones compatibles y no duplicadas para comunicarse directamente.

## IPv4 e IPv6

IPv6 se creo para ampliar enormemente el espacio de direcciones disponible. Utiliza direcciones de 128 bits, representadas en hexadecimal.
