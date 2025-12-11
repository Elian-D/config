# Guía de Optimización para Laravel + Vite (Desarrollo Rápido)

Esta guía explica **qué hacer** y **cuándo hacerlo** para que tu proyecto Laravel funcione rápido mientras desarrollas. Incluye comandos de Laravel, Vite y notas importantes.

---

# 🚀 1. Comandos Esenciales de Optimización en Laravel

Laravel es muy rápido cuando usa **cache**. Cada vez que limpias o regeneras el cache, tu aplicación se acelera.

## ✔️ Limpiar todo (antes de reconstruir cache)

```
php artisan optimize:clear
```

Esto limpia:

* cache de rutas
* cache de configuración
* cache de vistas
* cache de eventos
* cache general

## ✔️ Optimizar todo (activar caches)

```
php artisan optimize
```

Esto genera:

* route cache
* config cache
* event cache
* compiled services
* optimized class loader

Después de este comando **Laravel queda rápido**.

---

# ⚙️ 2. Comandos Individuales (dependiendo de lo que cambies)

## 🔸 Si cambias rutas

```
php artisan route:clear
php artisan route:cache
```

## 🔸 Si cambias `.env`

```
php artisan config:clear
php artisan config:cache
```

## 🔸 Si cambias vistas Blade

```
php artisan view:clear
```

## 🔸 Si instalas un paquete o modificas providers

```
php artisan optimize:clear
php artisan optimize
```

---

# ⚡ 3. Mejores Prácticas Durante Desarrollo

## ✅ Antes de iniciar un día de trabajo

```
php artisan optimize:clear
php artisan optimize
```

## ✅ Después de un merge que toca rutas o config

```
php artisan optimize
```

## ✅ Antes de hacer pruebas de velocidad

```
php artisan optimize:clear
php artisan optimize
```

---

# 🖥️ 4. NPM / Vite en Desarrollo

Vite compila los assets (Tailwind + JS).

## ✔️ Para desarrollo (“modo rápido”)

```
npm run dev
```

* usa hot module reload
* recompila en vivo
* es más lento en el navegador, pero cómodo para editar

## ✔️ Para producción / velocidad máxima

```
npm run build
```

Esto genera archivos **minificados, comprimidos y optimizados**.

Luego Laravel usa lo que está en `public/build/`, que es MUCHO más rápido.

## ✔️ Usar el build en local (opcional, pero acelera)

Si no necesitas cambios al CSS/JS cada dos minutos:

```
npm run build
php artisan optimize
```

Y apagas `npm run dev`.

El navegador cargará:

* CSS real (minificado)
* JS real (minificado)
* 0 proceso adicional de Vite

Resultado:
👉 la velocidad que notaste hoy.

---

# 📌 5. Qué hacer si el proyecto vuelve a ponerse lento

1. Cierra `npm run dev`
2. Ejecuta:

```
php artisan optimize:clear
php artisan optimize
npm run build
```

3. Abre tu proyecto (con Apache o php artisan serve)

Tiempo estimado:

* login: **0.2 - 0.6s**
* dashboard: **0.3 - 1.0s**
* vistas CRUD: **0.3 - 1.0s**

---

# 🧠 6. Notas para Windows

Windows es más lento para:

* acceso a archivos
* composer autoload
* compilación de Vite
* file watchers

Por eso **es obligatorio usar cache** para tener buena velocidad.

---

# 🏁 Conclusión

Estos comandos son tu mejor amigo para que Laravel vuele:

```
php artisan optimize:clear
php artisan optimize
npm run build
```

Si necesitas, puedo crear un **script automático** o un **alias** para hacer todo con un solo comando.
