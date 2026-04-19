<!--
Source: homelab/index.md
Last translated: 2026-04
-->

# 🏠 Homelab

Guías para construir un homelab soberano, centrado en la privacidad y completamente bajo tu control.

Esta sección se enfoca en:

- Autoalojar servicios críticos  
- Eliminar dependencias innecesarias de la nube  
- Diseñar sistemas que sean estables, observables y mantenibles  
- Recuperar la propiedad de tus datos e infraestructura  

---

## ⚠️ Principio Fundamental

> Si no controlas tu infraestructura, no controlas tus datos.

---

## 🧭 Qué Encontrarás Aquí

- **Despliegue de Servicios** → Qué autoalojar y cómo ejecutarlo de forma confiable  
- **Redes** → Acceso seguro sin exponer todo tu sistema  
- **Almacenamiento y Copias de Seguridad** → Durabilidad de datos y estrategias de recuperación  
- **Estándares** → Patrones que evitan que tu homelab se convierta en caos  

---

## 🔧 Áreas Clave

### 🧩 Servicios

Aplicaciones que vale la pena autoalojar y cómo desplegarlas correctamente.

Enfoque:

- Medios (Plex, Jellyfin)  
- Almacenamiento de archivos (Nextcloud)  
- Monitoreo (Grafana, Prometheus, Uptime Kuma)  
- Automatización y herramientas  

> No todo debe ser autoalojado — solo lo que puedas mantener de forma realista.

---

### 🌐 Redes

Cómo se conecta todo — de forma segura y predecible.

Incluye:

- Proxies inversos (Nginx Proxy Manager)  
- Acceso privado (Tailscale, VPNs)  
- Diseño de DNS  
- Estrategia de exposición de servicios  

!!! warning
    Abrir puertos sin control es cómo los homelabs se ven comprometidos.

    Esta sección prioriza el **acceso controlado**, no la conveniencia.

---

### 💾 Almacenamiento

Tu capa de datos; donde la mayoría de los homelabs fallan.

Enfoque:

- Integración con NAS  
- Estrategias de montaje (NFS, SMB)  
- Arquitectura de copias de seguridad  
- Organización de medios y archivos  

> Si tu estrategia de respaldo no está probada, no existe.

---

### 📏 Estándares

La diferencia entre un homelab limpio y un desastre imposible de mantener.

Incluye:

- Patrones de Docker Compose  
- Estructuras de carpetas  
- Convenciones de nombres  
- Gestión de variables de entorno  
- Infraestructura versionada con Git  

!!! tip
    La mayoría de los problemas en homelab no son técnicos; son organizativos.

---

## 🧱 Filosofía de Diseño

El homelab RebelRx se construye sobre:

- Infraestructura local-first  
- Dependencias externas mínimas  
- Separación clara de servicios  
- Configuraciones reproducibles  

Evita:

- Sobreingeniería por el simple hecho de añadir complejidad  
- Copiar configuraciones sin entenderlas  
- Sistemas de “configurar y olvidar” que fallan silenciosamente  

---

## 📚 Guías

- [Home Lab + Docker Self-Hosting](docker-home-lab.md)

---

## 🚧 Guías en Desarrollo

- Montaje de particiones NAS  
- Túnel VPN con Tailscale  
- Nginx Proxy Manager  
- Gaming retro autoalojado con RomM  

---

## 🧠 Reflexión Final

Las plataformas en la nube optimizan para la escala.

Tu homelab debería optimizar para:

> Control, confiabilidad y comprensión.
