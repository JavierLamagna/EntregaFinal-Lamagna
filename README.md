# Proyecto Final — Desarrollo Web · CoderHouse

## Panadería Los 5 Hermanos

**Alumno:** Javier Lamagna  
**Curso:** Desarrollo Web — CoderHouse  
**Repositorio:** [EntregaFinal-Lamagna](https://github.com/JavierLamagna/EntregaFinal-Lamagna)

---

## Sitio en vivo (GitHub Pages)

El proyecto está desplegado y disponible para su evaluación en:

**[https://javierlamagna.github.io/EntregaFinal-Lamagna/](https://javierlamagna.github.io/EntregaFinal-Lamagna/)**

### Páginas del sitio

| Sección | Enlace directo |
|---|---|
| Historia (Inicio) | [index.html](https://javierlamagna.github.io/EntregaFinal-Lamagna/) |
| Elaboración | [elaboracion.html](https://javierlamagna.github.io/EntregaFinal-Lamagna/pages/elaboracion.html) |
| Productos | [productos.html](https://javierlamagna.github.io/EntregaFinal-Lamagna/pages/productos.html) |
| Nos encontrarás | [nos-encontraras.html](https://javierlamagna.github.io/EntregaFinal-Lamagna/pages/nos-encontraras.html) |
| Contactos | [contactos.html](https://javierlamagna.github.io/EntregaFinal-Lamagna/pages/contactos.html) |

---

## Descripción del proyecto

Sitio web institucional para **Panadería Los 5 Hermanos**, desarrollado como proyecto integrador del curso de Desarrollo Web. El sitio presenta la historia de la panadería, el proceso de elaboración artesanal, el catálogo de productos, la ubicación con mapa interactivo y un formulario de contacto.

El objetivo es ofrecer una experiencia clara, atractiva y accesible en dispositivos móviles, tablets y escritorio.

---

## Evidencias solicitadas en el enunciado

### 1. HTML semántico y estructura

- Uso de etiquetas semánticas: `header`, `nav`, `main`, `aside`, `section` y `footer`.
- Navegación consistente entre las 5 páginas del sitio.
- Contenido organizado por secciones con encabezados jerárquicos (`h2`, `h3`).
- Atributo `lang="es"` en todas las páginas.

**Archivos de referencia:** `index.html`, `pages/elaboracion.html`, `pages/productos.html`, `pages/nos-encontraras.html`, `pages/contactos.html`

---

### 2. SASS — preprocesador CSS

Se implementó una arquitectura modular con `@use` y archivos parciales:

| Técnica SASS | Implementación |
|---|---|
| **Variables** | `assets/scss/componentes/_variables.scss` — colores y fuentes (`$color-principal`, `$color-secundario`, `$fuente-texto`, `$fuente-titulos`) |
| **Mixins** | `assets/scss/componentes/_mixins.scss` — `flex-centro`, `titulo`, `parrafo`, `campo-formulario`, `boton` |
| **Extends** | Placeholder `%tarjeta` aplicado en `_contactos.scss` |
| **Anidaciones** | Selectores anidados en `style.scss` y parciales de páginas |
| **Módulos Sass** | `sass:color` con `color.adjust()` en mixin de botón |
| **Parciales por página** | `_productos.scss`, `_elaboracion.scss`, `_nos_encontraras.scss`, `_contactos.scss` |
| **Archivo principal** | `assets/scss/style.scss` importa todos los parciales y compila a `assets/css/style.css` |

**Compilación:**

```bash
npm install
npm run sass
```

---

### 3. Diseño responsive

- Media queries en `assets/scss/componentes/_responsive.scss`.
- Breakpoints: **768px** (tablets) y **480px** (móviles).
- Adaptación de navbar, galería de productos, carrusel, tarjetas, formulario, footer y mapa.
- Uso complementario de **Bootstrap 5.3.8** para el carrusel de elaboración y grilla responsive.

---

### 4. SEO (Search Engine Optimization)

En **todas las páginas** se incluyó:

- `<title>` descriptivo y único por sección.
- `<meta name="description">` y `<meta name="keywords">`.
- `<meta name="robots" content="index, follow">`.
- `<link rel="canonical">` con URL absoluta de GitHub Pages.
- Etiquetas **Open Graph** (`og:title`, `og:description`, `og:image`, `og:url`, `og:type`).
- Imágenes con atributo `alt` descriptivo.
- Formato optimizado en imágenes: `.webp`, `.avif` y `.jpg`.
- `loading="lazy"` en el iframe del mapa de Google Maps.

---

### 5. Accesibilidad

- `role="navigation"` y `aria-label` en la barra de navegación.
- `aria-current="page"` en el enlace de la página activa.
- `aria-label` en el formulario de contacto y en la galería de productos.
- Etiquetas `<label>` asociadas a cada campo del formulario (`for` + `id`).
- Atributos `aria-required="true"` en campos obligatorios.
- Textos alternativos en todas las imágenes del sitio.

---

### 6. Animaciones y transiciones

- Efecto `hover` con `transform: scale()` en enlaces del navbar, tarjetas de productos y footer.
- Transiciones en botones, inputs y campos del formulario (`transition: 0.3s`).
- Transición del carrusel de Bootstrap en la página de elaboración.
- Efecto hover en imágenes de la galería de productos.

---

### 7. Formulario de contacto

- Página `pages/contactos.html` con formulario funcional.
- Campos: nombre, email, teléfono y mensaje.
- Validación HTML5 con atributo `required` en campos obligatorios.
- Tipos de input semánticos: `text`, `email`, `tel`.
- Envío mediante `action="mailto:Panaderia5Hermanos@gmail.com"`.
- Estilos del formulario generados con mixins SASS (`campo-formulario`, `boton`).

---

### 8. Bootstrap

- Framework **Bootstrap 5.3.8** integrado vía CDN.
- Componente **Carousel** en la página de Elaboración (`data-bs-ride="carousel"`).
- Clases utilitarias de Bootstrap en imágenes del carrusel (`d-block w-100`).

---

### 9. Git y GitHub

- Control de versiones con Git.
- Código alojado en GitHub: [JavierLamagna/EntregaFinal-Lamagna](https://github.com/JavierLamagna/EntregaFinal-Lamagna).
- Historial de commits documentando avances del proyecto (SEO, responsive, accesibilidad, nueva página de elaboración).

---

### 10. Despliegue en GitHub Pages

**Configuración actual:**

| Parámetro | Valor |
|---|---|
| Fuente de publicación | Rama `main` |
| Carpeta de origen | `/` (raíz del repositorio) |
| URL pública | `https://javierlamagna.github.io/EntregaFinal-Lamagna/` |

**Pasos para verificar el despliegue (evaluador):**

1. Ir al repositorio en GitHub → **Settings** → **Pages**.
2. Confirmar que **Source** esté en `Deploy from a branch`.
3. Confirmar que la rama sea `main` y la carpeta `/ (root)`.
4. Acceder al sitio desde el enlace de la tabla superior.

---

## Estructura del proyecto

```
EntregaFinal-Lamagna/
├── index.html                      # Página principal — Historia
├── pages/
│   ├── elaboracion.html            # Proceso de elaboración + carrusel
│   ├── productos.html              # Catálogo y galería de productos
│   ├── nos-encontraras.html        # Mapa de ubicación
│   └── contactos.html              # Formulario de contacto
├── assets/
│   ├── css/
│   │   └── style.css               # CSS compilado desde SASS
│   ├── scss/
│   │   ├── style.scss              # Archivo principal SASS
│   │   ├── componentes/
│   │   │   ├── _variables.scss
│   │   │   ├── _mixins.scss
│   │   │   └── _responsive.scss
│   │   └── pages/
│   │       ├── _productos.scss
│   │       ├── _elaboracion.scss
│   │       ├── _nos_encontraras.scss
│   │       └── _contactos.scss
│   └── images/                     # Imágenes del sitio
├── package.json                    # Dependencias y script de SASS
└── README.md                       # Este documento
```

---

## Tecnologías utilizadas

- HTML5
- CSS3
- SASS (Dart Sass)
- Bootstrap 5.3.8
- Google Fonts (Poppins, Nunito)
- Git y GitHub
- GitHub Pages

---

## Instalación y ejecución local

```bash
# Clonar el repositorio
git clone https://github.com/JavierLamagna/EntregaFinal-Lamagna.git
cd EntregaFinal-Lamagna

# Instalar dependencias
npm install

# Compilar SASS (modo watch)
npm run sass
```

Abrir `index.html` en el navegador o usar una extensión como **Live Server** en VS Code.

---

## Wireframe de referencia

El archivo `wiframe.png` en la raíz del repositorio contiene el wireframe inicial del diseño del sitio.

---

## Autor

**Javier Lamagna** — Proyecto entregado para la cursada de Desarrollo Web en CoderHouse.
