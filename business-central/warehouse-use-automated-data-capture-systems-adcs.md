---
title: Usar los sistemas de captura de datos automatizado (ADCS) | Documentos de Microsoft
description: "Puede utilizar su sistema de captura automática de datos (ADCS) para registrar el movimiento de productos en el almacén y para registrar algunas actividades del diario, como los ajustes de cantidad en el diario de productos de almacén y los inventarios físicos."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b7887206991a6e31994e3efc4942c7b1254bb805
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="enable-automated-data-capture-systems-adcs"></a>Habilitar el sistema de captura de datos automatizado (ADCS)
Puede utilizar su sistema de captura automática de datos (ADCS) para registrar el movimiento de productos en el almacén y para registrar algunas actividades del diario, como los ajustes de cantidad en el diario de productos de almacén y los inventarios físicos.  

Para utilizar un ADCS, deberá asignar un identificador de producto para cada producto almacenado. También debe configurar los miniformularios de instalación, funciones portátiles, intercambios de datos y especificar las opciones de los campos que controlan un ADCS. Especifique si desea utilizar un ADCS en la ficha de almacén de un almacén.

Basándose en las necesidades de su almacén, se define la cantidad de información que se muestra en la configuración del miniformulario para el dispositivo portátil determinado. Los siguientes son ejemplos de la información que puede mostrar:  

- Datos de las tablas dentro de [!INCLUDE[d365fin](includes/d365fin_md.md)], como una lista de documentos de picking de los que el usuario puede seleccionar.  
- Información de texto.  
- Los mensajes para mostrar las confirmaciones o los errores sobre las actividades preformadas y registradas por el usuario del dispositivo portátil.

Para obtener más información, consulte [Configuración de un sistema de captura de datos automatizado](/dynamics-nav/Configuring-Automated-Data-Capture-System) en la ayuda para desarrolladores e informáticos.

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Para configurar un almacén para utilizar ADCS (sistema de captura de datos automatizado)  
Para utilizar un ADCS, debe especificar qué ubicaciones de almacén utilizan la tecnología.  

> [!NOTE]  
>  Se recomienda no configurar un almacén para utilizar un ADCS si dicho almacén también tiene una directiva de capacidad de la ubicación.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Ubicaciones** y elija el enlace relacionado.
2.  Seleccione un almacén de lista para la que desea activar un ADCS y seleccione **Editar**.
3. En la ventana **Ficha almacén**, active la casilla  **Utilizar ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Para especificar que un producto utilice ADCS  
Cada artículo de almacén que desea utilizar con un ADCS debe tener asignado un código de identificador para asociarlo al número de producto. Por ejemplo, podrá utilizar el código de barras del artículo como código de identificador. Un artículo puede tener varios códigos de identificador. Puede que esto le sea útil si un producto está disponible en varias unidades de medida, como por ejemplo piezas y paletas. En este caso, asigne un código de identificador a cada una de ellas.    

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2.  Seleccione un elemento de la lista que forma parte de la solución ADCS y seleccione **Editar**.
3. En la ventana **Tarjeta de producto**, seleccione la acción **Identificadores**.
4. En la ventana **Identificadores producto**, seleccione la acción **Nuevo**.
5. En el campo **Código**, especifique el identificador del producto. Por ejemplo, podría ser el código de barras.  

    Puede introducir **Cód. variante** y un código **Unidad medida**.  

6. Si es necesario, introduzca varios códigos para cada artículo.
7. Elija el botón **Aceptar**.  
8.  Para revisar información, seleccione el campo **Código identificador** para abrir la ventana **Identificadores producto**.

