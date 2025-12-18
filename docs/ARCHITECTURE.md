# Arquitectura del sistema

## Principios fundamentales

1. La Shell no contiene lógica de dominio
2. Los módulos no se conocen entre sí
3. Quitar un módulo nunca rompe la aplicación
4. Añadir un módulo no requiere modificar otros módulos
5. La Shell puede arrancar sin módulos

---

## Componentes principales

### Shell

La Shell es la aplicación principal.
Es la única aplicación que el usuario abre.

#### Responsabilidades

- Definir el layout común
- Gestionar la navegación
- Descubrir y registrar módulos
- Gestionar estado global
- Proveer servicios comunes

#### No es responsabilidad de la Shell

- Lógica de negocio
- Reglas de dominio
- Pantallas especializadas

---

### Módulos

Los módulos son unidades funcionales independientes.

Cada módulo:
- Resuelve un dominio concreto
- Vive en su propia carpeta
- Se describe mediante un manifest
- Puede activarse o desactivarse sin impacto global

---

## Estructura del proyecto

```txt
app/
├── shell/
├── modules/
├── common/
├── config/
├── infra/
└── docs/
```

---

## Proceso de arranque de la Shell

1. Bootstrap básico
2. Carga de configuración
3. Descubrimiento de módulos
4. Validación de manifests
5. Registro de módulos válidos
6. Inicialización de navegación
7. Arranque completo

Un fallo en un módulo no impide el arranque del sistema.

---

## Qué evita esta arquitectura

- Dependencias cruzadas
- Efectos dominó
- Acoplamiento fuerte
- Sobreingeniería temprana