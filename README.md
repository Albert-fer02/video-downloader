# 🎬 Descargador Universal de Videos v3.0 - Arch Linux

## 🚀 **NUEVO EN v3.0 - CARACTERÍSTICAS AVANZADAS**

### ✨ **Novedades Principales:**
- 🖥️ **Interfaz Gráfica Completa** con Zenity
- 📋 **Sistema de Colas de Descarga** con procesamiento concurrente
- 🔔 **Notificaciones de Escritorio** con sonidos
- 💾 **Backup Automático** con encriptación
- 📱 **Integración con Redes Sociales** (Twitter, Telegram, Discord)
- 📊 **Logs y Monitoreo Avanzado**
- 🎨 **Temas Personalizables**
- 🔄 **Actualización Automática**
- 🛡️ **Seguridad Mejorada**

---

## 📋 Descripción
Sistema profesional y completo para descargar videos de múltiples plataformas sin virus ni malware. Ahora con interfaz gráfica, sistema de colas, backup automático y muchas más características avanzadas.

## 🛠️ Instalación Completa

### Instalación Automática (Recomendado)
```bash
# Ejecutar el instalador v3.0
./install-video-downloader-v3.sh
```

### Instalación Manual
```bash
# Instalar dependencias principales
sudo pacman -S yt-dlp ffmpeg python-pip jq zenity libnotify

# Instalar herramientas adicionales
sudo pacman -S xclip curl wget tar gzip openssl

# Instalar navegadores (opcional pero recomendado)
sudo pacman -S firefox chromium

# Configurar PATH
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

---

## 🚀 Guía de Inicio Rápido

### 🖥️ **Modo Gráfico (Recomendado para Principiantes)**
```bash
# Abrir interfaz gráfica principal
video-downloader-gui
```

### ⌨️ **Modo Terminal (Para Usuarios Avanzados)**
```bash
# Descarga directa
download-video "URL"

# Añadir a cola
download-queue-manager add "URL"

# Iniciar procesamiento de cola
download-queue-manager start
```

---

## 🎯 Comandos Principales v3.0

### 🎬 **Comandos de Descarga**
```bash
# Descargador universal
download-video "URL" [opciones]

# Comandos especializados
download-tiktok "URL"
download-youtube "URL" [video|audio|playlist]
download-instagram "URL"

# Opciones avanzadas
download-video "URL" --quality 720p --audio --info
```

### 🖥️ **Interfaz Gráfica**
```bash
# Ventana principal
video-downloader-gui

# Acceso directo (crear en el escritorio)
echo '[Desktop Entry]
Name=Video Downloader
Exec=video-downloader-gui
Icon=download
Type=Application
Categories=AudioVideo;' > ~/Desktop/video-downloader.desktop
```

### 📋 **Gestión de Colas**
```bash
# Añadir video a la cola
download-queue-manager add "URL" [calidad] [directorio]

# Gestionar cola
download-queue-manager start     # Iniciar procesamiento
download-queue-manager stop      # Detener procesamiento
download-queue-manager status    # Ver estado
download-queue-manager clean     # Limpiar trabajos antiguos
```

### 💾 **Sistema de Backup**
```bash
# Crear backup manual
video-downloader-backup create manual

# Restaurar configuración
video-downloader-backup restore archivo_backup.tar.gz

# Gestión completa
video-downloader-backup interactive

# Verificar integridad
video-downloader-backup verify
```

### 🔧 **Mantenimiento**
```bash
# Actualizar sistema completo
video-downloader-update

# Limpiar archivos temporales
find ~/.cache/video-downloader -type f -delete

