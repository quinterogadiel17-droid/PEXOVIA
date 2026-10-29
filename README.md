# PEXOVIA

Sitio web estático multipágina para una marca ficticia de hamburguesas y comida rápida. Interfaz en español, precios de ejemplo en pesos colombianos y compra completamente demostrativa.

## Tecnologías

HTML5, CSS3 y JavaScript ES6. No requiere frameworks, paquetes ni backend.

## Ejecutar

Abre el directorio con cualquier servidor estático local. Por ejemplo, con Python:

```bash
python -m http.server 8000
```

Luego visita `http://localhost:8000`. También puedes abrir `index.html` directamente, aunque un servidor local ofrece una experiencia más consistente.

## Estructura

- `index.html`: inicio y productos destacados.
- `pages/menu.html`: búsqueda, filtros y ordenamiento.
- `pages/producto.html?id=BUR-001`: ficha configurable reutilizable.
- `pages/promociones.html`: combos del catálogo.
- `pages/carrito.html`: carrito, checkout ficticio y confirmación local.
- `pages/nosotros.html`: historia y valores ficticios.
- `pages/contacto.html`: formulario validado localmente.
- `js/data.js`: catálogo y promociones centralizados.
- `js/app.js`: navegación, render, carrito y formularios.
- `css/styles.css`: estilos globales y responsive.
- `assets/`: imágenes adjuntas para el sitio.

## Catálogo

Edita el arreglo `PRODUCTS` en `js/data.js`. Cada producto define ID, nombre, categoría, precio entero COP, descripción, imagen, ingredientes, destacado y opciones. Los precios de tarjeta, detalle, carrito y pedidos se derivan del mismo catálogo. Las promociones están definidas en `PROMOS` y los artículos de combo en el propio catálogo.

## Datos locales

- `pexoviaCart`: líneas de carrito y opciones.
- `pexoviaOrders`: hasta 30 pedidos ficticios guardados localmente.
- `pexoviaOrderSequence`: secuencia demostrativa del navegador.

El navegador controla estos datos y no se sincronizan con otros dispositivos.

## Funciones simuladas y límites

El carrito persiste con `localStorage`; el domicilio de demostración es COP $3.000 cuando hay artículos. Finalizar genera un número ficticio y una confirmación en este navegador. No hay pagos, envío de pedidos, correo, autenticación ni backend. Los teléfonos, correo, horarios e historia son ilustrativos. Las opiniones de clientes no se presentan como reales.

## Revisión manual sugerida

1. Agrega un producto desde inicio, menú y promoción.
2. Cambia la búsqueda/categoría/orden en el menú y abre distintos detalles con `?id=`.
3. Personaliza un producto, ajusta cantidades y recarga para confirmar persistencia.
4. Elimina líneas, vacía el carrito y completa un pedido de prueba.
5. Prueba el formulario de contacto con datos inválidos y válidos.
6. Revisa menú móvil y navegación con teclado.

No se ejecutaron pruebas automatizadas; el proyecto no tiene configuración de testing.
