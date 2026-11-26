🚀 Proyecto Turbina de Gas Didáctica

Este repositorio contiene la documentación técnica, hojas de cálculo de dimensionamiento y planos constructivos para el diseño y desarrollo de una **Turbina de Gas Didáctica**.

---

## 📐 Descripción del Proyecto

El objetivo principal es el diseño y manufactura de una turbina de gas didáctica. El sistema opera mediante el ingreso de aire suministrado por un compresor que se mezcla con Gas Licuado de Petróleo (GLP) regulado a una presión de **2,2 bar**.

### Componentes Clave:
* **Cámara de Combustión:** Diseño tubular de tres etapas (primaria, secundaria y dilución).
* **Tubo de Llama:** Fabricado en tramos tubulares con perforaciones calibradas para el ingreso progresivo de aire y refrigeración.
* **Torbellinador / Remolinador:** Elemento de 12 paletas (ángulo de 62°) encargado de inducir turbulencia al aire para estabilizar la ignición del gas.
* **Domo Divergente y Convergente:** Zonas destinadas al control de velocidad y presión estática para optimizar la ignición y la descarga hacia la turbina.

---

## ⚙️ Especificaciones Técnicas y Dimensionamiento

### 1. Parámetros de Operación
* **Combustible:** GLP regulado a 2,2 bar.
* **Límite de Temperatura a la Entrada de Turbina:** 800 °C.
* **Caudal Másico Total de Combustión:** 34,49 g/s (gas de combustión) + 121,7 g/s (exceso de aire).

### 2. Distribución del Aire de Entrada (Compresor)
* **Zona Primaria (13% del aire):** Destinado a la combustión e ignición directa.
* **Zona Secundaria (30% del aire):** Utilizado para completar la oxidación del combustible y enfriamiento superficial.
* **Zona Terciaria / Dilución (57% del aire):** Encargado de reducir la temperatura de los gases antes del ingreso a la turbina.

### 3. Resumen de Dimensiones Constructivas

| Elemento / Zona | Diámetro / Especificación | Longitud | Perforaciones / Orificios |
| :--- | :--- | :--- | :--- |
| **Entrada del Compresor** | ø int. 45 mm | — | — |
| **Lanza de Gas** | ø ½” | — | — |
| **Torbellinador** | ø 35 mm (Ángulo: 62°) | — | — |
| **Domo Divergente** | 114° incl. total | 11 mm | Agujeros de refrigeración |
| **Zona Primaria** | Caño 2 ½" SCH40 (ø int. 62,68 mm) | 60 mm | ø 1,75 mm (60 orificios distribuidos en anillos) |
| **Zona Secundaria** | Caño 3" SCH40 (ø int. 77,92 mm) | 60 mm | ø 4 mm |
| **Zona Terciaria** | Caño 3 ½" SCH40 (ø int. 90,12 mm) | 80 mm (Tubo de llama) / 3500 mm total | ø 6 mm |
| **Carcasa (Casing)** | ø int. 112 mm | 336 mm | Espesor: 2 mm |

---

## 📂 Sistema de Codificación de Partes

El proyecto utiliza una nomenclatura estandarizada para la identificación de piezas y subconjuntos en los planos y listas de materiales:

**Formato del Código:** `[CONJUNTO]-[SUBCONJUNTO]-[POSICIÓN]-[VALIDACIÓN]`
*(Ejemplo: `CC-TU-01-0` -> Cámara de Combustión / Tubo de Llama / Posición 01 / Pendiente de validación)*

* **Conjuntos (`CC`):** Cámara de Combustión (`CC`), Sistema de Lubricación (`SL`), Sistema de Ignición (`SI`), Partes Comerciales (`PC`), Turbocompresor (`TC`), etc.
* **Subconjuntos (`SU`):** Tubo de Llama (`TU`), Casing (`CA`), Torbellinador (`TO`), Difusor (`DI`), Tobera (`TO`).
* **Estado de Validación:** `0` = No validado / Pendiente, `1` = Validado.

---

## 📜 Planos y Documentación Incluida

* `CC-TU-00-0_TUBO DE LLAMA.Rev.00.pdf`: Plano de conjunto y despiece del tubo de llama con tolerancias bajo norma **DIN ISO 2768 Clase M**.
* `CAMARA DE COMBUSTION.R01.docx`: Memoria descriptiva del funcionamiento y etapas de la cámara.
* `CAMARA DE COMBUSTION.xlsx`: Memoria de cálculo termodinámico y fluido-dinámico (caudales volumétricos, velocidades y áreas).
* `CODIFICACION DE PARTES.xlsx`: Matriz de codificación estandarizada para la gestión de piezas.

---

## 🛠️ Normas y Tolerancias
* **Tolerancias Dimensionales:** DIN ISO 2768-m.
* **Soldaduras:** Especificación de soldadura completa continua según planos de ensamble.
¿Te gustaría que agregue alguna sección adicional, como instrucciones de montaje o requisitos de software para abrir los planos CAD?
---

## 🌿 Estructura de ramas

Este repositorio sigue una convención de dos ramas principales:

| Rama | Propósito |
|------|-----------|
| `main` | Código estable. Nunca se pushea directo. Solo acepta merges via PR aprobada por un docente. |
| `develop` | Rama de integración. Cualquier becario puede hacer merge via PR sin requerir aprobación. |

Las ramas de trabajo se crean a partir de `develop` con nombres descriptivos:

```
feature/nombre-de-la-funcionalidad
fix/descripcion-del-bug
docs/lo-que-se-documenta
```

---

## 🔄 Flujo de trabajo

```
[rama feature] → PR → [develop] → PR (aprobación docente) → [main]
```

1. Creá tu rama desde `develop`:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/mi-feature
   ```

2. Trabajá en tu rama y commiteá con mensajes descriptivos:
   ```bash
   git commit -m "feat: agrega validación de formulario"
   ```

3. Abrí una **Pull Request** hacia `develop` cuando terminés
4. Una vez integrado en `develop` y validado, un docente abre la PR hacia `main`

> ⚠️ **Nunca pushear directamente a `main` ni a `develop`.** Siempre trabajar desde ramas propias y abrir PR.

---

## 📋 Convención de commits

Usamos una convención simple basada en prefijos:

| Prefijo | Cuándo usarlo |
|---------|---------------|
| `feat:` | Nueva funcionalidad |
| `fix:` | Corrección de bug |
| `docs:` | Cambios en documentación |
| `refactor:` | Refactorización sin cambio de comportamiento |
| `chore:` | Tareas de mantenimiento, dependencias |

---

## 👥 Equipo

| Rol | Responsabilidades en GitHub |
|-----|-----------------------------|
| **Docentes** | Aprueban PRs hacia `main`, administran la organización |
| **Becarios** | Crean ramas, abren PRs hacia `develop`, participan en revisiones |

---

## 🔗 Recursos

- [Organización en GitHub](https://github.com/utn-fra-lse)
- [Tablero del laboratorio (GitHub Projects)](https://github.com/orgs/utn-fra-lse/projects/2)
- [Repositorio de gestión operativa](https://github.com/utn-fra-lse/gestion) *(issues, documentación, inventario)*

---

## 📝 Notas adicionales

> Agregá acá cualquier información específica del proyecto: dependencias necesarias, cómo correr el proyecto localmente, contexto relevante, etc.
