# Neurofit · Experience Studio

Portafolio responsive en español de experiencias WebAR y activaciones de marca. Los botones de contacto abren WhatsApp en el +52 720 703 5759.

## Vista local

Desde la raíz del repositorio, ejecuta:

```powershell
python -m http.server 8000 --directory frontend
```

Abre http://localhost:8000. Python solo sirve los archivos para esta vista local. El sitio público se compone de HTML, CSS, JavaScript y recursos estáticos.

## Publicación en Cloudflare Pages

1. Sube el proyecto a un repositorio nuevo de GitHub.
2. En Cloudflare, abre **Workers & Pages**, crea un proyecto de **Pages** y conecta el repositorio de GitHub.
3. Selecciona la rama de producción (por ejemplo, `main`). Deja vacío el comando de compilación y usa `frontend` como directorio de salida. Deja el directorio raíz en su valor predeterminado.
4. Publica y prueba la dirección `<proyecto>.pages.dev`. Cloudflare vuelve a desplegar el sitio al recibir cambios en la rama de producción.

La URL `pages.dev` está incluida en el plan gratuito. La compra y renovación de un dominio propio se pagan al registrador. [Guía de Cloudflare Pages](https://developers.cloudflare.com/pages/get-started/git-integration/) · [Límites del plan gratuito](https://developers.cloudflare.com/pages/platform/limits/)

### Dominio de IONOS

- Para usar el dominio principal (por ejemplo, `ejemplo.com`), conserva el registro en IONOS, añade el dominio a Cloudflare y configura en IONOS los servidores de nombres que indique Cloudflare. Después vincula el dominio en **Custom domains** dentro de Pages.
- Para usar solo `www.ejemplo.com` con el DNS administrado por IONOS, añade primero ese subdominio en **Custom domains** de Pages y crea en IONOS el CNAME de `www` hacia `<proyecto>.pages.dev`.

[Dominios personalizados en Cloudflare Pages](https://developers.cloudflare.com/pages/configuration/custom-domains/) · [Configuración DNS de IONOS](https://www.ionos.com/help/domains/general-information-about-dns-settings/managing-dns-settings-in-control-center/)

## Contenidos y recursos

- `frontend/index.html` contiene los textos, las tarjetas y los enlaces de WhatsApp.
- `frontend/css/styles.css` define el diseño responsive.
- `frontend/js/app.js` controla el menú, los filtros, los detalles de casos y las animaciones.
- `frontend/assets/` contiene las imágenes WebP y los logos que usa el sitio.
- `source-assets/` conserva los recursos gráficos fuera del directorio de publicación.
- `backend/`, `data/` y `java/` conservan componentes de la maqueta original fuera del despliegue.

Las imágenes, los QR y las promociones de los casos son demostraciones conceptuales. El portafolio presenta las ideas de WebAR mediante imágenes y descripciones.
