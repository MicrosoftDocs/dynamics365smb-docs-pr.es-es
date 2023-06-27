---
title: Configurar información de activos fijos
description: 'Antes de trabajar con activos fijos, debe configurar las cuentas contables predeterminadas, los grupos contables, las claves de asignación, las plantillas y secciones de diario, y los códigos de clase.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-general-fixed-assets-information" />Configurar información general de activos fijos

Para poder gestionar activos fijos, debe configurar las cuentas predeterminadas, las claves de asignación, las plantillas y las secciones del diario que se utilizan para registrar y reclasificar los activos fijos, y clasificar los activos fijos en clases como, por ejemplo, Tangible e Intangible.

## <a name="to-set-up-general-default-values-for-fixed-assets" />Para configurar los valores predeterminados generales de los activos fijos

Defina el comportamiento general o la funcionalidad de los activos y configure las series numéricas del documento en la página **Configuración de activos fijos**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de activos fijos** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups" />Para configurar los grupos contables de activos fijos

Puede utilizar grupos de registro para definir los grupos contables de activos fijos. Los movimientos de estos grupos contables se registran en las mismas cuentas contables.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos registro A/F**, y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.
3. En la página **A/F Ficha grupo contable**, rellene los campos según sea necesario.

    > [!NOTE]  
    >   ara asegurarse de que las cuentas de contrapartida de los diferentes registros de activos se insertan automáticamente en las líneas del diario al elegir la acción **Introducir saldo AF**, vaya al siguiente paso que se basa en el registro de apreciación.
4. En la ficha desplegable **Saldo**, en el campo **Cta. contrap. apreciación**, seleccione la cuenta contable en la que desea registrar las contrapartidas para la apreciación.

Para obtener más información sobre cómo usar la acción **Introducir saldo AF** en las líneas del diario general de activos, vea, por ejemplo, [Revalorizar activos fijos](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys" />Para configurar claves de distribución de activos fijos

Las transacciones pueden distribuirse en varios departamentos y proyectos, según las claves de distribución definidas por el usuario. Por ejemplo, puede configurar una clave de distribución para distribuir los costes de amortización de automóviles con el 35% para el departamento de administración y el 65% para el de ventas. Para obtener más información, consulte [Asignar costes e ingresos](year-allocate-costs-income.md).

Las claves de asignación se aplican a las clases de activos, no a los activos individuales.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos registro A/F**, y luego elija el enlace relacionado.  
2. En la página **A/F Grupos contables**, elija la acción **Distribuciones** y, a continuación, elija un tipo de registro.
3. En la página **A/F Distribuciones**, rellene los campos según sea necesario.
4. Repita los pasos 2 y 3 en todos los tipos de registro para los que desea definir claves de distribución.

## <a name="to-set-up-fixed-asset-journal-templates" />Para configurar las plantillas del diario de activos

Un libro es un diseño predeterminado de un diario. El libro contiene información de los códigos de seguimiento, informes y números de serie. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] crea automáticamente una plantilla de diario de activos la primera vez que abre la página **Diario de activos**, pero puede configurar plantillas de diario adicionales.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros diarios activos**, y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## <a name="to-set-up-fixed-asset-journal-batches" />Para configurar las secciones del diario de activos

Puede configurar múltiples secciones de diario, que son diarios individuales para cada libro de diario. Por ejemplo, los empleados pueden tener su propia sección de diario que utiliza las iniciales del empleado como nombre de la sección. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros diarios activos**, y luego elija el enlace relacionado.  
2. Seleccione la plantilla de diario correspondiente y, a continuación, elija la acción **Secciones**.
3. En la página **A/F Secciones diario**, rellene los campos según sea necesario.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates" />Para configurar las plantillas del diario de reclasificación de activos

Use los diarios de reclasificación dedicados cuando deba transferir, dividir o combinar activos fijos. [!INCLUDE[prod_short](includes/prod_short.md)] crea automáticamente una plantilla del diario de reclasificación de activos la primera vez que se abre la página **A/F Diario reclasif.**, pero puede configurar plantillas de diarios de reclasificación adicionales. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Libros diarios reclasif.**, y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches" />Para configurar las secciones del diario de reclasificación de activos

