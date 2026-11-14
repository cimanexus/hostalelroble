# El Roble · Propuesta CIMA

Sitio de prueba para validar una web a medida y un panel de edición reutilizable.

## Alcance

- Diseño adaptable a móvil y escritorio; fotografías auténticas extraídas del blog público del hostal.
- Textos e imágenes separados del diseño en `dist/content.json`.
- Panel generado a partir de la estructura de contenidos: cuatro combinaciones de color, cuatro fuentes, tres densidades de distribución, alineación por sección, tamaños y encuadres de imágenes.
- Edición con vista previa inmediata, borrador, guardado local, restauración, importación/exportación JSON y compresión de imágenes WebP.
- Consulta de fechas por WhatsApp. El envío lo realiza el visitante desde WhatsApp; no hay reservas confirmadas, pagos ni disponibilidad en tiempo real.

## Límites de esta prueba

El panel no es un administrador autenticado de producción. `localStorage` conserva la versión y el borrador exclusivamente en el navegador utilizado. Otras personas y dispositivos ven la versión inicial. La vista previa original en ChatGPT Sites tiene acceso privado. Este código exportado no incorpora ese control de acceso: en un alojamiento público, la página y el panel de prueba serán accesibles públicamente. El panel solo modifica contenidos locales y no escribe datos compartidos.

Para producción falta integrar autenticación, autorización y persistencia compartida (Supabase según la arquitectura acordada), almacenamiento de imágenes, versiones/borradores publicados y políticas de acceso. No se han creado cuentas ni modificado los servicios CIMA existentes. La prueba no debe presentarse como un CMS de producción.

## Fuentes y contenidos pendientes

Fuente: https://hostal-el-roble-algarrobo.blogspot.com/ y su página de reservas. Revisado el 14-11-2026. Las entradas del blog son de 2022. Dos fotos del inmueble utilizadas como referencia en propuesta privada; no se ha acreditado licencia para publicación comercial. Confirmar permiso y contenido con el propietario antes de lanzar.

No se publican estrellas hoteleras, calificación, precios, disponibilidad, estacionamiento ni políticas de mascotas o accesibilidad como hechos vigentes. El desayuno figura como información histórica por confirmar. La ilustración costera está identificada como esquema, no ubicación cartográfica exacta.

Inspiración de estructura hotelera: Casa Higueras (https://casahigueras.cl/) y Hotel Alaia (https://hotelalaia.com/). No se copiaron sus diseños, fotografías, marcas ni textos.

## Desarrollo

Sitio estático sin dependencias. Servir `dist/` por HTTP. No requiere build. Entrar con `?editar=1` o desde el pie de página para abrir el panel de prueba.

Los archivos JSON importados se validan contra las claves conocidas. La edición usa `textContent`; no se interpreta HTML del cliente. Las imágenes se restringen a HTTPS, activos locales o datos JPG/PNG/WebP. El prototipo no solicita credenciales ni guarda datos de visitantes.


## Publicación desde este repositorio

- Rama: `main`.
- Sitio estático sin framework ni instalación de dependencias.
- Directorio de publicación: `dist`.
- Comando de compilación: ninguno.
- No requiere variables de entorno en esta versión.
- Para revisión local: `python3 -m http.server 8080 --directory dist` y abrir `http://localhost:8080`.

Este repositorio contiene la propuesta aprobada visualmente, sin cambios de diseño. El traslado a GitHub no crea ni configura las cuentas de Cloudflare o Supabase. Para la etapa de producción, usar cuentas independientes y bajo control del cliente, conforme al modelo comercial de CIMA.

## Activos

La fuente Manrope se distribuye con su licencia SIL OFL 1.1 en `dist/assets/Manrope-OFL.txt`. La identidad y fotografías del hostal conservan sus derechos originales.
