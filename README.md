# Simple Chat (Twitch & Kick)

Una aplicación de escritorio minimalista y unificada para leer y moderar los chats de Twitch y Kick simultáneamente. Creada con Flutter, pensada para ser rápida, personalizable (soporta 7TV) y no consumir apenas recursos.

## Características

- **Chat Unificado**: Lee mensajes de Twitch y Kick en una sola columna o pestaña separada.
- **Soporte de Emotes (7TV)**: Integra automáticamente los emotes globales y de canal (Twitch & Kick) a través de la API de 7TV.
- **Acciones de Moderación Oficiales**:
  - **Twitch**: Ban, timeout y borrado de mensajes utilizando la API oficial de Helix.
  - **Kick**: Ban, timeout y borrado de mensajes integrados usando la API Pública V1 oficial de Kick.
- **Panel de Viewers Activos**: Contadores independientes para Twitch y Kick con una lista de usuarios actualmente hablando en el chat.
- **Transparencia y Always-On-Top**: Ventana minimalista ideal para tener superpuesta en tu pantalla mientras haces streaming o juegas, con soporte "pin" (fijar) para que siempre esté encima de otras ventanas.

## Uso y Ejecutables

Para usar la aplicación, simplemente extrae la carpeta del ejecutable `Release` (que contiene `chat_simple.exe` y la carpeta `data`).

Tus credenciales y configuraciones se guardan **localmente en tu PC** (mediante *SharedPreferences* de Windows). Si mueves la carpeta o la pasas a otra persona, la aplicación se abrirá "limpia" y le pedirá a esa persona configurar sus propios canales y hacer sus propios logins en Ajustes. 

**Tus datos no viajan con el ejecutable.**

### Configuración de Desarrollador (Si vas a compilar tú mismo)

El código fuente necesita un archivo de entorno (`.env`) en la raíz del proyecto (junto a `pubspec.yaml`) para que la app tenga las credenciales globales con las que conectarse a las APIs.

Debes crear el archivo `.env` tomando como base `.env.example`:

```env
TWITCH_CLIENT_ID="tu_twitch_client_id"
KICK_CLIENT_ID="tu_kick_client_id"
KICK_CLIENT_SECRET="tu_kick_client_secret"
```

Los *tokens de acceso de usuario* (para leer o escribir como moderador) no van en el `.env`. El usuario final los obtiene haciendo login directamente en la UI de Ajustes de la app.

## Compilación

Para construir tu propio ejecutable de producción para Windows:

```bash
flutter clean
flutter pub get
flutter build windows
```

El resultado aparecerá en `build/windows/x64/runner/Release`. Copia el contenido entero de esa carpeta donde quieras ejecutarlo.
