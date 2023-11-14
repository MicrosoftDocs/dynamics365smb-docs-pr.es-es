---
title: Introducción a la Administración de servicio de Contoso Coffee
description: Este artículo le presenta los datos de demostración de Consoso Coffee para gestión de servicio.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Introducción a la Administración de servicio de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para Business Central agregan datos de demostración que puede usar para aprender a usar las capacidades de administración de servicio en Business Central.

Esta aplicación proporciona varios elementos que se utilizan para los tutoriales principales:

- Recursos con capacidades asignadas
- Artículos configurados para crear artículos de servicio
- Artículos prestados

> [!IMPORTANT]
> Antes de ejecutar cualquiera de los escenarios para Contoso Coffee, registre las líneas del diario de productos con saldos iniciales. Para ver más requisitos, consulte la sección [Configurar datos de Contoso Coffee](#set-up-contoso-coffee-service-management-data).
>
> 
## Configuración de datos de demostración de Contoso Coffee para administración de servicio

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Una vez instaladas las aplicaciones relevantes, vaya a la página de la [Herramienta de demostración de Contoso](https://businesscentral.dynamics.com/?page=5194) en [!INCLUDE [prod_short](../../includes/prod_short.md)], seleccione la línea *Módulo de servicio* y use la acción **Configurar** para preparar los módulos. En las siguientes tablas se describen las configuraciones:  

|Campo  |Descripción  |
|---------|---------|
|**Nº cliente**  |El cliente que se utilizará para los escenarios en las operaciones de venta.|
|**N.º proveedor**  |El proveedor que se utilizará para todos los escenarios en las operaciones de compra.|
|**N.º de producto 1**  |El producto que se usará para los escenarios de reparación y mantenimiento.|
|**N.º prod. servicio 1**  |El elemento de tipo servicio que se utilizará en el escenario de reparación.|
|**N.º prod. servicio 2**  |El elemento de tipo servicio que se utilizará en el escenario de reparación.|
|**N.º recurso 1**  |El recurso que se usará para los escenarios de contrato.|
|**N.º recurso 2**  |El recurso que se usará para los escenarios de sustitución.|
|**Ubicación de servicio** |Especifica el almacén que desea usar para las operaciones de servicio. El valor predeterminado es *PRINCIPAL*, pero puede cambiarlo para adaptarlo a sus necesidades.|


Una vez que esté listo, elija la acción **Crear datos de demostración** acción. Se tarda unos minutos en agregar los datos a la base de datos subyacente, pero luego ya está listo para ejecutar los distintos escenarios.  

## Escenarios

Los datos de demostración de Contoso Coffee admiten actualmente los siguientes escenarios de servicio para pruebas y formación:

1. Cree una orden de servicio para solicitudes de reparación ad hoc, coloque y reciba préstamos, registre el tiempo y facture a los clientes con el [Tutorial de órdenes de servicio para artículos de servicio](service-basic-flow-order.md)
2. Cree contratos de servicio, genere órdenes de servicio, facture tarifas de contratos y asigne recursos con el [Tutorial de contratos de servicio para artículos de servicio](service-contract-flow.md)

Lea los pasos para cada escenario en el artículo correspondiente.  

> [!IMPORTANT]
> Los tutoriales de servicio requieren que la experiencia del usuario esté establecida en **Premium** en la página **Información empresa**.


## Consulte también .

[Servicio](../../service-service.md)
