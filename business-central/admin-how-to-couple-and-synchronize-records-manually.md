---
title: Emparejamiento y sincronización (contiene vídeo)
description: La sincronización de una asignación de tablas de integración permite la sincronización de datos de todos los registros de una tabla de Business Central y de la tabla de Dynamics 365 Sales que están emparejadas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
---

# <a name="couple-and-synchronize-records-between-dataverse-and-business-central"></a><a name="couple-and-synchronize-records-between-dataverse-and-business-central"></a>Empareje y sincronice registros entre Dataverse y Business Central

En este tema se describe cómo emparejar uno o más registros de [!INCLUDE[prod_short](includes/prod_short.md)] con registros de Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. El emparejamiento de registros le permite ver información de Dataverse desde [!INCLUDE[prod_short](includes/prod_short.md)], y viceversa. El emparejamiento también le permite sincronizar datos entre los registros. Puede emparejar registros existentes o crear y emparejar nuevos registros.

> [!NOTE]
> El emparejamiento y la sincronización de datos solo están disponibles si el administrador del sistema ha creado una conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. Una forma rápida de comprobarlo es abrir la ficha **Cliente** y buscar la acción **Configurar emparejamiento**. Si la acción está disponible, las aplicaciones se conectan.

## <a name="video-example"></a><a name="video-example"></a>Ejemplo de video

