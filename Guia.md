# Guía Profesional de Commits (Estándar Senior)

## Índice

* [Regla de Oro](#1-regla-de-oro)
* [Estructura del Mensaje](#2-estructura-del-mensaje)
* [Tipos de Commits](#3-tipos-de-commits)
* [Qué es el scope y cómo usarlo](#4-qué-es-el-scope-y-cómo-usarlo)
* [Cuándo dividir un commit](#5-cuándo-dividir-un-commit)
* [Ejemplos prácticos (Laravel / Tu proyecto)](#6-ejemplos-prácticos-laravel--tu-proyecto)
* [Buenas prácticas al escribir mensajes](#7-buenas-prácticas-al-escribir-mensajes)
* [Convención de nombres para ramas](#8-convención-de-nombres-para-ramas)
* [Cómo debe verse tu historial ideal](#9-cómo-debe-verse-tu-historial-ideal)
* [Regla Final](#10-regla-final)

## 1. Regla de Oro

La regla principal al hacer commits es **hacerlos pequeños y con un propósito claro**. Un commit debe representar un cambio aislado y coherente. Si haces más de una cosa a la vez, divídelo.

---

## 2. Estructura del Mensaje

Un mensaje profesional sigue este formato:

```
<tipo>(<scope>): <descripción breve>

<detalle opcional explicando el "qué" y el "por qué">
```

**Características:**

* Máximo 50-70 caracteres en la línea principal.
* Escribe en imperativo: "add", "fix", "update".
* Evita detalles técnicos irrelevantes.

---

## 3. Tipos de Commits

Lista de los tipos estándar:

* **feat:** Nueva funcionalidad.
* **fix:** Corrección de errores.
* **refactor:** Reorganización sin cambiar comportamiento.
* **style:** Cambios visuales o de formato.
* **docs:** Cambios en documentación.
* **test:** Añadir o actualizar pruebas.
* **chore:** Tareas internas sin impacto al producto.
* **perf:** Optimizaciones de rendimiento.
* **build:** Cambios en dependencias o herramientas.
* **ci:** Configuraciones de CI/CD.

---

## 4. Qué es el scope y cómo usarlo

El **scope** indica qué módulo o parte del proyecto fue afectado.
Ejemplos:

* `auth`
* `user`
* `dashboard`
* `models`
* `api`
* `ui`

**Correcto:** `feat(auth): add login validation`

**Incorrecto:** `feat: changes in system`

---

## 5. Cuándo dividir un commit

Divide el commit cuando:

* Hiciste más de una cosa.
* Hay cambios no relacionados.
* Un archivo se modificó por razones distintas.
* La explicación del commit se vuelve muy larga.

**Regla simple:** si puedes separar el cambio sin romper el código, divídelo.

---

## 6. Ejemplos prácticos (Laravel / Tu proyecto)

### Ejemplo 1: Crear controlador

```
feat(user): add UserController with index and store methods
```

### Ejemplo 2: Arreglar validación

```
fix(auth): correct login request validation rules
```

### Ejemplo 3: Refactorizar servicio

```
refactor(payment): reorganize service class to simplify logic
```

### Ejemplo 4: Cambiar estilos

```
style(ui): update navbar spacing and colors
```

### Ejemplo 5: Commit incorrecto (NO HACER)

```
update files
```

---

## 7. Buenas prácticas al escribir mensajes

* Escribe pensando en el historial del proyecto.
* No describas *cómo* lo hiciste, describe *qué* y *por qué*.
* Evita commits gigantes.
* Evita commits basura como:

  * "arreglo"
  * "cosas"
  * "avances"
  * "ya funciona"

---

## 8. Convención de nombres para ramas

Estructura recomendada:

```
<tipo>/<scope>-<descripcion-breve>
```

Ejemplos:

* `feature/user-crud`
* `fix/login-bug`
* `refactor/payment-service`

---

## 9. Cómo debe verse tu historial ideal

Un historial profesional debe verse así:

```
feat(auth): add login route and controller
fix(auth): correct password hashing
docs(api): update auth endpoints documentation
refactor(user): simplify repository structure
style(ui): improve button spacing
```

Debe ser **limpio**, **legible** y **coherente**.

---

## 10. Regla Final

Cada commit debe contestar dos preguntas:

1. **¿Qué hice?**
2. **¿Por qué era necesario?**

Si tu mensaje responde ambas, tu commit es profesional.
