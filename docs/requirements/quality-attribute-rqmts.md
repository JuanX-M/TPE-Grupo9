# Atributos de Calidad y Casos de Uso Asociados

| **ID**   | **Quality Attribute**   | **Escenario**                                                                                                                                | **Caso de Uso Asociado** |
|----------|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| QA-1     | Performance             | El sistema debe manejar hasta 5,000 solicitudes simultáneas de clientes accediendo a sus datos personales con una latencia de < 2 segundos. | UC-1, UC-8               |
| QA-2     | Availability            | El servicio de pedidos debe tener un tiempo de actividad del 99.9%, garantizando que las tres fases del pedido se procesen correctamente.   | UC-2                     |
| QA-3     | Scalability             | El sistema debe soportar el procesamiento de hasta 50,000 pedidos por hora durante picos de alta demanda.                                   | UC-2, UC-7               |
| QA-4     | Security                | El sistema debe proteger los datos de rutas y repartos contra accesos no autorizados, asegurando que solo administradores tengan acceso.    | UC-3                     |
| QA-5     | Usability               | Los administradores deben poder visualizar estadísticas en tiempo real en menos de 5 segundos después de realizar una consulta.             | UC-4                     |
| QA-6     | Security                | Los datos de los clientes deben estar protegidos contra accesos no autorizados, aplicando cifrado tanto en tránsito como en reposo.         | UC-1, UC-8               |
| QA-7     | Interoperability        | La integración con la pasarela de pago MercadoLibre debe garantizar transacciones seguras.                                                  | UC-6                     |
| QA-8     | Maintainability         | La lógica de negocio debe estar desacoplada, permitiendo implementar nuevas optimizaciones en los algoritmos de reparto o cambios en las rutas producidos por fallas en durante el envio sin afectar a otros envios.| UC-3, UC-5               |
