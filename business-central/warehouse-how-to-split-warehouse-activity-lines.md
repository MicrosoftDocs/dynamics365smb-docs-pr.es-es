---
title: Cómo dividir líneas de actividad de almacén
description: Obtenga información sobre cómo dividir líneas de actividad del almacén si la capacidad disponible en una ubicación sugerida no es suficiente.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# Dividir líneas de actividad de almacén

En almacenamientos, movimientos o picking de almacén y en almacenamiento y picking de inventario, se sugieren las ubicaciones para el picking o el almacenamiento de productos. La cantidad real de la ubicación sugerida quizá no sea suficiente, o no haya sitio suficiente en la ubicación sugerida para almacenar la cantidad requerida. En estos casos, puede dividir la línea para que los productos de esa línea se obtengan o coloquen en varias ubicaciones.  

El siguiente procedimiento se aplica a los siguientes documentos de almacén:

* Almacenamientos de almacén
* Movimientos de almacén
* Pickings de almacén
* Almacenamientos de inventario
* Movimientos de inventario
* Picking de inventario  

## Para dividir líneas de actividad de almacén  

1. Abra una línea de actividad de almacén en donde esté intentando gestionar una cantidad insuficiente.  
2. En el campo de **Cdad. a manipular**, introduzca la cantidad reducida que pueda manipular.  
3. En la ficha desplegable **Líneas**, elija **Acciones**, **Funciones** y **Dividir línea**. Aparece una nueva línea. La línea es una copia de la línea original, excepto en que el campo **Cdad. a manipular** contiene la cantidad que ha eliminado de la línea original.  
4. Asigne una ubicación y, si utiliza el almacenamiento y el picking dirigidos, una zona, o continúe dividiendo la línea según sea necesario hasta que encuentre ubicaciones apropiadas para toda la cantidad.  

> [!NOTE]  
> Si utiliza ubicación y picking directos y divide las líneas, debe estar familiarizado con el almacén y poder elegir una ubicación que cumpla los requisitos de almacenamiento del producto y cubra los requisitos generales del documento de almacén. Por ejemplo, no debería dividir una línea de un documento de picking y colocar algunos productos en el área de almacenamiento masivo.  

## Consulte también  

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]