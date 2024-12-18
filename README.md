# ProtegeDNI

Esta aplicación web permite procesar imágenes de un DNI (Documento Nacional de Identidad) u otro documento (pasaporte, carnet de conducir, tarjeta de la seguridad social, etc.), para generar una copia en blanco y negro con marcas de agua y un patrón anti-fraude. Además, ofrece la posibilidad de ocultar manualmente datos sensibles “pintando” sobre la imagen resultante.

*Características

Soporte de formatos:
-Permite subir imágenes en formato PNG, JPG, JPEG y también ficheros PDF (en este último caso, se procesa la primera página del documento).

Marcas de agua:
-Convierte el documento a escala de grises.
-Añade un patrón semitransparente (rejilla) para dificultar la modificación.
-Añade una marca de agua diagonal con el texto "NO COMPARTIR".
-Añade texto adicional proporcionado por el usuario (el motivo de la copia) en la parte superior, central e inferior del documento.
-Edición manual: Tras generar el documento modificado, es posible "pintar" sobre la imagen con un rotulador virtual negro semitransparente para ocultar información sensible (como la fotografía o los números de serie).

Descarga del resultado: 
-Una vez finalizado el proceso y las modificaciones manuales, se puede descargar la imagen resultante.

*Requisitos

-Un navegador web moderno.
-Conexión a internet si se desea usar pdf.js desde un CDN (en caso de querer soporte para PDF).

*Uso

-Abre el fichero index.html en tu navegador.
-Sube una imagen o un PDF del DNI.
-Especifica el motivo por el que se facilita la copia (ejemplo: "Copia para registro en Hotel").
-Haz clic en "Procesar".
-Se generará la imagen en blanco y negro con las marcas de agua.
-(Opcional) Pasa el ratón sobre la imagen, manteniendo el botón pulsado para pintar sobre las zonas que quieras ocultar.
-Cuando estés satisfecho con el resultado, haz clic en "Descargar imagen procesada" para guardarla.

*Seguridad

-La página no guarda cookies
-Una vez el usuario descarga la imagen, la página se refresca y no se guarda ni la imagen suministrada ni la generada
-Se recomienda servir esta página a través de HTTPS o ejecutarla en local.
-Por defecto, los scripts externos (como pdf.js) se cargan desde CDN. Se puede añadir Subresource Integrity (SRI) para mejorar la seguridad.
-Si se monta en un servidor Web público, las cabeceras de seguridad (CSP, HSTS, X-Content-Type-Options, X-Frame-Options, etc.) deben configurarse a nivel de servidor web, no en el HTML.
-Si no se quiere soporte para PDF, se recomienda eliminar la llamada a pdf.js para cear un sistema totalmente aislado e independiente.

*Licencia

Está permitido su uso libremente.
