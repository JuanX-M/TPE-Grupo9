
# ***Actores***

- Cliente
- Administrador
- Base de datos de Clientes:
- Base de datos de Pedidos:
- Sistema de monitoreo
- Sistema de pago externo(MercadoLibre)
- Repartidor

<br>

# Casos de Uso

## <UC-1> Gestión de Datos de Clientes
**Descripción**: Permite a los clientes gestionar su información personal, como datos de contacto, dirección y detalles de pago.
**Actores**: [Cliente], [Base de datos de Clientes].

## <UC-2> Realizar Pedido
**Descripción**: Los clientes pueden realizar pedidos de productos, con un límite de 3 intentos para completar el pedido, pasando por las fases de preprocesado, autorización y aceptación.  
**Actores**: [Cliente], [Base de datos de Pedidos].

## <UC-3> Gestión de Reparto y Rutas
**Descripción**:   Los administradores gestionan las rutas de reparto y optimizan los algoritmos de distribución de los camiones según la demora.  
**Actores**: [Administrador],[Sistema de monitoreo],[Base de datos de Pedidos].

## <UC-4> Generación de Estadísticas
**Descripción**: Proporciona datos en tiempo real sobre pedidos, clientes y el estado de los camiones.  
**Actores**: [Administrador], [Sistema de monitoreo],[Base de Datos de Pedidos].

## <UC-5> Gestión de Incidencias
**Descripción**: Permite registrar y gestionar problemas relacionados con las rutas, como retrasos o fallas en los camiones.  
**Actores**: [Repartidor], [Administrador],[Base de Datos de Pedidos].

## <UC-6> Procesamiento de Pagos
**Descripción**: Gestiona los pagos de los clientes a través de la pasarela de pago de MercadoLibre, asegurando la seguridad y compatibilidad.
**Actores**: [Cliente], [Sistema de pago externo(MercadoLibre)], [Base de datos de Clientes].

## <UC-7> Actualización de Inventarios
**Descripción**: Gestiona la información de inventarios actualizada en función de los pedidos realizados y entregados.  
**Actores**: [Administrador], [Sistema de monitoreo], [Base de datos].


## <UC-8> Gestionar Información de Clientes
**Descripción**:  Los administradores pueden acceder, actualizar y gestionar los datos de los clientes.
**Actores**: [Administrador], [Base de Datos de Clientes].


