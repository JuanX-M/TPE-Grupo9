
# ***Actores***

- Clientes PC y movil
- Administrador del sistema

<br>

# Restricciones:

## R-1: 
**Descripción**: El nuevo sistema debe ser una arquitectura basada en microservicios.

## R-2:  
**Descripción**: El acceso a los datos en el nuevo sistema debe ser por medio de protocolos HTTP/REST-
# Casos de Uso

## UC-1: Acceder a datos personales
**Descripción**: Los clientes (PC y móvil) y administrador del sistema deben de acceder a los datos personales de los clientes (alojados en la base de datos Clientes) para realizar consultas, verificar o modificar ciertos datos.

## UC-2: Solicitar pedidos
**Descripción**: Los clientes (PC y movil) deben de poder realizar pedidos a la compañía de productos.

## UC-3: Gestion de reparto
**Descripción**: El administrador del sistema debe poder visualizar cómo el sistema asignó la distribución de productos entre los repartidores.

## UC-4: Gestion de rutas
**Descripción**: El administrador del sistema debe de poder visualizar cómo el sistema calculo las rutas de recorrido para los repartidores.

## UC-5: Generar reportes estadisticos
**Descripción**: El administrador del sistema puede acceder a reportes detallados sobre estadísticas generadas a partir de los estados de los pedidos, situación en tiempo real de los camiones e información de los clientes.

## UC-6: Obtener reportes de incidencias
**Descripción**: El administrador del sistema debe poder recibir incidencias ocurridas durante el reparto de los productos alimenticios.

## UC-7: Realizar pagos
**Descripción**: Los clientes (PC y movil) deben de poder realizar pagos seguros utilizando una pasarela de pagos externa integrada al sistema.
