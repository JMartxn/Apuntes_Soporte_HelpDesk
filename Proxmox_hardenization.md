
### **Requisitos Previos**

* **Hardware:** Confirma que el servidor cumpla con los requisitos mínimos de Proxmox VE:  
  * Procesador con soporte para virtualización (Intel VT-x/AMD-V).  
  * Mínimo 8 GB de RAM (recomendado: 16 GB o más).  
  * Almacenamiento rápido (NVMe/SSD preferido para rendimiento de máquinas virtuales).  
* **Red:** Asegúrate de tener al menos dos interfaces de red (una para la gestión y otra para las máquinas virtuales).  
* **Licencia y Soporte:** Considera adquirir una suscripción Proxmox para acceso completo a los repositorios empresariales.

### **Configuración Básica Post-Instalación**

**Actualiza el sistema:**

```bash
apt update && apt full-upgrade
```

**Configura los repositorios empresariales:**

Elimina el repositorio de pruebas y usa el repositorio "enterprise" para mayor estabilidad.

### **Hardenización**

| **A. Sistema Operativo**  | **B. Red** | **C. Cifrado** | **D. Seguridad de VM** |
|--------------------------|------------|----------------|-----------------------|
| - Actualiza Proxmox y el kernel regularmente. | - Segrega la red: Usa VLANs para separar el tráfico de gestión y las máquinas virtuales. | - Habilita HTTPS con certificados válidos: Usa Let's Encrypt o un certificado de tu CA empresarial. | - Limita los recursos: Usa cgroups para limitar CPU y RAM de cada VM. |
| - Habilita actualizaciones automáticas críticas usando `unattended-upgrades`. | - Configura un bridge seguro (`vmbrX`) solo para las máquinas virtuales. | - Cifra las comunicaciones: Asegúrate de que todas las conexiones usan TLS 1.2 o superior. | - Habilita Secure Boot y TPM (si es compatible): Esto mejora la seguridad de las máquinas virtuales modernas. |
| - Deshabilita servicios innecesarios. Verifica qué servicios están activos con `systemctl list-units --type=service`. | | | |

### **Configuración Avanzada**

- **Alta disponibilidad (HA):** Si tienes varios nodos Proxmox, configura un clúster para HA.  
- **Usa Ceph para almacenamiento compartido redundante.**  
- **Backups:** Configura copias de seguridad automáticas en un almacenamiento externo (NFS, SMB o ZFS).  
- **Monitoreo:**  
  - Herramientas internas: Usa la interfaz de Proxmox para monitorear recursos.  
  - Herramientas externas: Considera herramientas como Zabbix o Grafana para supervisar el sistema.

### **Hardenización de Proxmox VE**

- **Restringir puertos y servicios:** Limita el acceso solo a los puertos esenciales.  
  - Usa un cortafuegos como `ufw` para restringir el tráfico:
    ```bash
    apt install ufw
    ufw allow 8006/tcp # Interfaz web de Proxmox
    ufw allow 22/tcp # SSH
    ufw enable
    ```

- **Seguridad de SSH:**  
  - Desactiva el acceso SSH para el usuario root y usa autenticación por clave pública:
    ```bash
    nano /etc/ssh/sshd_config # Configura: PermitRootLogin no
    PasswordAuthentication no
    PubkeyAuthentication yes
    systemctl restart sshd
    ```

- **Instalar Fail2Ban:** Configura Fail2Ban para proteger contra intentos de fuerza bruta:
  ```bash
  apt install fail2ban
  ```

- **Desactivar servicios innecesarios:**  
  - Deshabilita servicios como `spiceproxy` si no los necesitas:
    ```bash
    systemctl mask --now spiceproxy
    ```

- **Usar VPN para administración:**  
  - Configura una VPN como OpenVPN para que la administración de Proxmox se haga únicamente dentro de una red segura. Esto implica crear un puente de red dedicado en Proxmox【14】【13】.

- **Revisión de puertos activos:**  
  - Analiza qué puertos están en uso para confirmar que no hay servicios innecesarios activos:
    ```bash
    ss -atlnup
    ```

- **Monitoreo y parches regulares:**  
  - Instala herramientas de monitoreo como `pve-manager` y asegúrate de que los parches se apliquen de forma regular.
