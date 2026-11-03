# ⚽ Estadio 3D — Partido (Three-proyecto)

Proyecto web interactivo que combina un **juego de fútbol 3D en el navegador** construido con **Three.js** y un panel administrativo personalizado basado en **SB Admin 2 (Bootstrap 4)** con la misma paleta temática verde esmeralda.

---

## ✨ Características Principales

### 🎮 Juego 3D (`juego.html`)
- **Estadio 3D completo**: Cancha con franjas de césped, líneas reglamentarias, porterías con red, banderines de córner, gradas, vallas publicitarias, reflectores de estadio y marcador electrónico 3D en tiempo real.
- **Partido 1 vs 1 contra IA**: Juega con el dorsal `#10` contra un rival controlado por inteligencia artificial (`#7`) que persigue el balón, regatea y dispara a portería.
- **Física y mecánicas de juego**:
  - Gravedad, rebote y fricción del balón sobre el césped.
  - Conducción automática (dribbling) y disparo con elevación.
  - Sistema de resistencia (*stamina*) que se consume al esprintar y se regenera al caminar o detenerse.
  - Detección de goles (incluyendo goles en propia puerta), temporizador de partido (3 minutos) y efectos de sonido generados con **Web Audio API**.
- **Interfaz HUD**: Marcador superior, reloj del partido, barra de resistencia, guía de controles en pantalla y menú de pausa/fin de partido.

### 📊 Panel Administrativo (`startbootstrap-sb-admin-2/`)
- Plantilla **SB Admin 2** adaptada con una paleta de colores personalizada acorde al estadio (`#047857` Primary, `#16a34a` Success, `#0e7490` Info, `#e8b03a` Warning, `#dc4a42` Danger).
- Incluye vistas de dashboard, gráficas (`Chart.js`), tablas (`DataTables`), páginas de autenticación y utilidades SCSS/CSS.

---

## 🕹️ Controles del Juego

| Tecla / Entrada | Acción |
| :--- | :--- |
| `W` `A` `S` `D` / `Flechas` | Mover al futbolista |
| `Ratón` (arrastrar) | Girar la cámara en 3ª persona |
| `Clic izquierdo` o `E` | Patear el balón |
| `Shift` | Correr (consume resistencia) |
| `Espacio` | Saltar |
| `P` | Pausar / Reanudar el partido |
| `R` | Reiniciar el partido |

---

## 📁 Estructura del Proyecto

```text
Three-proyecto/
├── juego.html                     # Juego interactivo 3D de fútbol con Three.js
├── startbootstrap-sb-admin-2/     # Dashboard administrativo (Bootstrap 4 + SCSS)
│   ├── index.html                 # Panel principal del dashboard
│   ├── css/                       # Hojas de estilo compiladas
│   ├── js/                        # Scripts del tema y demos de gráficos
│   ├── scss/                      # Archivos fuente Sass personalizados
│   └── vendor/                    # Dependencias (Bootstrap, jQuery, Chart.js, FontAwesome)
└── README.md                      # Documentación del proyecto
```

---

## 🚀 Cómo Ejecutar el Proyecto

### 1. Jugar al Partido 3D
No requiere instalación de dependencias. Simplemente abre el archivo `juego.html` en cualquier navegador web moderno (Chrome, Firefox, Edge) o sírvelo con una extensión como **Live Server** en VS Code.

> **Nota:** Requiere conexión a internet para cargar `three.min.js` (r128) desde el CDN de Cloudflare.

### 2. Ver o Modificar el Dashboard (`startbootstrap-sb-admin-2`)
Para visualizar el panel administrativo, abre `startbootstrap-sb-admin-2/index.html` en tu navegador.

Si deseas recompilar los archivos **SCSS** o ejecutar el entorno de desarrollo con Gulp:

```bash
cd startbootstrap-sb-admin-2
npm install
npm start
```

---

## 🛠️ Tecnologías Utilizadas

- **[Three.js (r128)](https://threejs.org/)** — Renderizado WebGL 3D, luces, sombras y geometrías.
- **HTML5 Canvas & Web Audio API** — Texturas dinámicas en 3D (marcador, dorsales, vallas) y efectos de sonido sintetizados.
- **[Bootstrap 4](https://getbootstrap.com/) & [SB Admin 2](https://startbootstrap.com/theme/sb-admin-2)** — Estructura y estilos del panel de administración.
- **Sass (SCSS) & Gulp** — Personalización de estilos y flujo de compilación del dashboard.
