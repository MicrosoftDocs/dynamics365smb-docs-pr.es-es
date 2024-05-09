---
title: Introducción a datos de demostración de Contoso Coffee
description: Descripción general de escenarios sobre cómo los datos de demostración de Contoso Coffee pueden ayudarle a aprender a usar las capacidades de Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# Introducción a datos de demostración de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para [!INCLUDE [prod_short](../includes/prod_short.md)] agregan datos de demostración que puede usar para aprender a usar las capacidades de [!INCLUDE [prod_short](../includes/prod_short.md)].  

## Configurar datos de Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

Cuando las aplicaciones estén instaladas, en la página **Herramienta de demostración de Contoso**, use la acción **Configurar** para preparar los siguientes módulos. Puede optar por instalar todos los datos disponibles, que incluyen datos de configuración y producción, o solo datos de configuración.

 - El **Módulo Común** para preparar la configuración general que requiere [!INCLUDE [prod_short](../includes/prod_short.md)]. Por ejemplo, cosas como series numéricas. Tenga en cuenta que el **Módulo común** contiene datos complementarios para los escenarios de almacén, fabricación y servicio únicamente. No se recomienda ejecutarlo de forma aislada.

En la siguiente tabla se describen las configuraciones:  

|Campo  |Descripción  |
|---------|---------|
|**Año inicial** |Especifica el primer año en el que desea usar los datos de demostración de Contoso Coffee. Según la configuración de la empresa, el año es un año natural o un año fiscal.|
|**Código de país o región**|Especifica un código de país o región para clientes y proveedores nacionales.|
|**Tipo de empresa**    |Especifica si la empresa actual debe declarar el IVA o el impuesto de venta. |
|**Factor precio**     |Especifica un factor para convertir un precio de USD/EUR a la divisa local. *1* significa que el precio es la misma cantidad en cualquier divisa. Se utilizará un número mayor para obtener el precio en la divisa local. |
|**Precisión de redondeo**  |Especifica la Precisión de redondeo con la que desea crear los datos de demostración.|

 - El [Módulo de fabricación](manufacturing/contoso-coffee-manufacturing-intro.md) para preparar los [Escenarios de fabricación](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - El [Módulo de almacenamiento](warehousing/contoso-coffee-warehousing-intro.md) para preparar el uso de los [Escenarios de almacenamiento](warehousing/contoso-coffee-warehousing-intro.md#scenarios).
 - El [Módulo de servicio](service/contoso-coffee-service-intro.md) para preparar el uso de los [Escenarios de servicio](service/contoso-coffee-service-intro.md#scenarios).

Después de configurar los módulos que desea probar, elija la acción **Generar** para crear datos de demostración para ellos.

## Consulte también .

[Fabricación](../production-manage-manufacturing.md)  
[Gestión de almacén](../warehouse-manage-warehouse.md)  
[Servicio](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

