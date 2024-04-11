---
title: Configurar procesos de gestión de servicio
description: Aprenda a configurar procesos que ayuden a asegurar que sus clientes estén completamente satisfechos con sus servicios.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Configurar procesos de gestión de servicios

A continuación se muestran algunos ejemplos de la configuración que puede aplicar a los procesos de gestión de servicios:  
  
* Algunos ajustes generales para varios procesos, tales como las advertencias, los cálculos de servicios posteriores para los productos de servicio, la tarifa de inicio para evaluar, el nivel de notificación de defectos a utilizar, etc.  
* Los tipos de información que un técnico debe introducir en los documentos de servicio. Por ejemplo, puede solicitar que especifiquen el tipo de orden, las fechas de inicio o finalización del trabajo y el tipo de trabajo que se realizó.  
* Algunos ajustes predeterminados para tiempos de respuesta y garantías. Estos incluyen un tiempo de respuesta predeterminado para iniciar el servicio, porcentajes de descuento de garantía para piezas y mano de obra y el tiempo de validez de las garantías.  
* Ajustes de los contratos, como el número máximo de días que se pueden utilizar para las órdenes de servicio contractuales, el uso de códigos de razón cuando se cancela un contrato, los textos estándar para las descripciones y los valores del contrato.  
* Secuencias numéricas para documentos y productos relacionados con el servicio.  

## Para introducir valores generales y obligatorios

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de administración de servicios** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Configurar directivas de publicación de facturas de servicios para usuarios

Las empresas a menudo tienen procesos únicos para facturas y envíos. Por ejemplo, los procesos pueden variar desde una persona que registra todo en un pedido de servicio hasta varios empleados, cada uno trabajando con sus propias páginas.

Puede utilizar directivas de registro para impedir que los usuarios registren facturas de servicios o exigirles que registren facturas junto con el envío de servicios relacionado. Para configurar una directiva de registro, en la página **Configuración de usuario**, en el campo **Directiva de registro de facturas de servicio**, elija una de las siguientes opciones:

* **Permitido** (Predeterminado): mantiene el comportamiento actual, donde puede elegir la opción de publicación, como **Enviar**, **Factura** y **Envío y Factura**.
* **Prohibido**: impide que el usuario registre facturas de servicio. [!INCLUDE [prod_short](includes/prod_short.md)] muestra un cuadro de diálogo de confirmación que solo proporciona la opción **Envío**.
* **Obligatorio**: permite que las personas registren facturas junto con los envíos de servicios. [!INCLUDE [prod_short](includes/prod_short.md)] muestra un cuadro de diálogo de confirmación que solo proporciona la opción **Enviar y facturar**.

Esta configuración afecta a los siguientes documentos:

* Pedidos de servicio
* Envíos de almacén
* Facturas de servicios
* Notas de abono de servicio

La siguiente tabla describe los efectos en documentos diferentes.

|Documento  |Permitir<br>Muestra una serie de opciones   |Prohibido<br>Cuadro de diálogo de confirmación  |Obligatorio<br>Cuadro de diálogo de confirmación  |
|---------|---------|---------|---------|
|Pedido servicio     | * Enviar<br>* Facturar<br>* Enviar y facturar<br>* Enviar y consumir         |* Enviar<br>* Enviar y consumir  |¿Confirma que desea registrar el envío y la factura?         |
|Envío almacén     |* Enviar<br>* Enviar y facturar         |¿Confirma que desea registrar el envío?         | ¿Confirma que desea registrar el envío y la factura?        |
|Factura de servicio     | ¿Confirma que desea registrar la factura?         | Error: no puede registrar.       |¿Confirma que desea registrar la factura?         |
|Nota de abono de servicio     | ¿Confirma que desea registrar la nota de abono?         | Error: no puede registrar.        |¿Confirma que desea registrar la nota de abono?         |

> [!NOTE]
> Cuando registra facturas de servicio y notas de abono, no tiene ninguna opción de publicación. Los documentos siempre registran juntas las transacciones físicas y financieras. No se pueden contabilizar parcialmente facturas de servicio y notas de abono.

## Consulte también  

[Configurar información de defectos](service-how-setup-fault-reporting.md)  
[Configurar la asignación de recursos](service-how-setup-resource-allocation.md)  
[Configurar códigos para servicios estándar](service-how-setup-service-coding.md)  
[Configurar costes adicionales de servicios](service-how-setup-service-costs-pricing.md)  
[Configurar detección errores](service-how-setup-troubleshooting.md)  
[Gestión de servicios](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
