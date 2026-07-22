Aquí tienes un caso de estudio más sencillo, ideal para un ejercicio básico de Modelo Entidad-Relación (MER).

Caso de estudio: Restaurante de comidas rápidas "Sabor Express"
Contexto

"Sabor Express" es un pequeño restaurante de comidas rápidas que vende hamburguesas, perros calientes, papas fritas y bebidas.

Los clientes realizan pedidos en el mostrador. Cada pedido puede incluir uno o varios productos y se registra la fecha en que fue realizado. El sistema debe calcular el valor total del pedido según los productos y las cantidades solicitadas.

Cada producto tiene un código, nombre, precio y categoría. Un mismo producto puede formar parte de diferentes pedidos.

El restaurante cuenta con empleados que atienden a los clientes. De cada empleado se registra su identificación, nombre y cargo. Cada pedido es atendido por un solo empleado, pero un empleado puede atender muchos pedidos.

Al finalizar la compra, el cliente realiza un único pago, que puede ser en efectivo, tarjeta o transferencia.

Reglas de negocio
Cada producto tiene un código único.
Un pedido debe contener al menos un producto.
Un producto puede estar en varios pedidos.
Cada pedido es atendido por un solo empleado.
Un empleado puede atender muchos pedidos.
Cada pedido tiene un único pago.
El total del pedido corresponde a la suma del precio de los productos por la cantidad solicitada.

Este caso permite identificar fácilmente entidades como Producto, Pedido, Empleado, Pago y la entidad asociativa DetallePedido, además de definir sus relaciones y cardinalidades.
