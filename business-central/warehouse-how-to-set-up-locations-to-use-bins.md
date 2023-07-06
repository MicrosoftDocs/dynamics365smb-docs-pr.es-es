---
title: Cómo configurar almacenes para utilizar ubicaciones
description: Las ubicaciones representan la estructura del almacén básico y se utilizan para realizar sugerencias sobre la colocación de los artículos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# <a name="set-up-locations-to-use-bins"></a><a name="set-up-locations-to-use-bins"></a><a name="set-up-locations-to-use-bins"></a><a name="set-up-locations-to-use-bins"></a>Configurar almacenes para utilizar las ubicaciones

Las ubicaciones representan la estructura básica del almacén y puede usarlos para sugerir dónde colocar los productos. Cuando haya creado sus ubicaciones, puede definir sus contenidos, o dejar que sirvan como ubicaciones flotantes sin contenido específico.

Para utilizar la funcionalidad de ubicación en un almacén, aactive el conmutador **Obligatorio en ubicación**, en la tarjeta **Ubicación**. Después de activar el conmutador, los campos **Código de ubicación** y **Código de zona** están disponibles en los siguientes documentos:

* Cabecera de recepción de almacén
* Líneas de recepción de almacén
* Líneas almacenamiento de almacén
* Cabecera de envío de almacén
* Líneas de envío de almacén
* Líneas almacenamiento de almacén

El siguiente paso es diseñar el flujo del producto en la ubicación, especificando los códigos de ubicación en los campos de configuración que representan a los distintos flujos.  

> [!NOTE]  
> Debe crear códigos de ubicación antes de especificarlos para el almacén. Para obtener más información, consulte [Crear ubicaciones](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins"></a><a name="to-set-up-a-location-to-use-bins"></a><a name="to-set-up-a-location-to-use-bins"></a><a name="to-set-up-a-location-to-use-bins"></a>Configurar una situación para utilizar las ubicaciones

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
2. Seleccione la situación donde desea utilizar las ubicaciones.  
3. Seleccione la acción **Editar**.  
4. En la ficha desplegable **Almacén**, elija la casilla **Ubicación obligatoria**.  
5. Si no utiliza ubicación y selección directos para el almacén, en el campo **Selección predeterminada de ubicaciones**, elija el método que desea que use [!INCLUDE [prod_short](includes/prod_short.md)] para asignar una ubicación predeterminada a un producto.  
6. Abra la tarjeta de ubicación para la que desea configurar las ubicaciones.
7. En la ficha desplegable **Ubicaciones**, seleccione las ubicaciones a usar como predeterminadas para recepción, envío, entrada, salida y aprovisionamiento manual.  

    Los códigos de ubicación que especifique aparecerán automáticamente en las cabeceras y en las líneas de diversos documentos de almacén. Las ubicaciones genéricas definen todos los lugares de inicio y fin de productos del almacén.  
8. Si utiliza ubicación y selección directos, seleccione una ubicación para los ajustes de almacén. El código de ubicación del campo **Código de ubicación de ajuste** define la ubicación virtual en la que registrar discrepancias de inventario:

    * Al observar diferencias registradas en el diario de productos de almacén
    * Diferencias calculadas al registrar un inventario físico de almacén  
9. Opcional: rellene los campos de la ficha desplegable **Directivas de ubicación**. Los campos más importantes son **Política capacidad ubicación**, **Permite división bulto** y **Cód. plantilla ubicar**.  
10. En la ficha desplegable **Almacén**, rellene los campos **Tiempo manip. alm. salida**, **Tiempo manip. alm. entrada** y **Código calendario base**. Para obtener más información, vaya a [Configurar calendarios de base](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin"></a><a name="fill-in-the-consumption-bin"></a><a name="fill-in-the-consumption-bin"></a><a name="fill-in-the-consumption-bin"></a>Relleno en la ubicación de consumo

El siguiente organigrama muestra cómo se rellena el campo de **Código de ubicación** en las líneas del componente de la orden de producción según la configuración de ubicación.

:::image type="content" source="media/binflow.png" alt-text="Campo de código de ubicación en líneas de componentes de orden de producción.":::

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/configure-bins-location/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