# Ver estadísticas
video-downloader-gui  # → Estadísticas
```

---

## 🌐 Plataformas Soportadas v3.0

| Plataforma | URL de Ejemplo | Estado | Características |
|------------|----------------|--------|-----------------|
| **TikTok** | `tiktok.com/@user/video/ID` | ✅ Completo | Metadatos, miniaturas |
| **YouTube** | `youtube.com/watch?v=ID` | ✅ Completo | Videos, audio, playlists, subtítulos |
| **Instagram** | `instagram.com/p/ID/` | ✅ Completo | Posts, reels, stories |
| **Twitter/X** | `twitter.com/user/status/ID` | ✅ Completo | Videos, GIFs |
| **Facebook** | `facebook.com/watch/?v=ID` | ⚠️ Limitado | Requiere cookies |
| **Reddit** | `reddit.com/r/sub/comments/ID` | ✅ Completo | Videos, GIFs |
| **Vimeo** | `vimeo.com/ID` | ✅ Completo | HD, metadatos |
| **Dailymotion** | `dailymotion.com/video/ID` | ✅ Completo | Múltiples calidades |
| **Twitch** | `twitch.tv/videos/ID` | ✅ Completo | VODs, clips |
| **Más...** | | ✅ | Soporte para +1000 sitios |

---

## 📁 Estructura del Sistema v3.0

```
~/
├── .local/bin/                     # Ejecutables
│   ├── download-video              # → Descargador universal
│   ├── video-downloader-gui        # → Interfaz gráfica
│   ├── download-queue-manager      # → Gestor de colas
│   ├── video-downloader-backup     # → Sistema de backup
│   ├── download-tiktok             # → Especializado TikTok
│   ├── download-youtube            # → Especializado YouTube
│   ├── download-instagram          # → Especializado Instagram
│   └── video-downloader-update     # → Actualizador
│
├── .config/video-downloader/       # Configuración principal
│   ├── config.conf                 # → Configuración general
│   ├── social.conf                 # → Redes sociales
│   ├── backups/                    # → Backups automáticos
│   ├── queue/                      # → Cola de descargas
│   ├── logs/                       # → Registros del sistema
│   └── themes/                     # → Temas personalizados
│
├── Descargas/Videos/               # Directorio de descargas
│   ├── TikTok/                     # → Videos de TikTok
│   ├── YouTube/                    # → Videos de YouTube
│   │   ├── Audio/                  # → Solo audio
│   │   └── Playlists/              # → Listas de reproducción
│   ├── Instagram/                  # → Contenido de Instagram
│   ├── Twitter/                    # → Videos de Twitter/X
│   ├── Facebook/                   # → Videos de Facebook
│   ├── Otros/                      # → Otras plataformas
│   └── README-DESCARGADOR-v3.md    # → Esta documentación
│
└── .cache/video-downloader/        # Cache temporal
    ├── downloads/                  # → Descargas en progreso
    └── metadata/                   # → Metadatos temporales
```

---

## 🎨 Interfaz Gráfica - Guía Completa

### 🏠 **Ventana Principal**
La interfaz gráfica ofrece acceso completo a todas las funciones:

1. **🎥 Descargar Video** - Descarga individual con opciones
2. **📝 Descarga por Lotes** - Múltiples URLs a la vez
3. **📋 Administrar Cola** - Gestión de descargas en cola
4. **⚙️ Configuración** - Ajustes del sistema
5. **📊 Estadísticas** - Métricas y reportes
6. **📱 Compartir Redes** - Integración social
7. **🔧 Herramientas** - Utilidades avanzadas
8. **ℹ️ Acerca de** - Información del sistema

### 🎯 **Diálogo de Descarga**
- **URL del Video**: Pega aquí tu enlace
- **Calidad**: best, 720p, 480p, 360p, audio
- **Directorio**: Personalizar ubicación
- **Acción**: Descargar, Solo Info, Añadir a Cola

### 📋 **Gestión de Colas**
- **Ver Estado**: Trabajos pendientes/activos
- **Iniciar/Detener**: Control del procesamiento
- **Limpiar**: Eliminar trabajos antiguos
- **Monitoreo**: Progreso en tiempo real

### 📊 **Panel de Estadísticas**
- Contadores por plataforma
- Espacio usado en disco
- Estado de la cola
- Historial de descargas

---

## 📋 Sistema de Colas Avanzado

### 🎯 **Características**
- ⚡ **Procesamiento Concurrente**: Hasta 3 descargas simultáneas
- 🔄 **Reintentos Automáticos**: 5 intentos por defecto
- 📊 **Seguimiento en Tiempo Real**: Estado JSON detallado
- 🔔 **Notificaciones**: Inicio, completado, error
- 📝 **Logs Completos**: Registro de toda la actividad

### 📝 **Estados de Trabajo**
- `pending` - En espera
- `downloading` - Descargando
- `completed` - Completado
- `failed` - Fallido
- `retrying` - Reintentando

### 🎛️ **Uso Avanzado**
```bash
# Añadir con prioridad personalizada
download-queue-manager add "URL" "720p" "~/Videos/Especiales"

