# ADR 02: Comunicación entre Microservicios mediante Servicios REST 

## Estado  
Aceptada.


## Contexto y Declaración del Problema  
Como parte de la migración de la arquitectura monolítica a una basada en microservicios para la compañía de productos alimenticios, hay que establecer cómo se comunicarán los servicios. 

## Drivers de decisión  
* R-1
* **R-2**: Necesidad de mejorar la escalabilidad y la flexibilidad.

## Opciones Consideradas  
1. **Comunicación mediante mensajes**: Usar un sistema de mensajes o eventos para manejar la comunicación entre microservicios.
3. **Servicios REST a través de solicitudes HTTP**: Implementar una arquitectura basada en REST utilizando solicitudes HTTP y respuestas en formato JSON.

## Resultado de la Decisión  
**Opción elegida:** Servicios REST a través de solicitudes HTTP, porque:  
* Es ampliamente soportado y compatible con aplicaciones web y móviles existentes.  
* Permite una escalabilidad independiente de los servicios al ser fácil de replicar.  
* Facilita la independencia de los servicios, lo que resulta esencial en una arquitectura de microservicios.

### Consecuencias  
**Positivas, porque:**  
* Compatible con aplicaciones web, móviles y servicios externos.  
* El uso de métodos HTTP y respuestas JSON proporciona una estructura clara de comunicación.  
* REST es ampliamente soportado por herramientas y frameworks modernos.  

**Negativas, porque:**  
* A medida que aumenta la carga de trabajo, se pueden generar cuellos de botella. 
* La latencia de las comunicaciones puede ser un problema, especialmente si el sistema se encuentra bajo alta demanda.
