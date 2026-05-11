# Guía práctica: cómo subir YOPI a GitHub Pages

Instrucciones paso a paso, sin asumir nada.

---

## Paso 1 — Instalar Git (si no lo tienes)

**Mac:**
```
brew install git
```
O descárgalo desde https://git-scm.com/download/mac

**Windows:**
Descarga desde https://git-scm.com/download/win e instala con todas las opciones por defecto.

Verifica que funciona:
```
git --version
```

---

## Paso 2 — Crear el repositorio en GitHub

1. Ve a https://github.com y entra a tu cuenta (o crea una)
2. Clic en el **+** arriba a la derecha → **New repository**
3. Nombre del repositorio: `yopi` (o `yopi-site`)
4. Selecciona **Public** (obligatorio para GitHub Pages gratis)
5. NO marques ningún checkbox (sin README, sin .gitignore)
6. Clic en **Create repository**
7. Copia la URL que aparece — se ve así:
   `https://github.com/TU-USUARIO/yopi.git`

---

## Paso 3 — Subir los archivos desde tu computadora

Abre la Terminal (Mac/Linux) o Git Bash (Windows).

```bash
# 1. Entra a la carpeta del sitio
cd ruta/a/yopi-site

# 2. Inicia Git en esa carpeta
git init

# 3. Agrega todos los archivos
git add .

# 4. Primer commit
git commit -m "Lanzamiento YOPI v1"

# 5. Conecta con GitHub (cambia la URL por la tuya)
git remote add origin https://github.com/TU-USUARIO/yopi.git

# 6. Sube todo
git branch -M main
git push -u origin main
```

Si te pide usuario y contraseña, usa tu usuario de GitHub y un **Personal Access Token** (no tu contraseña). Para crearlo: GitHub → Settings → Developer settings → Personal access tokens → Generate new token.

---

## Paso 4 — Activar GitHub Pages

1. Ve a tu repositorio en GitHub
2. Clic en **Settings** (la pestaña con el engranaje)
3. En el menú lateral izquierdo: **Pages**
4. En *Source*: selecciona **Deploy from a branch**
5. *Branch*: `main` | *Folder*: `/ (root)`
6. Clic en **Save**
7. Espera 1–2 minutos

Tu sitio estará en:
```
https://TU-USUARIO.github.io/yopi/
```

---

## Paso 5 — Actualizar el sitio cuando publiques nueva nota

```bash
# Dentro de la carpeta yopi-site:
git add .
git commit -m "Nueva nota: título de la nota"
git push
```

En 1–2 minutos los cambios aparecen en el sitio.

---

## Paso 6 — Conectar tu dominio propio (cuando estés listo)

1. Compra el dominio en **Namecheap** o **Porkbun** (fuera de El Salvador)
2. En tu repositorio: Settings → Pages → Custom domain
3. Escribe tu dominio: `yopi.press` o `yopi.media`
4. En tu proveedor de dominio, crea estos registros DNS:
   ```
   Tipo: A     Host: @    Valor: 185.199.108.153
   Tipo: A     Host: @    Valor: 185.199.109.153
   Tipo: A     Host: @    Valor: 185.199.110.153
   Tipo: A     Host: @    Valor: 185.199.111.153
   Tipo: CNAME Host: www  Valor: TU-USUARIO.github.io
   ```
5. Marca **Enforce HTTPS** en GitHub Pages
6. Espera hasta 48 horas para que el DNS se propague

---

## Cómo agregar tu primera fotografía real

1. Pon la foto en `assets/images/hero/` con el nombre `hero-01.jpg`
2. Abre `index.html` en un editor de texto (VSCode o Notepad++)
3. Busca: `.hero-image-frame::before`
4. Agrega esto dentro del CSS de esa regla:
   ```css
   background-image: url('assets/images/hero/hero-01.jpg');
   background-size: cover;
   background-position: center;
   ```
5. Guarda, haz commit y push

---

## Editor de texto recomendado

**Visual Studio Code** — gratuito  
https://code.visualstudio.com

Extensión útil: **Live Server** (para previsualizar el sitio localmente antes de subir)

---

*Cualquier duda, el archivo README.md tiene contexto adicional.*
