# Guía de Git y GitHub

---

## 1. Instalación

- **Git:**  
  Descarga e instala Git desde [https://git-scm.com/downloads](https://git-scm.com/downloads) según tu sistema operativo.

- **GitHub:**  
  Crea una cuenta en [https://github.com/](https://github.com/) para alojar tus repositorios.

---

## 2. Comandos básicos

```bash
# Clonar un repositorio
git clone https://github.com/usuario/repositorio.git

# Ver estado de archivos
git status

# Agregar cambios para preparar commit
git add archivo.txt
git add .

# Confirmar cambios
git commit -m "Mensaje descriptivo"

# Subir cambios al repositorio remoto
git push origin main

# Crear una nueva rama
git checkout -b nombre-rama

# Cambiar a otra rama existente
git checkout nombre-rama

# Actualizar repositorio local
git pull origin main
```
## 3. Buenas prácticas
- Trabaja en ramas separadas para nuevas funcionalidades o correcciones.
- Realiza commits claros y descriptivos.
- Sincroniza frecuentemente con el repositorio remoto para evitar conflictos.

## 4. Tipos de Commits (Conventional Commits)

Usar un **formato estándar** para los mensajes de commit ayuda a mantener un historial claro, facilitar la colaboración y automatizar tareas como generación de changelogs o despliegues.

Los prefijos más comunes son:

```bash
# Nueva funcionalidad
feat: agregar formulario de contacto

# Corrección de errores
fix: corregir bug en login

# Mantenimiento o tareas internas (configuración, dependencias, etc.)
chore: agregar .gitignore

# Cambios en la documentación
docs: actualizar README

# Cambios de formato o estilo de código sin afectar funcionalidad
style: mejorar indentación

# Reestructuración del código sin cambiar su comportamiento
refactor: simplificar función de búsqueda

# Añadir o modificar pruebas
test: agregar test para registro

# Mejoras de rendimiento
perf: optimizar carga de imágenes
```
