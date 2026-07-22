# Caso de Estudio: Sistema de Gestión para el Negocio de Comidas Rápidas "Sabor Express"

## Descripción del negocio

**Sabor Express** es un negocio local de comidas rápidas ubicado en un sector comercial de la ciudad. Ofrece productos como hamburguesas, perros calientes, salchipapas, papas fritas, bebidas y combos. Debido al aumento de clientes, el propietario desea desarrollar un sistema de información que permita organizar las ventas, controlar el inventario, administrar los pedidos y gestionar la información de clientes y empleados.

Actualmente, la mayor parte de la información se registra manualmente, lo que ocasiona errores en el control de inventario, demoras en la atención y dificultades para generar reportes de ventas.

---

## Funcionamiento del negocio

El negocio cuenta con un catálogo de productos. Cada producto posee:

- Código único.
- Nombre.
- Descripción.
- Precio de venta.
- Categoría a la que pertenece.

Las categorías incluyen, entre otras:

- Hamburguesas
- Perros Calientes
- Salchipapas
- Papas Fritas
- Bebidas
- Combos

### Inventario

Los ingredientes utilizados para preparar los productos se almacenan en un inventario. De cada ingrediente se registra:

- Código.
- Nombre.
- Unidad de medida.
- Cantidad disponible.
- Nivel mínimo de existencias.

Un producto puede requerir varios ingredientes y un ingrediente puede utilizarse en diferentes productos. Además, se registra la cantidad necesaria de cada ingrediente para elaborar un producto.

---

## Gestión de clientes

Los clientes pueden realizar pedidos:

- En el establecimiento.
- Por teléfono.
- Mediante plataformas de mensajería.

Para los clientes frecuentes se almacena la siguiente información:

- Documento de identidad.
- Nombre completo.
- Teléfono.
- Dirección.
- Correo electrónico.

---

## Gestión de pedidos

Cada pedido posee:

- Número consecutivo.
- Fecha y hora.
- Estado.
- Tipo de pedido.
- Valor total.

### Estados posibles

- Pendiente
- En preparación
- Listo
- Entregado
- Cancelado

### Tipos de pedido

- En mesa
- Para llevar
- Domicilio

Cada pedido puede contener uno o varios productos.

Para cada producto solicitado se registra:

- Cantidad.
- Precio aplicado al momento de la venta.
- Observaciones (por ejemplo: *sin cebolla* o *extra queso*).

---

## Gestión de empleados

El negocio cuenta con empleados que desempeñan diferentes funciones.

De cada empleado se registra:

- Número de identificación.
- Nombres.
- Apellidos.
- Cargo.
- Teléfono.
- Salario.
- Fecha de ingreso.

Los cargos existentes son:

- Administrador
- Cajero
- Cocinero
- Domiciliario

### Participación de los empleados

- El **cajero** registra el pedido.
- Uno o varios **cocineros** preparan el pedido.
- El **domiciliario** entrega únicamente los pedidos de tipo domicilio.

---

## Gestión de proveedores

Los ingredientes son suministrados por diferentes proveedores.

De cada proveedor se almacena:

- NIT.
- Nombre de la empresa.
- Persona de contacto.
- Teléfono.
- Dirección.
- Correo electrónico.

Un proveedor puede suministrar varios ingredientes y un ingrediente puede ser adquirido a diferentes proveedores.

Para cada relación proveedor–ingrediente se registra:

- Precio de compra.
- Fecha de la última adquisición.

---

## Reportes requeridos

El administrador necesita consultar información como:

- Ventas diarias.
- Ventas semanales.
- Ventas mensuales.
- Productos más vendidos.
- Clientes frecuentes.
- Ingredientes con bajo inventario.
- Pedidos realizados por cliente.
- Desempeño de los empleados.
- Compras realizadas a proveedores.

---

# Reglas de negocio

1. Cada producto pertenece únicamente a una categoría.
2. Una categoría puede contener muchos productos.
3. Un pedido debe contener al menos un producto.
4. Un cliente puede realizar muchos pedidos.
5. Un pedido pertenece a un solo cliente (si está registrado).
6. Cada pedido es registrado por un único cajero.
7. Un pedido puede ser preparado por uno o varios cocineros.
8. Solo los pedidos de domicilio son asignados a un domiciliario.
9. Un producto utiliza uno o varios ingredientes.
10. Un ingrediente puede formar parte de varios productos.
11. Un proveedor puede suministrar múltiples ingredientes.
12. Un ingrediente puede tener varios proveedores.
13. El precio almacenado en el detalle del pedido corresponde al valor vigente en el momento de la venta.
14. No puede prepararse un pedido si el inventario no dispone de los ingredientes necesarios.

---

# Objetivos del sistema

El sistema deberá permitir:

- Gestionar clientes.
- Gestionar empleados.
- Administrar productos y categorías.
- Controlar el inventario de ingredientes.
- Gestionar proveedores.
- Registrar compras de ingredientes.
- Registrar pedidos y sus detalles.
- Actualizar el estado de los pedidos.
- Generar reportes de ventas e inventario.

---

# Posibles entidades del Modelo Entidad-Relación

A partir del caso de estudio pueden identificarse las siguientes entidades:

| Entidad | Descripción |
|----------|-------------|
| Cliente | Personas que realizan pedidos. |
| Empleado | Personal del negocio. |
| Cargo | Clasificación del rol de un empleado. |
| Pedido | Venta realizada por un cliente. |
| DetallePedido | Productos incluidos en cada pedido. |
| Producto | Artículos disponibles para la venta. |
| Categoría | Clasificación de los productos. |
| Ingrediente | Insumos utilizados para preparar productos. |
| ProductoIngrediente | Relación entre productos e ingredientes. |
| Proveedor | Empresas que suministran ingredientes. |
| ProveedorIngrediente | Relación entre proveedores e ingredientes. |
| Compra | Registro de adquisiciones de ingredientes. |
| DetalleCompra | Ingredientes incluidos en una compra. |
| PreparaciónPedido | Relación entre pedidos y cocineros responsables de su preparación. |

---

# Objetivo académico

Este caso de estudio está diseñado para servir como base para el análisis y diseño de una base de datos relacional. A partir de él es posible construir un **Modelo Entidad-Relación (MER)** identificando:

- Entidades.
- Atributos.
- Llaves primarias.
- Llaves foráneas.
- Relaciones **1:1**, **1:N** y **N:M**.
- Entidades asociativas.
- Restricciones y reglas de negocio.
