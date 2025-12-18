# Sistema de módulos

## Qué es un módulo

Un módulo es una unidad funcional autocontenida que:

- Aporta una funcionalidad concreta
- Puede añadirse o eliminarse sin romper la Shell
- No conoce a otros módulos
- Se describe mediante un manifest

---

## Qué NO es un módulo

No son módulos:
- Componentes UI genéricos
- Utilidades compartidas
- Servicios comunes
- Código transversal

---

## Estructura de un módulo

```txt
modules/<module_name>/
├── views/
├── state/
├── services/
├── config/
└── manifest/
```

---

## El manifest del módulo

El manifest es el contrato entre la Shell y el módulo.

### Contiene información descriptiva:

- Identidad (id, nombre, versión)
- Navegación (ruta base, menú)
- Visibilidad y activación
- Permisos requeridos
- Dependencias externas
- Configuración aceptada
- Estado informativo

### Reglas del manifest

- No contiene lógica
- No referencia otros módulos
- No define layout
- No ejecuta código

---

## Independencia del módulo

Un módulo:
- No importa código de otros módulos
- No asume que otro módulo existe
- No modifica el comportamiento global

Eliminar un módulo no debe requerir cambios adicionales.

---

## Estados de un módulo

Durante el arranque, un módulo puede estar en:

- discovered
- disabled
- invalid
- registered
- active

Estos estados son gestionados por la Shell.

---

## Plantilla de módulo

Existe un módulo `_template` que sirve como base para crear nuevos módulos.

Crear un nuevo módulo debe ser:
1. Copiar la plantilla
2. Renombrar
3. Ajustar el manifest
4. Implementar la funcionalidad