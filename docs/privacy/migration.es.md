<!--
Source: privacy/migration.md
Last translated: 2026-04
-->

# 🏗️ Guía de Migración

Cómo alejarte de Big Tech **sin romper tu flujo de trabajo**.

---

## ⚠️ Regla de Oro

> NO migres todo de una vez.

Esta es la razón #1 por la que la gente falla.

---

## 🧭 Visión General de la Estrategia de Migración

Seguirás un enfoque por fases:

1. Configuración en paralelo  
2. Migración gradual  
3. Uso dual  
4. Transición completa  
5. Desmantelamiento  

---

## 🪜 Fase 1: Configuración en Paralelo

Configura tus nuevas herramientas **sin eliminar nada**.

### Apps Principales para Instalar Primero

- Navegador → **Brave**
- Gestor de contraseñas → **Bitwarden / Proton Pass**
- Correo → **Proton Mail / Tuta**
- Mensajería → **Signal**

---

### Opcional (Infraestructura Temprana)

Si vas a autoalojar:

- **Nextcloud (o Sync.com si es alojado)**
- **Immich (fotos)**
- **AdGuard Home / Pi-hole**
- **Tailscale**

> 💡 No sobreconstruyas al inicio—haz que las cosas funcionen primero.

---

## 🔄 Fase 2: Migración Gradual

Mueve una categoría a la vez.

---

### 🌐 Navegador

- Instala Brave  
- Añade extensiones (mínimas):  
  - uBlock Origin (opcional—Brave ya bloquea anuncios)  
- Importa marcadores desde Chrome  

---

### 🔐 Contraseñas

- Exporta desde Chrome  
- Importa en:  
  - Bitwarden **o**  
  - Proton Pass  
- Activa 2FA  

> ⚠️ Haz esto temprano—todo depende de ello  

---

### 📧 Correo

- Crea cuenta en Proton Mail o Tuta  
- Configura:  
  - Reenvío desde Gmail → nueva bandeja  
  - Empieza a usar el nuevo correo para inicios de sesión  

> 💡 Opcional: configura un dominio personalizado  

---

### ☁️ Archivos

**Opción A (Autoalojado):**

- Subir datos → Nextcloud  

**Opción B (Alojado):**

- Subir datos → Sync.com  

Empieza con:

- Documentos  
- Archivos personales  
- Datos no críticos  

---

### 📸 Fotos

- Exporta desde Google Photos  
- Sube a Immich  

> ⚠️ Esto puede tomar tiempo—hazlo por lotes  

---

### 📝 Notas

- Exporta Google Keep / Apple Notes  
- Importa en Joplin  

---

### 📆 Calendario y Contactos

- Exporta datos de Google  
- Importa en:  
  - Nextcloud  
  - o Baikal / Radicale  

---

### 🌍 Red

- Despliega AdGuard Home o Pi-hole  
- Actualiza DNS en:  
  - Router (opcional)  
  - Dispositivos  

---

### 🔒 VPN / Acceso

- Instala Mullvad (VPN de privacidad)  
- Configura Tailscale (acceso remoto a tu homelab)  

---

### 📚 Documentos

- Escanea/importa en Paperless-ngx  
- Reemplaza flujos PDF:  
  - Sumatra PDF  
  - BentoPDF  

---

### 🎥 Medios

- Configura Jellyfin  
- (Opcional avanzado):  
  - Despliega stack Arr (Sonarr, Radarr, Prowlarr)  

---

### 📚 Libros y Audio

- Importa ebooks → Calibre-Web / Kavita  
- Importa audiolibros/podcasts → Audiobookshelf  

---

### 💰 Finanzas

- Configura Actual Budget  
- Importa/exporta datos financieros (si aplica)  

---

### 🧰 Desarrollo

- Reemplaza flujos de GitHub con Forgejo (opcional)  
- Cambia a VSCodium  

---

## 🔁 Fase 3: Uso Dual

Ejecuta ambos sistemas simultáneamente.

Valida:

- Fiabilidad de sincronización  
- Acceso móvil  
- Copias de seguridad  
- Rendimiento  

---

## 🔌 Fase 4: Transición Completa

Empieza a cambiar completamente:

- Actualiza correos de inicio de sesión en cuentas  
- Mueve flujos diarios:  
  - Notas → Joplin  
  - Archivos → Nextcloud / Sync.com  
  - Fotos → Immich  
- Reduce dependencia de Google/Apple  

---

## 🧹 Fase 5: Desmantelamiento

Cuando estés seguro:

- Exporta copias finales de servicios antiguos  
- Desactiva cuentas no utilizadas  
- Elimina apps que ya no uses  

> ⚠️ Mantén copias de seguridad antes de eliminar cualquier cosa  

---

## ⚠️ Errores Comunes

- Migrar demasiado rápido  
- Romper flujos familiares/compartidos  
- No tener estrategia de respaldo  
- Sobreingeniería temprana  
- Perseguir “privacidad perfecta” en lugar de sistemas utilizables  

---

## 🔐 Mejores Prácticas de Seguridad

- Usa un gestor de contraseñas (Bitwarden / Proton Pass)  
- Activa 2FA en todas partes  
- Mantén sistemas actualizados  
- Mantén **copias de seguridad externas (offsite)**  
- Prueba restauraciones (no solo backups)  

---

## 🧠 Consejos Pro

### 1. Prioriza las Victorias de Alto Impacto

Empieza con:

- Navegador  
- Gestor de contraseñas  
- Correo  

---

### 2. Separa Alojado vs Autoalojado

| Tipo | Cuándo Usar |
|------|-------------|
| Alojado (Proton, Sync.com) | Configuración más simple y rápida |
| Autoalojado (Nextcloud, Immich) | Máximo control |

---

### 3. Construye por Capas

- Capa 1 → Apps (Brave, Signal, Bitwarden)  
- Capa 2 → Servicios (Correo, Almacenamiento)  
- Capa 3 → Infraestructura (Nextcloud, DNS, VPN)  

---

## 🚀 Reflexión Final

> La migración es un proceso, no un evento.

No necesitas reemplazar todo de la noche a la mañana.

Enfócate en:

- Progreso  
- Estabilidad  
- Control  
