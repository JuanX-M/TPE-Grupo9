# ***Atributos de calidad***
## Escalabilidad

### Q-1

El sistema debe ser capaz de soportar un aumento significativo de solicitudes de productos en horas pico. Se espera del sistema que escale y proporcione una respuesta de las solicitudes en menos 1 segundo.

**Caso de uso que ataca**: UC-2

**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Clientes solicitando productos

**Artefacto**: Sistema

**Ambiente**:El sistema se encuentra bajo alta demanda de solicitudes.

**Respuesta**: El sistema escala automaticamente levantando los servicios necesarios para manejar la demanda de solicitudes.

**Medida de respuesta**: El sistema debe mantener un tiempo de respuesta menor a 1 segundo para cada solicitud.

## Performace

### Q-2

El sistema de pedidos sigue una secuencia estricta de tres fases: preprocesado del pedido, autorización y aceptación. Cada fase debe completarse correctamente antes de avanzar a la siguiente. El tiempo total para completar estas fases no debe exceder 1 segundo.
**Caso de uso que ataca**: UC-2

**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Solicitudes de productos.

**Artefacto**: Pagina web y aplicación de celular.

**Ambiente**: El sistema esta funcionando correctamente.

**Respuesta**: El sistema completa cada fase.

**Medida de respuesta**: El tiempo total para completar estas fases no debe exceder 1 segundo.

### Q-3:

Un conductor quiere saber la ruta de reparto, el sistema de reparto y rutas debe determinar la ruta optima según el nivel de demora de cada camión en menos de 1 minuto.

**Caso de uso que ataca**: UC-3,UC-4.

**Origen del estímulo**: Conductor.

**Estimulo**: Solicitud de ruta de reparto.

**Artefacto**: Sistema de reparto y rutas.

**Ambiente**: El sistema esta funcionando correctamente.

**Respuesta**: El sistema determina la ruta a utilizar.

**Medida de respuesta**: La asignacion de ruta se realiza en un tiempo menor a 1 minuto.

### Q-4:

Un cliente desea acceder a sus datos personales. Se espera que esta operación se realice mientras el sistema funcione en condiciones normales con un tiempo de respuesta de 1 segundo

**Caso de uso que ataca**: UC-1.

**Origen del estímulo**: Clientes (PC y móvil).

**Estimulo**: Solicitud de acceso a datos personales.

**Artefacto**: Sistema.

**Ambiente**: El sistema esta funcionando correctamente.

**Respuesta**: El sistema debe permitir que los clientes accedan a sus datos sin interrupciones ni demoras.

**Medida de respuesta**: El tiempo de acceso no debe ser mayor a un segundo.

## Usabilidad

### Q-5:

El administrador del sistema necesita consultar informacion valiosa (como estado de pedidos, camiones y clientes) de manera rapida, para tomar decisiones operativas.

**Caso de uso que ataca**: UC-5.

**Origen del estímulo**: Administrador del sistema.

**Estimulo**: Administrador realizando consultas de estadisticas.

**Artefacto**: Sistema de reportes estadisticos.

**Ambiente**: Sistema funcionando correctamente.

**Respuesta**: El sistema genera reportes de estadisticas y se los envia al administrador.

**Medida de respuesta**: El sistema envia los reportes al administrador en menos de 30 segundos.

## Modificabilidad

### Q-6

La lógica de negocio debe estar desacoplada, permitiendo realizar cambios rapidamente en sus dominios sin afectar a otras partes del sistema.

**Caso de uso que ataca**: UC-3,UC-4.

**Origen del estímulo**: Equipo de desarrolladores

**Estimulo**: Cambios en el sistema.

**Artefacto**: Sistema.

**Ambiente**: Sistema funcionando con normalidad.

**Respuesta**:Los cambios realizados se aplican de manera aislada sin afectar a otras funcionalidades del sistema.

**Medida de respuesta**: Los cambios deben de poder realizarse en menos de 1 mes.

## Interoperabilidad

### Q-7

El sistema de pago debe aceptar la integración con la pasarela de pago externa que proporciona la empresa MercadoLibre para garantizar la seguridad de los pagos y compatibilidad con otros clientes.

**Caso de uso que ataca**: UC-5,UC-7.

**Origen del estímulo**: Clientes (PC y móvil).

**Estimulo**: Solicitud de pago.

**Artefacto**: Sistema de pago.
**Ambiente**: Sistema funcionando correctamente.

**Respuesta**: El sistema verifica el saldo de la persona en su sistema y realiza el pago por medio de la pasarela de pago(MercadoLibre).

**Medida de respuesta**: La verificacion de los datos del cliente y el pago se deben de realizar en menos de 5 segundos.