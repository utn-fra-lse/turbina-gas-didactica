# 📦 [Nombre del repositorio]

> Breve descripción del proyecto o componente que vive en este repositorio.

---

## 🚀 Primeros pasos

### Cómo usar este template

Este repositorio fue creado a partir del template de la organización [utn-fra-lse](https://github.com/utn-fra-lse). Al crear un repo nuevo desde el template, asegurate de:

1. **Cambiar el nombre y descripción** del repositorio desde *Settings → General*
2. **Actualizar este README** — reemplazá el título, descripción y secciones que no apliquen
3. **Configurar los branch rulesets** si no se aplicaron automáticamente desde la organización (ver sección de flujo de trabajo)
4. **Asignar el repositorio al proyecto** de GitHub Projects de la organización si corresponde

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
