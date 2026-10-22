# Reservas de hoy · vista para mesa y recepción

- `index.html` es la página que ven en la mesa y en recepción. Muestra **solo las reservas de hoy** de la hora en curso y cambia sola. No muestra otros días.
- `admin.html` es la página donde tú (y quien registre reservas) captura, edita y borra, desde celular o computadora.
- `data.json` guarda las reservas. El botón «Publicar cambios» lo actualiza por ti.

## Cómo cambia la hora
La ventana cambia al minuto :01 de cada hora:
- A las 10:01 aparecen las reservas de 10:01 a 11:00.
- A las 11:01 aparecen las de 11:01 a 12:00. Y así sucesivamente.

Usa la hora del dispositivo que tenga la página abierta.

## Instalación (una sola vez)
1. En github.com crea un repositorio nuevo, por ejemplo `reservas-isla`.
2. **Add file → Upload files**: sube `index.html`, `admin.html`, `data.json` y este `README.md`. Confirma con **Commit changes**.
3. **Settings → Pages**: en *Build and deployment* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`. Guarda.
4. En uno o dos minutos GitHub muestra la dirección, algo como `https://TU-USUARIO.github.io/reservas-isla/`.
   - Mesa y recepción: esa dirección.
   - Tú: esa dirección más `admin.html`.

## Conectar tu celular y tu computadora (una vez en cada uno)
1. Abre `admin.html`. Se abre la pestaña **Publicación**.
2. Crea el token como indica esa pestaña (Contents: Read and write, solo para este repositorio).
3. Pega usuario, repositorio y token, y pulsa **Guardar y probar**.

## Uso diario
1. Abre `admin.html`, elige el día y agrega las reservas (hora, nombre, personas, nota).
2. Pulsa **Publicar cambios**. En 1 o 2 minutos se ven en la página pública.

## Importante
- Un repositorio público lo ve cualquiera con el enlace, y `data.json` contiene **todas** las reservas, no solo las de hoy. Conviene capturar solo el nombre de pila, sin apellidos ni teléfonos.
- Cualquiera puede abrir `admin.html`, pero sin tu token no puede publicar nada.
- El token vive solo en tu dispositivo. Si lo pierdes, bórralo en GitHub (Settings → Developer settings → Personal access tokens) y crea otro.
- Si dos personas editan desde dispositivos distintos, la última en publicar sobrescribe a la otra. Conviene que solo una persona publique.