Puede configurar múltiples secciones de diario, que son diarios individuales para cada libro de diario reclasificación. Por ejemplo, los empleados pueden tener su propia sección de diario reclasificación que utiliza las iniciales del empleado como nombre de la sección de diario reclasificación. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Libros diarios reclasif.**, y luego elija el enlace relacionado.  
2. Seleccione la plantilla de diario correspondiente y, a continuación, elija la acción **Secciones**.
3. En la página **A/F Secciones diario reclasif.**, rellene los campos según sea necesario.

## <a name="to-set-up-fixed-asset-class-codes" />Para configurar códigos de clase de activos

Los códigos de clase de activos fijos se pueden usar para agrupar los activos fijos, por ejemplo, en activos tangibles y activos intangibles.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clases A/F** y luego elija el enlace relacionado.
2. Especifique los códigos y nombres que desea crear.

## <a name="to-set-up-fixed-asset-subclass-codes" />Para configurar códigos de subclase de activos

Puede utilizar los códigos de subclase de activos fijos para agrupar sus activos en las categorías, por ejemplo, edificios, vehículos, mobiliario o maquinaria.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Subclases A/F** y luego elija el enlace relacionado.
2. Especifique los códigos y nombres que desea crear.

## <a name="to-set-up-fixed-asset-location-codes" />Para configurar códigos de ubicación de activos

Puede usar el códigos de almacén A/F para registrar la ubicación del activo, por ejemplo, departamento de ventas, recepción, administración, producción o almacén. Esta información es útil a efectos de seguros e inventario.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones A/F** y luego elija el enlace relacionado.
2. Especifique los códigos y nombres que desea crear para las ubicaciones de activos.

## <a name="to-register-opening-entries" />Para registrar movimientos pendientes

Si es la primera vez que utiliza los activos fijos en [!INCLUDE[prod_short](includes/prod_short.md)], deberá configurar antes el área de aplicación Contabilidad antes de configurar los activos fijos. La forma de hacerlo depende de si los activos fijos están integrados con la contabilidad.  

 El siguiente procedimiento se utiliza si se van a registrar las transacciones de activos en la contabilidad.  

1. Asegúrese de completar los procedimientos de configuración básica de los activos fijos.  
2. Cree una ficha de activo para cada activo existente.  
3. Cree un libro de amortización de activos fijos para cada propósito de depreciación (como impuestos y estados financieros). Por cada libro de amortización debe definir los términos y las condiciones como, por ejemplo, la integración con la contabilidad.  

    Active la integración en contabilidad siguiendo estos pasos. Primero, asegúrese de que la integración del libro mayor esté deshabilitada para todos los libros de amortización, luego publique los movimientos pendientes y, finalmente, active la integración del libro mayor.  
4. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros amortización** y luego elija el enlace relacionado.  
5. Seleccione el libro de amortización correspondiente y, a continuación, elija la acción **Editar** para abrir la página **Ficha libro amortización**.
6. Asegúrese de que todos los campos estén vacíos borrando todas las marcas en la ficha desplegable **Integración**. Si dispone de más de un libro de amortización, desactive la integración contable de cada uno.  
7. En el diario de activos fijos, introduzca las siguientes líneas por activo:
   * Línea con el coste.
   * Una línea con la amortización acumulada hasta el final del año fiscal anterior.
   * Una línea con la amortización acumulada desde el inicio del año fiscal en curso hasta la fecha en que [!INCLUDE[prod_short](includes/prod_short.md)] está establecido para comenzar a calcular la amortización.

    Si tiene otros saldos pendientes, también puede especificarlos ahora, como depreciación o apreciación.  
8. Una vez que haya especificado y registrado las líneas del diario para cada activo, active la integración de la contabilidad general en los libros de amortización.

Si los activos fijos no se integran en la contabilidad, omita los pasos 6 y 8.

## <a name="see-related-microsoft-training" />Consultar la [formación de Microsoft](/training/paths/set-up-fixed-assets-management/) relacionada

## <a name="see-also" />Consulte también .

[Configuración de activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
