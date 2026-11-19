# Política de privacidad de TV BRIDGE

**TV BRIDGE — Tu teléfono, conectado a tu TV.**

Versión 1.0 · En vigor desde el 19 de noviembre de 2026.

## 1. Responsable

ASTRIM · <https://astrim-web.web.app/productos/tv-bridge>

## 2. Resumen

- TV BRIDGE **no pide cuenta, nombre, correo ni teléfono**.
- Para vincular el teléfono con la TV usa un **código temporal** y una **sesión anónima** en Firebase (Google).
- Los **APK que envías** viajan cifrados del teléfono a la TV; ASTRIM no recibe ni guarda una copia.
- Los **enlaces y códigos** que envías pasan por la sesión de Firebase para llegar a la TV, y la TV descarga el archivo directamente desde su origen.
- TV BRIDGE **no tiene publicidad ni analítica** y no vende ni comparte datos con fines comerciales.

## 3. Información que procesa la aplicación

**En la sesión de vinculación (Firebase Realtime Database):**

- Un **identificador anónimo** de Firebase Authentication para el teléfono y otro para la TV. No están ligados a tu identidad.
- Un **resumen (hash) del código** de 6 dígitos, el identificador de la sesión, su estado (esperando, vinculada o terminada) y sus fechas de creación y vencimiento.
- El **último enlace o código de descarga** que envías a la TV y la hora de envío.
- Los **datos técnicos de conexión** que el teléfono y la TV intercambian para conectarse entre sí (ofertas y respuestas de sesión y "candidatos" de red). Estos datos incluyen **direcciones IP** de tus dispositivos.

Al desconectar, la sesión queda marcada como terminada y deja de poder usarse, pero sus datos no se borran en ese momento.

**En tus dispositivos:**

- La TV guarda los APK recibidos o descargados en su carpeta pública de **Descargas**, donde puedes verlos y borrarlos desde **Archivos** en la app o desde el sistema.

## 4. Archivos que envías o descargas

- **Envío de APK (teléfono → TV):** la transferencia usa WebRTC, que la cifra de punta a punta. Cuando la red lo permite, va directa entre tus dispositivos. Si no, pasa por un servidor de relevo (TURN) de Open Relay Project (metered.ca), que solo ve datos cifrados.
- **Enlaces y códigos:** la TV descarga el archivo directamente desde el servidor de origen (por ejemplo MediaFire, Google Drive, Mega o Dropbox). Ese servidor recibe la dirección IP de tu TV, como en cualquier descarga. Para los **códigos de descarga**, el teléfono y la TV consultan el servicio de AFTVnews (`aftv.news`) para obtener el enlace real. Para los enlaces de **Mega**, la TV consulta la API de Mega; la clave del archivo está en el enlace y nunca se envía a Mega.
- ASTRIM **no aloja, revisa ni distribuye** los archivos que transfieres o descargas.

## 5. Permisos que solicita la aplicación

**Teléfono:**

- **Internet:** vincularse con la TV, enviar archivos y enlaces, y comprobar códigos de descarga.
- **Selector de archivos del sistema:** para enviar un APK. TV BRIDGE solo recibe el archivo que eliges; no pide acceso general a tus archivos.

**TV:**

- **Internet y estado de la red:** vincularse con el teléfono, recibir archivos y descargar enlaces.
- **Instalar aplicaciones:** abrir el instalador de Android con el APK recibido. La instalación siempre la confirmas tú en la pantalla del sistema.
- **Consultar las aplicaciones instaladas:** mostrar si la app recibida ya está instalada y qué permisos pide antes de instalarla.
- **Almacenamiento** (solo Android 9 a 12): guardar los APK en la carpeta de Descargas.

## 6. Servicios de terceros

- **Firebase (Google):** autenticación anónima y base de datos de la sesión. <https://firebase.google.com/support/privacy>
- **STUN de Google** y **Open Relay Project (metered.ca):** establecer la conexión entre teléfono y TV.
- **AFTVnews:** traducir códigos de descarga.
- **Servicios de archivos que tú elijas:** MediaFire, Google Drive, Mega, Dropbox, etc., conforme a sus propias políticas.

## 7. Conservación y eliminación

Los APK guardados en la TV permanecen hasta que los borras. Desinstalar TV BRIDGE elimina la sesión anónima del dispositivo. Para solicitar la eliminación de datos de sesiones, escribe a ASTRIM por los canales indicados en <https://astrim-web.web.app/>.

## 8. Menores

TV BRIDGE no está dirigida específicamente a menores ni recoge a sabiendas información personal de ellos.

## 9. Cambios

Si esta política cambia, se publicará la nueva versión en este repositorio con su fecha de entrada en vigor.

## 10. Contacto

ASTRIM · <https://astrim-web.web.app/>

© 2026 ASTRIM. Todos los derechos reservados.
