---
title: Mover productos no planificados en configuraciones básicas de almacén
description: Este producto explica los movimientos internos no planificados entre ubicaciones sin una demanda de un documento de origen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# Mover productos internamente en configuraciones básicas de almacén

Es posible que desee mover productos entre ubicaciones sin una demanda de un documento de origen. Por ejemplo, como parte de las siguientes actividades:

* Reorganizar el almacén.
* Llevar los productos a una zona de inspección.
* Mueva elementos adicionales hacia y desde un área de producción. 

La forma de mover productos depende de si el almacén se configuró como ubicación. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).

En las configuraciones de almacén en las que la opción **Ubicac. obligatoria** está activada, pero no **Ubic. y pick. dirigido** puede registrar movimientos no planificados en las siguientes páginas:  

* En la página **Movimiento interno**.
* En la página **Diario reclasificación productos**.  

## Movimientos internos

La página **Movimientos internos** le permite especificar líneas de Traer y colocar cuando no hay una demanda de un documento de origen. La página Movimiento Interno es como una hoja de trabajo para organizar cosas. No puede procesar el movimiento real directamente desde ella. Cuando se complete una línea, use la acción **Crear movimiento de inventario** para enviar la línea a la página **Movimiento de inventario**, que es donde se tramita y registra el movimiento.

### Para mover los artículos como movimiento interno

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") escriba **Movimientos internos** y, a continuación, elija el vínculo relacionado.  
2. Elija la acción **Nuevo**. Asegúrese de que el campo **N.º** en desplegable **General** se haya rellenado.
3. En el campo de **Cód. almacén**, escriba la ubicación donde tiene lugar el movimiento.  

    Si la ubicación está configurada como predeterminada como empleado de almacén, el código de almacén se agregará automáticamente.  
4. En el campo **Hasta cód. ubicación**, introduzca el código para la ubicación a la que desea mover el producto.

    Por ejemplo, en producción, la ubicación podría ser la ubicación de aprovisionamiento manual, tal como se define en la ficha de almacén o del centro de trabajo.  
5. En el campo **Fecha vencimiento**, introduzca la fecha en la que debe completarse el movimiento.  
6. En cada línea, rellene los campos de la línea como sea necesario. Los documentos de movimiento interno tienen una línea por movimiento. La línea contiene las acciones de traer y colocar.
7. Elija el campo **Nº producto** para abrir la página **Lista de contenidos de ubicaciones** . Seleccione el producto para mover en función de su disponibilidad en ubicaciones. También puede elegir la acción **Traer conten. ubicac.** para llenar las líneas de movimiento internas según sus filtros.  

    Después de seleccionar el producto, el campo **Desde cód. ubicación** se completa automáticamente de acuerdo con el contenido de la ubicación seleccionada. Puede elegir cualquier ubicación donde el producto esté disponible. Los campos **Nº producto** y **Desde cód. ubicación** están relacionados. Cambiar el valor en un campo puede cambiar el valor en el otro.  

    El campo **Hasta cód. ubicación** se completa con el valor que especificó en el encabezado. Puede cambiarlo en la línea a cualquier otro código de ubicación que no esté bloqueado o dedicado para fines especiales. Obtenga más información en [El campo dedicado](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Cuando haya definido que las ubicaciones desde y a las que desea mover los productos, introduzca la cantidad para mover en el campo **Cantidad**.  

    > [!NOTE]  
    > La cantidad debe estar disponible en la ubicación especificada en el campo **Desde cód. ubicación**.  

9. Cuando vaya para procesar el movimiento, elija la acción **Crear movimiento de inventario**.  

    > [!NOTE]  
    >  Cuando se haya creado el movimiento, se eliminarán las líneas de movimientos internos.  

Realice el resto del movimiento no planificado en la página **Movimiento inventario** de la misma forma que lo haría en un movimiento basado en los documentos de origen.

### Para registrar el movimiento de inventario

1. En la página **Movimiento inventario**, abra el documento para registrar el movimiento.  
2. En las líneas de movimiento del campo **Cód. ubicación**, la ubicación desde la cual se debe realizar el picking de productos es donde el producto está disponible. Puede cambiar la ubicación si lo necesita.
3. Realice el movimiento e introduzca la información de la cantidad movida en el campo **Cdad. a manipular**. El valor de Toma y las líneas de Plaza deben iguales. Si no, no podrá registrar el movimiento.

    Si debe tomar los producto para una línea de más de una ubicación, por ejemplo porque no está toda la cantidad en la ubicación, utilice la acción **Dividir línea** de la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.  
4. Elija la acción **Registro movimiento de inventario**.  

Lo siguiente sucede durante el proceso de publicación:

* Las entradas de almacén indican que la cantidad se transfiere de las ubicaciones de toma a las ubicaciones de colocación.

## Para mover productos con el diario de reclasificación de productos:

En lugar de utilizar documentos de movimiento, puede registrar los movimientos reclasificando sus códigos de ubicación en productos. Obtenga más información en [Recuento, ajuste y reclasificación de inventario con diarios](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Los movimientos registrados con diarios de reclasificación no hacen que los documentos de movimiento estén listos para moverse.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios reclasif. producto**, y luego elija el enlace relacionado.  
2. En cada línea del diario, defina las ubicaciones de las que y a las que desea mover los productos rellenando los campos **Cód. ubicación** y **Nueva ubicación**.  

    1. Para mover todo el contenido de una ubicación a otra, elija la acción **Traer conten. ubicac.**.  
    2. Utilice los filtros para buscar la ubicación cuyo contenido desea mover y a continuación seleccione **Aceptar**. Las líneas del diario se rellenan con el contenido de la ubicación.  
3. Rellene el resto de los campos de cada línea del diario.
4. Registre el diario de reclasificación.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
