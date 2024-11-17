# ***Atributos de calidad***
## Escalabilidad
### Q-1

El sistema debe ser capaz de soportar un aumento significativo de solicitudes solicitudes de productos en horas pico. Se espera del sistema que escale y proporcione una respuesta rápida y eficiente ante las solicitudes.

**Caso de uso que ataca**: UC-2

**Origen del estímulo**: Clientes (PC y móvil)

**Estimulo**: Clientes solicitando productos

**Artefacto**: Pagina web y aplicación de compras del celular
**Ambiente**:El sistema está en funcionamiento normal, pero en una hora pico de alta demanda
**Respuesta**: El sistema debe de mostrar al usuario la solicitud confirmada sin demoras
**Medida de respuesta**: El sistema debe mantener un tiempo de respuesta menor a 1 segundo para cada operación de pedido

### Q-2

El sistema debe tener la capacidad de gestionar las todas las incidencias debido a un incremento de situaciones imprevistas, como fallos masivos en camiones o condiciones climáticas adversas

**Caso de uso que ataca**: UC-6

**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 

## Performace

### Q-3

El sistema de pedidos sigue una secuencia estricta de tres fases: preprocesado del pedido, autorización y aceptación. Cada fase debe completarse correctamente antes de avanzar a la siguiente. El tiempo total para completar estas fases no debe exceder 1 segundo.
**Caso de uso que ataca**: UC-2
**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 
### Q-4:

El sistema de optimización de rutas gestiona el reparto de las flotas de transporte a los clientes y determina las rutas de los camiones. Para ello, utiliza dos algoritmos de optimización que calculan las rutas y se seleccionan dinámicamente según el nivel de demora de cada camión.

**Caso de uso que ataca**: UC-3,UC-4
**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 

## Disponibilidad
### Q-5:
Un cliente desea acceder a sus datos personales de un cliente. Se espera que esta operación se realice mientras el sistema funcione en condiciones normales y esté operativo.


**Caso de uso que ataca**: UC-1
**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 

### Q-6:
El administrador del sistema necesita consultar estadísticas en tiempo real (como estado de pedidos, camiones y clientes) para tomar decisiones operativas.

**Caso de uso que ataca**: UC-5
**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 

## Mantenibilidad

### Q-7

La lógica de negocio debe estar desacoplada, permitiendo realizar optimizaciones en los algoritmos de reparto o cambios en las rutas producidos por fallas durante el envío, sin afectar a otros envíos ni realizar cambios en otras partes del sistema.

**Caso de uso que ataca**: UC-3,UC-4
**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 

## Interoperabilidad

### Q-8

La integración con la pasarela de pago externa que 
proporciona la empresa MercadoLibre para garantizar la seguridad de los pagos y la 
compatibilidad con otros clientes

**Caso de uso que ataca**: UC-5,UC-7
**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 


## Seguridad

### Q-9

Los datos de los clientes deben estar protegidos contra accesos no autorizados, permitiendo su acceso solo al administradros del sistema con los cumplimiendo con las normativas de protección de datos.

**Caso de uso que ataca**: UC-1,UC-7
**Origen del estímulo**: 

**Estimulo**: 

**Artefacto**: 
**Ambiente**:
**Respuesta**: 
**Medida de respuesta**: 