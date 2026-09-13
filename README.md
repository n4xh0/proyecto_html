# El Terremoto

Proyecto educativo de una fonda con carta, carrito y mantenedor de productos.

## Estructura

- `index.html`: inicio, receta, carta filtrable y carrito de demostración.
- `login.html`: formulario de acceso administrativo local.
- `productos.html`: mantenedor para agregar, editar y eliminar productos.
- `img/`: imágenes del proyecto.
- `config.example.js`: plantilla sin contraseña para la demostración local.

El CSS y JavaScript están incorporados en las páginas HTML. No necesita instalación de dependencias.

## Ejecutar la demostración

1. Descarga o clona el proyecto.
2. Copia `config.example.js` como `config.local.js`.
3. En el archivo local, coloca una contraseña ficticia en `password`. No reutilices contraseñas reales.
4. Sirve la carpeta con un servidor estático local, por ejemplo Live Server de tu editor. Abre `index.html` desde ese servidor y usa siempre el mismo origen.
5. Para el mantenedor, entra con el usuario `admin` y la contraseña ficticia configurada localmente.

`config.local.js` está excluido mediante `.gitignore`. Sin ese archivo, la carta funciona y el login informa que falta configuración. No publiques ese archivo ni lo incluyas en una subida manual.

## Alcance

Los productos y el carrito se guardan en `localStorage`; la sesión, en `sessionStorage`, con vencimiento de 30 minutos. Los datos pertenecen al navegador y al origen utilizados. No existe un servidor, base de datos compartida, pago ni envío real de pedidos.

La autenticación es una simulación educativa del lado del cliente. Separar la clave del repositorio evita incluirla en Git, pero no convierte esta página en una autenticación segura: cualquier configuración servida al navegador puede ser leída. Una versión real necesita autenticación y autorización en el servidor.

## Preparación para publicación

Se retiró del HTML la contraseña de demostración que tenía el original y se agregó una plantilla vacía y `.gitignore`. No se incluyeron archivos locales de credenciales. La carpeta original del Escritorio se conserva sin cambios.
