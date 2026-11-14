# Demostración en Cloudflare

- URL pública: https://hostalelroble.cimanexus.workers.dev/
- Cuenta: CIMA (cimanexus@gmail.com).
- Recurso: Worker `hostalelroble` con Static Assets, sin módulos de servidor.
- Archivos publicados: contenido de `dist/` del commit `b33ff177e14cfbbb0708b005a40389750e1bb6ef`.
- Fecha de publicación: 14 de noviembre de 2026.
- Despliegue: `3b9b0f9279064b71852d29a1f77f84d9`.

## Alcance

Demostración pública para presentar al cliente, sin backend, usuarios ni base de datos. El panel de prueba conserva cambios únicamente en el navegador del visitante y no modifica el sitio que ven otras personas.

Se conserva el aviso de propuesta de diseño y la etiqueta `noindex,nofollow`. Se comprobó la apertura sin inicio de sesión, la carga de las cuatro imágenes de la página y la apertura del panel de edición.

La publicación se realizó directamente mediante la API de Cloudflare. No hay despliegue automático configurado desde GitHub; los nuevos commits requieren otra publicación. No se modificó el sitio corporativo CIMA ni se crearon recursos Supabase.
