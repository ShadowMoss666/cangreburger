# CangreBurger
Página web para hamburguesería local, interactiva, con el objetivo de mostrar los menús, promociones o demás aspectos que se requiera. Permitiendo seleccionar modalidad de compra (ya sea delivery o local) y comunicando directamente por whatsapp con el comercio.

## Objetivo del Proyecto
Proveer una experiencia de compra ágil, atractiva y moderna desde dispositivos móviles y de escritorio, optimizando el canal de ventas principal del comercio.

### Requerimientos Funcionales
#### RF-01 Modalidad de compra
* RF-01.1: Al ingresar a la plataforma, se debe permitir al usuario elegir la modalidad de compra.
* RF-01.2: En caso de elegir local, se debe seleccionar el local.
* RF-01.3: En caso de elegir delivery, se debe seleccionar la dirección de envío.
* RF-01.4: La selección debe persistir durante la sesión.

#### RF-02 Catálogo y Menú interactivo
* RF-02.1: Se debe permitir al usuario visualizar los diferentes tipos de menús, ya sea de hamburguesas, promociones, postres y lo que sea oportuno.
* RF-02.2: Cada producto debe mostrar:
  * Imagen promocional.
  * Nombre del producto.
  * Precio actualizado.
  * Lista detallada de ingredientes (al clickear en el producto).
  * Tag o insignias (promo, más vendido, nuevo, etc).
 
#### RF-03 Carrito de compras
* RF-03.1: Botón de "Agregar al carrito" en cada producto.
* RF-03.2: Panel desplegable o pantalla de resumen del carrito.
* RF-03.3: Permitir modificar cantidades o eliminar ítems individuales.
* RF-03.4: Campo de texto para notas o aclaraciones por producto (sin x ingrediente).
* RF-03.5: Cálculo en tiempo real del subtotal y total de la compra.

#### RF-04 Checkout y redirección a Whatsapp
* RF-04.1: Formulario de datos basicos:
  * Nombre del cliente.
  * Dirección de entrega (solo si seleccionó Delivery).
  * Forma de pago.
* RF-04.2: Botón de "Confirmar y Enviar pedido" que genera una URL con el esquema de mensaje para whatsapp.
* RF-04.3: Redirección automática al chat oficial de la hamburguesería con el mensaje formateado (para poder editar si se lo desea).

### Requerimientos No Funcionales
* RNF-01 UX/UI: Interfaz responsive.
* RNF-02 Rendimiento: Carga rápida y transiciones fluidas en dispositivos móviles.
* RNF-03 Arquitectura: Aplicación de una sola página (SPA).

## Estructura del mensaje de whatsapp
El mensaje generado y enviado al whatsapp del local sigue la siguiente plantilla:
```text
 🍔 *¡NUEVO PEDIDO!*
--------------------------------
📍 *Modalidad:* Delivery / Local
👤 *Cliente:* Juan Pérez
🏠 *Dirección:* Av. Siempre Viva 123 (Solo en Delivery)
💳 *Forma de Pago:* Transferencia

📋 *DETALLE DEL PEDIDO:*
• 2x Doble Cheeseburger (\$12.000)
  _Nota: Una sin cebolla_
• 1x Combo Promocional 2 (\$7.500)
• 1x Sundae Dulce de Leche (\$2.500)

--------------------------------
💰 *TOTAL A PAGAR:* \$22.000
