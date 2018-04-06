---
title: "Preparar migración de datos de cliente | Documentos de Microsoft"
description: "Una vez que haya importado y aplicado los datos de configuración en la nueva base de datos, podrá comenzar a migrar los datos maestros existentes del cliente, tales como nombres y números de cliente y producto. Para asegurarse de que estos datos se crean de forma rápida y precisa en la empresa nueva, debe usar plantillas para estructurar los datos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 260f9c87f3c824e2eeced45fb4943784a03cb641
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="prepare-to-migrate-customer-data"></a>Preparar migración de datos de cliente
Una vez que haya importado y aplicado los datos de configuración en la nueva base de datos, podrá comenzar a migrar los datos maestros existentes del cliente, tales como nombres y números de cliente y producto. Para asegurarse de que estos datos se crean de forma rápida y precisa en la empresa nueva, debe usar plantillas para estructurar los datos.  

Normalmente, se crean plantillas de datos para las siguientes tablas de datos maestros:  

-   **Contacto**  
-   **Cliente**  
-   **Producto**  
-   **Proveedor**  

Sin embargo, puede crear una estructura de plantilla y aplicarla en cualquier tabla en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  También puede usar plantillas de datos para operaciones diarias a fin de crear registros nuevos basados en plantillas. Estas plantillas de datos funcionan sólo para las tablas de datos maestros compatibles. Para obtener más información, consulte, por ejemplo, [Registrar nuevos productos](inventory-how-register-new-items.md).  

Al importar datos de cliente, tal como los datos de producto, de la plantilla de datos vinculada se obtienen los datos de campos obligatorios especificados. Al crear un producto nuevo, especifique solo información general, tal como el nombre, la descripción y precio de producto. A continuación, recopile el resto de los datos del campo obligatorio a partir de una plantilla de datos seleccionada.  

Cuando se crea un nuevo registro de datos maestros, como una ficha de cliente, algunos campos son obligatorios y deben rellenarse. Puede agrupar la mayoría de los campos obligatorios, como grupos contables y condiciones de pago, para facilitar la creación de registros de datos maestros y hacerla más estable. Por ejemplo, puede agrupar campos obligatorios para la tabla 18, **Cliente**, como tipos **Nacional**, **Internacional** o **Exportar**.

## <a name="to-select-a-data-template"></a>Para seleccionar una plantilla de datos
Al seleccionar una plantilla existente de datos maestros, debe evaluar si las plantillas creadas para la nueva empresa son suficientes para el cliente. Revise los campos y los valores proporcionados para determinar qué plantillas son adecuadas para una empresa nueva.  

> [!TIP]  
>  También puede usar plantillas de datos para crear nuevos registros de forma rápida. Utilícelas para una creación de datos más rápida y más exacta. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas de configuración** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Lista plantilla de configuración**, seleccione una plantilla de datos de lista y después seleccione **Editar**.  

Si las plantillas predeterminadas no satisfacen sus necesidades, puede crear nuevas plantillas o agregar campos a una plantilla existente. Si las plantillas predeterminadas son suficientes, puede utilizarlas para crear registros basados en las plantillas de datos principales.

## <a name="to-create-a-data-template"></a>Para crear una plantilla de datos
Puede crear una nueva plantilla de datos si las plantillas predeterminadas no satisfacen las necesidades de su empresa nueva. Si crea más de una, puede resultar útil adoptar una convención de nomenclatura para el campo **Código**.

Cada plantilla consta de una cabecera y líneas. Cuando crea una plantilla, puede especificar los campos que siempre se deben aplicar a los datos de un tipo determinado. Por ejemplo, puede crear distintas plantillas de cliente para aplicar distintos tipos de cliente. Cuando crea el cliente mediante una plantilla, puede usar los datos de esta para rellenar determinados campos automáticamente.

### <a name="to-create-a-data-template-header"></a>Para crear una cabecera de plantilla de datos
1. Abra la ventana **Lista plantilla de configuración**.
2. Seleccione la acción **Nuevo**.
3. En el campo **Id. de tabla**, introduzca la tabla a la que se aplica esta plantilla. El campo **Nombre de tabla** se completa automáticamente cuando se establece el campo **Id. de tabla**.

### <a name="to-create-a-data-template-line"></a>Para crear una línea de plantilla de datos
1. En la primera línea, seleccione el campo **Nombre campo**. La ventana **Nombre de campo** muestra la lista de campos en la tabla.
2. Seleccione un campo y luego seleccione el botón **Aceptar**. El campo **Título de campo** se rellena con el nombre del campo.
3. En el campo **Valor predeterminado**, introduzca el valor correspondiente. En algunos casos, es posible que desee usar un valor que no sea un valor disponible en la base de datos. En dicho caso, puede activar la casilla **Omitir comprobación de relación** para permitir la aplicación de datos sin errores.

    > [!TIP]  
    > Puesto que el campo **Valor predeterminado** no contempla las opciones correspondientes del campo [!INCLUDE[d365fin](includes/d365fin_md.md)], copie y pegue el valor que desea de la página relacionada en la plantilla.

    > Seleccione la casilla de verificación **Obligatorio**. La casilla es solo para fines informativos. Indica que la información la debe especificar en el campo el usuario, pero no se aplica ninguna lógica empresarial. Por ejemplo, no podrá facturar ni registrar un pedido si no se han configurado grupos contables. Dado que se requieren grupos contables, puede activar la casilla **Obligatorio** para dichos campos.

