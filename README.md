# 🎬 Video Downloader Universal v3.0

¡Bienvenido al **Video Downloader Universal v3.0**! Esta es una solución completa y robusta para descargar videos y audios de múltiples plataformas, diseñada específicamente para usuarios de Arch Linux. Con una interfaz gráfica intuitiva, sistema de colas, notificaciones y backups automáticos, tendrás el control total sobre tus descargas.

---

## ✨ Características Principales

*   **Interfaz Gráfica (GUI)**: Fácil de usar con Zenity.
*   **Sistema de Colas**: Gestiona múltiples descargas de forma eficiente.
*   **Notificaciones de Escritorio**: Mantente informado sobre el estado de tus descargas.
*   **Backup Automático de Configuración**: Protege tus ajustes y datos.
*   **Integración con Redes Sociales**: Soporte para TikTok, YouTube, Instagram, Twitter/X, Facebook y más.
*   **Logs y Monitoreo Avanzado**: Para un seguimiento detallado.
*   **Actualización Automática**: Mantén el sistema al día con un simple comando.
*   **Encriptación de Backups**: Seguridad adicional para tus datos.
*   **Basado en `yt-dlp`**: Potente y versátil motor de descarga.

---

## 🚀 Instalación (¡Automática!)

La instalación es sencilla y completamente automatizada gracias al script `install.sh`.

1.  **Clonar el Repositorio**:
    ```bash
    git clone https://github.com/DreamCoder08/video-downloader-github.git
    cd video-downloader-github
    ```

2.  **Ejecutar el Instalador**:
    ```bash
    chmod +x install.sh
    ./install.sh
    ```
    El script te guiará a través del proceso, solicitando tu contraseña de `sudo` para instalar las dependencias necesarias y preguntando si deseas instalar navegadores para un soporte completo de cookies.

---

## 💡 Uso

Una vez instalado, puedes interactuar con el descargador de videos de varias maneras:

### Interfaz Gráfica (Recomendado)

Para iniciar la interfaz gráfica, simplemente ejecuta:

```bash
video-downloader-gui
```

### Comandos de Línea (CLI)

*   **Descarga Universal**:
    ```bash
    download-video 'URL_DEL_VIDEO'
    ```
    Ejemplo:
    ```bash
    download-video 'https://www.tiktok.com/@silentxploitt/video/7505853157516414213'
    ```
    Puedes usar opciones como `--audio` para descargar solo el audio o `--quality 720p` para especificar la calidad.

*   **Gestor de Colas**:
    ```bash
    download-queue-manager add 'URL1'
    download-queue-manager add 'URL2'
    download-queue-manager start
    ```

*   **Sistema de Backup**:
    ```bash
    video-downloader-backup interactive
    ```

*   **Actualización del Sistema**:
    ```bash
    video-downloader-update
    ```

### Comandos Especializados por Plataforma

*   **TikTok**: `download-tiktok 'URL'`
*   **YouTube**: `download-youtube 'URL'`
*   **Instagram**: `download-instagram 'URL'`

---

## 📂 Estructura del Proyecto

*   `config/`: Contiene archivos de configuración, temas e iconos.
*   `scripts/`: Contiene todos los scripts ejecutables (`download-video`, `video-downloader-gui`, etc.).
*   `install.sh`: El script de instalación automática.
*   `README.md`: Este archivo.

---

## 🏆 Créditos y Agradecimientos

### 👨‍💻 Desarrollo
- **Autor Principal**: DreamCoder08
- **Versión**: 3.0
- **Fecha**: 2025-07-13 (Actualizado)
- **Licencia**: Uso personal y educativo

### 🙏 Tecnologías Utilizadas
- **yt-dlp**: Motor principal de descarga
- **FFmpeg**: Procesamiento de video/audio
- **Zenity**: Interfaz gráfica
- **Bash**: Scripting y automatización
- **jq**: Procesamiento JSON
- **OpenSSL**: Encriptación de backups

### 🌟 Agradecimientos Especiales
- Comunidad de yt-dlp
- Desarrolladores de FFmpeg
- Comunidad de Arch Linux
- Usuarios beta testers
- Contribuidores de feedback

---

## 🔮 Roadmap Futuro (v4.0)

### 🚀 Características Planificadas

- 🌐 **Interfaz Web**: Panel de control vía navegador
- 🐳 **Soporte Docker**: Containerización completa
- 🤖 **Integración IA**: Detección automática de contenido
- 📱 **App Móvil**: Control remoto desde smartphone
- ☁️ **Sincronización en la Nube**: Sincronización con servicios en la nube
- 🎵 **Gestión de Música**: Organización automática de música
- 📺 **Servidor Multimedia**: Servidor de streaming integrado
- 🔄 **Actualizaciones Automáticas**: Actualizaciones automáticas sin intervención

### 🎯 Mejoras Técnicas

- 🚀 **Rendimiento**: Optimización de velocidad
- 🔒 **Seguridad**: Mejoras de seguridad
- 🎨 **UI/UX**: Interfaz más moderna
- 🌍 **i18n**: Soporte multiidioma
- 📊 **Analíticas**: Métricas avanzadas

---

## ⚠️ Notas Importantes

1.  **Reinicia tu terminal** o ejecuta `source ~/.zshrc` (o `source ~/.bashrc`) después de la instalación para que los comandos estén disponibles.
2.  Usa responsablemente respetando los términos de servicio de las plataformas.
3.  Ejecuta `video-downloader-update` semanalmente para mantener `yt-dlp` actualizado y asegurar la funcionalidad.
4.  Lee la documentación completa en el README para más detalles.

---

**🎉 ¡Disfruta descargando videos de forma segura y profesional con Video Downloader v3.0!**

_Desarrollado con ❤️ por DreamCoder08 para la comunidad de Arch Linux_