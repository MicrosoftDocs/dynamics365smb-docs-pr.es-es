---
title: Trabajar con ingresos recurrentes
description: Conozca las opciones disponibles para automatizar el envío de facturas de suscripción a sus clientes y registre ingresos recurrentes.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'recurring, invoicing, subscription, billing'
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: bholtorf
---
# Trabajar con ingresos recurrentes en [!INCLUDE[prod_short](includes/prod_short.md)]

Muchas empresas están pasando de un modelo de ingresos de negocio en el que los ingresos se obtienen de la compra única de un cliente a un modelo de suscripción en el que los ingresos se realizan de forma periódica a cambio de un acceso constante a la entrega de un bien o servicio.
[!INCLUDE[prod_short](includes/prod_short.md)] tiene las siguientes opciones para automatizar la manera en que envía las facturas de suscripción a sus clientes y registra ingresos recurrentes. 

## Registrar ingresos con un diario general periódico

Un diario periódico es un diario general con campos específicos para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno, como el alquiler, las suscripciones, la electricidad o la calefacción. Al usar estos campos para las transacciones periódicas, puede registrar importes tanto fijos como variables. En un diario periódico, los movimientos que se van a registrar con regularidad sólo hay que escribirlos una vez. Por tanto, las cuentas, las dimensiones, los valores de dimensiones, etc. que se introduzcan permanecerán en el diario después del registro. Si hay que hacer algún cambio, puede realizarlo en cada registro.

### Por qué usar esta opción

