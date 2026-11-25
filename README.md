# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-8
1. Entidades Principales y Tablas del Sistema
deposito:

Estructura mejorada para el control de almacenes y su personal responsable.

Campos: id_deposito (clave primaria), nombre, direccion, numero_calle, responsable_cargo, responsable_nombre y apellido.

producto:

Catálogo general de artículos disponibles.

Campos: codigo_barras (clave primaria), descripcion, stock global, peso y dimensiones.

proveedor:

Registro de fabricantes y proveedores externos.

Campos: cuit (clave primaria), razon_social, pais_origen, telefono y correo.

2. Tablas Intermedias (Relaciones Muchos a Muchos)
producto_proveedor:

Tabla asociativa que conecta qué productos suministra cada proveedor y el costo asociado.

Campos: Clave primaria compuesta por (codigo_barras, cuit) y el campo precio.

stock_deposito:

Tabla asociativa que gestiona el inventario distribuido por depósito.

Campos: Clave primaria compuesta por (id_deposito, codigo_barras) y el atributo stock_disponible.

3. Restricciones e Integridad Referencial (Foreign Keys)
El script configura las reglas de validación para garantizar la consistencia relacional mediante las siguientes restricciones:

producto_proveedor_codigo_barras_fkey: Vincula el código de barras con el catálogo de productos.

producto_proveedor_cuit_fkey: Relaciona el CUIT con la tabla de proveedores.

stock_deposito_codigo_barras_fkey: Conecta el stock por depósito con los productos registrados.

IMAGEN DE EJEMPLO DE CONSULTA:
<img width="1337" height="362" alt="image" src="https://github.com/user-attachments/assets/217c6935-d0ef-4830-80b8-85765192cdae" />
