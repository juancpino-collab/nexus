# NEXUS GSS — Especificación Completa del Sitio Web
**Versión:** 1.0  
**Fecha:** 2026-09-01  
**Repositorio:** https://github.com/juancpino-collab/nexus.git  
**Publicación:** GitHub Pages (sitio completamente estático)  
**Idiomas:** Español (predeterminado) + Inglés (switcher JS en la misma página)  
**Autor de la especificación:** Proceso de diseño asistido por IA  

---

## TABLA DE CONTENIDOS

1. [Visión general y propósito](#1-visión-general-y-propósito)  
2. [Referentes visuales](#2-referentes-visuales)  
3. [Arquitectura de información](#3-arquitectura-de-información)  
4. [Identidad visual](#4-identidad-visual)  
5. [Sistema tipográfico](#5-sistema-tipográfico)  
6. [Sistema de componentes](#6-sistema-de-componentes)  
7. [Estructura de archivos](#7-estructura-de-archivos)  
8. [Especificación página a página](#8-especificación-página-a-página)  
   - 8.1 [index.html — Página principal](#81-indexhtml--página-principal)  
   - 8.2 [oficina-estrategica/index.html](#82-oficina-estrategicaindexhtml)  
   - 8.3 [areas/index.html](#83-areasindexhtml)  
   - 8.4 [contacto/index.html](#84-contactoindexhtml)  
9. [Sistema bilingüe](#9-sistema-bilingüe)  
10. [Imágenes y medios](#10-imágenes-y-medios)  
11. [SEO y metadatos](#11-seo-y-metadatos)  
12. [Accesibilidad](#12-accesibilidad)  
13. [Comportamiento responsive](#13-comportamiento-responsive)  
14. [Despliegue en GitHub Pages](#14-despliegue-en-github-pages)  
15. [Criterios de aceptación](#15-criterios-de-aceptación)  

---

## 1. VISIÓN GENERAL Y PROPÓSITO

### Descripción de la empresa
**NEXUS GSS — Governance and Sustainable Solutions** (en español: Soluciones de Gobernanza y Sostenibilidad) es una firma consultora colombiana especializada en el diseño, formulación y estructuración de proyectos ambientales y de desarrollo territorial. Opera en la intersección de gobernanza, sostenibilidad, cambio climático, biodiversidad y fortalecimiento institucional, con énfasis en el Caribe colombiano y América Latina.

### Propósito del sitio web
- Establecer la presencia digital institucional de NEXUS GSS ante clientes potenciales (gobiernos, cooperación internacional, fundaciones, ONG, empresas).
- Comunicar la propuesta de valor diferencial: empresa nueva construida sobre décadas de experiencia real.
- Presentar sus líneas de servicio, enfoque metodológico y equipo fundador.
- Generar contacto cualificado a través de tres puertas de entrada diferenciadas.

### Audiencia objetivo
| Audiencia | Interés principal |
|-----------|-----------------|
| Gobiernos y entidades territoriales | Proyectos, cartera, planificación |
| Cooperación internacional y financiadores | Credenciales, enfoque, áreas temáticas |
| Autoridades ambientales | Servicios técnicos especializados |
| ONG y fundaciones | Alianzas, formulación de proyectos |
| Empresas privadas | Consultoría técnica |
| Universidades y centros de conocimiento | Investigación aplicada |

### Tono de comunicación
- **Profesional pero cálido:** No corporativo frío; tampoco informal.
- **Técnico pero accesible:** Expertise visible sin jerga innecesaria.
- **Optimista y propositivo:** Transforma desafíos en oportunidades.
- **Territorialmente anclado:** Énfasis en lo real, lo local, lo concreto.

---

## 2. REFERENTES VISUALES

Los siguientes sitios orientan las decisiones de diseño. No se trata de copiar sino de capturar el nivel de sofisticación buscado:

| Referente | URL | Qué tomar de referencia |
|-----------|-----|------------------------|
| World Resources Institute | wri.org | Estructura limpia, autoridad institucional, uso de datos, paleta azul/verde |
| Systemiq | systemiq.earth | Consultoría de impacto moderna, tipografía grande y bold, secciones con contraste |
| Conservation International | conservation.org | Imágenes territoriales inmersivas, storytelling visual |
| GIZ (Alemania) | giz.de | Rigor institucional bilingüe, navegación clara |
| IDOM | idom.com | Firma consultora técnica, presentación de proyectos, perfiles de equipo |

**Síntesis de dirección estética:** Firmeza institucional (WRI/GIZ) + narrativa territorial visual (Conservation International) + modernidad de consultoría de impacto (Systemiq). Resultado: elegante, limpio, con peso visual en grandes titulares y fuerte uso de la paleta extraída del logo.

---

## 3. ARQUITECTURA DE INFORMACIÓN

### Estructura de páginas

```
nexus-gss (raíz del repositorio)
├── index.html                    ← Página principal (scroll largo)
├── oficina-estrategica/
│   └── index.html                ← Subpágina: Oficina Estratégica de Proyectos
├── areas/
│   └── index.html                ← Subpágina: Áreas temáticas de trabajo
├── contacto/
│   └── index.html                ← Subpágina: Contacto
├── assets/
│   ├── css/
│   │   ├── main.css              ← Estilos globales + tokens de diseño
│   │   └── components.css        ← Estilos de componentes reutilizables
│   ├── js/
│   │   ├── main.js               ← Lógica global (navbar, lang switcher, scroll)
│   │   └── lang.js               ← Diccionario bilingüe y lógica de idioma
│   └── images/
│       ├── logo/
│       │   ├── nexus-gss-logo.png          ← Logo color (para fondos claros)
│       │   └── nexus-gss-logo-white.png    ← Logo blanco (para fondos oscuros)
│       ├── hero/
│       │   └── hero-bg.jpg                 ← [PLACEHOLDER] Imagen hero principal
│       ├── team/
│       │   ├── juan-carlos-pino.jpg        ← [PLACEHOLDER] Foto perfil
│       │   ├── carol-sierra.jpg            ← [PLACEHOLDER] Foto perfil
│       │   ├── walter-gil.jpg              ← [PLACEHOLDER] Foto perfil
│       │   └── gleirys-amaya.jpg           ← [PLACEHOLDER] Foto perfil
│       ├── territory/
│       │   ├── territory-01.jpg            ← [PLACEHOLDER] Paisaje/comunidad 1
│       │   ├── territory-02.jpg            ← [PLACEHOLDER] Paisaje/comunidad 2
│       │   └── territory-03.jpg            ← [PLACEHOLDER] Paisaje/comunidad 3
│       └── areas/
│           ├── agua-cuencas.jpg            ← [PLACEHOLDER] Imagen área temática
│           ├── mares-costas.jpg
│           ├── biodiversidad.jpg
│           ├── cambio-climatico.jpg
│           ├── desarrollo-territorial.jpg
│           ├── gobernanza.jpg
│           ├── educacion-innovacion.jpg
│           └── desarrollo-comunitario.jpg
├── _config.yml                   ← Configuración GitHub Pages
└── README.md                     ← Documentación del repositorio
```

### Navegación principal (navbar)

| Ítem ES | Ítem EN | Destino |
|---------|---------|---------|
| Inicio | Home | index.html |
| Qué hacemos | What we do | index.html#servicios |
| Oficina Estratégica | Strategic Office | /oficina-estrategica/ |
| Áreas | Areas | /areas/ |
| Equipo | Team | index.html#equipo |
| Contacto | Contact | /contacto/ |
| [ES / EN] | [ES / EN] | Switcher de idioma (JS) |

### Secciones de la página principal (index.html)

La página principal es un scroll narrativo continuo con anclas:

| ID de ancla | Sección ES | Sección EN |
|-------------|-----------|-----------|
| `#hero` | Hero / Tagline | Hero / Tagline |
| `#que-es` | ¿Qué es NEXUS? | What is NEXUS? |
| `#servicios` | Qué hacemos | What we do |
| `#enfoque` | Nuestro enfoque | Our approach |
| `#como-trabajamos` | Cómo trabajamos | How we work |
| `#tecnologia` | Tecnología e inteligencia | Technology & intelligence |
| `#para-quien` | Para quién trabajamos | Who we serve |
| `#iniciativas` | Iniciativas en desarrollo | Initiatives in development |
| `#equipo` | Quiénes somos | About us |
| `#caribe` | El Caribe como origen | The Caribbean: our roots |
| `#contacto-home` | Contacto (teaser) | Contact (teaser) |

---

## 4. IDENTIDAD VISUAL

### Paleta de colores

Extraída del logo original del cliente y refinada para uso web.

```css
:root {
  /* Colores primarios */
  --color-primary:      #003C5A;   /* Azul océano profundo — color dominante del logo */
  --color-primary-dark: #002840;   /* Variante más oscura para hover/énfasis */
  --color-primary-mid:  #00607A;   /* Azul teal — color secundario del logo */

  /* Colores de acento (verde) */
  --color-accent:       #5AB41E;   /* Verde vivo — acento energético del logo */
  --color-accent-dark:  #3C8A1A;   /* Verde bosque — apoyo y profundidad */

  /* Neutros */
  --color-dark:         #0D1B2A;   /* Casi negro — texto principal */
  --color-gray-700:     #374151;   /* Texto secundario */
  --color-gray-400:     #9CA3AF;   /* Texto deshabilitado / captions */
  --color-gray-200:     #E5E7EB;   /* Bordes / separadores */
  --color-gray-100:     #F3F4F6;   /* Fondos alternos claros */
  --color-bg:           #F5F8FA;   /* Fondo base del sitio */
  --color-white:        #FFFFFF;   /* Blanco puro */

  /* Usos semánticos */
  --color-text:         var(--color-dark);
  --color-text-muted:   var(--color-gray-700);
  --color-link:         var(--color-primary-mid);
  --color-link-hover:   var(--color-accent-dark);
  --color-border:       var(--color-gray-200);
  --color-surface:      var(--color-white);
  --color-surface-alt:  var(--color-gray-100);
}
```

### Uso de la paleta por sección

| Sección | Fondo | Texto | Acento |
|---------|-------|-------|--------|
| Navbar (scroll) | `--color-white` | `--color-dark` | `--color-accent` |
| Navbar (top) | Transparente sobre hero | Blanco | `--color-accent` |
| Hero | `--color-primary` (con imagen overlay) | Blanco | `--color-accent` |
| ¿Qué es NEXUS? | `--color-white` | `--color-dark` | `--color-primary` |
| Qué hacemos | `--color-primary` | Blanco | `--color-accent` |
| Oficina Estratégica (teaser) | `--color-accent` | Blanco | `--color-white` |
| Nuestro enfoque | `--color-bg` | `--color-dark` | `--color-primary` |
| Cómo trabajamos | `--color-white` | `--color-dark` | `--color-primary-mid` |
| Tecnología | `--color-primary-dark` | Blanco | `--color-accent` |
| Para quién | `--color-bg` | `--color-dark` | `--color-primary` |
| Iniciativas | `--color-white` | `--color-dark` | `--color-primary-mid` |
| Equipo | `--color-primary` | Blanco | `--color-accent` |
| El Caribe | Imagen con overlay `--color-primary` 70% | Blanco | `--color-accent` |
| Footer | `--color-primary-dark` | Blanco / gray-400 | `--color-accent` |

---

## 5. SISTEMA TIPOGRÁFICO

### Fuentes

```html
<!-- En el <head> de todas las páginas -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
```

```css
:root {
  --font-heading: 'Montserrat', system-ui, -apple-system, sans-serif;
  --font-body:    'Inter', system-ui, -apple-system, sans-serif;
}
```

**Justificación:** Montserrat aporta autoridad institucional con sus trazos geométricos Bold/ExtraBold, adecuado para grandes titulares de impacto. Inter es la tipografía de cuerpo más legible en pantalla, usada por firmas líderes como Linear, Vercel y Notion.

### Escala tipográfica

```css
:root {
  /* Tamaños base (mobile first) */
  --text-xs:   0.75rem;   /*  12px */
  --text-sm:   0.875rem;  /*  14px */
  --text-base: 1rem;      /*  16px */
  --text-lg:   1.125rem;  /*  18px */
  --text-xl:   1.25rem;   /*  20px */
  --text-2xl:  1.5rem;    /*  24px */
  --text-3xl:  1.875rem;  /*  30px */
  --text-4xl:  2.25rem;   /*  36px */
  --text-5xl:  3rem;      /*  48px */
  --text-6xl:  3.75rem;   /*  60px */
  --text-7xl:  4.5rem;    /*  72px */
}

/* Uso por elemento */
h1 { font-family: var(--font-heading); font-size: var(--text-5xl); font-weight: 800; line-height: 1.1; }
h2 { font-family: var(--font-heading); font-size: var(--text-4xl); font-weight: 700; line-height: 1.2; }
h3 { font-family: var(--font-heading); font-size: var(--text-2xl); font-weight: 700; line-height: 1.3; }
h4 { font-family: var(--font-heading); font-size: var(--text-xl);  font-weight: 600; line-height: 1.4; }
p  { font-family: var(--font-body);    font-size: var(--text-base); line-height: 1.7; }
.lead { font-size: var(--text-xl); font-weight: 400; line-height: 1.6; }
.caption { font-size: var(--text-sm); color: var(--color-gray-400); }
.label-tag { font-size: var(--text-xs); font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; }

/* Responsive: en desktop los h1 escalan */
@media (min-width: 1024px) {
  h1 { font-size: var(--text-7xl); }
  h2 { font-size: var(--text-5xl); }
}
```

---

## 6. SISTEMA DE COMPONENTES

### 6.1 Navbar

**Comportamiento:**
- Posición: `fixed` en la parte superior, `z-index: 1000`.
- Estado inicial (sobre hero): fondo transparente, texto blanco.
- Al hacer scroll > 80px: transición suave a fondo `--color-white` con sombra `box-shadow: 0 2px 20px rgba(0,0,0,0.08)`.
- Logo: a la izquierda. Al lado en fondos oscuros, usar `nexus-gss-logo-white.png`. En fondo blanco, usar `nexus-gss-logo.png`.
- Links de navegación: `font-family: var(--font-heading); font-size: var(--text-sm); font-weight: 600; text-transform: uppercase; letter-spacing: 0.05em;`
- El ítem activo recibe `border-bottom: 2px solid var(--color-accent)`.
- Language switcher: botón tipo pill `[ES / EN]` en el extremo derecho. El idioma activo va en `font-weight: 700` y el inactivo en `color: var(--color-gray-400)`.
- Mobile: hamburger menu (≤768px). Al abrir, menú desplegable full-width con fondo `--color-primary` y texto blanco.

```html
<!-- Estructura HTML del navbar -->
<nav id="main-nav" class="navbar">
  <div class="nav-container">
    <a href="/" class="nav-logo">
      <img src="/assets/images/logo/nexus-gss-logo.png" 
           id="nav-logo-img" alt="NEXUS GSS" height="48">
    </a>
    <button class="nav-hamburger" aria-label="Menú" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
    <ul class="nav-links">
      <li><a href="/#servicios" data-i18n="nav.services">Qué hacemos</a></li>
      <li><a href="/oficina-estrategica/" data-i18n="nav.office">Oficina Estratégica</a></li>
      <li><a href="/areas/" data-i18n="nav.areas">Áreas</a></li>
      <li><a href="/#equipo" data-i18n="nav.team">Equipo</a></li>
      <li><a href="/contacto/" data-i18n="nav.contact">Contacto</a></li>
      <li class="lang-switcher">
        <button id="lang-btn" onclick="toggleLang()">
          <span id="lang-es" class="lang-active">ES</span>
          <span class="lang-sep">/</span>
          <span id="lang-en">EN</span>
        </button>
      </li>
    </ul>
  </div>
</nav>
```

### 6.2 Hero Section

**Estructura visual:**
- Fondo: imagen `hero-bg.jpg` (placeholder: vista aérea de territorio costero o de cuenca hídrica colombiana) con overlay `background: linear-gradient(135deg, rgba(0,60,90,0.85) 0%, rgba(0,40,64,0.75) 100%)`.
- Altura: `min-height: 100vh`.
- Contenido centrado horizontalmente, alineado a la izquierda, posicionado en el tercio inferior-izquierdo del viewport.
- Animación de entrada: fade-in + slide-up (0.3s delay escalonado entre elementos).

**Contenido del hero:**

```
[LABEL TAG — acento verde]
ES: NEXUS GSS · Gobernanza y Sostenibilidad
EN: NEXUS GSS · Governance and Sustainability

[H1 — blanco, peso 800]
ES: Transformamos desafíos territoriales en soluciones que pueden hacerse realidad.
EN: We transform territorial challenges into solutions that can become reality.

[LEAD PARAGRAPH — blanco 90% opacidad]
ES: Integramos conocimiento, territorio, información, financiación y capacidades institucionales para diseñar y desarrollar soluciones ambientales y de desarrollo sostenible.
EN: We integrate knowledge, territory, information, financing, and institutional capacities to design and develop environmental and sustainable development solutions.

[BOTONES CTA — en fila]
Botón primario (fondo --color-accent, texto blanco):
  ES: Desarrollar un proyecto
  EN: Develop a project
  href: /contacto/?tipo=proyecto

Botón secundario (borde blanco, texto blanco, hover: fondo blanco texto --color-primary):
  ES: Conocer nuestras soluciones
  EN: Explore our solutions
  href: /#servicios

[SCROLL INDICATOR — abajo centrado]
Ícono de flecha animada (bounce) apuntando hacia abajo.
```

### 6.3 Section Template (patrón reutilizable)

Todas las secciones siguen esta estructura base:

```html
<section id="[ancla]" class="section section--[variante]">
  <div class="container">
    <div class="section-header">
      <span class="label-tag" data-i18n="[clave].tag">ETIQUETA</span>
      <h2 data-i18n="[clave].title">Título de sección</h2>
      <p class="lead" data-i18n="[clave].subtitle">Subtítulo o bajada.</p>
    </div>
    <div class="section-body">
      <!-- Contenido específico -->
    </div>
  </div>
</section>
```

**Variantes de sección:**
- `.section--light`: fondo `--color-white`
- `.section--alt`: fondo `--color-bg` (gris muy suave)
- `.section--dark`: fondo `--color-primary`, texto blanco
- `.section--accent`: fondo `--color-accent`, texto blanco
- `.section--image`: background-image con overlay oscuro, texto blanco

**Espaciado de sección:**
```css
.section { padding: 6rem 0; }
@media (max-width: 768px) { .section { padding: 4rem 0; } }
.container { max-width: 1200px; margin: 0 auto; padding: 0 2rem; }
.section-header { max-width: 720px; margin-bottom: 4rem; }
.label-tag { color: var(--color-accent); margin-bottom: 1rem; display: block; }
```

### 6.4 Service Card (tarjeta de servicio)

Usada en la sección "Qué hacemos" (4 líneas de servicio).

```html
<div class="service-card">
  <div class="service-number">01</div>
  <h3 class="service-title" data-i18n="services.s1.title">Desarrollo de proyectos</h3>
  <p class="service-desc" data-i18n="services.s1.desc">
    Transformamos necesidades, oportunidades e ideas en proyectos estructurados...
  </p>
  <ul class="service-tags">
    <li>Diagnóstico</li>
    <li>Formulación</li>
    <li>Teoría del cambio</li>
    <li>Indicadores</li>
    <li>Presupuestos</li>
  </ul>
</div>
```

**Estilo del service card:**
- Fondo: transparente (sobre fondo `--color-primary`)
- Borde izquierdo: `4px solid var(--color-accent)`
- Número: `font-size: var(--text-6xl); font-weight: 800; color: rgba(255,255,255,0.1);` (grande y fantasmal, esquina superior derecha)
- Tags: pequeñas píldoras con borde `1px solid rgba(90,180,30,0.4)`, texto `--color-accent`, `font-size: var(--text-xs)`
- Layout en desktop: grid 2×2. En mobile: stack vertical.
- Hover: `border-color` pasa a `--color-accent` a full opacity, leve `translateY(-4px)`.

### 6.5 Process Step (paso del proceso)

Usado en "Cómo trabajamos" (6 pasos).

```html
<div class="process-step">
  <div class="process-icon">
    <span class="process-num">01</span>
  </div>
  <div class="process-content">
    <h4 data-i18n="process.s1.title">Comprender</h4>
    <p data-i18n="process.s1.desc">Territorio · problema · actores · información · antecedentes.</p>
  </div>
  <div class="process-connector" aria-hidden="true"></div>
</div>
```

**Estilo:** Layout horizontal en desktop (6 columnas), vertical en mobile. Cada paso conectado por una línea punteada `--color-gray-200`. El número en círculo `--color-primary`. Hover: número cambia a `--color-accent`.

### 6.6 Team Card (tarjeta de integrante)

```html
<div class="team-card">
  <div class="team-photo">
    <img src="/assets/images/team/juan-carlos-pino.jpg" 
         alt="Juan Carlos Pino Renjifo" loading="lazy">
    <!-- PLACEHOLDER: si no hay foto, mostrar iniciales sobre fondo --color-primary-mid -->
  </div>
  <div class="team-info">
    <h3 class="team-name">Juan Carlos Pino Renjifo</h3>
    <p class="team-role" data-i18n="team.jcp.role">Socio fundador · Director Técnico y de Estrategia</p>
    <p class="team-credentials">Biólogo Marino · Esp. Administración Ambiental Zonas Costeras</p>
    <p class="team-bio" data-i18n="team.jcp.bio">Más de 31 años de experiencia en gestión ambiental...</p>
    <div class="team-tags">
      <span>visión sistémica</span>
      <span>gobernanza</span>
      <span>desarrollo de proyectos</span>
      <span>conocimiento territorial</span>
    </div>
  </div>
</div>
```

**Layout:** Grid de 2 columnas en desktop (foto izq, info der). Stack vertical en mobile. Foto: círculo o cuadrado con border-radius: 12px, aspect-ratio 1:1, `object-fit: cover`. Fondo de sección: `--color-primary`.

### 6.7 Área Temática Card

Usada en `/areas/index.html`. Grid 4×2.

```html
<a href="#agua-cuencas" class="area-card">
  <div class="area-image">
    <img src="/assets/images/areas/agua-cuencas.jpg" alt="Agua y cuencas" loading="lazy">
    <div class="area-overlay"></div>
  </div>
  <div class="area-content">
    <h3 data-i18n="areas.water.title">Agua y cuencas</h3>
    <p data-i18n="areas.water.desc">Breve descripción del área.</p>
  </div>
</a>
```

**Estilo:** Imagen de fondo con overlay gradiente `--color-primary` al 60%. Texto blanco sobre imagen. Hover: overlay reduce a 40%, imagen hace ligero zoom (transform: scale(1.05)).

### 6.8 CTA Banner (Oficina Estratégica teaser)

Banner de transición entre secciones. Fondo `--color-accent`.

```html
<section class="cta-banner section--accent">
  <div class="container">
    <div class="cta-content">
      <h2 data-i18n="office.cta.title">
        Su organización conserva las decisiones. NEXUS aporta capacidad para convertirlas en proyectos.
      </h2>
      <a href="/oficina-estrategica/" class="btn btn--white" data-i18n="office.cta.btn">
        Conocer la Oficina Estratégica de Proyectos →
      </a>
    </div>
  </div>
</section>
```

### 6.9 Footer

```html
<footer class="site-footer">
  <div class="container">
    <div class="footer-grid">
      <!-- Col 1: Logo + tagline -->
      <div class="footer-brand">
        <img src="/assets/images/logo/nexus-gss-logo-white.png" alt="NEXUS GSS" height="48">
        <p data-i18n="footer.tagline">
          Transformamos desafíos territoriales en soluciones que pueden hacerse realidad.
        </p>
        <a href="https://www.linkedin.com/in/nexus-gss-governance-and-sustainability-solutions-a768623a8" 
           target="_blank" rel="noopener" class="social-link" aria-label="LinkedIn">
          [ícono LinkedIn SVG inline]
        </a>
      </div>
      <!-- Col 2: Navegación -->
      <div class="footer-nav">
        <h4 data-i18n="footer.nav.title">Navegación</h4>
        <ul>
          <li><a href="/#servicios" data-i18n="nav.services">Qué hacemos</a></li>
          <li><a href="/oficina-estrategica/" data-i18n="nav.office">Oficina Estratégica</a></li>
          <li><a href="/areas/" data-i18n="nav.areas">Áreas</a></li>
          <li><a href="/#equipo" data-i18n="nav.team">Equipo</a></li>
          <li><a href="/contacto/" data-i18n="nav.contact">Contacto</a></li>
        </ul>
      </div>
      <!-- Col 3: Contacto -->
      <div class="footer-contact">
        <h4 data-i18n="footer.contact.title">Contacto</h4>
        <p>
          <a href="mailto:info@nexusgss.co">info@nexusgss.co</a>
        </p>
        <p data-i18n="footer.location">Caribe colombiano · Colombia</p>
      </div>
    </div>
    <div class="footer-bottom">
      <p>&copy; 2026 NEXUS GSS — Governance and Sustainable Solutions. 
         <span data-i18n="footer.rights">Todos los derechos reservados.</span>
      </p>
    </div>
  </div>
</footer>
```

**Nota sobre el email:** `info@nexusgss.co` es un email a confirmar / reemplazar con el email real de la empresa.

---

## 8. ESPECIFICACIÓN PÁGINA A PÁGINA

### 8.1 `index.html` — Página principal

**`<head>` requerido:**
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NEXUS GSS — Gobernanza y Soluciones Sostenibles | Colombia</title>
<meta name="description" content="Firma especializada en diseño, formulación y estructuración de proyectos ambientales y de desarrollo territorial en Colombia y América Latina.">
<meta property="og:title" content="NEXUS GSS — Gobernanza y Soluciones Sostenibles">
<meta property="og:description" content="Transformamos desafíos territoriales en soluciones que pueden hacerse realidad.">
<meta property="og:image" content="/assets/images/hero/hero-bg.jpg">
<meta property="og:type" content="website">
<link rel="canonical" href="https://[dominio-final]/">
<link rel="icon" type="image/png" href="/assets/images/logo/nexus-gss-logo.png">
<link rel="stylesheet" href="/assets/css/main.css">
<link rel="stylesheet" href="/assets/css/components.css">
```

---

#### SECCIÓN 1: HERO (`#hero`)
*(Ver especificación del componente Hero en §6.2)*

---

#### SECCIÓN 2: ¿QUÉ ES NEXUS? (`#que-es`)
**Variante:** `.section--light`  
**Layout:** Dos columnas en desktop (60% texto / 40% imagen). Una columna en mobile.

**Contenido:**

```
[LABEL TAG]
ES: Una nueva manera de desarrollar soluciones territoriales
EN: A new way to develop territorial solutions

[H2]
ES: ¿Qué es NEXUS?
EN: What is NEXUS?

[PÁRRAFO]
ES: NEXUS GSS — Soluciones de Gobernanza y Sostenibilidad — nace para responder a una dificultad recurrente: territorios y organizaciones poseen necesidades, oportunidades y buenas ideas que muchas veces no logran convertirse en soluciones estructuradas, financiables y ejecutables.

EN: NEXUS GSS — Governance and Sustainable Solutions — was created to address a recurring challenge: territories and organizations have needs, opportunities, and good ideas that often fail to become structured, financeable, and executable solutions.

[PÁRRAFO 2]
ES: Integramos experiencia profesional, conocimiento territorial, análisis espacial, metodologías de planificación y desarrollo de proyectos e inteligencia artificial para cerrar esa brecha. Nuestro enfoque combina visión estratégica y capacidad técnica con una estructura flexible de especialistas que se conforma según las características de cada desafío.

EN: We integrate professional expertise, territorial knowledge, spatial analysis, planning methodologies, project development, and artificial intelligence to close that gap. Our approach combines strategic vision and technical capacity with a flexible structure of specialists configured according to each challenge's characteristics.

[PÁRRAFO DESTACADO — frase en grande, peso 700]
ES: NEXUS busca traducir agendas de sostenibilidad en soluciones accionables basadas en el territorio.
EN: NEXUS translates sustainability agendas into actionable, territory-based solutions.

[IMAGEN columna derecha — PLACEHOLDER]
Fotografía: equipo trabajando en campo / revisando mapas / reunión con comunidad.
Alt text ES: "Equipo NEXUS trabajando en territorio"
Alt text EN: "NEXUS team working in the field"
aspect-ratio: 4/5, border-radius: 16px, object-fit: cover
```

---

#### SECCIÓN 3: QUÉ HACEMOS (`#servicios`)
**Variante:** `.section--dark` (fondo `--color-primary`)  
**Layout:** Grid 2×2 de service cards (ver §6.4).

**Contenido de las 4 service cards:**

```
[CARD 01]
ES: Desarrollo de proyectos
EN: Project development
ES desc: Transformamos necesidades, oportunidades e ideas en proyectos estructurados, financiables y ejecutables.
EN desc: We transform needs, opportunities, and ideas into structured, financeable, and executable projects.
Tags ES: Diagnóstico · Diseño de soluciones · Formulación · Teoría del cambio · Marco lógico · Indicadores · Presupuestos · Perfiles de propuesta
Tags EN: Diagnosis · Solution design · Formulation · Theory of change · Logical framework · Indicators · Budgets · Proposal profiles

[CARD 02]
ES: Desarrollo y gestión de carteras de proyectos
EN: Project portfolio development & management
ES desc: Ayudamos a organizaciones que manejan múltiples iniciativas a convertirlas en una cartera priorizada y gestionable.
EN desc: We help organizations managing multiple initiatives turn them into a prioritized, manageable portfolio.
Tags ES: Identificación · Evaluación de madurez · Priorización · Estructuración · Pipeline · Seguimiento
Tags EN: Identification · Maturity assessment · Prioritization · Structuring · Pipeline · Monitoring

[CARD 03]
ES: Inteligencia territorial
EN: Territorial intelligence
ES desc: Integramos información ambiental, social, económica, institucional y espacial para comprender territorios y orientar decisiones.
EN desc: We integrate environmental, social, economic, institutional, and spatial information to understand territories and guide decisions.
Tags ES: SIG · Análisis territorial · Actores · Conflictos · Oportunidades · Escenarios · Soporte a decisiones
Tags EN: GIS · Territorial analysis · Stakeholders · Conflicts · Opportunities · Scenarios · Decision support

[CARD 04]
ES: Financiación y cooperación
EN: Financing & cooperation
ES desc: Ayudamos a relacionar proyectos con las fuentes de recursos adecuadas en Colombia y el mundo.
EN desc: We help match projects with the right funding sources in Colombia and around the world.
Tags ES: Mapeo de financiación · Cooperación internacional · Fondos climáticos · Inversión pública · Adaptación de propuestas
Tags EN: Financing mapping · International cooperation · Climate funds · Public investment · Proposal adaptation
```

---

#### SECCIÓN 4: CTA BANNER — OFICINA ESTRATÉGICA
*(Ver especificación §6.8)*

---

#### SECCIÓN 5: NUESTRO ENFOQUE (`#enfoque`)
**Variante:** `.section--alt`  
**Layout:** Header centrado + grid de 5 tarjetas de principios (en desktop: fila de 5; en tablet: 3+2; en mobile: 1 columna).

**Contenido:**

```
[LABEL TAG]
ES: Cómo pensamos
EN: How we think

[H2]
ES: Pensamos integralmente. Actuamos sistemáticamente.
EN: We think holistically. We act systematically.

[5 PRINCIPIOS — cards con ícono SVG + título + descripción corta]

Principio 1:
  ES título: Territorio
  EN título: Territory
  ES desc: Las soluciones se construyen entendiendo las condiciones reales donde deben funcionar.
  EN desc: Solutions are built by understanding the real conditions where they must work.
  Ícono: mapa / topografía

Principio 2:
  ES título: Integralidad
  EN título: Holism
  ES desc: Los problemas ambientales y de desarrollo rara vez pertenecen a una sola disciplina.
  EN desc: Environmental and development problems rarely belong to a single discipline.
  Ícono: nodos conectados / red

Principio 3:
  ES título: Gobernanza
  EN título: Governance
  ES desc: Las instituciones, comunidades y actores forman parte de la solución.
  EN desc: Institutions, communities, and stakeholders are part of the solution.
  Ícono: personas / red de actores

Principio 4:
  ES título: Financiabilidad
  EN título: Financeability
  ES desc: Un buen proyecto debe concebir desde el comienzo cómo podrá ejecutarse y sostenerse.
  EN desc: A good project must conceive from the start how it will be implemented and sustained.
  Ícono: flujo de recursos / moneda

Principio 5:
  ES título: Aprendizaje
  EN título: Learning
  ES desc: La información generada por cada proyecto debe mejorar las decisiones siguientes.
  EN desc: Information generated by each project must improve future decisions.
  Ícono: ciclo / flecha circular
```

---

#### SECCIÓN 6: CÓMO TRABAJAMOS (`#como-trabajamos`)
**Variante:** `.section--light`  
**Layout:** Header + línea de proceso horizontal con 6 pasos (ver §6.5). En mobile: acordeón vertical.

**Contenido:**

```
[LABEL TAG]
ES: Proceso
EN: Process

[H2]
ES: Un proceso continuo desde el desafío hasta la implementación
EN: A continuous process from challenge to implementation

[6 PASOS]

01 Comprender / Understand
ES: Territorio · problema · actores · información · antecedentes.
EN: Territory · problem · stakeholders · information · background.

02 Diagnosticar / Diagnose
ES: Causas · restricciones · capacidades · oportunidades.
EN: Causes · constraints · capacities · opportunities.

03 Diseñar / Design
ES: Alternativas · objetivos · intervención · resultados.
EN: Alternatives · objectives · intervention · outcomes.

04 Estructurar / Structure
ES: Actividades · productos · indicadores · presupuesto · SIG · requisitos.
EN: Activities · outputs · indicators · budget · GIS · requirements.

05 Financiar / Finance
ES: Fuentes · compatibilidad · propuestas · ruta de acceso.
EN: Sources · compatibility · proposals · access route.

06 Acompañar y aprender / Implement & learn
ES: Implementación · seguimiento · resultados · conocimiento.
EN: Implementation · monitoring · results · knowledge.
```

---

#### SECCIÓN 7: TECNOLOGÍA E INTELIGENCIA (`#tecnologia`)
**Variante:** `.section--dark` (fondo `--color-primary-dark`)  
**Nota de contenido:** Sección presente desde el lanzamiento pero deliberadamente discreta — la tecnología existe pero está en desarrollo. El tono es "capacidad emergente", no promesa concreta.

**Layout:** Dos columnas en desktop. Columna izquierda: texto. Columna derecha: elemento visual abstracto (opcional: animación CSS simple de nodos conectados o gradiente dinámico).

**Contenido:**

```
[LABEL TAG — acento verde]
ES: Capacidad tecnológica
EN: Technology capability

[H2]
ES: Experiencia humana aumentada por tecnología
EN: Human expertise augmented by technology

[PÁRRAFO]
ES: NEXUS combina criterio profesional, información territorial, sistemas de información geográfica e inteligencia artificial para analizar problemas complejos, integrar grandes volúmenes de información y desarrollar soluciones con mayor consistencia y trazabilidad.
EN: NEXUS combines professional judgment, territorial information, geographic information systems, and artificial intelligence to analyze complex problems, integrate large volumes of information, and develop solutions with greater consistency and traceability.

[BLOQUE DESTACADO — caja con borde izquierdo --color-accent]
ES título: NEXUS Project Intelligence
ES texto: Desarrollamos un sistema propio de conocimiento y gestión de proyectos que integrará formulación, información territorial, documentación, evaluación y financiación dentro de un mismo entorno de trabajo. [En desarrollo]
EN título: NEXUS Project Intelligence
EN texto: We are developing a proprietary project knowledge and management system that will integrate formulation, territorial information, documentation, evaluation, and financing within a single work environment. [In development]
```

---

#### SECCIÓN 8: PARA QUIÉN TRABAJAMOS (`#para-quien`)
**Variante:** `.section--alt`  
**Layout:** Header + grid de 8 tarjetas de audiencia (2 filas × 4 cols en desktop; 2×2 en tablet; 1 col en mobile). Cada tarjeta: ícono SVG + nombre de audiencia.

**Audiencias (íconos sugeridos en paréntesis):**

```
ES → EN                                             Ícono
Comunidades vulnerables → Vulnerable communities    🏘️ / grupo de personas
Gobiernos y entidades territoriales → Governments  🏛️ / edificio institucional
Autoridades ambientales → Environmental authorities 🌿 / hoja
Cooperación internacional y financiadores → Intl. cooperation 🌐 / globo
Fundaciones y ONG → Foundations & NGOs             🤝 / apretón de manos
Empresas y firmas consultoras → Companies          💼 / maletín
Universidades y centros de conocimiento → Universities 🎓 / birrete
Organizaciones comunitarias → Community organizations 👥 / personas en red
```

---

#### SECCIÓN 9: INICIATIVAS EN DESARROLLO (`#iniciativas`)
**Variante:** `.section--light`  
**Nota:** Estas son propuestas e iniciativas propias, no contratos. Deben rotularse explícitamente como *"Iniciativas y soluciones en desarrollo"* para evitar interpretaciones como contratos ejecutados.

**Layout:** Header + grid de cards tipo "proyecto" (3 cols en desktop, 1 en mobile). Cada card: imagen [PLACEHOLDER] + etiqueta "En desarrollo" + título + descripción breve.

**Contenido de cards:**

```
[CARD 1]
ES etiqueta: En desarrollo
EN etiqueta: In development
ES título: Sistema de Planificación Ambiental Estratégica — Santa Marta
EN título: Strategic Environmental Planning System — Santa Marta
ES desc: Propuesta que integra Agenda Ambiental, Observatorio, estrategia de financiación y tres proyectos territoriales para la ciudad de Santa Marta.
EN desc: A proposal integrating an Environmental Agenda, Observatory, financing strategy, and three territorial projects for the city of Santa Marta.

[CARD 2]
ES etiqueta: En desarrollo
EN etiqueta: In development
ES título: Portafolio DTSM — Distrito Turístico y Cultural de Santa Marta
EN título: DTSM Portfolio — Tourist and Cultural District of Santa Marta
ES desc: Tres líneas operativas: hídrica, marino-costera y Sierra-Mar.
EN desc: Three operational lines: water resources, coastal-marine, and Sierra-Mar corridor.

[CARD 3]
ES etiqueta: En desarrollo
EN etiqueta: In development
ES título: Manglares, bioeconomía y gobernanza marino-costera
EN título: Mangroves, Bioeconomy, and Coastal-Marine Governance
ES desc: Iniciativas de restauración, economía local y gobernanza en ecosistemas de manglar del Caribe colombiano.
EN desc: Restoration, local economy, and governance initiatives in Colombian Caribbean mangrove ecosystems.

[CTA al pie de las cards]
ES: ¿Tiene una iniciativa o territorio en mente? Conversemos.
EN: Do you have an initiative or territory in mind? Let's talk.
href: /contacto/?tipo=iniciativa
Botón estilo: primario `--color-primary`
```

---

#### SECCIÓN 10: QUIÉNES SOMOS (`#equipo`)
**Variante:** `.section--dark` (fondo `--color-primary`)

**Sub-sección 10a: Descripción institucional**

```
[LABEL TAG]
ES: Nuestro equipo
EN: Our team

[H2]
ES: Las capacidades detrás de NEXUS
EN: The capabilities behind NEXUS

[PÁRRAFO LEAD]
ES: Una empresa nueva construida sobre experiencia real.
EN: A new company built on real experience.

[PÁRRAFO]
ES: NEXUS es una empresa nueva construida sobre décadas de experiencia profesional acumulada por sus socios y especialistas en algunos de los principales desafíos ambientales, territoriales y de infraestructura de Colombia. Nuestro equipo integra dirección estratégica, ciencias ambientales, ingeniería, restauración ecológica, economía y planeación para abordar los proyectos como sistemas y no como componentes aislados.
EN: NEXUS is a new company built on decades of professional experience accumulated by its partners and specialists across Colombia's main environmental, territorial, and infrastructure challenges. Our team integrates strategic direction, environmental sciences, engineering, ecological restoration, economics, and planning to address projects as systems, not isolated components.

[FRASE POTENTE — tipografía grande, centrada, peso 800]
ES: NEXUS es nueva. La experiencia que la hace posible, no.
EN: NEXUS is new. The experience that makes it possible is not.
```

**Sub-sección 10b: Diagrama de complementariedad del equipo**

```
[ELEMENTO VISUAL: diagrama tipo flujo / cascada]

ES: UN PROBLEMA TERRITORIAL
EN: A TERRITORIAL CHALLENGE
        ↓
Juan Carlos Pino: ¿Qué está pasando y qué solución integral necesitamos?
                  What is happening and what integrated solution do we need?
        ↓
Walter Gil:       ¿Qué requiere el territorio y el ecosistema?
                  What does the territory and ecosystem require?
        ↓
Gleirys Amaya:    ¿Qué ocurre con las personas, la economía y el desarrollo?
                  What is happening with people, the economy, and development?
        ↓
Carol Sierra:     ¿Cómo lo convertimos en una intervención estructurada, viable y ejecutable?
                  How do we turn it into a structured, viable, and executable intervention?
        ↓
ES: NEXUS → PROYECTO INTEGRAL + FINANCIACIÓN + IMPLEMENTACIÓN
EN: NEXUS → INTEGRATED PROJECT + FINANCING + IMPLEMENTATION
```

**Sub-sección 10c: 4 Team Cards** (ver §6.6)

**Datos de cada integrante:**

```
[INTEGRANTE 1]
Nombre: Juan Carlos Pino Renjifo
Rol ES: Socio fundador · Director Técnico y de Estrategia
Rol EN: Founding Partner · Technical and Strategy Director
Credenciales: Biólogo Marino · Esp. Administración Ambiental Zonas Costeras · MSc. Gestión de Sistemas Marino-Costeros (en curso)
Experiencia ES: Más de 31 años en gestión ambiental, planificación territorial, manejo de ecosistemas marino-costeros, estructuración y dirección de proyectos y articulación institucional.
Experiencia EN: Over 31 years in environmental management, territorial planning, coastal-marine ecosystem management, project structuring and direction, and institutional coordination.
Tags: visión sistémica · dirección estratégica · gobernanza · desarrollo de proyectos · conocimiento territorial · articulación institucional
Foto: /assets/images/team/juan-carlos-pino.jpg [PLACEHOLDER]

[INTEGRANTE 2]
Nombre: Carol Miley Sierra Pachón
Rol ES: Socia · Directora de Proyectos y Estructuración
Rol EN: Partner · Projects and Structuring Director
Credenciales: Ingeniera Civil · Magíster en Gestión en la Industria de los Hidrocarburos · Esp. Administración Ambiental Zonas Costeras
Experiencia ES: Aproximadamente 20 años en consultoría ambiental, infraestructura, ordenamiento territorial y coordinación técnica, administrativa y financiera de proyectos.
Experiencia EN: Approximately 20 years in environmental consulting, infrastructure, territorial planning, and technical, administrative, and financial coordination of projects.
Tags: estructuración · ingeniería · inversión pública · presupuestos · infraestructura · gestión de proyectos
Foto: /assets/images/team/carol-sierra.jpg [PLACEHOLDER]

[INTEGRANTE 3]
Nombre: Walter Gil Torres
Rol ES: Socio · Director de Ecosistemas y Restauración
Rol EN: Partner · Ecosystems and Restoration Director
Credenciales: Ingeniero Forestal · Candidato a Magíster en Restauración Ecológica
Experiencia ES: Más de 28 años en planificación, manejo y restauración de ecosistemas tropicales, especialmente manglares, zonas costeras y cuencas hidrográficas.
Experiencia EN: Over 28 years in planning, management, and restoration of tropical ecosystems, particularly mangroves, coastal areas, and river basins.
Tags: restauración · biodiversidad · SbN/AbE · manglares · cambio climático · comunidades
Foto: /assets/images/team/walter-gil.jpg [PLACEHOLDER]

[INTEGRANTE 4]
Nombre: Gleirys Amaya Mendoza
Rol ES: Economista Senior · Planeación e Impacto Socioeconómico
Rol EN: Senior Economist · Planning and Socioeconomic Impact
Credenciales: Economista · Magíster en Economía
Experiencia ES: Trayectoria en planeación estratégica, proyectos de inversión, investigación y análisis socioeconómico, con experiencia en instrumentos de planeación de largo plazo.
Experiencia EN: Background in strategic planning, investment projects, research, and socioeconomic analysis, with experience in long-term planning instruments.
Tags: economía · planeación · análisis socioeconómico · indicadores · investigación · desarrollo territorial
Foto: /assets/images/team/gleirys-amaya.jpg [PLACEHOLDER]
```

---

#### SECCIÓN 11: EL CARIBE COMO ORIGEN (`#caribe`)
**Variante:** `.section--image` (imagen territorial de fondo con overlay `--color-primary` 70%)  
**Imagen:** [PLACEHOLDER] — Vista aérea/paisaje del Caribe colombiano (manglar, bahía, sierra nevada de fondo, comunidad costera).

**Contenido:**

```
[LABEL TAG — acento verde]
ES: Nuestro territorio de origen
EN: Our home territory

[H2]
ES: Nacemos en el Caribe. Diseñamos soluciones replicables.
EN: Born in the Caribbean. Building replicable solutions.

[PÁRRAFO]
ES: El Caribe colombiano constituye nuestro principal territorio de conocimiento y experimentación. Su diversidad ambiental, cultural, institucional y socioeconómica ofrece un escenario excepcional para desarrollar soluciones capaces de adaptarse a otros territorios de Colombia y América Latina.
EN: The Colombian Caribbean is our primary territory of knowledge and experimentation. Its environmental, cultural, institutional, and socioeconomic diversity provides an exceptional setting for developing solutions adaptable to other territories in Colombia and Latin America.
```

---

#### SECCIÓN 12: CONTACTO TEASER (`#contacto-home`)
**Variante:** `.section--accent` (fondo `--color-accent`)  
**Layout:** Centrado, simple.

**Contenido:**

```
[H2]
ES: ¿Qué necesita convertir en realidad?
EN: What do you need to make a reality?

[TRES BOTONES TIPO PILL — en fila, fondo blanco con texto --color-primary]

Botón A:
  ES: Tengo una idea o proyecto
  EN: I have an idea or project
  href: /contacto/?tipo=proyecto

Botón B:
  ES: Necesito desarrollar una cartera de proyectos
  EN: I need to develop a project portfolio
  href: /contacto/?tipo=cartera

Botón C:
  ES: Busco proyectos o territorios donde invertir
  EN: I'm looking for projects or territories to invest in
  href: /contacto/?tipo=inversion
```

---

### 8.2 `oficina-estrategica/index.html`

**Título de la página:**
```
ES: Oficina Estratégica de Proyectos — NEXUS GSS
EN: Strategic Project Office — NEXUS GSS
```

**Estructura de secciones:**

**Sec 1 — Hero de subpágina**
- Fondo: `--color-primary` (sin imagen, solo color) con patrón geométrico sutil (líneas finas, opacidad 5%)
- H1 + bajada + breadcrumb `Inicio / Oficina Estratégica`

```
[H1]
ES: Capacidad permanente para desarrollar proyectos sin ampliar permanentemente su estructura.
EN: Permanent capacity to develop projects without permanently expanding your structure.

[LEAD]
ES: La Oficina Estratégica de Proyectos NEXUS acompaña a organizaciones y entidades en la identificación, priorización, estructuración y búsqueda de financiación para sus iniciativas.
EN: The NEXUS Strategic Project Office accompanies organizations and entities in identifying, prioritizing, structuring, and securing financing for their initiatives.
```

**Sec 2 — Qué es**
- Variante: `.section--light`
- Descripción extensa del producto (ver LIBRETO §4)

**Sec 3 — El flujo (diagrama vertical)**
Diagrama visual del flujo de conversión:
```
IDEAS Y NECESIDADES → Evaluación → Priorización → Estructuración → 
Cartera de proyectos → Oportunidades de financiación → Presentación y seguimiento
```
Implementar como lista vertical con línea conectora, iconos y colores alternados `--color-primary` / `--color-accent`.

**Sec 4 — Por qué NEXUS**
Grid de 3 ventajas comparativas (cards simples con ícono + título + descripción).

**Sec 5 — CTA**
```
ES: Su organización conserva las decisiones. NEXUS aporta la capacidad para convertirlas en proyectos.
EN: Your organization keeps the decisions. NEXUS brings the capacity to turn them into projects.
[Botón] → /contacto/?tipo=cartera
```

---

### 8.3 `areas/index.html`

**Título:**
```
ES: Áreas de trabajo — NEXUS GSS
EN: Work areas — NEXUS GSS
```

**Estructura:**

**Sec 1 — Hero de subpágina**
```
[H1]
ES: Las áreas en las que trabajamos
EN: The areas where we work

[LEAD]
ES: NEXUS opera en la intersección de los principales desafíos ambientales y de desarrollo de Colombia y América Latina.
EN: NEXUS operates at the intersection of Colombia and Latin America's main environmental and development challenges.
```

**Sec 2 — Grid de 8 áreas temáticas**
Grid 4×2 de Area Cards (ver §6.7). Cada card lleva a un anchor `#[area]` más abajo.

**8 ÁREAS:**
```
01. Agua y cuencas / Water & river basins
02. Mares y costas / Seas & coasts
03. Biodiversidad y ecosistemas / Biodiversity & ecosystems
04. Cambio climático y riesgo / Climate change & risk
05. Desarrollo territorial y bioeconomía / Territorial development & bioeconomy
06. Gobernanza y fortalecimiento institucional / Governance & institutional strengthening
07. Educación e innovación / Education & innovation
08. Desarrollo comunitario / Community development
```

**Sec 3 — Detalle de cada área (8 sub-secciones)**
Para cada área: ancla, título, descripción de 100-150 palabras, imagen [PLACEHOLDER], palabras clave de servicios aplicables. Alternar variante `.section--light` y `.section--alt`.

---

### 8.4 `contacto/index.html`

**Título:**
```
ES: Contacto — NEXUS GSS
EN: Contact — NEXUS GSS
```

**Estructura:**

**Sec 1 — Hero de subpágina**
```
[H1]
ES: Conversemos
EN: Let's talk

[LEAD]
ES: ¿Tiene una necesidad, una idea o un proyecto que quiere convertir en realidad? Cuéntenos.
EN: Do you have a need, an idea, or a project you want to turn into reality? Tell us.
```

**Sec 2 — Tres puertas de entrada**
Cards clickeables que preseleccionan el tipo de consulta.

```
Puerta A:
ES: Tengo una idea o proyecto
EN: I have an idea or project
Ícono: bombilla / mapa

Puerta B:
ES: Necesito desarrollar una cartera de proyectos
EN: I need to develop a project portfolio
Ícono: portafolio / carpetas

Puerta C:
ES: Busco proyectos o territorios donde invertir
EN: I'm looking for projects or territories to invest in
Ícono: globo / brújula
```

**Sec 3 — Botón de contacto (mailto)**

```html
<!-- Botón principal de contacto -->
<a href="mailto:info@nexusgss.co?subject=[Tipo de consulta]" 
   class="btn btn--primary btn--large"
   id="contact-btn">
  <span data-i18n="contact.email.btn">Escribirnos por correo</span>
</a>

<!-- Nota explicativa -->
<p class="caption" data-i18n="contact.email.note">
  ES: Al hacer clic se abrirá su cliente de correo electrónico.
  EN: Clicking will open your email client.
</p>
```

Cuando el usuario llega con `?tipo=proyecto`, `?tipo=cartera` o `?tipo=inversion`, el JS ajusta el `subject` del mailto automáticamente:
```javascript
const params = new URLSearchParams(window.location.search);
const tipo = params.get('tipo');
const subjects = {
  proyecto: 'Consulta: Tengo una idea o proyecto — NEXUS GSS',
  cartera: 'Consulta: Cartera de proyectos — NEXUS GSS',
  inversion: 'Consulta: Inversión en territorios — NEXUS GSS'
};
if (tipo && subjects[tipo]) {
  document.getElementById('contact-btn').href = 
    `mailto:info@nexusgss.co?subject=${encodeURIComponent(subjects[tipo])}`;
}
```

**Sec 4 — LinkedIn**
```
[Enlace a LinkedIn]
https://www.linkedin.com/in/nexus-gss-governance-and-sustainability-solutions-a768623a8

[Texto]
ES: También puede encontrarnos en LinkedIn.
EN: You can also find us on LinkedIn.
```

**Sec 5 — Localización**
```
ES: Caribe colombiano · Colombia
EN: Colombian Caribbean · Colombia

[Mapa estático — OPCIONAL]
Si se desea mostrar ubicación geográfica sin API de Google Maps, usar imagen estática 
de OpenStreetMap centrada en el Caribe colombiano, con marcador en Santa Marta.
Alternativa: elemento decorativo con silueta del mapa de Colombia resaltando la región Caribe (SVG inline).
```

---

## 9. SISTEMA BILINGÜE

### Estrategia
Sitio con un único set de archivos HTML. Cada elemento de texto tiene un atributo `data-i18n="clave.subkey"`. Un objeto JavaScript contiene el diccionario completo en dos idiomas. Un función `setLanguage(lang)` actualiza el DOM en tiempo real.

### Implementación

```javascript
// lang.js — estructura
const translations = {
  es: {
    "nav.services": "Qué hacemos",
    "nav.office": "Oficina Estratégica",
    "nav.areas": "Áreas",
    "nav.team": "Equipo",
    "nav.contact": "Contacto",
    "hero.tag": "NEXUS GSS · Gobernanza y Sostenibilidad",
    "hero.h1": "Transformamos desafíos territoriales en soluciones que pueden hacerse realidad.",
    "hero.lead": "Integramos conocimiento, territorio, información, financiación y capacidades institucionales para diseñar y desarrollar soluciones ambientales y de desarrollo sostenible.",
    "hero.cta1": "Desarrollar un proyecto",
    "hero.cta2": "Conocer nuestras soluciones",
    // ... [continúa con todas las claves]
    "footer.tagline": "Transformamos desafíos territoriales en soluciones que pueden hacerse realidad.",
    "footer.rights": "Todos los derechos reservados."
  },
  en: {
    "nav.services": "What we do",
    "nav.office": "Strategic Office",
    "nav.areas": "Areas",
    "nav.team": "Team",
    "nav.contact": "Contact",
    "hero.tag": "NEXUS GSS · Governance and Sustainability",
    "hero.h1": "We transform territorial challenges into solutions that can become reality.",
    "hero.lead": "We integrate knowledge, territory, information, financing, and institutional capacities to design and develop environmental and sustainable development solutions.",
    "hero.cta1": "Develop a project",
    "hero.cta2": "Explore our solutions",
    // ... [continúa con todas las claves en inglés]
    "footer.tagline": "We transform territorial challenges into solutions that can become reality.",
    "footer.rights": "All rights reserved."
  }
};

function setLanguage(lang) {
  document.querySelectorAll('[data-i18n]').forEach(el => {
    const key = el.getAttribute('data-i18n');
    if (translations[lang] && translations[lang][key]) {
      el.textContent = translations[lang][key];
    }
  });
  document.documentElement.lang = lang;
  localStorage.setItem('nexus-lang', lang);
  // Actualizar estado visual del switcher
  document.getElementById('lang-es').classList.toggle('lang-active', lang === 'es');
  document.getElementById('lang-en').classList.toggle('lang-active', lang === 'en');
}

function toggleLang() {
  const current = localStorage.getItem('nexus-lang') || 'es';
  setLanguage(current === 'es' ? 'en' : 'es');
}

// Al cargar: aplicar idioma guardado
document.addEventListener('DOMContentLoaded', () => {
  const saved = localStorage.getItem('nexus-lang') || 'es';
  setLanguage(saved);
});
```

**Nota:** Los atributos `alt` de imágenes también deben ser bilingües. Usar `data-i18n-alt` y actualizar con `el.setAttribute('alt', translations[lang][key])`.

---

## 10. IMÁGENES Y MEDIOS

### Política de imágenes
El cliente aportará fotografías propias en una segunda fase. El sitio debe funcionar correctamente con **imágenes de placeholder** en el lanzamiento inicial.

### Especificaciones de placeholders

| Imagen | Dimensiones mínimas | Ratio | Contenido esperado |
|--------|---------------------|-------|-------------------|
| hero-bg.jpg | 1920×1080px | 16:9 | Vista aérea: costa/cuenca/sierra del Caribe colombiano |
| team/*.jpg | 600×600px | 1:1 | Retrato profesional en exterior o campo |
| territory-01/02/03.jpg | 1200×800px | 3:2 | Paisaje territorial / comunidad / equipo en campo |
| areas/*.jpg | 800×600px | 4:3 | Ecosistema representativo de cada área |

### Placeholder visual en ausencia de foto real
Para las fotos de equipo, implementar un fallback CSS/JS:
```css
.team-photo img { display: none; } /* Si la imagen falla */
.team-photo::after {
  content: attr(data-initials);
  display: flex; align-items: center; justify-content: center;
  width: 100%; height: 100%;
  background: var(--color-primary-mid);
  color: white;
  font-size: 2rem;
  font-weight: 700;
  font-family: var(--font-heading);
}
```
Añadir en cada `<img>` de equipo: `data-initials="JCP"` (iniciales del integrante).

### Optimización
- Todos los `<img>` de contenido (no hero): `loading="lazy"`.
- El hero usa `background-image` CSS para mayor control del overlay.
- Dimensiones `width` y `height` siempre declaradas en el HTML para evitar CLS (Cumulative Layout Shift).
- Formato recomendado: JPEG para fotografías (calidad 80%), SVG para íconos y logotipo.

---

## 11. SEO Y METADATOS

### Meta tags requeridos en cada página

```html
<!-- index.html -->
<title>NEXUS GSS — Gobernanza y Soluciones Sostenibles | Colombia</title>
<meta name="description" content="Firma especializada en diseño, formulación y estructuración de proyectos ambientales y de desarrollo territorial en Colombia y América Latina.">

<!-- oficina-estrategica/index.html -->
<title>Oficina Estratégica de Proyectos | NEXUS GSS</title>
<meta name="description" content="Capacidad permanente de formulación y gestión de proyectos para organizaciones y entidades que quieren convertir sus iniciativas en proyectos financiables.">

<!-- areas/index.html -->
<title>Áreas de trabajo | NEXUS GSS</title>
<meta name="description" content="Agua y cuencas, mares y costas, biodiversidad, cambio climático, desarrollo territorial, gobernanza y más. Las áreas temáticas de NEXUS GSS.">

<!-- contacto/index.html -->
<title>Contacto | NEXUS GSS</title>
<meta name="description" content="¿Tiene una idea, proyecto o necesita asesoría en gobernanza ambiental y sostenibilidad? Conversemos con NEXUS GSS.">
```

### Open Graph y Twitter Card
```html
<meta property="og:type" content="website">
<meta property="og:site_name" content="NEXUS GSS">
<meta property="og:locale" content="es_CO">
<meta property="og:locale:alternate" content="en_US">
<meta property="og:image" content="https://[dominio]/assets/images/hero/hero-bg.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta name="twitter:card" content="summary_large_image">
```

### Robots y canonical
```html
<meta name="robots" content="index, follow">
<link rel="canonical" href="https://[dominio]/[ruta-de-página]/">
```

### Sitemap
Crear `sitemap.xml` en la raíz con las 4 URLs principales. Indicar `<lastmod>` y `<changefreq>weekly</changefreq>`.

---

## 12. ACCESIBILIDAD

### Estándares
- Nivel WCAG 2.1 AA como mínimo.
- Contraste de color: ratio mínimo 4.5:1 para texto normal, 3:1 para texto grande.

### Requisitos específicos
- Todos los `<img>` deben tener `alt` descriptivo (bilingüe vía JS).
- Íconos decorativos: `aria-hidden="true"`.
- Botones del hamburger menu: `aria-label`, `aria-expanded`.
- Orden de foco lógico (Tab order).
- Skip link al inicio: `<a href="#main-content" class="skip-link">Saltar al contenido</a>`.
- El switcher de idioma debe anunciar el cambio: `aria-live="polite"`.
- Focus visible en todos los elementos interactivos.
- Semántica HTML5 correcta: `<main>`, `<nav>`, `<header>`, `<footer>`, `<section>`, `<article>`.

---

## 13. COMPORTAMIENTO RESPONSIVE

### Breakpoints

```css
/* Mobile first */
/* xs: < 480px — implícito */
@media (min-width: 480px) { /* sm */ }
@media (min-width: 768px) { /* md — tablets */ }
@media (min-width: 1024px) { /* lg — desktop */ }
@media (min-width: 1280px) { /* xl — large desktop */ }
```

### Comportamiento por componente

| Componente | Mobile (<768px) | Desktop (≥1024px) |
|-----------|----------------|-------------------|
| Navbar | Hamburger menu | Links horizontales |
| Hero H1 | `var(--text-4xl)` | `var(--text-7xl)` |
| Grid servicios | 1 col | 2×2 cols |
| Proceso | Acordeón vertical | Línea horizontal 6 cols |
| Team cards | 1 col | 2 cols (foto+info) |
| Áreas grid | 1 col | 4×2 grid |
| Footer | 1 col stacked | 3 cols |

---

## 14. DESPLIEGUE EN GITHUB PAGES

### Configuración

**`_config.yml`** (necesario si se usan rutas relativas con Jekyll; opcional para HTML puro):
```yaml
# _config.yml
title: NEXUS GSS
description: Gobernanza y Soluciones Sostenibles
baseurl: ""
url: "https://juancpino-collab.github.io/nexus"
```

**Si el dominio es `juancpino-collab.github.io/nexus`**, todas las rutas de assets deben ser relativas o usar `/nexus/` como prefijo. Alternativa más limpia: usar rutas relativas en HTML (`../assets/`) o configurar un dominio personalizado.

**Configuración de GitHub Pages:**
- En el repositorio: Settings → Pages → Branch: `main` / folder: `/ (root)`
- Si se usa dominio personalizado: añadir archivo `CNAME` en la raíz con el dominio (ej: `nexusgss.co`).

**`README.md`:**
- Descripción del proyecto, instrucciones para actualizar contenido, lista de archivos placeholder a reemplazar.

### Archivo `.nojekyll`
Crear un archivo vacío llamado `.nojekyll` en la raíz para evitar que GitHub Pages procese el sitio con Jekyll (innecesario para HTML puro):
```bash
touch .nojekyll
```

### Flujo de actualización de contenido
1. Editar archivos HTML/CSS/JS localmente.
2. `git add . && git commit -m "Descripción del cambio"`.
3. `git push origin main`.
4. GitHub Pages publica automáticamente en ~60 segundos.

---

## 15. CRITERIOS DE ACEPTACIÓN

El sitio se considera correctamente implementado cuando cumple **todos** los siguientes criterios:

### Funcional
- [ ] El sitio carga correctamente en `juancpino-collab.github.io/nexus` (o dominio personalizado).
- [ ] El switcher de idioma ES/EN funciona en todas las páginas y el idioma se mantiene al navegar.
- [ ] El navbar se vuelve opaco al hacer scroll y transparente al volver al top.
- [ ] El menú hamburger abre y cierra correctamente en mobile.
- [ ] Los 3 botones de la sección de contacto home redirigen a `/contacto/` con el parámetro correcto.
- [ ] El botón mailto de contacto abre el cliente de correo con subject prellenado.
- [ ] Los links de navegación llevan a las anclas correctas en la página principal.
- [ ] Las subpáginas (Oficina Estratégica, Áreas, Contacto) cargan sin errores 404.

### Visual
- [ ] Los colores coinciden con la paleta definida en §4 (tolerancia: ΔE < 2).
- [ ] Las fuentes Montserrat e Inter cargan correctamente (verificar en DevTools → Network).
- [ ] El logo se muestra correctamente en navbar transparente (blanco) y opaco (color).
- [ ] Los placeholders de imágenes muestran el color de fondo y/o iniciales del equipo, sin imágenes rotas.
- [ ] El hero ocupa `100vh` en desktop y ≥80vh en mobile.

### Responsive
- [ ] Probado en Chrome/Firefox/Safari en: 375px (iPhone SE), 768px (iPad), 1440px (desktop).
- [ ] Sin scroll horizontal en ningún breakpoint.
- [ ] El menú hamburger funciona en mobile.
- [ ] Los grids se reorganizan correctamente según los breakpoints especificados en §13.

### Accesibilidad
- [ ] Contraste texto/fondo aprobado en verificador WCAG (ej: webaim.org/resources/contrastchecker/).
- [ ] Tab order lógico en toda la página.
- [ ] Todos los `<img>` tienen `alt` no vacío.
- [ ] El sitio es usable solo con teclado.

### Rendimiento (Lighthouse)
- [ ] Performance ≥ 85 en mobile.
- [ ] Accessibility ≥ 90.
- [ ] Best Practices ≥ 90.
- [ ] SEO ≥ 90.

---

*Fin de la especificación. Versión 1.0 — 2026-09-01*  
*Para actualizar esta especificación, editar este archivo y hacer commit al repositorio.*
