# El Rincón Veggie

Sitio web de recetas vegetarianas, desarrollado como proyecto final del curso de Desarrollo Web de Coderhouse.

## Autora
Florencia Melina Francos

## Descripción
El Rincón Veggie reúne recetas vegetarianas simples y caseras, pensadas para el día a día, con ingredientes fáciles de conseguir. El sitio incluye desayunos, almuerzos, snacks y una sección personal donde se cuenta la historia detrás del proyecto.

## Tecnologías utilizadas
- HTML5
- SCSS (arquitectura con partials, variables, mixins, extend)
- Bootstrap 5.3.8
- Animate.css
- Git / GitHub

## Estructura del proyecto
```
├── index.html
├── styles.css
├── assets/
├── scss/
│   ├── main.scss
│   ├── base/
│   │   ├── _base.scss
│   │   └── _tipografias.scss
│   ├── components/
│   │   ├── _buttons.scss
│   │   └── _cards.scss
│   ├── layout/
│   │   ├── _footer.scss
│   │   ├── _header.scss
│   │   └── _nav.scss
│   └── utilities/
│       ├── _mixins.scss
│       └── _variables.scss
└── pages/
    ├── desayunos.html
    ├── almuerzos.html
    ├── snacks.html
    └── sobre-mi.html
```

## Páginas del sitio
- `index.html` — Inicio, con banner y categorías
- `pages/desayunos.html` — Desayunos y meriendas
- `pages/almuerzos.html` — Almuerzos y cenas
- `pages/snacks.html` — Snacks
- `pages/sobre-mi.html` — Historia personal de la autora

## Características del diseño
- **Mobile-first**: el layout base se apila al 100% del ancho, y escala hacia tablet y desktop mediante mixins de SCSS.
- **CSS Grid**, incluyendo `grid-template-areas` para organizar contenido con roles distintos (texto e imagen).
- **Flexbox** para centrado y distribución de elementos (navbar, footer).
- **Diseño fluido**: uso de `vw` para el banner, adaptándose de forma proporcional a distintos anchos de pantalla.
- **Operadores aritméticos de SASS** para calcular espaciados y tamaños a partir de variables base.

## SCSS avanzado
- **Arquitectura de partials**: organización en `base/`, `components/`, `layout/` y `utilities/`, importados desde `main.scss`.
- **Variables**: colores, tipografías y espaciados centralizados en `utilities/_variables.scss`.
- **Mixins con parámetros**: usados para los breakpoints responsive (`tabletUp`, `desktopUp`).
- **Extend con placeholders**: estilos compartidos entre tarjetas, habilidades y links (`%modogrilla`, `%modolinks`, `%modotarjetas`).
- **Nesting**: anidamiento de selectores para mantener el código organizado y legible.

## Animaciones
- **Animate.css**: animaciones de entrada aplicadas a títulos, texto e imágenes (`fadeInLeft`, `fadeInRight`, `bounceInDown`, `bounceInLeft`, entre otras).
- **@keyframes nativo**: animación propia (`pulsoHabilidad`) aplicada con `animation-name`.
- **Transiciones**: efecto de escala y torsión 3D al pasar el mouse sobre las tarjetas (`transition` + `transform`).

## SEO
- Cada página cuenta con `<title>`, `<meta description>` y `<meta keywords>` propios y descriptivos.
- Todas las imágenes incluyen atributos `alt` descriptivos.

## Cómo verlo
Abrí `index.html` en el navegador, o usá la extensión **Live Server** en VS Code para verlo con recarga automática.

Si querés modificar los estilos, corré el compilador de SCSS en modo watch:
```
npx sass --watch scss/main.scss:styles.css
```

vercel: https://coderhouse-entregafinal.vercel.app/index.html