## <a name="to-add-an-adcs-user"></a>Para agregar a un usuario de un ADCS  
Puede agregar a cualquier usuario al sistema de captura de datos automatizados (ADCS). Cuando realice esta operación, el usuario debe proporcionar a una contraseña. Opcionalmente, también puede proporcionar un anexo que identifica al usuario de un ADCS como empleado de almacén. La contraseña de usuario de un ADCS puede ser diferente de la de inicio de Windows. Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Usuarios ADCS** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3.  En el campo **Nombre**, escriba un nombre para el usuario. El nombre no puede contener más de 20 caracteres, incluidos los espacios.  
4.  En el campo **Contraseña**, introduzca una contraseña. La contraseña se enmascara.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Para especificar que un empleado del almacén es usuario de un ADCS  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2.  Si es necesario, agregue un nuevo empleado de almacén. Para obtener más información, vea [Configurar los empleados de almacén](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Seleccione la acción **Editar lista**.  
4.  Seleccione un empleado de almacén de la lista. En el campo **Usuario ADCS**, seleccione la flecha desplegable y el nombre de un usuario de un ADCS de la lista.  

> [!NOTE]  
>  El almacén predeterminado para el empleado debe ser uno que utilice el sistema ADCS.

## <a name="to-create-and-customize-miniforms"></a>Para crear y personalizar miniformularios
Utilice los miniformularios que describen la información que desea fabricar en un dispositivo portátil. Por ejemplo, puede crear los miniformularios para utilizar la actividad de almacén de los artículos de picking. Una vez cree un miniformulario, puede agregar las funciones para las acciones comunes que un usuario tiene con dispositivos portátiles, como desplazarse arriba y abajo en una línea.  

Para ejecutar o cambiar las funcionalidad de una función del miniformulario, debe crear un nuevo codeunit o modificar uno existente para realizar la acción o respuesta requeridas. Puede obtener más información acerca de la funcionalidad de un ADCS examinando las unidades de código como 7705, que es el codeunit de control de la funcionalidad de inicio. El codeunit 7705 muestra cómo funciona un miniformulario tipo tarjeta.  

### <a name="to-create-a-miniform-for-adcs"></a>Para crear un miniformulario para un ADCS  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Miniformularios** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3.  Escriba un código para el miniformulario en el campo **Código**. Opcionalmente, introduzca los valores en el resto de campos.  

    Seleccione la casilla de **Iniciar Miniform.** para indicar que el este es el primer formulario que ve el usuario cuando se conecta.  

4.  En la ficha desplegable **Líneas**, defina los campos que aparecen en el miniformulario. El orden en que introduzca las líneas es en el que aparecen en el dispositivo portátil.  

Cuando haya creado un miniformulario, los pasos siguientes son crear las funciones y asociarlas la diversas entradas de teclado.  

### <a name="to-add-support-for-a-function-key"></a>Para agregar ayuda para una clave de función  
1.  Agregue el código similar al ejemplo siguiente al archivo the.xsl del complemento. Esto crea una función para la clave de **F6**. La información de la secuencia clave se puede obtener del fabricante del dispositivo.  
    ```xml  
    <xsl:template match="Function[.='F6']">  
      <Function Key1="27" Key2="91" Key3="49" Key4="55" Key5="126" Key6="0"><xsl:value-of select="."/></Function>  
    </xsl:template>  
    ```  
2.  En entorno de desarrollo de [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la tabla 7702 y agregue un código que represente la nueva clave. En este ejemplo, cree una clave llamada **F6**.  
3.  Agregue el código C/AL a la función correspondiente del codeunit específico del miniformulario para gestionar la clave de ejecución.  

### <a name="to-customize-miniform-functions"></a>Para personalizar las funciones del miniformulario  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Miniformularios** y luego elija el enlace relacionado.  
2.  Seleccione un miniformulario de la lista y, a continuación, seleccione la acción **Editar**.  
3.  Seleccione la acción **Funciones**.  
4.  En la lista desplegable de **Cód. función**, seleccione un código que represente la función que desea asociar con el miniformulario. Por ejemplo, puede seleccionar ESC, que asocia la funcionalidad con la pulsación de la tecla ESC.  

En el entorno de desarrollo de [!INCLUDE[d365fin](includes/d365fin_md.md)], modifique el código del campo **Manejar Codeunit** para crear o modificar código para que realice la acción o respuesta requeridas.

Para obtener más información, consulte [Configuración de un sistema de captura de datos automatizado](/dynamics-nav/Configuring-Automated-Data-Capture-System) en la ayuda para desarrolladores e informáticos.

## <a name="see-also"></a>Consulte también  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

