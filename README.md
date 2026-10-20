# Profundia — política de privacidad portable

Copia de la página original de privacidad de AverisYT, recuperada el 20/10/2026. El archivo `public/index.html` conserva exactamente el contenido publicado el 16/10/2026 para Profundia 0.51.0.

**Antes de sustituir la URL de privacidad en la versión actual:** el texto recuperado dice que la 0.51 no incorpora SDK publicitarios. Como el juego ya está integrando AdMob, esa sección necesita revisión con el código y configuración actuales. Este paquete exporta la página existente; no certifica las prácticas de datos de versiones posteriores ni incorpora una auditoría del SDK actual. No publiques esa afirmación antigua como descripción de la versión con anuncios, aunque sean anuncios de prueba.

## Archivos

- `public/index.html`: página completa, con estilos incluidos y diseño adaptable.
- `vercel.json`: configuración de sitio estático, sin instalaciones ni compilación.
- `.gitignore`: evita subir archivos locales y credenciales habituales.

No necesita Node.js, npm, una base de datos, APIs, una cuenta de ChatGPT ni scripts externos para servir la página. Los enlaces de Google y AEPD son enlaces de consulta; no son dependencias de carga. No se han incluido el repositorio privado de origen, credenciales ni configuración de Sites. El sitio original no se ha modificado ni despublicado.

## Coste y condiciones de Vercel

Vercel Hobby es gratuito, pero sus condiciones lo limitan a uso personal no comercial. Profundia tiene monetización prevista o integrada: no se garantiza que esta página asociada al juego sea elegible para Hobby. Confírmalo con Vercel antes de depender de ese plan; si consideran el uso comercial, necesitarías un plan permitido o un proveedor distinto. Este paquete no contrata ningún plan de pago ni configura cobros.

Condiciones: https://vercel.com/docs/limits/fair-use-guidelines

## Subir a GitHub

1. Descomprime el ZIP.
2. En GitHub, crea un repositorio llamado `profundia-privacidad` en tu cuenta personal. Puede ser público o privado si tu plan de hosting admite esa integración.
3. Abre el repositorio y usa **Add file → Upload files**.
4. Sube el contenido de esta carpeta: `public/`, `vercel.json` y `README.md` (y `.gitignore` si puedes seleccionarlo). No subas el ZIP.
5. Comprueba que `vercel.json` está en la raíz del repositorio y que existe `public/index.html`. No dejes todos los archivos dentro de una carpeta adicional.
6. Guarda con **Commit changes**.

También puedes usar Git desde esta carpeta: `git init`, añadir tu remoto, añadir archivos y hacer commit/push normalmente. No se ha elegido ni creado un remoto por ti.

## Publicar en Vercel

1. Entra con tu cuenta en https://vercel.com/.
2. Selecciona **Add New → Project** e importa el repositorio de GitHub. Autoriza acceso solo al repositorio necesario.
3. Framework Preset: **Other**. Root Directory: raíz del repositorio (`./`).
4. Build Command e Install Command: vacíos. Output Directory: **public**. El archivo `vercel.json` ya configura estos valores.
5. No hay variables de entorno que añadir. No actives servicios de analítica o funciones que no necesites.
6. Pulsa **Deploy**, siempre que el plan elegido permita tu uso.
7. Utiliza la URL estable de producción que te asigne Vercel, de la forma `https://TU-PROYECTO.vercel.app/`. Es un ejemplo: el nombre definitivo lo determina tu proyecto.
8. Abre esa URL en una ventana de incógnito, sin iniciar sesión. La política debe verse sin contraseña, sin iniciar sesión en Vercel y sin pantalla de protección del despliegue. Si aparece una barrera de acceso, revisa **Settings → Deployment Protection** para el dominio de producción.

No se ha desplegado este paquete en Vercel desde este chat: el despliegue se hará en tu cuenta.

Documentación: https://vercel.com/docs/builds/configure-a-build

## Cambiar desde la URL antigua

Cuando el texto actualizado esté publicado y accesible:

1. Cambia el enlace de política de privacidad en Play Console, dentro de **Contenido de la aplicación → Política de privacidad**.
2. Cambia el enlace en AdMob, incluidos los mensajes de privacidad/consentimiento que lo utilicen.
3. Pasa la nueva URL al chat que está desarrollando Profundia para actualizar cualquier enlace que siga apuntando al sitio antiguo y mantener coherente el texto dentro del juego.
4. Elige el dominio estable de producción, no una URL temporal de preview.
5. Conserva el sitio antiguo durante la transición y revisa enlaces de versiones antiguas antes de retirarlo.

Si también quieres alojar `app-ads.txt`, copia exactamente la línea que proporciona tu cuenta de AdMob en `public/app-ads.txt` y configura este dominio como web del desarrollador en la ficha de Google Play. No basta con ponerlo como política de privacidad. No se incluye una línea ficticia en este paquete.

## Modificar el texto después

Edita `public/index.html`, actualiza la fecha de revisión cuando cambien las prácticas y guarda el cambio en GitHub. Si mantienes la integración Git de Vercel, un nuevo commit en la rama de producción generará un nuevo despliegue.

## Alternativa de despliegue estático

Los archivos de `public/` son HTML estándar y se pueden alojar con otro proveedor, sin convertir el proyecto. En Cloudflare Pages con integración Git: usa el repositorio, framework **None**, build command `exit 0` y build output directory `public`. Revisa las condiciones y los límites del plan que elijas. La configuración específica de Vercel no es necesaria para servir el HTML en otro proveedor.

https://developers.cloudflare.com/pages/framework-guides/deploy-anything/
