# Reservas · isla

Archivos que van en el repositorio (los 5 que ya conoces más los que crea el sistema):

- `index.html` · **mesa y recepción**. Muestra las reservas de hoy de las **próximas 2 horas**, deja marcar quién llegó y se sincroniza sola.
- `agenda.html` · **socios**. Agregan, editan y borran reservas con su nombre y una contraseña compartida.
- `admin.html` · **administración**. Calendario completo, publicar y crear el acceso de los socios.
- `data.json` · las reservas (lo actualizan las páginas, no lo edites a mano).
- `acceso.json` · lo crea `admin.html` (token cifrado con la contraseña de los socios). No lo edites.

No subas `socios.html`, `config.js` ni `codigo-servidor.gs`: son de otra versión (servidor de Google) y no se usan.

## Mesa y recepción (`index.html`)
- **Ventana de 2 horas.** Cambia al minuto :01. A las 10:01 se ve de 10:01 a 12:00; a las 11:01, de 11:01 a 13:00.
- **Las retrasadas no desaparecen.** Una reserva cuya hora ya pasó sigue en la sección «Ya debieron llegar», con el tiempo de retraso, hasta que alguien pulse **Ya llegó** o **No llegó**.
- **Ya llegó**: antes de pulsarlo, ajusta con − / + cuántas personas llegaron (viene con lo reservado). Se guarda quién y a qué hora.
- **No llegó**: pide un segundo toque de confirmación.
- **Atendidas hoy**: botón al final de la lista; ahí está **Deshacer** por si alguien se equivocó.
- **Sincronización**: lo que se marca en un dispositivo aparece en los demás en unos 20 segundos, sin recargar.
- **Primera vez en cada dispositivo**: tocar **Entrar**, escribir nombre y contraseña. Después ya no la pide. Sin entrar, la página funciona en solo lectura.

## Socios (`agenda.html`)
Calendario del mes, agregar reservas de cualquier día, editar y borrar. Cada reserva guarda quién la capturó. Se guarda al momento.

## Crear o cambiar el acceso de los socios
1. Abre `admin.html` → pestaña **Publicación** → bloque **Acceso para socios**.
2. Escribe la contraseña (mínimo 8 caracteres) y, recomendado, un token aparte solo para ellos (mismos pasos que el tuyo, con otro nombre).
3. **Crear acceso para socios**. En 1 o 2 minutos funciona el enlace `…/agenda.html`.
4. Para cambiar la contraseña o cortar el acceso: vuelve a crearlo con otra contraseña y/o borra ese token en GitHub.

## Seguridad: lo que conviene saber
- La contraseña no está en ningún archivo; solo abre un token cifrado. Aun así, el repositorio es público: una contraseña corta o fácil de adivinar se puede descubrir probando muchas. Usa una larga si puedes.
- Cualquiera con la contraseña puede cambiar las reservas (también desde fuera de las páginas). Compártela solo con quien deba tenerla.
- `data.json` es público y contiene **todas** las reservas y las llegadas. Captura solo nombres de pila, sin apellidos ni teléfonos.
- `admin.html` no necesita contraseña para abrirse, pero sin tu token no puede publicar.

## Instalación (una sola vez)
1. Repositorio nuevo en github.com. **Add file → Upload files**: sube `index.html`, `agenda.html`, `admin.html`, `data.json` y este `README.md`.
2. **Settings → Pages** → *Deploy from a branch* → `main` → `/ (root)`.
3. En `admin.html` → **Publicación**: conecta con tu token (Contents: Read and write, solo ese repositorio) y crea el acceso de socios.
4. Mesa, recepción y socios: cada quien abre su enlace y entra una vez.