# Monitoreo continuo
watch -n 2 "download-queue-manager status"

# Procesamiento en segundo plano
nohup download-queue-manager start > /dev/null 2>&1 &

# Limpiar trabajos de más de 7 días
download-queue-manager clean 7
```

---

## 💾 Sistema de Backup Profesional

### 🔐 **Características de Seguridad**
- 🔒 **Encriptación AES-256**: Backups seguros
- ✅ **Verificación SHA-256**: Integridad garantizada
- 📅 **Programación Automática**: Daily, weekly, monthly
- 🗂️ **Metadatos JSON**: Información detallada
- 🧹 **Limpieza Automática**: Retención configurable

### 🎛️ **Configuración Avanzada**
```bash
# Editar configuración de backup
vim ~/.config/video-downloader/config.conf

# Variables importantes:
BACKUP_ENABLED=true
BACKUP_FREQUENCY="daily"  # daily, weekly, monthly
BACKUP_RETENTION_DAYS=30
ENCRYPT_BACKUPS=true
CHECKSUM_VALIDATION=true
```

### 📅 **Backup Automático**
```bash
# Configurar en crontab (ya incluido en instalador)
0 2 * * * $HOME/.local/bin/video-downloader-backup scheduled

# Verificar configuración
crontab -l | grep video-downloader
```

### 🔧 **Gestión Manual**
```bash
# Crear backup inmediato
video-downloader-backup create "mi_backup_$(date +%Y%m%d)"

# Listar backups con detalles
video-downloader-backup list json | jq .

# Restaurar con confirmación
video-downloader-backup restore backup_manual_20250614.tar.gz

# Verificar todos los backups
video-downloader-backup verify
```

---

## 📱 Integración con Redes Sociales

### 🌐 **Plataformas Soportadas**
- 🐦 **Twitter/X**: Compartir automáticamente
- 📱 **Telegram**: Envío a chats/canales
- 💬 **Discord**: Webhooks y mensajes
- 📋 **Portapapeles**: Copia automática

### ⚙️ **Configuración**
```bash
# Editar configuración social
vim ~/.config/video-downloader/social.conf

# Variables importantes:
TWITTER_ENABLED=true
TELEGRAM_ENABLED=true
DISCORD_ENABLED=true
AUTO_SHARE=false
DEFAULT_HASHTAGS="#VideoDownloader #YTdlp"
```

### 📱 **Uso desde GUI**
1. Descargar video
2. Ir a "Compartir Redes"
3. Personalizar mensaje
4. Seleccionar plataforma
5. ¡Compartir!

---

## 📊 Monitoreo y Logs

### 📝 **Archivos de Log**
```bash
# Log principal de la cola
tail -f ~/.config/video-downloader/logs/queue.log

# Log de backups
tail -f ~/.config/video-downloader/logs/backup.log

# Logs de descargas individuales
ls ~/.config/video-downloader/logs/downloads/
```

### 📊 **Métricas en Tiempo Real**
```bash
# Ver estadísticas
video-downloader-gui  # → Estadísticas

# Estado de la cola
watch -n 5 "download-queue-manager status"

