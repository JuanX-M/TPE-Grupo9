# ADR 001: Migración de una Arquitectura Monolítica a Microservicios para una Compañía de Productos Alimenticios  

## Contexto  
La compañía actualmente opera con un sistema monolítico que utiliza dos bases de datos SQL:  
- **Base de Clientes**: Contiene datos personales de clientes y pagos.  
- **Base de Pedidos**: Almacena los datos de pedidos y su información relacionada.  

El sistema soporta clientes en PC y móvil, pero la arquitectura actual es rígida y difícil de evolucionar. Esto limita la escalabilidad y la capacidad de adaptación a las necesidades del negocio.  

Para solucionar estas limitaciones, se propone migrar a una arquitectura basada en microservicios que permita:  
- Desacoplar funcionalidades críticas y no críticas.  
- Mejorar la escalabilidad y modificabilidad del sistema.  

### Módulos funcionales actuales  
1. **Clientes (Crítico)**: Gestiona los datos personales de los clientes.  
2. **Pedidos (Semi-Crítico)**: Procesa pedidos mediante un flujo de tres fases: preprocesamiento, autorización y aceptación.  
3. **Reparto y rutas (Crítico)**: Gestiona la logística, incluyendo optimización de rutas de transporte.  
4. **Estadísticas (No Crítico)**: Proporciona información sobre pedidos y la logística de la flota.  
5. **Incidencias (Semi-Crítico)**: Reporta problemas como fallas en la entrega o averías de vehículos.  
6. **Pagos (Crítico)**: Utiliza una pasarela de pago externa para garantizar transacciones seguras.  

## Decisión  
La migración se realizara de manera gradual utilizando el patrón Strangler. En cada fase, se reemplazarán progresivamente partes del sistema monolítico por microservicios independientes. Este enfoque permite que el sistema siga funcionando durante todo el proceso de transición, garantizando la continuidad del negocio mientras se realiza la modernización de manera incremental y controlada.

## Razonamiento  
Una migración en fases ofrece varias ventajas:  
- **Control de riesgos**: Permite abordar de manera incremental los desafíos técnicos y organizacionales de la migración.  
- **Continuidad operativa**: Garantiza que el sistema esté funcional durante todo el proceso de transición.  
- **Priorización**: Se pueden abordar primero los módulos críticos, asegurando que las funcionalidades esenciales estén optimizadas lo antes posible.  

### Primera fase propuesta  
La fase inicial incluirá los módulos más críticos:  
- **Clientes**: Proporciona una base sólida para manejar la información esencial de los usuarios.  
- **Pagos**: Mejora la seguridad y confiabilidad de las transacciones financieras.  

## Alternativa Rechazada 
Migración total en una sola fase: Rechazada por ser de alto riesgo y complejidad. Migrar todos los módulos a la vez podría generar interrupciones operativas significativas, una carga de trabajo excesiva y dificultades para validar cambios de forma incremental.

## Estado  
Propuesta.  

## Consecuencias  
### Resultados positivos  
- Mejora de la escalabilidad y el rendimiento en servicios críticos.  
- Progreso incremental con validación en cada fase, reduciendo riesgos.  
- Simplificación del mantenimiento y la integración de nuevas funcionalidades.  

### Desafíos  
- Diseñar un plan de migración claro. 
- Asegurar la compatibilidad entre el sistema monolítico y los microservicios durante la transición.  
- Capacitar al equipo en herramientas y frameworks clave, como Docker y Spring Boot.  
