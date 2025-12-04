---

## 🎯 Tipos de Commit (Commit Types)

Utiliza uno de los siguientes prefijos para el `<tipo>`:

| Prefijo | Propósito | Ejemplo de Commit | Impacto en SemVer |
| :--- | :--- | :--- | :--- |
| **`feat`** | **Nueva funcionalidad** o característica. | `feat: agregar formulario de contacto` | MINOR |
| **`fix`** | **Corrección de errores** en el código de producción. | `fix: corregir bug en login` | PATCH |
| **`perf`** | **Mejoras de rendimiento** del código. | `perf: optimizar carga de imágenes` | PATCH |
| **`refactor`** | **Reestructuración** de código sin cambiar su comportamiento. | `refactor: simplificar función de búsqueda` | PATCH |
| **`test`** | Añadir o modificar **pruebas** (unitarias, integración, etc.). | `test: agregar test para registro` | PATCH |
| **`docs`** | Cambios en la **documentación** (README, comentarios, etc.). | `docs: actualizar README` | No Impacta |
| **`style`** | Cambios de **formato o estilo** de código (indentación, punto y coma). | `style: mejorar indentación` | No Impacta |
| **`chore`** | Tareas de **mantenimiento** (configuración, dependencias no críticas). | `chore: agregar .gitignore` | No Impacta |
| **`build`** | Cambios relacionados con el **sistema de construcción** (npm, webpack, etc.). | `build: actualizar versión de webpack` | No Impacta |
| **`ci`** | Cambios en la configuración de **Integración Continua** (GitHub Actions, GitLab CI, etc.). | `ci: agregar paso de linting` | No Impacta |
| **`revert`** | **Revertir** por completo un commit anterior. | `revert: "feat: agregar módulo de pagos"` | PATCH (generalmente) |

---

## 🚨 Manejo de Cambios Mayores (`BREAKING CHANGE`)

Si un commit introduce un cambio que **rompe la compatibilidad** y requiere que los usuarios actualicen su código (por ejemplo, cambiar el nombre de una función o endpoint), debe ser indicado claramente.

Para esto, se debe agregar el texto **`BREAKING CHANGE:`** en el pie de página (*footer*) del mensaje de commit.

### Sintaxis en el pie de página:

```txt
BREAKING CHANGE: <Descripción de la ruptura de compatibilidad>
