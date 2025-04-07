# 🧱 Angular Base Template

Plantilla base para proyectos Angular con enfoque en buenas prácticas, escalabilidad y mantenibilidad.  
Ideal para proyectos medianos o grandes, siguiendo una estructura cercana a la arquitectura hexagonal.

Este template está pensado para ayudarte a iniciar proyectos Angular de forma rápida, con una organización sólida desde el primer commit.

---

## 🚀 Tecnologías utilizadas

- [Angular](https://angular.io/) **v19.1.7**
- [Node.js](https://nodejs.org/) **v20.18.1**
- [ESLint](https://eslint.org/) – Linting para mantener la calidad del código
- [Prettier](https://prettier.io/) – Formateo automático del código
- [Normalize.css](https://necolas.github.io/normalize.css/) – Consistencia visual entre navegadores
- Arquitectura inspirada en **Hexagonal / DDD** (Separación clara de dominio, infraestructura y presentación)

---

## 📁 Estructura del proyecto

```bash
src/
└── app/
    ├── core/                      # Lógica de dominio y utilidades globales
    │   ├── constants/             # Constantes globales
    │   ├── models/                # Modelos de datos
    │   ├── services/              # Servicios puros (sin dependencia externa)
    │   └── utils/                 # Funciones auxiliares puras
    │
    ├── infrastructure/           # Implementaciones específicas del sistema
    │   ├── http/
    │   │   ├── services/          # Servicios que interactúan con APIs externas
    │   │   ├── interceptors/      # Interceptores HTTP globales
    │   │   └── adapters/          # Adaptadores entre infraestructura y dominio
    │   └── routing/
    │       ├── guards/           # Guards de rutas protegidas
    │       └── resolvers/        # Carga previa de datos para rutas
    │
    ├── shared/                   # Reutilizables en toda la app
    │   ├── components/            # Componentes UI compartidos
    │   ├── directives/            # Directivas personalizadas
    │   ├── pipes/                 # Pipes reutilizables
    │   ├── styles/                # Estilos globales / normalización
    │   └── utilities/             # Funciones auxiliares generales
    │
    └── pages/                    # Módulos de funcionalidades o vistas