3. En el campo **Referencia**, escriba información sobre el campo si es necesario.
4. Elija el botón **Aceptar**.

## <a name="to-export-to-a-template-in-excel"></a>Para exportar a una plantilla en Excel
Puede crear rápidamente un libro de Excel para que sirva como plantilla basada en la estructura de una tabla de base de datos existente. A continuación, puede usar la plantilla para recopilar todos los datos de cliente en un formato coherente para su importación posterior en [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Hoja de configuración** y, a continuación, seleccione el vínculo relacionado.
2. Agregue una tabla a la lista o seleccione una tabla existente. Para obtener más información, vea [Gestionar la configuración de la empresa en una hoja de trabajo](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Defina los campos de la tabla que desea incluir en la plantilla.
4. Seleccione la acción **Exportar a plantilla**.
5. Asigne un nombre al archivo Excel y guárdelo. El libro de Excel se abre automáticamente.

Ahora puede introducir los datos de cliente en la hoja de cálculo de Excel. Si ha exportado varias tablas, cada tabla estará en su propia hoja de cálculo. Guarde el libro antes de continuar con el procedimiento siguiente.

> [!NOTE]  
> Es posible que se produzca el error siguiente cuando ejecuta una versión en inglés de Excel, pero las opciones de configuración regional están establecidas para un idioma que no sea el inglés: "Formato antiguo o biblioteca de tipos no válida". Para corregir este error, asegúrese de tener instalado el paquete de idioma para el idioma distinto del inglés.

## <a name="to-import-from-a-template-in-excel"></a>Procedimiento para importar desde una plantilla en Excel
1. En la ventana **Configurar hoja**, seleccione la acción **Importar desde plantilla**.
3. Vaya hasta la hoja de trabajo de la plantilla que ha creado y después seleccione la acción **Abrir**.
4. Para agregar los datos obtenidos del cliente a la base de datos, elija la acción **Aplicar datos**.

Cuando aplique los datos de una plantilla en Excel a una tabla que también tenga una plantilla de configuración vinculada en el paquete de configuración, también se aplican los valores de los campos predeterminados de la plantilla de configuración.

Los registros cuyos datos se apliquen de esta forma se habrán completado, ya que se compone de los datos que introdujo un usuario en Excel, más los valores predeterminados que se especifican en la plantilla de configuración.

## <a name="to-create-a-record-from-a-configuration-template"></a>Para crear un registro desde una plantilla de configuración
Puede utilizar la estructura de datos que se incluye en las plantillas de datos para convertir la información en registros de la base de datos, uno a uno. Para ello, utilice la función **Crear instancia**. Se trata de una versión en miniatura del proceso de migración de datos y puede ser útil para la creación de un prototipo o el tratamiento de tareas más pequeñas de creación de datos.  

Los pasos siguientes ilustran cómo crear una ficha de producto de una plantilla de datos de producto. Puede crear un registro de cualquier plantilla de datos mediante el mismo procedimiento.  

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas de configuración** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la plantilla **Artículo** y, a continuación, elija la acción **Editar**. Para obtener más información, consulte la sección "Para crear una plantilla de datos".
3. Seleccione la acción **Crear instancia**. Se creará una ficha de producto.  
4. Elija el botón **Aceptar**.  
5. Para revisar la nueva ficha de producto, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
6. Abra la ficha de producto nueva.  
7. Expanda diferentes fichas desplegables y verifique que la información fue creada correctamente en ellas.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Procedimiento para usar una plantilla de configuración en un registro
Se puede aplicar una plantilla de datos a cualquier registro que está en [!INCLUDE[d365fin](includes/d365fin_md.md)] y usar esta técnica para cambiar o modificar un registro. Sin embargo, al hacerlo, se sobrescriben los valores existentes en el registro con los de la plantilla. Por lo tanto, debe tener cuidado cuando aplica una plantilla a registros existentes.

> [!WARNING]  
>  La función **Aplicar plantilla** sobrescribe los datos existentes en un registro. Si esta función se utiliza en la migración de datos maestros, sobrescribirá los datos importados al crear los registros.

El procedimiento siguiente se basa en una nueva ficha cliente.  

1. Crear un cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).
2. En la ventana **Ficha de cliente**, seleccione la acción **Aplicar plantilla**.  
3. En la ventana **Plantillas cliente**, seleccione una de las plantillas y, a continuación, el botón **Aceptar**.  

Los valores predeterminados de la plantilla de cliente seleccionada se introducen en la ficha de cliente.

## <a name="see-also"></a>Consulte también  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)  
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)

