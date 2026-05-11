# YOPI — Territorios, memoria y resistencia

Revista biocultural con enfoque antropológico, científico y educativo.  
Periodismo de largo aliento sobre los pueblos y territorios de Centroamérica.

---

## Estructura del repositorio

```
yopi-site/
│
├── index.html                  ← Página principal (homepage)
│
├── secciones/
│   ├── biorelatos.html         ← Investigación de largo aliento
│   ├── palabra-antigua.html    ← Saberes ancestrales y etnoconocimientos
│   ├── colores-del-gris.html   ← Extractivismo, tierra, defensa del agua
│   ├── palabra-florida.html    ← Mitos, espiritualidad, paisaje mesoamericano
│   └── biogramas.html          ← Perfiles visuales de defensores y artistas
│
├── assets/
│   ├── css/
│   │   └── yopi.css            ← Estilos globales (extraídos del index)
│   ├── js/
│   │   └── yopi.js             ← Scripts globales
│   └── images/
│       ├── hero/               ← Imagen principal del hero (reemplazar)
│       ├── fotoreportajes/     ← Galerías fotográficas
│       ├── biorelatos/         ← Imágenes de investigaciones
│       ├── colores-del-gris/
│       ├── palabra-antigua/
│       ├── palabra-florida/
│       └── biogramas/
│
├── dossieres/                  ← PDFs descargables (investigaciones)
│
└── README.md                   ← Este archivo
```

---

## Cómo activar GitHub Pages

1. Sube esta carpeta completa a un repositorio en GitHub
2. Ve a **Settings → Pages**
3. En *Source*, selecciona **Deploy from a branch**
4. Selecciona la rama `main` y la carpeta `/ (root)`
5. Guarda — en 1-2 minutos el sitio estará en:
   `https://TU-USUARIO.github.io/yopi/`

---

## Cómo agregar una nota nueva

1. Abre `index.html`
2. Busca la sección correspondiente (Biorelatos, Los Colores del Gris, etc.)
3. Duplica un bloque `.card-nota` existente
4. Reemplaza: título, extracto, autor, fecha, formato (badge)
5. Agrega la imagen en `assets/images/[seccion]/`
6. Actualiza la ruta en el `div.nota-imagen-inner`
7. Sube los cambios con `git push`

---

## Cómo reemplazar imágenes placeholder

Las zonas oscuras con gradiente en el sitio son **placeholders**.  
Para reemplazarlas con tus fotografías:

```html
<!-- Antes (placeholder) -->
<div class="nota-imagen-inner img-biorelatos"></div>

<!-- Después (con tu foto) -->
<div class="nota-imagen-inner" style="background-image: url('assets/images/biorelatos/nombre-de-tu-foto.jpg'); background-size: cover; background-position: center;"></div>
```

**Formatos recomendados:**
- Hero principal: `1600 × 900px` mínimo, JPG optimizado
- Cards de notas: `800 × 500px`, JPG optimizado
- Fotoreportajes: `1200 × 800px`, JPG o WebP
- Peso máximo recomendado por imagen: **300KB** (usa [Squoosh](https://squoosh.app) para comprimir)

---

## Fuentes tipográficas

El sitio carga fuentes desde Google Fonts:
- **Cormorant Garamond** — display editorial, titulares
- **IBM Plex Mono** — labels, metadatos, navegación

No requieren instalación. Si quieres privacidad total (sin Google), descárgalas desde [Font Squirrel](https://www.fontsquirrel.com) y ponlas en `assets/fonts/`.

---

## Seguridad y hosting

Según tu estrategia editorial:

- **Dominio propio:** Compra `yopi.media` o `yopi.press` en Namecheap o Porkbun (fuera de El Salvador)
- **Hosting alternativo a GitHub:** Netlify o Cloudflare Pages (gratis, servidores en EE.UU./Europa)
- **Correo seguro:** ProtonMail para comunicaciones internas
- **No uses hosting .sv** para mantener el sitio fuera del alcance de órdenes administrativas locales

---

## Licencia editorial

El contenido editorial de YOPI se publica bajo licencia **Creative Commons BY-SA 4.0**  
(Atribución — CompartirIgual). El código del sitio es de uso libre.

---

*Hecho con barro y código desde El Salvador.*  
*La piel nueva sobre la vieja. — Xipe Tótec*
