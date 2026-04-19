<!--
Source: privacy/my-setup.md
Last translated: 2026-04
-->

# 🧪 Configuración de Privacidad RebelRx

Este es mi stack real enfocado en privacidad, diseñado para **control, rendimiento y usabilidad**.

Uso esta configuración a diario y actualizaré continuamente estas secciones a medida que aparezcan servicios mejores.

---

## 🧭 Filosofía

Esta configuración está construida alrededor de:

- **Propiedad** → Tus datos permanecen bajo tu control  
- **Practicidad** → Las herramientas deben funcionar en el día a día  
- **Escalabilidad** → Puede crecer con tus necesidades  
- **Seguridad** → Sin exposición innecesaria  

> 💡 Esta no es una configuración de “máxima privacidad”. Es un **sistema equilibrado y usable**.

---

## 🖥️ Resumen de Hardware

Mi configuración se ejecuta sobre una mezcla de **infraestructura autoalojada, dispositivos dedicados y equipos personales**, cada uno con un rol específico.

---

## 🧱 Infraestructura Principal

### Minisforum MS-A2 (Servidor Principal)

- **SO:** Devuan (bare metal)
- **Rol:** Host principal de Docker

> 💡 Esta es la columna vertebral de todo mi sistema

👉 Consulta la línea Minisforum Work Station Mini: <https://www.minisforum.com/collections/station-mini-series>

---

### QNAP TS-h1277AXU-RP (NAS)

- **Rol:** Almacenamiento masivo + backups
- Almacena:
  - Librerías multimedia  
  - Datos de Nextcloud  
  - Copias de seguridad  
  - Archivos (ROMs, documentos, etc.)  

> 💡 Separar cómputo (servidor) de almacenamiento (NAS) mejora la flexibilidad y resiliencia  

👉 Consulta las soluciones NAS de QNAP: <https://www.qnap.com/en-us/product>

---

## 💻 Sistemas Personales

### PC Ryzen 9 Personalizado (Windows 11)

- **Rol:** Gaming + aplicaciones exclusivas de Windows  
- Usado para:
  - Cargas de alto rendimiento  
  - Compatibilidad con software no disponible en Linux  

👉 Consulta Micro Center para ubicaciones cercanas: <https://www.microcenter.com/>

---

### Framework Desktop (Artix Linux)

- **Rol:** Estación de trabajo secundaria  
- Usado para:
  - Productividad general  
  - Flujos de trabajo centrados en Linux  

👉 Consulta Framework Desktop: <https://frame.work/marketplace/desktops>

---

### Laptop Framework 13 (Artix Linux)

- **Rol:** Equipo de viaje + desarrollo  
- Usado para:
  - Acceso remoto (vía Tailscale)  
  - Gestión de la infraestructura del hogar  
  - Productividad ligera  

👉 Consulta laptops Framework: <https://frame.work/marketplace/laptops>

---

## 🎮 Gaming y Emulación

### Raspberry Pi 5 (8GB)

- **SO:** Batocera  
- **Adicional:** MiSTer FPGA  
- **Rol:** Gaming retro / emulación  

👉 Consulta Vilros para Raspberry Pi: <https://vilros.com/>

---

## 🏠 Dispositivos Dedicados

### Beelink Mini S13

- **Rol:** Automatización del hogar  
- **SO:** Home Assistant OS  

👉 Consulta Beelink: <https://www.bee-link.com/collections/product>

---

### Umbrel Home

- **Rol:** Nodo de Bitcoin  
- Ejecuta:
  - Nodo completo BTC  
  - Lightning  

👉 Consulta Umbrel: <https://umbrel.com/>

---

### Intel NUC 13

- **Rol:** Servidor de audio  
- **SO:** Roon ROCK  

👉 Consulta B&H: <https://www.bhphotovideo.com/>

---

## 🧠 Filosofía de Diseño

Cada dispositivo tiene una **responsabilidad clara y única**:

- Servidor → Cómputo (Docker)  
- NAS → Almacenamiento  
- Clientes → Interacción  
- Dispositivos → Tareas específicas  

> 💡 Esta separación hace el sistema:
>
> - Más fácil de mantener  
> - Más resiliente  
> - Más escalable  

---

## ✅ Por Qué Esta Configuración Funciona

- Sin un único punto de fallo  
- Separación clara de responsabilidades  
- Rendimiento optimizado por dispositivo  
- Flexibilidad para actualizar componentes  

---

## 🚀 Reflexión Final sobre Hardware

No necesitas todo este hardware para empezar.

Esta configuración evolucionó con el tiempo—  
empieza pequeño y escala según tus necesidades.

---

## 🧱 Arquitectura Principal

- **Despliegue basado en Docker**  
- **Almacenamiento respaldado por NAS**  
- **Proxy inverso (Nginx Proxy Manager)**  
- **Acceso privado vía Tailscale (sin abrir puertos)**  

---

