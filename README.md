# ChatSimple

**ChatSimple** es una aplicación de escritorio ligera para streamers y creadores de contenido. Reúne el chat de Twitch, Kick, YouTube y TikTok en una sola ventana, con moderación integrada e integración directa con OBS Studio.

- [Plataformas](#plataformas)
- [Características](#características)
- [Instalación](#instalación)
- [Integración con OBS Studio](#integración-con-obs-studio)
- [Privacidad](#privacidad)
- [Limitaciones conocidas](#limitaciones-conocidas)
- [Contacto](#contacto)

## Plataformas

| Plataforma | Lectura del chat | Moderación | Notas |
|---|:---:|:---:|---|
| Twitch | ✅ | ✅ | Predicciones, Hype Train, badges, modos de chat |
| Kick | ✅ | ✅ | Ban, timeout y borrado de mensajes. Sin modos de chat (la API no lo permite) |
| YouTube | ✅ | ✅ | Requiere inicio de sesión con Google para moderar |
| TikTok | ✅ | — | Lectura del chat de tus directos |

## Características

- **Chat unificado.** Todos los mensajes se combinan en una lista, diferenciados por plataforma.
- **Moderación.** Borrar mensajes, poner en *timeout* o banear, y desbanear. También puedes usar el comando `/unban @usuario` desde el chat.
- **Modos de chat de Twitch.** Modo lento, solo seguidores, solo suscriptores y solo emotes, desde la ventana o desde el dock de OBS.
- **Predicciones y Hype Train de Twitch.** Progreso, porcentajes y temporizador en tiempo real.
- **Emotes.** Soporte para emotes de Twitch, YouTube y 7TV (canal y globales), con opción de activarlos o desactivarlos.
- **Menciones.** Escribe `@` para autocompletar nombres de espectadores.
- **Espectadores activos.** Panel con quién participa en el chat, por plataforma.
- **Siempre arriba.** Fija la ventana sobre tu juego o software de streaming.
- **Actualizaciones.** Avisa cuando hay una versión nueva disponible.

## Instalación

1. Descarga la última versión desde la sección de [releases](https://github.com/sargon494/ChatSimple-Releases/releases).
2. Descomprime la carpeta.
3. Ejecuta `ChatSimple.exe`.
4. Abre **Ajustes** (⚙️), conecta tu cuenta de Twitch o Kick, e introduce tu usuario de YouTube o TikTok.

La aplicación se conectará automáticamente a los chats configurados.

## Integración con OBS Studio

ChatSimple se integra con OBS mediante un servidor local:

1. **Dock de OBS.** En *Vista → Docks → Docks de navegador personalizados*, añade la URL del dock. Desde ahí puedes leer el chat, responder y moderar sin salir de OBS.
2. **Fuente de navegador.** Añade la URL del overlay como fuente de navegador en tu escena para mostrar el chat en el directo.

Ambos funcionan en tu equipo, en `localhost`.

## Privacidad

ChatSimple no tiene servidores propios que guarden tus datos. Los tokens se guardan en tu dispositivo, y la aplicación se comunica directamente con las plataformas que usas.

La información completa sobre qué datos se tratan, dónde se guardan y con qué servicios se comunica la aplicación está en **[docs/PRIVACY.md](docs/PRIVACY.md)**.

## Limitaciones conocidas

- **YouTube:** solo puedes desbanear a usuarios que hayas baneado desde la aplicación en el directo actual, porque la API de YouTube no permite listar los baneos. Los modos de chat no están disponibles en la API.
- **TikTok:** la conexión depende de un servicio de terceros (EulerStream) o del relay local, y puede dejar de funcionar si TikTok cambia su API.
- **Kick:** no hay API para cambiar los modos de chat.

## Contacto

**Sargon494**: hbosxojhi@mozmail.com
