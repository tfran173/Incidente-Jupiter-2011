# Incidente Júpiter 2011

Juego de acción y exploración basado en el meme. Funciona en el navegador, sin instalar nada.

## Cómo publicarlo en GitHub Pages (repositorio `tfran173/Incidente-Jupiter-2011`)

1. Abre https://github.com/tfran173/Incidente-Jupiter-2011
2. Pulsa **Add file → Upload files**.
3. Arrastra **el contenido de la carpeta** (no la carpeta en sí): `index.html`, la carpeta `audio`, `database.rules.json`, `README.md` y `.nojekyll`.
   - Si tu sistema no te deja arrastrar `.nojekyll` (empieza por punto), no pasa nada: se puede omitir.
4. Escribe un mensaje (por ejemplo "Subir juego") y pulsa **Commit changes**.
5. Ve a **Settings → Pages**. En **Source** elige **Deploy from a branch**, rama **main**, carpeta **/ (root)** y guarda.
6. Espera 1–3 minutos. La dirección será:
   **https://tfran173.github.io/Incidente-Jupiter-2011/**

## Probar el multijugador

1. Abre el juego en dos pestañas o en dos dispositivos.
2. En ambos: **Jugar → Multijugador**, escribe el mismo código de sala (por ejemplo `sala1`) y pulsa **Conectar**.
3. Elige **Mundo abierto** y pulsa **Iniciar partida**. En Júpiter, uno actúa de anfitrión y los demás ven las mismas Keys.

## Firebase

- Usa **Realtime Database** con las reglas de `database.rules.json` (ya publicadas en tu proyecto).
- En el plan gratuito (Spark) hay un máximo de **100 conexiones simultáneas** y límites mensuales de descarga y almacenamiento. Si se superan, la base de datos deja de responder hasta el siguiente ciclo.
- Las reglas dejan leer y escribir en `salas/*` a cualquiera que tenga el enlace. No guardes datos personales ahí.
- La clave `apiKey` de la web es pública por diseño; no es un secreto.
- Revisa el uso en Firebase → Realtime Database → Uso.

## Limitaciones conocidas

- Cada jugador calcula sus efectos (hazards, algunos efectos de las Keys T); el anfitrión manda sobre posición y vida de las Keys.
- El anfitrión puede hacer trampa porque la lógica corre en su navegador.
- El progreso (créditos, tecnología, lore) se guarda en el navegador de cada jugador (`localStorage`).