Con esta opción, se definen períodos de facturación flexibles con [Fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

Sin embargo, con esta opción, no puede imprimir ni enviar facturas en la versión predeterminada de [!INCLUDE[prod_short](includes/prod_short.md)].  

Para obtener más información, consulte [Trabajar con diarios periódicos](ui-work-general-journals.md#work-with-recurring-journals).  

## Crear varias facturas basadas en un diario periódico de proyecto

El diario periódico de proyecto es una alternativa más avanzada al diario general. Define Artículos, Recursos y Cuentas, que deben repetirse para cada trabajo, y especifica la frecuencia de periodicidad.  

Después de registrar un diario periódico de proyecto, puede crear varias facturas con la tarea **Crear factura de venta de proyecto**. Puede revisar y registrar facturas creadas en la página **Facturas de venta**.

### Por qué usar esta opción

Con esta opción, sigue el procedimiento de facturación estándar con todos los beneficios, incluidos los diseños estándar y del cliente para las preferencias de comunicación. También puede definir precios para cada trabajo individualmente.

Sin embargo, para cada nuevo cliente, debe crear un nuevo trabajo y agregar líneas al diario periódico. 

Para obtener más información, consulte [Crear líneas de diario de proyectos](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) y [Crear varias facturas de venta de proyecto](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## Crear varias facturas de venta basadas en líneas de ventas periódicas

Si suele necesitar crear líneas de ventas y de compras con información similar, puede configurar líneas de venta periódicas que puede insertar en documentos de ventas y compras periódicas, por ejemplo, para órdenes de reposición periódicas. Utilice el trabajo por lotes **Crear facturas de venta periódicas** para crear facturas de venta según las líneas de venta periódicas asignadas a los clientes y con fechas de registro dentro de las fechas de inicio y fin de validez que especifique en las líneas de ventas periódicas.  

### Por qué usar esta opción

Con esta opción, puede asignar las mismas líneas recurrentes a varios clientes. Puede definir el período de validez de las líneas de venta periódicas para un cliente específico. Puede asignar varias líneas periódicas al mismo cliente y todas se incluirán en la factura.

Sin embargo, no hay forma de establecer precios fijos para los artículos porque [!INCLUDE[prod_short](includes/prod_short.md)] utilizará los precios reales y el descuento válido en la fecha del documento, tratando de encontrar la mejor combinación que ofrezca el precio más bajo.  

Para obtener más información, vea [Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md).

## Facturas periódicas con contrato de servicio

Un contrato de servicio contiene los acuerdos de contrato de servicio entre sus clientes y su empresa. Los contratos de servicio incluyen acuerdos de servicio y los productos de servicio de los que se realiza el servicio como parte del contrato.  

Puede definir la fecha inicial del contrato, el período de la factura, si el contrato es de prepago o no, las especificaciones de actualización de precios si planea cambiar los precios mientras el contrato está activo. Puede usar artículos de servicio o artículos en líneas de contrato de servicio.
Puede crear plantillas de contrato para definir la creación de determinados tipos de contratos.  

### Por qué usar esta opción

Con esta opción, utiliza una parte de la funcionalidad avanzada de administración de servicios que no se limita a la emisión de facturas periódicas, sino que también respalda las operaciones de taller de reparación y servicio de campo.

Sin embargo, esta opción requiere la licencia Premium. Es posible que la configuración de la gestión del servicio y su mantenimiento no ofrezca grandes ventajas en escenarios de suscripción más sencillos.  

Para obtener más información, consulte [Trabajar con contratos de servicio y ofertas de contrato de servicio](service-how-to-create-service-contracts-and-service-contract-quotes.md) y [Facturar varios contratos de servicio](service-how-create-invoices.md#to-invoice-several-service-contracts).

## Características relacionadas
Hay varias capacidades relacionadas en [!INCLUDE[prod_short](includes/prod_short.md)].

### Pedidos abiertos de venta

Los pedidos abiertos de venta constituyen un marco de trabajo para establecer un acuerdo a largo plazo entre la empresa y un cliente.
Normalmente, un pedido abierto se utiliza cuando un cliente se ha comprometido a comprar grandes cantidades que se van a entregar en varios envíos más pequeños durante un periodo de tiempo determinado. A menudo, los pedidos abiertos sólo incluyen un producto con fechas de entrega predeterminadas. El motivo principal para utilizar un pedido abierto en lugar de un pedido de venta es que las cantidades especificadas en un pedido abierto no afectan a la disponibilidad de los artículos. Sin embargo, se puede utilizar con fines de planificación.

#### Por qué usar esta opción

Con esta opción, utiliza la demanda anticipada, por lo que la información se considera durante las rutinas de planificación normales. Para obtener más información, consulte [Previsiones de demanda y pedidos abiertos](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Sin embargo, la versión predeterminada no ofrece la posibilidad inmediata de procesar varios pedidos abiertos en bloque.

Consulte [Trabajar con pedidos de venta abiertos](sales-how-to-create-blanket-sales-orders.md) para obtener más información.

### Pedidos periódicos (Noruega)

Puede utilizar pedidos periódicos para crear plantillas de pedidos abiertos para que los pedidos de ventas se puedan crear según los intervalos de fechas que defina. Por ejemplo, si entrega el mismo pedido de ventas cada dos semanas, puede usar un pedido abierto de venta y crear pedidos periódicos.
Puede usar grupos periódicos para definir un rango de parámetros que muestren cómo realiza los pedidos. Estos grupos se asignan a pedidos abiertos que deben crearse con frecuencia. Para crear los pedidos periódicos, deberá ejecutar periódicamente el proceso de creación de pedidos periódicos. 

#### Por qué usar esta opción

Con esta opción, puede elegir entre precios fijos y "mejores".

Sin embargo, solo está disponible en Noruega. El período de validez se puede definir en el nivel de grupo periódico.

Para obtener más información, consulte [Pedidos periódicos](LocalFunctionality/Norway/recurring-orders.md).

### Ingresos periódicos y facturación de suscripción por otros proveedores

En [AppSource.microsoft.com](https://appsource.microsoft.com/), puede obtener extensiones para Business Central. Algunas de las extensiones las proporciona Microsoft y otras las proporcionan otras empresas. La lista de las extensiones de otras empresas aumenta cada mes. Esté atento a [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) y consiga aplicaciones que le ayudarán en su trabajo en Business Central.  

## Consulte también .

[Fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas)  
[Trabajar con diarios periódicos](ui-work-general-journals.md#work-with-recurring-journals)  
[Crear líneas de diario de proyectos](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Crear varias facturas de venta de proyecto](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md)  
[Trabajar con contratos de servicio y ofertas de contrato de servicio](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Facturar varios contratos de servicio](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Previsiones de demanda y pedidos abiertos](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Trabajar con pedidos de venta abiertos](sales-how-to-create-blanket-sales-orders.md)  
[Pedidos periódicos (Noruega)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]