## ☁️ Datos y Productividad

### Nextcloud AIO

- Archivos  
- Calendario (CalDAV)  
- Contactos (CardDAV)  
- Almacenamiento en NAS  

### Almacenamiento en la Nube (Alojado)

- pCloud.com  

---

## 📧 Correo

- Proton Mail  

---

## 📸 Fotos

### Immich

- Reemplazo de Google Photos  
- Interfaz moderna y rápida  
- Totalmente autoalojado  

---

## 📝 Oficina

### ONLYOFFICE

- Reemplazo de Microsoft Office 365  
- Suite completa (documentos, hojas de cálculo, presentaciones, PDF y formularios)  
- Gratis y de código abierto  

---

## 📄 PDFs y Documentos

- Sumatra PDF (lector ligero)  
- BentoPDF (herramientas PDF)  
- Paperless-ngx (archivo documental)  

---

## 📝 Notas y Conocimiento

### Joplin

- Basado en Markdown  
- Multiplataforma  
- Sincronización con Nextcloud  

### Paperless-ngx

- Sistema de gestión documental  
- OCR + etiquetas  
- Reemplaza papel físico  

---

## 🔐 Seguridad e Identidad

### Gestor de Contraseñas

- Proton Pass (opción alojada)

### 2FA

- Activado en todos los servicios  
- Passkeys cuando estén disponibles  

---

## 🌍 Capa de Red y Privacidad

### Bloqueo DNS

- AdGuard Home  
- Bloqueo de anuncios y rastreo a nivel de red  

### VPN

- Mullvad (VPN centrada en privacidad)  

### Acceso Privado

- Tailscale  
- Acceso remoto seguro  
- Sin puertos expuestos  

---

## 🌐 Navegador

- Brave  
  - Bloqueo integrado de anuncios/rastreadores  
  - Extensiones mínimas  

---

## 🎥 Medios y Entretenimiento

### Jellyfin

- Streaming autoalojado  
- Reemplazo de Netflix / HBO  

### Stack Arr

- Sonarr  
- Radarr  
- Prowlarr  
- Gestión automatizada de medios  

---

## 📚 Libros y Audio

### Calibre-Web / Kavita

- Librerías de ebooks  

### Audiobookshelf

- Audiolibros y podcasts  
- Totalmente autoalojado  

---

## 💰 Finanzas

### Actual Budget

- Presupuesto autoalojado  
- Alternativa privada a Mint/YNAB  

---

## 🧰 Desarrollo e Infraestructura

### Git

- Forgejo (autoalojado)

### Editor

- VSCodium (sin telemetría)

---

## 🌐 Herramientas de Red

- LibreSpeed  
- Speedtest-tracker  

Pruebas de red autoalojadas sin seguimiento.

---

## 🔁 Qué Reemplaza Esta Configuración

| Big Tech | Reemplazo |
|---------|-----------|
| Google Drive | Nextcloud |
| Google Photos | Immich |
| Google Calendar | Nextcloud |
| Google Contacts | Nextcloud |
| Gmail | Proton Mail / Tuta |
| Chrome Passwords | Vaultwarden / Proton Pass |
| Chrome | Brave |
| Google Docs (parcial) | Nextcloud + Joplin |
| Netflix / HBO | Jellyfin + stack Arr |
| Kindle / Audible | Calibre-Web / Audiobookshelf |
| Adobe Acrobat | Sumatra PDF / BentoPDF |
| Mint / YNAB | Actual Budget |
| GitHub | Forgejo |
| DNS del ISP | AdGuard Home / Pi-hole |
| Speedtest.net | LibreSpeed / Speedtest-tracker |

---

## 🧠 Principios de Diseño

### 1. Local-First Siempre que Sea Posible

Los datos viven:

- En tu servidor  
- En tu NAS  

---

### 2. Autoalojar Cuando Aporta Valor

No todo necesita ser autoalojado.

Enfoque equilibrado:

- Autoalojado → datos críticos (archivos, fotos, contraseñas)  
- Alojado → conveniencia (correo, si se prefiere)  

---

### 3. Seguridad por Defecto

- Sin puertos expuestos  
- Acceso solo vía Tailscale  
- Proxy inverso para enrutamiento interno  

---

### 4. Mantenibilidad

- Servicios basados en Docker  
- Estructura clara de directorios  
- Configuraciones versionadas (Forgejo)  

---

## ⚖️ Por Qué Funciona Esta Configuración

- Alto control de datos  
- Coste bajo continuo  
- Arquitectura escalable  
- Acceso remoto seguro  
- Funciona en todos los dispositivos  

---

## 🚀 Reflexión Final sobre Infraestructura

No es la única forma de hacerlo ni es perfecta.

Pero es una **configuración real y probada** que equilibra:

- Privacidad  
- Usabilidad  
- Fiabilidad  

> 🧠 El objetivo no es la perfección; es **control sin fricción**.
