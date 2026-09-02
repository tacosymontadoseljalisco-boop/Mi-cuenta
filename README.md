# Sistema POS · Tacos y Montados El Jalisco

Repositorio del punto de venta del restaurante.

- **App (frontend):** https://el-jalisco-pos.vercel.app (creada en v0.dev, desplegada en Vercel)
- **Base de datos:** Supabase, proyecto "Sistema POS" (`uaperjykllcugmgbeyph`)

## Marcapasos automático

En `.github/workflows/mantener-activo-pos.yml` hay una tarea programada que cada
6 horas visita la app y hace una consulta a la base de datos. Esto evita que
Supabase (plan gratuito) pause el proyecto tras 7 días sin actividad, que es lo
que causaba el "Error de conexión" en el login.

Si algún día vuelve a aparecer "Error de conexión":

1. Entrar a https://supabase.com/dashboard/project/uaperjykllcugmgbeyph
   (ver la página en inglés — el traductor automático del navegador rompe el panel).
2. Si dice "Project paused", presionar **Restore project** y esperar 5 minutos.

> Nota: GitHub desactiva las tareas programadas si el repositorio pasa 60 días
> sin movimiento; avisa por correo antes. Basta con presionar "Keep workflow
> enabled" en ese correo, o hacer cualquier cambio en el repositorio.

## Pendiente

- Subir aquí el código de la app desde v0.dev ("Push to GitHub") para tener respaldo.
