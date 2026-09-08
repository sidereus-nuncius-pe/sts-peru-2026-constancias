# Verificación de constancias — III Encuentro CTS Perú 2026

Página estática (sin backend) para verificar la autenticidad de las constancias
de participación del III Encuentro CTS Perú 2026. La persona ingresa el código
impreso en su certificado (formato `CTS26-XXXXXX`) y la página muestra a quién
pertenece — o indica que el código no existe.

## Cómo publicarlo en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `sts-peru-verificacion`).
   Puede ser público.
2. Sube estos dos archivos a la raíz del repositorio:
   - `index.html`
   - `data.json`
3. Ve a **Settings → Pages** en el repositorio.
4. En "Source", selecciona la rama `main` (o `master`) y la carpeta `/ (root)`.
5. Guarda. GitHub te dará una URL parecida a:
   `https://<tu-usuario>.github.io/sts-peru-verificacion/`
6. Ese es el enlace que puedes compartir junto con las constancias (por
   ejemplo, en el correo de envío o en el pie de la web del evento).

No necesitas ningún paso adicional: `index.html` carga `data.json` directamente
por lo que funciona apenas GitHub Pages sirve los archivos, sin backend ni
base de datos externa.

## Si agregan más constancias después

Vuelve a generar `data.json` con los nuevos códigos y afiliaciones, y súbelo
al repositorio reemplazando el archivo existente (mismo nombre). GitHub Pages
se actualiza solo en 1–2 minutos tras el commit.

## Privacidad

La página solo muestra el registro correspondiente al código ingresado — nunca
la lista completa. Aun así, `data.json` como archivo es técnicamente
descargable por cualquiera que sepa buscarlo (como cualquier sitio estático
público). Si en el futuro necesitan que ni siquiera el archivo crudo sea
accesible, la alternativa es mover la búsqueda a un backend real (por ejemplo,
una función serverless que consulte una base de datos privada) — pero eso ya
excede lo que un sitio estático en GitHub Pages puede ofrecer.
