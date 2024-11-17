# ADR 01: Migración de una Arquitectura Monolítica a Microservicios  

## Contexto y Declaración del Problema  
La compañía opera con un sistema monolítico que utiliza dos bases de datos SQL:  
* **Base de Clientes**: Contiene datos personales de clientes y pagos.  
* **Base de Pedidos**: Almacena datos de pedidos y su información relacionada.  

Esta arquitectura es rígida, difícil de evolucionar y limita la escalabilidad y la capacidad de adaptación a nuevas necesidades.  

## Drivers de decisión  
* R-1
* QA-7: Modificabilidad

## Opciones Consideradas  
1. **Migración total en una sola fase.**  
2. **Migración gradual utilizando el patrón Strangler.**  

## Resultado de la Decisión  
**Opción elegida:** Migración gradual utilizando el patrón Strangler, porque:  
* Permite realizar una transición controlada.
* Mantiene el sistema funcional durante la transición.  
* Facilita priorizar módulos críticos, logrando mejoras inmediatas en funcionalidades esenciales. 

### Consecuencias  
**Positivas, porque:**  
* Mejora la escalabilidad y el rendimiento de servicios clave desde el inicio.  
* Simplifica el mantenimiento y la integración de nuevas funcionalidades al desacoplar partes del sistema.  
* Reduce riesgos al permitir validaciones incrementales en cada fase.  

**Negativas, porque:**  
* Requiere diseñar un plan de migración para evitar problemas de compatibilidad.  
* Genera complejidad al mantener operativos el monolito y los microservicios simultáneamente.  
* Costo extra para aprender nuevas tecnologías como Docker y Spring Boot.  

## Confirmación  
Aceptada