Este video muestra el acoplamiento y la sincronización de datos en el contexto de una integración con [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><a name="to-couple-a-record"></a>Para emparejar un registro

1. En [!INCLUDE[prod_short](includes/prod_short.md)], abra la tarjeta para el registro que desea emparejar. Por ejemplo, la tarjeta Cliente o Contacto.  

    También puede abrir simplemente la página de lista y seleccionar el registro que desee emparejar.  

2. Seleccione la acción **Configurar emparejamiento**.  
3. Rellene los campos y, a continuación, elija **Aceptar**.  

## <a name="to-synchronize-a-single-record"></a><a name="to-synchronize-a-single-record"></a>Para sincronizar un solo registro

1. En [!INCLUDE[prod_short](includes/prod_short.md)], abra la tarjeta para el registro que desea emparejar. Por ejemplo, la tarjeta Cliente o Contacto.  
2. Seleccione la acción **Sincronizar ahora**.  
3. Si un registro se puede sincronizar en una dirección, seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.  

## <a name="to-synchronize-a-single-record-from-"></a><a name="to-synchronize-a-single-record-from-"></a>Para sincronizar un solo registro en [!INCLUDE[crm_md](includes/crm_md.md)]

1. En [!INCLUDE[crm_md](includes/crm_md.md)], abra el formulario para el registro que desea emparejar. Por ejemplo, el formulario Tarjeta de cuenta o Tarjeta de contacto.  
2. Elija la acción **[!INCLUDE[prod_short](includes/prod_short.md)]** en la cinta para abrir y emparejar el registro automáticamente.

    > [!Note]
    > Puede sincronizar un solo registro desde [!INCLUDE[crm_md](includes/crm_md.md)] automáticamente solo cuando **Sincronizar solo reg. emparejados** está deshabilitado y la dirección de sincronización se establece en **Bidireccional** o **Desde la tabla de integración** en la página **Asignación de tabla de integración** para el registro. Para más información, vea [Asignación de tablas y campos para sincronizar](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## <a name="to-couple-multiple-records-using-match-based-coupling"></a><a name="to-couple-multiple-records-using-match-based-coupling"></a>Para emparejar varios registros mediante el emparejamiento basado en coincidencias

Especifique los datos que se sincronizarán para una entidad, como un cliente o un contacto, mediante el emparejamiento de registros basado en coincidencias. Acote las coincidencias haciendo que la búsqueda distinga entre mayúsculas y minúsculas y asignando una prioridad para cada coincidencia. Si no se encuentra ninguna coincidencia, también puede especificar que desea crear la entidad en Dataverse. Para más información, vaya a [Personalizar emparejamiento basado en coincidencias](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> El proceso de acoplamiento basado en coincidencias omite los registros que ya tienen coincidencias. Para incluir esos registros cuando ejecuta el acoplamiento basado en coincidencias, desacople los registros y vuelva a intentarlo. Para obtener más información sobre cómo desacoplar registros, vaya a [Desacoplamiento de registros](#uncoupling-records).

1. En el cliente de [!INCLUDE[prod_short](includes/prod_short.md)], abra la página de lista para el registro, como las páginas de lista Clientes o Contactos.
2. Elija la acción **Emparejamiento basado en coincidencias**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a><a name="to-synchronize-multiple-records"></a>Para sincronizar varios registros

1. En [!INCLUDE[prod_short](includes/prod_short.md)], abra la página de lista para el registro, como las páginas de Clientes o Contactos.  
2. Seleccione los registros que desea sincronizar y, después, seleccione la acción **Sincronizar ahora**.  
3. Si los registros se pueden sincronizar en una dirección, seleccione la opción que especifica la dirección y, a continuación, seleccione **Aceptar**.  

## <a name="bulk-insert-and-couple-records"></a><a name="bulk-insert-and-couple-records"></a>Registros de emparejamiento e inserción en lote

Si tiene una gran cantidad de entidades de Dataverse que corresponden a registros en [!INCLUDE [prod_short](includes/prod_short.md)], puede insertarlas y emparejarlas en lote. Por ejemplo, es posible que desee realizar una inserción en lote y emparejar registros cuando configure la sincronización por primera vez.

Utilizará el **Asistente de importación de datos** en el **Centro de administración de Microsoft Power Platform**.

El siguiente ejemplo describe cómo realizar una inserción en lote y vincular clientes con cuentas en Dataverse. Utilice el mismo proceso para otros tipos de entidades, como proveedores, artículos y recursos.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Elija la acción **Abrir en Excel** para abrir los datos del cliente en Excel. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Para asignar e importar datos a la entidad **Cuenta** en Dataverse, siga los pasos descritos en [Importar datos (todos los tipos de registro ) de varios orígenes](/power-platform/admin/import-data-all-record-types).  

    Si la entidad Cuenta tiene una columna **bcbi_companyid**, cuando asigne las columnas de datos, asegúrese de que la importación asigne el id. de empresa adecuado en la columna para cada registro importado. Para encontrar el id. de la empresa en [!INCLUDE [prod_short](includes/prod_short.md)], siga estos pasos:

    1. Abra la página **Asignaciones de tablas de integración**.
    2. Eliga la asignación **CLIENTE** y luego **Editar lista**.
    3. Desplácese hacia la derecha y elija el botón de edición asistida :::image type="icon" source="media/assist-edit-icon.png" border="false"::: en el campo **Filtro de tabla de integración**. Esto muestra el filtro predeterminado para la asignación de clientes y contiene el id. de la empresa. El id. de la empresa es la primera parte del valor. Copie solo esa parte e ignore los 0. El siguiente ejemplo resalta la parte a copiar.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Muestra la parte del id. de la empresa a copiar.":::

    > [!NOTE]
    > No todos los nombres de entidades de Dataverse y registros de Business Central coinciden. Dependiendo de lo que esté importando, vuelva a comprobar que las siguientes columnas tengan los siguientes valores después de importar:
    >
    >* Para los clientes, la columna **CustomerTypeCode** debe contener **Cliente**.
    >* Para los proveedores, la columna **CustomerTypeCode** debe contener **Proveedores**. 
    >* Para artículos, la columna **ProductTypeCode** debe contener **Inventario de ventas**.
    >* Para recursos, la columna **ProductTypeCode** debe contener **Servicio**.
 
4. Después de importar datos al entorno de Dataverse, en [!INCLUDE [prod_short](includes/prod_short.md)], siga los pasos [Emparejar varios registros mediante el emparejamiento basado en coincidencias](#to-couple-multiple-records-using-match-based-coupling) para emparejar las entidades de Dataverse con registros de [!INCLUDE [prod_short](includes/prod_short.md)]. 

## <a name="uncoupling-records"></a><a name="uncoupling-records"></a>Desemparejamiento de registros

Puede desacoplar uno o más registros de las páginas de lista o la página **Errores de sincronización de datos acoplados** eligiendo una o más líneas y eligiendo **Eliminar acoplamiento**. También puede eliminar todos los acoplamientos para una o más asignaciones de tabla en la página **Asignaciones de tablas de integración**.

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Usar Dynamics 365 Sales desde Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
