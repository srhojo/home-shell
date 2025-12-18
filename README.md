# Home-Shell

Plataforma web personal modular diseñada para centralizar múltiples aplicaciones sencillas
bajo una única interfaz común.

El objetivo principal es evitar el caos de múltiples apps independientes,
facilitar el mantenimiento y permitir crecer de forma incremental sin reescrituras.

---

## 🎯 Objetivos

- Tener una aplicación principal (Shell) que actúe como contenedor
- Añadir o quitar módulos sin romper el sistema
- Mantener una interfaz consistente
- Minimizar el esfuerzo para crear nuevas funcionalidades
- Usar inicialmente un solo lenguaje (Python)

---

## 🧱 Conceptos clave

- **Shell**: aplicación principal que define layout, navegación y contexto
- **Módulo**: unidad funcional independiente
- **Manifest**: contrato declarativo entre la Shell y los módulos

Estos conceptos están definidos en detalle en la documentación.

---

## 🛠️ Stack (fase inicial)

- Lenguaje: Python
- Framework: Reflex
- Despliegue: Docker
- Control de versiones: GitHub

El diseño permite integrar en el futuro módulos que consuman APIs externas
(Java, Python u otros).

---

## 📚 Documentación

Toda la documentación del diseño vive en `docs/`:

- [`docs/README.md`](docs/README.md)
- [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md)
- [`docs/MODULES.md`](docs/MODULES.md)

---

## 🚧 Estado del proyecto

Proyecto en fase de **diseño**.  
No hay código implementado todavía.