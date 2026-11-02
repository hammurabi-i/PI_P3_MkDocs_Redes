# Diagnostico de red

Cuando una conexion falla, conviene comprobar los elementos uno por uno en lugar de cambiar toda la configuracion a la vez.

## 1. Comprobar la configuracion IP

En Windows:

```powershell
ipconfig /all
```

En Linux:

```bash
ip addr
ip route
```

Comprueba que el equipo tenga una direccion IP, una mascara y una puerta de enlace correctas.

## 2. Probar la comunicacion con ping

El comando `ping` envia solicitudes ICMP para comprobar si otro dispositivo responde.

```bash
ping 192.168.1.1
```

Si recibes respuestas, existe comunicacion IP con ese destino. Si no recibes respuesta, puede haber un problema de conexion, configuracion o filtrado ICMP.

## 3. Comprobar la ruta

En Windows:

```powershell
tracert 8.8.8.8
```

En Linux:

```bash
traceroute 8.8.8.8
```

Estos comandos muestran los saltos que siguen los paquetes hacia el destino.

## Problemas frecuentes

| Problema | Posible causa |
|---|---|
| No hay direccion IP | DHCP no responde o adaptador desconectado |
| No se alcanza el router | Cable, Wi-Fi o configuracion incorrecta |
| Se alcanza el router pero no Internet | Problema del router o del proveedor |
| Solo falla un nombre web | Problema de DNS |

!!! danger "Importante"
    Que `ping` no reciba respuesta no demuestra por si solo que el dispositivo este apagado. Algunos equipos o cortafuegos bloquean ICMP.

!!! success "Orden recomendado"
    1. Revisar la conexion fisica o Wi-Fi.
    2. Revisar la configuracion IP.
    3. Hacer ping a la puerta de enlace.
    4. Probar una IP externa.
    5. Comprobar la resolucion DNS.

## Fuentes

- [Documentacion de MkDocs](https://www.mkdocs.org/)
- [Documentacion de Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [Guia de comandos de red de Microsoft](https://learn.microsoft.com/es-es/windows-server/administration/windows-commands/windows-commands)