# Uso de espacio
du -sh ~/Descargas/Videos/*
```

### 🔍 **Debugging**
```bash
# Habilitar modo debug
echo "LOG_LEVEL=DEBUG" >> ~/.config/video-downloader/config.conf

# Ver logs en tiempo real
multitail ~/.config/video-downloader/logs/*.log
```

---

## 🎨 Personalización y Temas

### 🎨 **Configurar Temas**
```bash
# Editar tema por defecto
vim ~/.config/video-downloader/themes/default.conf

# Crear tema personalizado
cp ~/.config/video-downloader/themes/default.conf ~/.config/video-downloader/themes/mi_tema.conf
```

### 🖥️ **Variables de Tema**
```bash
THEME_NAME="Mi Tema"
THEME_PRIMARY_COLOR="#FF5722"    # Color principal
THEME_SECONDARY_COLOR="#4CAF50"  # Color secundario
THEME_SUCCESS_COLOR="#2196F3"    # Color de éxito
THEME_ERROR_COLOR="#F44336"      # Color de error
THEME_BACKGROUND="#FAFAFA"       # Fondo
THEME_FONT="Ubuntu 11"           # Fuente
```

---

## 🔧 Configuración Avanzada

### ⚙️ **Archivo Principal: config.conf**
```bash
# Ubicación
~/.config/video-downloader/config.conf

# Secciones principales:
[BÁSICA]         # Directorios, calidad, etc.
[GUI]            # Interfaz gráfica
[COLA]           # Sistema de colas
[BACKUP]         # Copias de seguridad
[REDES]          # Integración social
[RENDIMIENTO]    # Optimizaciones
[SEGURIDAD]      # Configuración de seguridad
```

### 🎯 **Optimización de Rendimiento**
```bash
# Configuración para máximo rendimiento
MAX_CONCURRENT_DOWNLOADS=5
USE_PARALLEL_DOWNLOADS=true
MAX_DOWNLOAD_SPEED="0"  # Sin límite
RETRY_ATTEMPTS=3
FRAGMENT_RETRIES=5
USE_ARIA2=true  # Si está instalado
```

### 🛡️ **Configuración de Seguridad**
```bash
# Filtros de contenido
BLOCK_NSFW=false
MIN_DURATION="0"
MAX_DURATION="0"
BLOCKED_KEYWORDS=""
ALLOWED_FORMATS="mp4,webm,mkv"

# Autenticación
USE_BROWSER_COOKIES=true
PREFERRED_BROWSER="firefox"
USE_OAUTH=false
```

---

## 📖 Ejemplos Detallados

### 🎵 **Ejemplo 1: TikTok (Tu enlace)**
```bash
# Modo gráfico
video-downloader-gui
# → Descargar Video → Pegar URL → Descargar

# Modo terminal
download-video "https://www.tiktok.com/@silentxploitt/video/7505853157516414213?is_from_webapp=1&sender_device=pc"

# Con opciones específicas
download-tiktok "https://www.tiktok.com/@silentxploitt/video/7505853157516414213" --quality best
```

### 🎬 **Ejemplo 2: YouTube con Opciones**
```bash
# Video en calidad específica
download-video "https://youtu.be/dQw4w9WgXcQ" --quality 720p

# Solo audio MP3
download-video "https://youtu.be/dQw4w9WgXcQ" --audio

# Playlist completa
download-youtube "https://youtube.com/playlist?list=PLxxx" playlist

# Con subtítulos
download-video "https://youtu.be/dQw4w9WgXcQ" --subs
```

### 📱 **Ejemplo 3: Instagram Stories**
```bash
# Post normal
download-instagram "https://www.instagram.com/p/ABC123/"

# Reel
download-instagram "https://www.instagram.com/reel/XYZ789/"

# Desde la GUI con vista previa
video-downloader-gui
# → Descargar Video → URL → Solo Info (para preview)
```

### 📋 **Ejemplo 4: Descarga por Lotes**
```bash
# Preparar lista de URLs
cat > mis_videos.txt << EOF
https://www.tiktok.com/@user1/video/123
https://youtu.be/abc123
https://www.instagram.com/p/def456/
EOF

# Añadir todos a la cola
while read url; do
    download-queue-manager add "$url" "720p"
done < mis_videos.txt

# Iniciar procesamiento
download-queue-manager start

# O usar la GUI:
video-downloader-gui
# → Descarga por Lotes → Pegar URLs → Configurar → Añadir
```

### 🔄 **Ejemplo 5: Automatización Completa**
```bash
#!/bin/bash
# Script de automatización completa

# 1. Actualizar sistema
video-downloader-update

# 2. Limpiar cola antigua
download-queue-manager clean 7

# 3. Añadir videos a la cola
download-queue-manager add "$1" "best"

# 4. Iniciar procesamiento si no está activo
if ! pgrep -f "download-queue-manager start" > /dev/null; then
    nohup download-queue-manager start > /dev/null 2>&1 &
fi

# 5. Crear backup si es necesario
video-downloader-backup scheduled

# 6. Notificar
notify-send "📥 Video Añadido" "Video añadido a la cola de descarga"
```

---

## 🚨 Solución de Problemas v3.0

### ❌ **Errores Comunes y Soluciones**

#### 🔧 **Error: "yt-dlp no está instalado"**
```bash
# Instalar/reinstalar
sudo pacman -S yt-dlp

# Verificar versión
yt-dlp --version

# Actualizar
yt-dlp --update
```

#### 🖥️ **Error: "zenity: command not found"**
```bash
# Instalar Zenity
sudo pacman -S zenity

# Verificar instalación
zenity --version
```

#### 📋 **Error: "No se puede iniciar la cola"**
```bash
# Verificar archivos de bloqueo
rm -f /tmp/download-queue.lock /tmp/download-queue.pid

# Reiniciar cola
download-queue-manager stop
download-queue-manager start
```

#### 💾 **Error: "Backup fallido"**
```bash
# Verificar permisos
chmod 755 ~/.config/video-downloader/backups/

# Espacio en disco
df -h ~/.config/video-downloader/

# Crear manualmente
video-downloader-backup create test
```

#### 🌐 **Error: "Video privado o región bloqueada"**
```bash
# Usar cookies de navegador
download-video "URL" --cookies-from-browser firefox

# Verificar login en navegador
firefox "URL"

# Usar VPN si es necesario
# sudo openvpn mi_config.ovpn
```

#### 🔔 **Error: "Notificaciones no funcionan"**
```bash
# Verificar notify-send
notify-send "Test" "Mensaje de prueba"

# Instalar si no está
sudo pacman -S libnotify

# Verificar servicio de notificaciones
systemctl --user status notification-daemon
```

### 🛠️ **Diagnóstico Avanzado**
```bash
# Verificar configuración completa
video-downloader-gui
# → Herramientas → Ver Logs

# Probar conectividad
curl -I "https://www.youtube.com"

# Verificar dependencias
ldd $(which yt-dlp)

# Modo debug completo
echo "LOG_LEVEL=DEBUG" >> ~/.config/video-downloader/config.conf
download-video "URL" 2>&1 | tee debug.log
```

### 🔧 **Reparación del Sistema**
```bash
# Reinstalación completa
rm -rf ~/.config/video-downloader/
rm -rf ~/.local/bin/download-*
rm -rf ~/.local/bin/video-downloader-*

# Ejecutar instalador nuevamente
./install-video-downloader-v3.sh
```

---

## 🔄 Actualización y Mantenimiento

### 📦 **Actualización Automática**
```bash
# Actualización completa del sistema
video-downloader-update

# Solo yt-dlp
yt-dlp --update

# Verificar actualizaciones
video-downloader-update --check
```

### 🧹 **Mantenimiento Regular**
```bash
# Limpieza semanal recomendada
#!/bin/bash
# ~/.local/bin/mantenimiento-semanal.sh

echo "🧹 Iniciando mantenimiento semanal..."

# 1. Actualizar sistema
video-downloader-update

# 2. Limpiar cache
rm -rf ~/.cache/video-downloader/*

# 3. Limpiar cola antigua
download-queue-manager clean 14

# 4. Verificar backups
video-downloader-backup verify

# 5. Limpiar logs antiguos
find ~/.config/video-downloader/logs/ -name "*.log" -mtime +30 -delete

# 6. Crear backup semanal
video-downloader-backup create "weekly_maintenance"

echo "✅ Mantenimiento completado"
```

### 📊 **Monitoreo de Salud**
```bash
# Script de monitoreo
#!/bin/bash
# ~/.local/bin/health-check.sh

echo "🔍 Verificando salud del sistema..."

# Verificar dependencias críticas
for cmd in yt-dlp ffmpeg jq zenity; do
    if command -v $cmd >/dev/null; then
        echo "✅ $cmd: OK"
    else
        echo "❌ $cmd: FALTANTE"
    fi
done

# Verificar espacio en disco
used=$(df -h ~/Descargas/Videos | tail -1 | awk '{print $5}' | sed 's/%//')
if [ $used -gt 90 ]; then
    echo "⚠️ Espacio en disco: $used% (CRÍTICO)"
else
    echo "✅ Espacio en disco: $used% (OK)"
fi

# Verificar cola
if pgrep -f "download-queue-manager" >/dev/null; then
    echo "✅ Cola de descarga: ACTIVA"
else
    echo "⚠️ Cola de descarga: INACTIVA"
fi

echo "🔍 Verificación completada"
```

---

## ⚖️ Consideraciones Legales y Éticas

### ⚠️ **IMPORTANTE - LEE ANTES DE USAR**

#### 📋 **Términos de Uso**
- ✅ **Uso Personal**: OK para uso personal y educativo
- ❌ **Redistribución**: No redistribuyas contenido con derechos de autor
- ❌ **Uso Comercial**: No uses para fines comerciales sin permiso
- ✅ **Contenido Propio**: OK para descargar tu propio contenido
- ✅ **Contenido Libre**: OK para contenido con licencias libres

#### 🛡️ **Responsabilidad**
- **El usuario es responsable** del cumplimiento de los términos de servicio
- **El desarrollador no se hace responsable** del mal uso del software
- **Respeta los derechos de autor** y la propiedad intelectual
- **Usa con moderación** para no sobrecargar los servidores

#### 📚 **Buenas Prácticas**
1. **Lee los términos** de cada plataforma antes de descargar
2. **Respeta los límites** de velocidad y frecuencia
3. **No descargues contenido protegido** sin autorización
4. **Usa para backup personal** de tu propio contenido
5. **Considera apoyar** a los creadores de contenido

---

## 🆘 Soporte y Comunidad

### 📞 **Obtener Ayuda**

#### 🔍 **Diagnóstico Propio**
1. **Verificar logs**:
   ```bash
   tail -f ~/.config/video-downloader/logs/queue.log
   ```

2. **Ejecutar verificación**:
   ```bash
   video-downloader-gui → Herramientas → Ver Logs
   ```

3. **Probar comando básico**:
   ```bash
   download-video --help
   ```

#### 📝 **Reportar Problemas**
Al reportar problemas, incluye:
- Sistema operativo y versión
- Versión de yt-dlp: `yt-dlp --version`
- URL problemática (si es pública)
- Mensaje de error completo
- Logs relevantes

#### 🌐 **Recursos Adicionales**
- **Documentación yt-dlp**: https://github.com/yt-dlp/yt-dlp
- **Arch Linux Wiki**: https://wiki.archlinux.org/
- **FFmpeg Docs**: https://ffmpeg.org/documentation.html

### 💡 **Contribuir**

#### 🐛 **Reportar Bugs**
- Usar el template de diagnóstico
- Incluir información completa
- Verificar que no sea un problema conocido

#### 🚀 **Sugerir Mejoras**
- Nuevas características
- Optimizaciones de rendimiento
- Mejoras de interfaz
- Soporte para nuevas plataformas

---

## 📚 Apéndices

### 📊 **A. Tabla de Calidades**
| Formato | Resolución | Bitrate Video | Bitrate Audio | Tamaño Aprox |
|---------|------------|---------------|---------------|---------------|
| `best` | Original | Original | Original | Máximo |
| `720p` | 1280x720 | ~2500k | ~128k | Alto |
| `480p` | 854x480 | ~1000k | ~128k | Medio |
| `360p` | 640x360 | ~500k | ~96k | Bajo |
| `audio` | N/A | N/A | ~128k | Mínimo |

### 🔧 **B. Variables de Configuración**
```bash
# Configuración completa disponible
cat ~/.config/video-downloader/config.conf

# Variables más importantes:
DOWNLOAD_DIR                 # Directorio base
DEFAULT_QUALITY              # Calidad por defecto
MAX_CONCURRENT_DOWNLOADS     # Descargas simultáneas
NOTIFICATIONS_ENABLED        # Habilitar notificaciones
BACKUP_ENABLED               # Habilitar backups
SOCIAL_SHARING_ENABLED       # Habilitar compartir
```

### 🎨 **C. Códigos de Color para Temas**
```bash
# Paleta Material Design
Blue:    #2196F3
Red:     #F44336
Green:   #4CAF50
Orange:  #FF9800
Purple:  #9C27B0
Teal:    #009688

# Paleta Oscura
Dark:    #212121
Gray:    #424242
Light:   #757575
White:   #FFFFFF
```

### 📱 **D. Comandos de Terminal Útiles**
```bash
# Ver descargas en tiempo real
watch -n 2 "ls -la ~/Descargas/Videos/*/"

