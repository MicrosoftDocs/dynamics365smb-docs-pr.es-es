---
title: Configurar información general de activos fijos (FA)
description: 'Antes de trabajar con activos fijos, debe configurar las cuentas contables predeterminadas, los grupos contables, las claves de asignación, las plantillas y secciones de diario, y los códigos de clase.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Configurar información general de activos fijos

Antes de poder administrar activos fijos (FA), debe configurar las cuentas contables predeterminadas, las claves de asignación, las plantillas y los lotes para registrar y reclasificar activos fijos. Asimismo, defina una jerarquía de clasificación (clases y subclases) para estructurar sus activos y, si es necesario, defina las ubicaciones en las que almacena los activos.

## Para configurar el comportamiento general de la funcionalidad de activos fijos

Defina el comportamiento general o la funcionalidad de los activos y configure las series numéricas del documento en la página **Configuración de activos fijos**.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Configuración de activos fijos** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Para configurar los grupos contables de activos fijos

Utilizar grupos contables para definir los grupos de activos fijos. Los movimientos de estos grupos contables se registran en las mismas cuentas contables.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos registro A/F**, y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.
3. En la página **A/F Ficha grupo contable**, rellene los campos según sea necesario.

    > [!NOTE]  
    >   ara asegurarse de que las cuentas de contrapartida de los diferentes registros de activos se insertan automáticamente en las líneas del diario al elegir la acción **Introducir saldo AF**, vaya al siguiente paso que se basa en el registro de apreciación.
4. En la ficha desplegable **Saldo**, en el campo **Cta. contrap. apreciación**, seleccione la cuenta contable en la que desea registrar las contrapartidas para la apreciación.

Para obtener más información sobre cómo usar la acción **Introducir saldo AF** en las líneas del diario general de activos, consulte [Revalorizar activos fijos](fa-how-revalue.md).

## Para configurar las plantillas del diario de activos

Un libro es un diseño predeterminado de un diario. El libro contiene información de los códigos de seguimiento, informes y números de serie. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] crea automáticamente una plantilla de diario de activos la primera vez que abre la página **Diario de activos**, pero puede configurar otras plantillas de diario.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros diarios activos**, y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## Para configurar códigos de subclase y clase de activos

En activos fijos, puede definir una jerarquía de clasificación que se puede utilizar para agrupar activos. La jerarquía tiene dos niveles: clases y subclases.

### Códigos de clase de activos fijos

Las clases de activos fijos son las entradas de nivel superior en la jerarquía de clasificación en la que agrupa los activos. Por ejemplo, utilice clases para dividir los activos en activos tangibles o intangibles. Debe crear al menos una clase de activo fijo en su configuración.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clases A/F** y luego elija el enlace relacionado.
2. Introduzca códigos y nombres para las clases de activos fijos que desee crear.

### Códigos de subclase de activos fijos

Las subclases de activos fijos son las entradas de segundo nivel en la jerarquía de clasificación en la que agrupa los activos. Cada subclase apunta a una clase de nivel superior. Utilice códigos de subclase de activos fijos para agrupar los activos fijos en categorías más específicas, como edificios, vehículos, mobiliario o maquinaria. Debe crear al menos una subclase de activo fijo en su configuración.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Subclases A/F** y luego elija el enlace relacionado.
2. Especifique los códigos y nombres que desea crear para las subclases de activos fijos.

## Empezar a registrar activos

Si es la primera vez que utiliza los activos fijos en [!INCLUDE[prod_short](includes/prod_short.md)], deberá configurar antes el área de aplicación Contabilidad antes de configurar los activos fijos. La forma de hacerlo depende de si integra los activos fijos con la contabilidad.  

El siguiente procedimiento se utiliza si se van a registrar las transacciones de activos en la contabilidad.  

1. Complete las configuraciones básicas para activos fijos.  
2. Rellene una ficha de activo para cada activo existente.  
3. Cree un libro de amortización de activos fijos para cada propósito de depreciación (como impuestos y estados financieros). Por cada libro de amortización debe definir los términos y las condiciones como, por ejemplo, la integración con la contabilidad.

    Active la integración en contabilidad siguiendo estos pasos. Primero, asegúrese de que la integración del libro mayor esté deshabilitada para todos los libros de amortización, luego publique los movimientos pendientes y, finalmente, active la integración del libro mayor.  
4. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros amortización** y luego elija el enlace relacionado.  
5. Seleccione el libro de amortización correspondiente y, a continuación, elija la acción **Editar** para abrir la página **Ficha libro amortización**.
6. En la pestaña desplegable **Integración**, desactive todas las opciones. Si dispone de más de un libro de amortización, repita este paso para cada uno.  
7. En el diario de activos fijos, introduzca las siguientes líneas por activo:
   * Línea con el coste.
   * Una línea con la amortización acumulada hasta el final del año fiscal anterior.
   * Una línea con la amortización acumulada desde el inicio del año fiscal en curso hasta la fecha en que [!INCLUDE[prod_short](includes/prod_short.md)] está establecido para comenzar a calcular la amortización.

    Si tiene otros saldos pendientes, también puede especificarlos ahora, como depreciación o apreciación.  
8. Una vez que haya introducido y registrado las líneas del diario para cada activo, active la integración de la contabilidad general en los libros de amortización.

Si los activos fijos no se integran en la contabilidad, omita los pasos seis y ocho.

## Para configurar códigos de ubicación de activos (opcional)

Los códigos de ubicación de los activos fijos definen los identificadores de los lugares donde se pueden ubicar los activos, como el departamento de ventas, la recepción, la administración, la producción o el almacén. Puede utilizarlos para registrar la ubicación de un activo fijo. Esta información es útil a efectos de seguros e inventario.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones A/F** y luego elija el enlace relacionado.
2. Especifique los códigos y nombres que desea crear para las ubicaciones de activos.

## Para configurar claves de distribución de activos fijos (opcional)

Utilice las claves de asignación para asignar las transacciones a varios departamentos o proyectos. Por ejemplo, puede configurar una clave de distribución para distribuir los costes de amortización de vehículos con el 35% para el departamento de administración y el 65% para el de ventas. Para obtener más información, consulte [Asignar costes e ingresos](year-allocate-costs-income.md).

Las claves de asignación se aplican a las clases de activos, no a los activos individuales.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos registro A/F**, y luego elija el enlace relacionado.  
2. En la página **A/F Grupos contables**, elija la acción **Distribuciones** y, a continuación, elija un tipo de registro.
3. En la página **A/F Distribuciones**, rellene los campos según sea necesario.
4. Repita los pasos 2 y 3 en todos los tipos de registro para los que desea definir claves de distribución.

## Para configurar las secciones del diario de activos fijos (opcional)

Puede configurar múltiples secciones de diario, que son diarios individuales para cada libro de diario. Por ejemplo, los empleados pueden tener su propia sección de diario que utiliza las iniciales del empleado como nombre de la sección. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros diarios activos**, y luego elija el enlace relacionado.  
2. Seleccione la plantilla de diario correspondiente y, a continuación, elija la acción **Secciones**.
3. En la página **A/F Secciones diario**, rellene los campos según sea necesario.

## Para configurar las plantillas del diario de reclasificación de activos (opcional)

Use los diarios de reclasificación dedicados para transferir, dividir o combinar activos fijos. [!INCLUDE[prod_short](includes/prod_short.md)] crea automáticamente una plantilla del diario de reclasificación de activos la primera vez que se abre la página **A/F Diario reclasif.**, pero puede configurar otras plantillas de diarios de reclasificación. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Libros diarios reclasif.**, y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## Para configurar las secciones del diario de reclasificación de activos (opcional)

Puede configurar múltiples secciones de diario, que son diarios individuales para cada libro de diario reclasificación. Por ejemplo, los empleados pueden tener su propia sección de diario reclasificación que utiliza las iniciales del empleado como nombre de la sección de diario reclasificación. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Libros diarios reclasif.**, y luego elija el enlace relacionado.  
2. Seleccione la plantilla de diario correspondiente y, a continuación, elija la acción **Secciones**.
3. En la página **A/F Secciones diario reclasif.**, rellene los campos según sea necesario.

## Consulte también

[Configuración de activos fijos](fa-setup.md)  
[Información general de los activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
