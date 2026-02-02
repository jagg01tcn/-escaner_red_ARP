# escaner_red_ARP

**Funcionalidad**  
Escáner ARP que envía solicitudes ARP en broadcast para identificar hosts activos dentro de un rango de red local.

**Problema que resuelve**  
Descubrimiento de dispositivos activos en una red LAN sin depender de ICMP u otros métodos filtrables.

**Escenarios de uso**  
- Enumeración de red interna  
- Fase inicial de pentesting en redes locales  
- Auditorías de inventario de dispositivos  
- Análisis defensivo de segmentación de red  

**Suposiciones importantes**  
- Debe ejecutarse dentro de la misma red local que los objetivos.  
- Requiere privilegios elevados para el envío de paquetes ARP.  
- No es efectivo a través de routers o redes segmentadas.

---

## Ejecución y uso

### Requisitos técnicos

- Python 3.x  
- Sistema operativo con soporte de sockets y paquetes ARP  
- Permisos adecuados (`root` para ARP)  

**Dependencias**
- `termcolor` (scanner TCP)
- `scapy` (scanner ARP)

### Ejecución básica


<img width="1548" height="649" alt="image" src="https://github.com/user-attachments/assets/de3b93b9-a35c-45ff-b1b3-e7835476ad82" />

```bash
sudo python3 escaner_red_ARP.py  -t <objetivo> 
