---
title: Migrar datos del cliente | Documentos de Microsoft
description: Puede migrar los datos existentes de cliente de un sistema de ERP existente a Business Central utilizando RapidStart Services. Puede usar archivos .xlsx de Excel como soporte de datos. También puede mover manualmente los datos al introducirlos directamente en la empresa.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e25082286f53c5b0458359d5f5c895b03c6f6bcf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927127"
---
# <a name="migrate-customer-data"></a>Migrar datos del cliente
Puede migrar los datos existentes de cliente de un sistema de ERP existente a [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizando las herramientas de migración de datos de RapidStart Services. Puede usar archivos de Excel como soporte de datos. También puede mover manualmente los datos al introducirlos directamente en la empresa.

> [!NOTE]
> Los campos de tipo BLOB no se pueden exportar/importar con Excel.

Las páginas **Info. gral. migración** y la **Configurar hoja** proporcionan acceso a las funciones y la vistas para realizar todas las tareas relacionadas con la migración de datos. Es recomendable que migre las tablas de una en una, para gestionar las dependencias en sus datos. En la migración, también tocará las tablas de los datos maestros, que contienen información acerca de los clientes, proveedores, productos, contacto y la contabilidad general.  

## <a name="to-import-configuration-packages"></a>Importar paquetes de configuración
Al crear una empresa nueva, puede importar las opciones de la empresa para la empresa nueva. Importa la configuración desde un archivo .rapidstart, que entrega los contenidos de paquete en un formato comprimido. Se importa un conjunto correspondiente de tablas de migración de datos predeterminadas. El conjunto de datos contiene tablas de datos maestros y las tablas de datos de configuración. Su primera tarea en la migración de datos es evaluar si la configuración predeterminada de migración cubre las necesidades de la empresa nueva.

> [!NOTE]  
>  No puede cambiar el nombre de un archivo que no es un paquete de configuración de RapidStart Services como un archivo de paquete de configuración .rapidstart y luego intentar importarlo. Si intenta hacerlo, recibirá un mensaje de error.  

Antes de comenzar, debe asegurarse de tener permiso para ejecutar los RapidStart Services objetos. Por ejemplo, puede tener los conjuntos de permisos SUPER o D365 RAPIDSTART. También le recomendamos que se encuentre en un área de trabajo con enlaces a RapidStart Services, como el Centro de funciones de administración. Para obtener más información, vea [Para cambiar el rol](ui-change-basic-settings.md#to-change-the-role).  

> [!IMPORTANT]  
> Al exportar e importar los paquetes de configuración entre dos bases de datos de empresa, las bases de datos deben tener el mismo esquema para garantizar que todos los datos se transferirán correctamente. Esto significa que las bases de datos deben tener la misma estructura de tablas y campos, en la que las tablas con las mismas claves principales y campos tienen los mismos identificadores y tipos de datos.  
>
>  Puede importar un paquete de configuración que se ha exportado desde una base de datos con un esquema distinto al de la base de datos de destino. Sin embargo, no se importarán las tablas o los campos del paquete de configuración que falten en la base de datos de destino.
>
> Tampoco se importarán las tablas que tengan diferentes claves principales ni los campos que tengan distintos tipos de datos. Por ejemplo, si el paquete de configuración incluye la tabla **50000 Cliente** que tiene la clave principal **Code20** y la base de datos a la que importa el paquete incluye la tabla **50000 Banco cliente** que tiene la clave principal **Code20 + Código 20**, no se importarán los datos.  

1. Abra la nueva empresa.  
2. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.  
3. Elija la acción **Importar paquete**. Navegue hasta el archivo del paquete .rapidstart que desea importar y luego elija la acción **Abrir**. Durante la importación, se descomprimen los contenidos del paquete y se crea el registro del paquete.  

    Cuando la importación esté completada, puede ver el número de tablas de configuración que se han importado en el campo **Nº de tablas**.  
4. Para revisar la lista de tablas de configuración, elija la acción de **Ver**.  
5. Para liquidar el paquete, elija la acción **Aplicar paquete**.  

    > [!NOTE]  
    >  La información de migración de datos se basa en plantillas de configuración, si se especifica una. Debe actualizar la plantilla primero para cambiar la lista de campos.  

6.  Para revisar las selecciones de campo, seleccione una tabla y luego, en la pestaña **Líneas**, elija la acción **Campos**. Compare y revise el número de campos que están disponibles con el número de campos cuyos datos se han aplicado.  

Si la selección de tablas no cubre sus necesidades, puede crear uno o varios nuevos archivos de migración de datos. Si los archivos de la migración de datos predeterminados son suficientes, puede continuar con la migración de datos mediante archivos Excel o XML.

## <a name="to-create-a-data-migration-file"></a>Para crear un archivo de migración de datos

Puede crear nuevos archivos de migración de datos y personalizarlos para satisfacer las necesidades de su negocio.  

> [!TIP]
> Un archivo solo se puede utilizar para migrar un campo que tenga su propiedad **FieldClass** establecida en **Normal**.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Paquete de configuración** y luego elija el enlace relacionado.  
2. Seleccione y abra el paquete que desea utilizar para migrar datos y después seleccione **Obtener tablas**. Se abre la página **Traer tabla de paquete**.  
3. En el campo **TableID**, introduzca un número de tabla o seleccione una tabla de la lista, por ejemplo, la tabla 18, **Cliente**. El campo **Nombre de tabla** se rellena automáticamente.  
4. Seleccione la nueva tabla de la migración y, a continuación, en la pestaña **Tablas**, elija la acción **Campos**. Se abre la página **Campos migración**.  
5. Desactive la casilla **Incluir campo** para los campos que no desee importar y después la acción **Definir incluido** o **Borrar incluido**.  

> [!IMPORTANT]  
>  Si la casilla **Incluir campo** está activada de forma predeterminada, dicho campo forma parte de la clave principal. La selección no se debe borrar o se introducirán errores y el registro no se podrá importar.  
>
>  Si incluye un campo que tenga una relación con otra tabla, la casilla **Validar campo** se activará automáticamente. La validación puede afectar a la actualización de otros campos en esta y tablas y se ejecuta en el orden del número de campo.  

Se creará una nueva tabla de migración.  

## <a name="to-export-data-migration-files"></a>Para exportar archivos de migración
Cuando haya determinado las tablas a las que desea transferir datos de cliente, debe exportar los archivos.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.  
2. Seleccione y abra el paquete que desee usar para la exportación.
3. Seleccione la tabla o tablas que desea exportar y después seleccione **Exportar a Excel**.
4. Guarde el archivo Excel exportado.  
5. Repita este procedimiento para todas las tablas de migración de datos pertinentes. Si selecciona varias tablas al mismo tiempo, la exportación de los datos se realiza en un libro común.  

Si la tabla está vacía, el archivo de migración de datos resultante contendrá las celdas vacías para los campos que ha seleccionado cuando eligió o creó las tablas de migración para la nueva empresa. Si la tabla de migración de datos seleccionada contiene datos, se exportará.  

## <a name="to-map-values-to-be-used-during-import"></a>Para asignar valores para utilizarlos durante la importación
Cuando liquide datos que ha importado desde Excel o desde un paquete RapidStart, [!INCLUDE[d365fin](includes/d365fin_md.md)] trata y maneja la asignación en función de las relaciones de la tabla:  

- Si define una asignación directamente para un campo de una tabla, entonces [!INCLUDE[d365fin](includes/d365fin_md.md)] la utiliza.  

- Si este campo tiene relación con otra tabla, [!INCLUDE[d365fin](includes/d365fin_md.md)] busca la asignación definida para el campo de clave principal en la tabla relacionada. La tabla relacionada, sin embargo, debe formar parte del paquete de configuración.  

- Si la información de asociación se define en ambos lugares, para el campo directamente y para la clave principal en la tabla relacionada, entonces [!INCLUDE[d365fin](includes/d365fin_md.md)] buscará la asociación en ambos lugares.  

- Si se definen directamente las mismas asignaciones para un campo y en la tabla relacionada, pero con valores nuevos distintos, la asignación que se defina directamente para el campo tiene prioridad sobre la asignación que se defina para la tabla a la que el campo está haciendo referencia.  

En los siguientes procedimientos, debe revisar por adelantado los valores que desea que se retengan durante el proceso de migración. Para realizar los procedimientos siguientes, necesitará los archivos de migración de datos (.xlsx) que haya exportado desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, consulte [Para exportar archivos de migración](admin-migrate-customer-data.md#to-export-data-migration-files).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.
2. Abra el paquete de la empresa en cuestión.  
3. Seleccione la tabla a la que desee asignar valores y en la pestaña **Tablas**, elija la acción **Campos**.  
4. Para cada campo que desee asignar, elija la acción **Asignación**.  
5. En el campo **Valor antiguo**, escriba el valor que desea cambiar. En el campo **Valor nuevo**, escriba el valor al que desea que se cambie el valor original. Elija el botón **Aceptar**.  
6. Importe los datos del cliente. Para obtener más información, consulte [Para importar datos del cliente](admin-migrate-customer-data.md#to-import-customer-data).
7. En el campo **Nº errores de paquete**, compruebe si hay errores notificados. Si es así, explore en profundidad para ver los errores. Se abre la página **Registros paquete config**.
8. Elija la acción **Mostrar error**. Recibirá el error siguiente: **XX no es una opción válida. Las opciones válidas son: XX**. Elija el botón **Aceptar**.  
9. Para liquidar la asignación que ha configurado, elija la acción **Aplicar datos**.  

### <a name="mapping-example"></a>Ejemplo de asignación  
El ejemplo siguiente ilustra cómo implementa [!INCLUDE[d365fin](includes/d365fin_md.md)] las definiciones de asignación.  

1. Crear una tabla de configuración que tenga una tabla **Vendedor/Comprador**. Definir una asignación para el campo **Código**.  
2. Añada tablas adicionales al paquete, por ejemplo, **Cliente** y **Proveedor**. Estas tablas hacen referencia a la tabla **Vendedor/Comprador** a través del **código de vendedor** y el **código de comprador**, respectivamente.  
3. Cuando se aplican datos, la asignación proporcionada en el campo **Código** de la tabla **Vendedor/Comprador** también se tendrá en cuenta al procesar los campos **Código de vendedor** y **Código de comprador**.

## <a name="to-add-additional-values-to-d365fin"></a>Para agregar valores adicionales a [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.  
2. Seleccione la tabla a la que desee asignar valores adicionales y en la pestaña **Tablas**, elija la acción **Campos**.  
3. Para los campos para los que desea que [!INCLUDE[d365fin](includes/d365fin_md.md)] permita valores adicionales durante la migración, seleccione la casilla **Crear códigos que faltan**.  
4. Importe los datos del cliente. Para obtener más información, consulte [Para importar datos del cliente](admin-migrate-customer-data.md#to-import-customer-data).

## <a name="to-clean-up-and-process-data-before-applying-data"></a>Para limpiar y procesar datos antes de aplicar datos
En algunos casos, puede que desee limpiar los datos de cliente y procesarlos para poder aplicarlos a la base de datos. Para hacer eso, puede usar el proceso **Paquete de configuración - Proceso** para solucionar problemas, como:  

- Convierta fechas y decimales al formato requerido por la configuración regional del equipo del usuario.  
- Elimine los espacios iniciales o los finales o los caracteres especiales.  

Cuando haya ejecutado el proceso, utilice el procedimiento siguiente para procesar los datos.  

1. Abra el paquete de configuración de la empresa.  
2. Seleccione la acción **Procesar datos**.  
3. Para liquidar la asignación que ha configurado, elija la acción **Aplicar datos**.

## <a name="to-migrate-customer-data"></a>Para migrar datos del cliente
Cuando haya exportado una tabla de migración, el siguiente paso es introducir datos heredados del cliente. Para simplificar sus tareas, puede aprovechar las herramientas de manipulación de XML que se integran en Excel. También puede utilizar las funciones integradas de Excel para ayudar con el formato de datos y para colocar los datos en la celda correcta.

Para obtener ayuda con XML, habilite la pestaña **Desarrollador** de la cinta de Excel y luego elija la acción **Fuente** para ver el esquema XML de su tabla de migración como se representa en Excel.

El procedimiento siguiente se basa en una hoja de cálculo de Excel que ha creado para la migración. Para obtener más información, consulte [Para exportar archivos de migración](admin-migrate-customer-data.md#to-export-data-migration-files).

> [!IMPORTANT]  
> No cambie las columnas en las hojas de cálculo Excel. Si se mueven, modifican o eliminan, la hoja de cálculo no podrá importarse a [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. En Excel, abra el archivo de datos exportado. Hay una hoja de cálculo con el nombre de la tabla.
2. Cambie el nombre de Sheet1 para indicar que la hoja de cálculo se utilizará para transformar los datos. Copie la fila de la cabecera sin su formato desde la tabla exportada hasta la nueva hoja de cálculo.
3. En una tercera hoja de cálculo, copie todos los datos de clientes. Cambie el nombre de la hoja para que se llame, por ejemplo, Datos heredados.
4. Haga una fórmula de Excel para asignar datos en la hoja de cálculo de transformación entre los campos en la hoja de cálculo exportada y los datos heredados del cliente.
5. Al asignar todos los datos, copie el intervalo de datos en la hoja de cálculo de la tabla.
6. Guarde el archivo y asegúrese de que no cambia el tipo de archivo.

Ahora podrá importar los archivos de migración de datos que contienen datos heredados del cliente a [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="to-import-customer-data"></a>Para importar datos del cliente
Cuando se hayan introducido los datos del cliente en los archivos de migración de datos en Excel, importe los archivos en [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Abra la página **Configurar tarjeta de paquete**.
2. Seleccione la tabla a la que desee importar datos y en la pestaña **Tablas**, elija la acción **Importar desde Excel**.
3. Localice y abra el archivo del que desea importar datos.
4. En la página **Config. vista previa importación paquetes**, revise el contenido que se va a importar.

    La página **Config. vista previa importación paquetes** proporciona una visión general del contenido del archivo de Excel que se va a importar. También indica si se crea un nuevo paquete de configuración o si se actualiza el existente, y si se crean nuevas líneas (tablas) de paquete de configuración o se actualizan las existentes.    
5. Seleccione la acción **Importar**.

Los datos del archivo se importan en las tablas de paquetes de configuración. En el campo **Nº registros de paquete**, puede ver el número de registros que se han importado. Además, puede ver el número de errores de la migración.

## <a name="to-validate-customer-data"></a>Para validar datos del cliente
Los datos del cliente deben validarse antes de aplicar registros a la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  En la mayoría de los casos, los datos no válidos no se crean en la base de datos. Sin embargo, la solicitud se puede bloquear de vez en cuando si una tabla de migración importada contiene errores.  

1. En la página **Info. gral. migración**, revise el campo **Nº errores migración** para ver si se han producido errores durante la importación.  
2. Si hay errores, seleccione la tabla de migración y en la pestaña **Tablas** elija la acción **Errores**. La casilla **No válido** se selecciona para cada registro que tenga un error.  
3. Para revisar errores, seleccione una línea y después la acción **Mostrar error**.  

    Este campo **Texto error** contiene el motivo del error. El campo **Título campo** contiene el título del campo que contiene el error.  
4.  Para corregir un error o realizar una actualización, en la página **Información general sobre migración**, seleccione la acción **Registro migración** y en la página **Registro de migración**, corrija el registro con el error.  

Cuando se haya realizado la corrección, el registro se eliminará de la lista de registros de la página **Errores migración datos**.  

Ahora podrá aplicar los datos del cliente a la base de datos.  

## <a name="to-apply-customer-data"></a>Procedimiento para aplicar datos del cliente
Cuando tenga todos los registros de migración de datos importados que sean válidos y no tengan ningún error, podrá aplicar los registros a la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Abra la página **Paquete de configuración**.  
2. Seleccione la tabla para el archivo de migración de datos que desea aplicar y elija la acción **Aplicar datos**.

Puede ver el número de registros de base de datos que se han creado en el campo **Nº registros de base de datos**. Puede verificar que se hayan creado los registros correctos seleccionando el enlace en el campo **Nº registros de base de datos**.  

Ya está configurada la base de datos de la empresa del cliente y se han importado los datos básicos. Los pasos siguientes en el proceso de implementación son entrenar a los usuarios, definir procesos, crear datos adicionales, personalizar informes, etc.

## <a name="see-also"></a>Consulte también  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)
