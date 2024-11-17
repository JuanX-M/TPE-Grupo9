# ***Atributos de calidad***
## Escalabilidad
### Q-1

El sistema debe ser capaz de soportar un aumento significativo de solicitudes solicitudes de productos en horas pico. Se espera del sistema que escale y proporcione una respuesta rápida y eficiente ante las solicitudes.

**Caso de uso que ataca**: UC-2

**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Clientes solicitando productos

**Artefacto**: Pagina web y aplicación de compras del celular
**Ambiente**:El sistema está en funcionamiento normal, pero en una hora pico de alta demanda
**Respuesta**: El sistema escala automaticamente levantando los servicios necesarios para manejar la demanda de solicitudes
**Medida de respuesta**: El sistema debe mantener un tiempo de respuesta menor a 1 segundo para cada operación de pedido

### Q-2

El sistema debe tener la capacidad de gestionar todas las incidencias debido a un incremento de situaciones imprevistas, como fallos masivos en camiones o condiciones climáticas adversas

**Caso de uso que ataca**: UC-6

**Origen del estímulo**: Choque imprevisto o condiciones climaticas adversas

**Estimulo**: Situaciones imprevistas

**Artefacto**: Sistema
**Ambiente**: Sistema operando con normalidad
**Respuesta**: El sistema debe escalar su infraestructura, levantando nuevos servidores o ajustando su capacidad para manejar la gestion de incidencias.
**Medida de respuesta**: El sistema debe generar la misma cantidad de reportes que incidencias en menos de un minuto ocurrida la incidencia

## Performace

### Q-3

El sistema de pedidos sigue una secuencia estricta de tres fases: preprocesado del pedido, autorización y aceptación. Cada fase debe completarse correctamente antes de avanzar a la siguiente. El tiempo total para completar estas fases no debe exceder 1 segundo.
**Caso de uso que ataca**: UC-2
**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Solicitudes de productos

**Artefacto**: Pagina web y aplicación de celular
**Ambiente**: El sistema esta funcionando correctamente
**Respuesta**: El sistema completa cada fase
**Medida de respuesta**: El tiempo total para completar estas fases no debe exceder 1 segundo.
### Q-4:

El sistema de optimización de rutas gestiona el reparto de las flotas de transporte a los clientes y determina las rutas de los camiones. Para ello, utiliza dos algoritmos de optimización que calculan las rutas y se seleccionan dinámicamente según el nivel de demora de cada camión.

**Caso de uso que ataca**: UC-3,UC-4
**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Solicitudes de productos

**Artefacto**: Pagina web y aplicación de celular
**Ambiente**: El sistema esta funcionando correctamente
**Respuesta**: El sistema selecciona que algoritmo de optimización debe usarse segun la demora de los camiones
**Medida de respuesta**: El analisis de que algoritmo se debe usar no debe ser superior a un minuto

## Disponibilidad
### Q-5:
Un cliente desea acceder a sus datos personales. Se espera que esta operación se realice mientras el sistema funcione en condiciones normales y esté operativo.


**Caso de uso que ataca**: UC-1
**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Solicitud de acceso a datos personales

**Artefacto**: Pagina web y aplicación de celular
**Ambiente**: El sistema esta funcionando correctamente
**Respuesta**: El sistema debe permitir que los clientes accedan a sus datos sin interrupciones ni demoras
**Medida de respuesta**: El tiempo de acceso no debe ser mayor a un segundo

### Q-6:
El administrador del sistema necesita consultar estadísticas en tiempo real (como estado de pedidos, camiones y clientes) para tomar decisiones operativas.

**Caso de uso que ataca**: UC-5
**Origen del estímulo**: Administrador del sistema

**Estimulo**: Administrador realizando consultas de estadisticas

**Artefacto**: Pagina web
**Ambiente**: Sistema funcionando correctamente bajo demanda
**Respuesta**: El sistema genera reportes de estadisticas y se los envia al administrador
**Medida de respuesta**: El sistema envia los reportes al administrador de forma inmediata una vez se hayan generado los reportes

## Mantenibilidad

### Q-7

La lógica de negocio debe estar desacoplada, permitiendo realizar optimizaciones en los algoritmos de reparto o cambios en las rutas producidos por fallas durante el envío, sin afectar a otros envíos ni realizar cambios en otras partes del sistema.

**Caso de uso que ataca**: UC-3,UC-4
**Origen del estímulo**: Administrador del sistema

**Estimulo**: Realizacion de optimizaciones en los algoritmos de reparto o cambios en las rutas producidos por fallas durante el envío

**Artefacto**: Sistema
**Ambiente**: Sistema funcionando correctamente
**Respuesta**:  Los cambios realizados no deben afectar otras funcionalidades o envíos, deben poder aplicarse de manera aislada
**Medida de respuesta**: Aquellos cambios realizados deben desplegarse de forma inmediata

## Interoperabilidad

### Q-8

La integración con la pasarela de pago externa que 
proporciona la empresa MercadoLibre para garantizar la seguridad de los pagos y la 
compatibilidad con otros clientes

**Caso de uso que ataca**: UC-5,UC-7
**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Solicitud de pago

**Artefacto**: Pagina web y aplicación de celular
**Ambiente**: Sistema funcionando correctamente
**Respuesta**: El sistema verifica el saldo de la persona en su sistema y realiza el pago por medio de la pasarela de pago(MercadoLibre)
**Medida de respuesta**: La verificacion de los datos del cliente se debe de realizar en dos segundos y notificar al cliente que el pago se realizo de forma inmediata una vez validada la operación


## Seguridad

### Q-9

Los datos de los clientes deben estar protegidos contra accesos no autorizados, permitiendo su acceso solo al administrador del sistema con los cumplimiendo con las normativas de protección de datos.

**Caso de uso que ataca**: UC-1,UC-7
**Origen del estímulo**: Clientes (PC y móvil) o administrador del sistema

**Estimulo**: Intento de acceso 

**Artefacto**: Pagina web y aplicación de celular
**Ambiente**: Sistema funcionando correctamente
**Respuesta**: El sistema verifica si el usuario esta autorizado
**Medida de respuesta**: En caso de no tener autorizacion de acceso, se realiza una notificacion al administrador de forma inmediata