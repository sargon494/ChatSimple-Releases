# Política de privacidad de ChatSimple

**Última actualización:** 31 de octubre de 2026

ChatSimple es una aplicación de escritorio que muestra en una sola ventana los chats en directo de Twitch, Kick, YouTube y TikTok, y permite moderarlos desde ahí. Esta política explica qué datos trata la aplicación, para qué, dónde se guardan y con quién se comparten.

## 1. Responsable y contacto

- **Alias:** Sargon494
- **Contacto:** hbosxojhi@mozmail.com

## 2. Datos que trata la aplicación

- **Tokens de acceso (OAuth)** de Twitch, Kick y YouTube, que se obtienen cuando inicias sesión en esas plataformas desde la aplicación. Se usan solo para leer el chat y ejecutar las acciones de moderación que tú eliges (borrar mensajes, banear, desbanear, enviar mensajes).
- **Nombres de usuario y canales** que introduces en los ajustes, para saber a qué chats conectarte.
- **Mensajes del chat en directo** de las plataformas. Se muestran en la ventana de la aplicación y, si usas el dock o el overlay de OBS, en el navegador integrado de OBS. ChatSimple no los guarda en ningún servidor.
- **Preferencias de la aplicación** (opciones de visualización, emotes, configuración del overlay).

## 3. Dónde se guardan los datos

- Los **tokens de acceso** se guardan solo en tu dispositivo, en el almacenamiento seguro del sistema operativo.
- Las **preferencias** se guardan solo en tu dispositivo.
- El **dock y el overlay de OBS** funcionan en tu propio equipo, a través de un servidor local que escucha en `localhost`. No se publican en internet.
- El **relay de TikTok** (si lo usas) también es local: escucha en `127.0.0.1`.

ChatSimple **no dispone de servidores propios que almacenen tus datos, tus tokens ni tu historial de chat.**

## 4. Servicios de terceros con los que se comunica la aplicación

Para funcionar, ChatSimple hace peticiones directas a los servicios siguientes. Cada uno trata los datos según su propia política de privacidad, y en esas peticiones recibe tu dirección IP y los datos necesarios para la operación.

| Servicio | Para qué | Datos que recibe |
|---|---|---|
| **Twitch** (`id.twitch.tv`, `api.twitch.tv`, `irc-ws.chat.twitch.tv`, `eventsub.wss.twitch.tv`) | Leer y moderar el chat, predicciones, Hype Train | Token de acceso, nombre de canal |
| **Kick** (`kick.com`, `api.kick.com`, `id.kick.com`, `ws-us2.pusher.com`) | Leer y moderar el chat | Token de acceso, nombre de canal |
| **YouTube / Google** (`www.googleapis.com`, `accounts.google.com`) | Leer y moderar el chat en directo, iniciar sesión | Token de acceso, ID del canal o del directo |
| **TikTok** (`www.tiktok.com`) | Comprobar si un usuario está en directo y leer su chat | Nombre de usuario de TikTok |
| **EulerStream** (`ws.eulerstream.com`) | Conexión alternativa al chat de TikTok, solo si configuras una clave | Nombre de usuario de TikTok y tu clave de API |
| **7TV** (`7tv.io`, `cdn.7tv.app`) | Descargar emotes | Dirección IP al cargar las imágenes |
| **IVR** (`api.ivr.fi`) | Obtener datos públicos de un canal de Twitch para los emotes de 7TV | Nombre de canal de Twitch |
| **Imágenes de las plataformas** (`yt3.ggpht.com`, `static-cdn.jtvnw.net`) | Mostrar avatares y emotes | Dirección IP al cargar las imágenes |
| **GitHub** (`api.github.com`) | Comprobar si hay una versión nueva de la aplicación | Ninguno personal; solo la petición de la versión |

ChatSimple **no vende, alquila ni comparte tus datos con terceros con fines publicitarios**, y no usa ningún servicio de analítica ni publicidad.

## 5. Permisos de YouTube

El inicio de sesión con YouTube pide a Google los siguientes permisos:

- **`youtube.force-ssl`**: leer el chat en directo y ejecutar las acciones de moderación y envío de mensajes.
- **`youtube.readonly`**: leer información de tu canal y de los directos. *(Se elimina de esta lista si deja de pedirse en la aplicación.)*

El uso de la información recibida de las APIs de Google cumple la [Política de datos de usuario de los servicios de API de Google](https://developers.google.com/terms/api-services-user-data-policy), incluidos los requisitos de uso limitado. Los datos se usan únicamente para las funciones de chat descritas en esta política.

Puedes revocar el acceso en cualquier momento desde tu cuenta de Google, en **Seguridad → Acceso de terceros**, o cerrar sesión en la aplicación.

## 6. Cuánto tiempo se conservan los datos

Los tokens y las preferencias se conservan en tu dispositivo hasta que cierras sesión, desconectas la cuenta o desinstalas la aplicación.

## 7. Tus derechos

Puedes, en cualquier momento:

- Cerrar sesión en cada plataforma desde los ajustes de la aplicación.
- Revocar el acceso de ChatSimple desde la configuración de cada plataforma (Twitch, Kick, Google).
- Eliminar los datos locales desinstalando la aplicación.
- Pedirnos información o plantear cualquier duda sobre esta política escribiendo a **hbosxojhi@mozmail.com**.

## 8. Cambios en esta política

Si esta política cambia, se actualizará la fecha de la parte superior. Los cambios importantes se comunicarán en el repositorio del proyecto.
