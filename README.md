# 🚀 UBERX — Space Travel App

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![BEM](https://img.shields.io/badge/BEM-Methodology-black?style=flat-square)
![Sin JavaScript](https://img.shields.io/badge/JavaScript-0%25-lightgrey?style=flat-square)

Aplicación web frontend de concepto que simula una plataforma de reservas de viajes espaciales al estilo Uber. Desarrollada íntegramente con **HTML5 y CSS3 puro**, sin ninguna dependencia de JavaScript ni librerías externas.

---

## 🌐 Vista previa

> 🔗 [Ver demo en GitHub Pages](https://alejandro0328.github.io/Paguina-CSS-HTML/) 

---

## 🛠️ Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| **HTML5** | Estructura semántica y navegación por `#anchors` |
| **CSS3** | Estilos, animaciones, layout y lógica de navegación vía `:target` |
| **BEM** | Metodología de nomenclatura para clases CSS |

---

## ✨ Características principales

- 🎯 **Navegación sin JavaScript** — Todas las transiciones entre pantallas se gestionan con `#anchors` y el pseudoselector CSS `:target`
- 📱 **Diseño mobile-first** — Optimizado para dispositivos móviles y centrado en desktop
- 🪐 **5 pantallas funcionales** — Splash, Home, Travel, Payments y Receipt
- 🎨 **CSS puro** — Sin frameworks, sin preprocesadores, sin dependencias externas
- ♿ **Accesibilidad básica** — Uso de `aria-label`, `aria-hidden`, roles semánticos y `role="list"`
- 🧩 **Metodología BEM** — Clases organizadas con convención Bloque__Elemento--Modificador

---

## 📁 Estructura del proyecto

```
uberx/
│
├── index.html               # Archivo principal — contiene todas las pantallas
│
├── css/
│   ├── app.css              # Estilos principales de la aplicación
│   └── utils.css            # Clases utilitarias y helpers
│
├── assets/
│   └── img/
│       ├── tierra.jpg
│       ├── marte.jpeg
│       ├── luna.jpg
│       └── station.jpeg
│
└── screens/                 # ⚠️ Solo referencia — NO funcionales
    ├── splash.html
    ├── home.html
    ├── travel.html
    ├── payments.html
    └── receipt.html
```

> **Nota:** La carpeta `screens/` contiene cada pantalla aislada únicamente con fines de estudio y referencia visual. El archivo funcional es exclusivamente `index.html`.

---

## ▶️ Cómo ejecutar el proyecto

No requiere instalación, servidor local ni dependencias.

**Opción 1 — Abrir directamente en el navegador:**
```
Doble clic sobre index.html
```

**Opción 2 — Con extensión Live Server (VS Code):**
1. Instalar la extensión [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
2. Clic derecho sobre `index.html` → `Open with Live Server`

---

## 🏗️ Arquitectura de navegación

La aplicación simula una SPA (Single Page Application) sin JavaScript, basándose en dos mecanismos nativos de HTML y CSS:

### `#anchors` + `:target`

Cada pantalla es una `<section>` con un `id` único dentro de `index.html`. La navegación funciona así:

```
Usuario hace clic en <a href="#travel">
       ↓
El navegador actualiza la URL → index.html#travel
       ↓
CSS aplica :target a la section con id="travel"
       ↓
Esa pantalla se hace visible; las demás se ocultan
```

**Ejemplo en CSS:**
```css
/* Por defecto todas las pantallas están ocultas */
.screen {
  display: none;
}

/* La pantalla activa se muestra al ser :target */
.screen:target {
  display: flex;
}

/* Excepción: splash se muestra por defecto */
.screen--active {
  display: flex;
}
```

### Inputs radio/checkbox para estado CSS

Algunos componentes interactivos (selector de naves, expansión del sheet) utilizan `<input type="radio">` y `<input type="checkbox">` ocultos como estado, combinados con el selector `~` (hermano general) en CSS para mostrar u ocultar contenido sin JavaScript.

---

## 📱 Responsividad

El diseño sigue el enfoque **mobile-first**:

- La maqueta base está diseñada para pantallas de **375–430 px** de ancho (smartphones)
- En desktop, el contenedor principal se centra horizontalmente simulando un dispositivo móvil
- No se utilizan frameworks de grid externos; el layout se construye con **Flexbox** nativo

---

## 🧩 Convenciones de código

### Nomenclatura BEM

Las clases CSS siguen estrictamente la metodología **BEM** (Block__Element--Modifier):

```
.home__banner-title        → Bloque: home / Elemento: banner-title
.screen--active            → Bloque: screen / Modificador: active
.loading__dot--delay-1     → Bloque: loading / Elemento: dot / Modificador: delay-1
```

### Organización CSS

| Archivo | Contenido |
|---|---|
| `css/app.css` | Estilos de cada pantalla y sus componentes, organizados por sección |
| `css/utils.css` | Clases de utilidad reutilizables (`.visually-hidden`, resets, etc.) |

### HTML semántico

Se utilizan etiquetas semánticas donde corresponde: `<header>`, `<nav>`, `<section>`, `<article>`, `<footer>`, `<time>`, `<dl>`, `<dt>`, `<dd>`.

---

## 📋 Pantallas del proyecto

| ID | Nombre | Descripción |
|---|---|---|
| `#splash` | Splash | Pantalla de bienvenida con animación de carga |
| `#home` | Inicio | Dashboard con destinos, buscador y acciones rápidas |
| `#travel` | Viajar | Mapa espacial + selector de naves + confirmación |
| `#payments` | Pagos | Listado de métodos de pago y selección |
| `#receipt` | Recibo | Resumen del vuelo reservado con detalles y acciones |

---

## 🚦 Estado del proyecto

```
Versión de concepto / UI prototype
```

- [x] Pantalla Splash
- [x] Pantalla Home
- [x] Pantalla Travel (selector de naves)
- [x] Pantalla Payments
- [x] Pantalla Receipt


---

## 👤 Autor

**Tu Nombre**
- GitHub: [@Alejandro0328](https://github.com/Alejandro0328)


---

> *Proyecto de práctica frontend. Diseño conceptual inspirado en apps de movilidad aplicadas al viaje espacial.*