# Monitorear uso de CPU/memoria
htop -p $(pgrep -f yt-dlp)

# Ver progreso de descarga
tail -f ~/.config/video-downloader/logs/queue.log | grep -E "(downloading|completed)"

# Estadísticas rápidas
find ~/Descargas/Videos -name "*.mp4" | wc -l
```

---

## 🏆 Créditos y Agradecimientos

### 👨‍💻 **Desarrollo**
- **Autor Principal**: DreamCoder08
- **Versión**: 3.0
- **Fecha**: 2025-06-14
- **Licencia**: Uso personal y educativo

### 🙏 **Tecnologías Utilizadas**
- **yt-dlp**: Motor principal de descarga
- **FFmpeg**: Procesamiento de video/audio
- **Zenity**: Interfaz gráfica
- **Bash**: Scripting y automatización
- **jq**: Procesamiento JSON
- **OpenSSL**: Encriptación de backups

### 🌟 **Agradecimientos Especiales**
- Comunidad de yt-dlp
- Desarrolladores de FFmpeg
- Comunidad de Arch Linux
- Usuarios beta testers
- Contribuidores de feedback

---

## 🔮 Roadmap Futuro (v4.0)

### 🚀 **Características Planificadas**
- 🌐 **Interfaz Web**: Panel de control via navegador
- 🐳 **Docker Support**: Containerización completa
- 🤖 **IA Integration**: Detección automática de contenido
- 📱 **App Móvil**: Control remoto desde smartphone
- ☁️ **Cloud Sync**: Sincronización con servicios en la nube
- 🎵 **Music Management**: Organización automática de música
- 📺 **Media Server**: Servidor de streaming integrado
- 🔄 **Auto-Updates**: Actualizaciones automáticas sin intervención

### 🎯 **Mejoras Técnicas**
- 🚀 **Performance**: Optimización de velocidad
- 🔒 **Security**: Mejoras de seguridad
- 🎨 **UI/UX**: Interfaz más moderna
- 🌍 **i18n**: Soporte multiidioma
- 📊 **Analytics**: Métricas avanzadas

---

**📞 ¿Necesitas ayuda? ¿Tienes sugerencias?**

> 💡 **TIP**: Para mejores resultados, mantén siempre actualizado yt-dlp ejecutando `video-downloader-update` semanalmente. Las plataformas cambian constantemente y las actualizaciones son críticas para mantener la funcionalidad.

---

**🎉 ¡Disfruta descargando videos de forma segura y profesional con Video Downloader v3.0!**

*Desarrollado con ❤️ por DreamCoder08 para la comunidad de Arch Linux*

