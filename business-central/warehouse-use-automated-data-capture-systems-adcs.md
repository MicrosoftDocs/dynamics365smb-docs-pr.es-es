---
title: Utilice la base del sistema de captura de datos automatizado (ADCS)
description: Obtenga información sobre cómo usar la captura automática de datos (ADCS) para registrar el movimiento de productos en el almacén.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7700, 7703, 7704, 7706, 7707, 7710, 9813, 9814'
---
# <a name="use-automated-data-capture-systems-adcs-foundation"></a>Utilice la base del sistema de captura de datos automatizado (ADCS)

> [!Important]
> La solución del Sistema Automatizado de Captura de Datos (ADCS) proporciona una forma para que [!INCLUDE[prod_short](includes/prod_short.md)] pueda comunicarse con dispositivos de mano a través de servicios web. Debe trabajar con un socio de Microsoft que pueda proporcionar el enlace entre el servicio web y el dispositivo portátil específico. 

Puede utilizar su sistema de captura automática de datos (ADCS) para registrar el movimiento de productos en el almacén y para registrar algunas actividades del diario, como los ajustes de cantidad en el diario de productos de almacén y los inventarios físicos. ADCS generalmente implica el escaneo un código de barras.

Para utilizar un ADCS, deberá asignar un identificador de producto para cada producto almacenado. También debe configurar los miniformularios de instalación, funciones portátiles, intercambios de datos y especificar las opciones de los campos que controlan un ADCS. Especifique si desea utilizar un ADCS en la ficha de almacén de un almacén.

Basándose en las necesidades de su almacén, se define la cantidad de información que se muestra en la configuración del miniformulario para el dispositivo portátil determinado. Los siguientes son ejemplos de la información que puede mostrar:  

- Datos de las tablas dentro de [!INCLUDE[prod_short](includes/prod_short.md)], como una lista de documentos de picking de los que el usuario puede seleccionar.  
- Información de texto.  
- Los mensajes para mostrar las confirmaciones o los errores sobre las actividades preformadas y registradas por el usuario del dispositivo portátil.

## <a name="to-enable-web-services-for-adcs"></a>Para habilitar los servicios web para ADCS

Para usar el Sistema Automatizado de Captura de Datos, debe habilitar el servicio web ADCS. Debe trabajar con un socio de Microsoft que pueda implementar un servicio web que pueda conectar ADCS y un dispositivo portátil específico. Puede obtener más información sobre el servicio web para ADCS examinando el codeunit 7714. 
 
## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Para configurar un almacén para utilizar ADCS (sistema de captura de datos automatizado)

Para utilizar un ADCS, debe especificar qué ubicaciones de almacén utilizan la tecnología.  

> [!NOTE]  
> Se recomienda no configurar un almacén para utilizar un ADCS si dicho almacén también tiene una directiva de capacidad de la ubicación.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y elija el enlace relacionado.
2. Seleccione el almacén para el que desea activar un ADCS y seleccione la acción **Editar**.
3. En la página **Ficha de almacén**, active el control de alternancia **Utilizar ADCS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Para especificar que un producto utilice ADCS

Cada artículo de almacén que desea utilizar con un ADCS debe tener asignado un código de identificador para asociarlo al número de producto. Por ejemplo, podrá utilizar el código de barras del artículo como código de identificador. Un artículo puede tener varios códigos de identificador. Puede que esto le sea útil si un producto está disponible en varias unidades de medida, como por ejemplo piezas y paletas. En este caso, asigne un código de identificador a cada una de ellas.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Seleccione un elemento de la lista que forma parte de la solución ADCS y seleccione **Editar**.
3. En la página **Tarjeta de producto**, seleccione la acción **Identificadores**.
4. En la página **Identificadores producto**, seleccione la acción **Nuevo**.
5. En el campo **Código**, especifique el identificador del producto. Por ejemplo, podría ser el código de barras.  

    Puede introducir **Cód. variante** y un código **Unidad medida**.  

6. Si es necesario, introduzca varios códigos para cada artículo.
7. Elija el botón **Aceptar**.  
8. Para revisar información, seleccione el campo **Código identificador** para abrir la página **Identificadores producto**.

## <a name="to-add-an-adcs-user"></a>Para agregar a un usuario de un ADCS

Puede agregar cualquier usuario a un ADCS. Cuando lo haga, el usuario debe proporcionar a una contraseña. Opcionalmente, también puede proporcionar un anexo que identifica al usuario de un ADCS como empleado de almacén. La contraseña de usuario de un ADCS puede ser diferente de la contraseña de inicio de sesión. Obtenga más información en [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Usuarios de ADCS** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Nombre**, escriba un nombre para el usuario. El nombre no puede contener más de 20 caracteres, incluidos los espacios.  
4. En el campo **Contraseña**, introduzca una contraseña.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Para especificar que un empleado del almacén es usuario de un ADCS

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2. Si es necesario, agregue un nuevo empleado de almacén. Para obtener más información, consulte [Configurar empleados de almacén](warehouse-how-to-set-up-warehouse-employees.md).  
3. Seleccione la acción **Editar lista**.  
4. Seleccione un empleado de almacén de la lista. En el campo **Usuario de ADCS**, seleccione el nombre de un usuario de ADCS en la lista.  

> [!NOTE]  
> El almacén predeterminado para el empleado debe ser uno que utilice el sistema ADCS.

## <a name="to-create-and-customize-miniforms"></a>Para crear y personalizar miniformularios

Utilice los miniformularios que describen la información que desea fabricar en un dispositivo portátil. Por ejemplo, puede crear los miniformularios para utilizar la actividad de almacén de los artículos de picking. Una vez cree un miniformulario, puede agregar las funciones para las acciones comunes que un usuario tiene con dispositivos portátiles, como desplazarse arriba y abajo en una línea.  

> [!NOTE]
> Para ejecutar o cambiar las funcionalidad de una función del miniformulario, debe crear una nueva codeunit para el campo **Gestionar Codeunit** para realizar la acción o respuesta necesaria. Puede obtener más información sobre la funcionalidad de ADCS en las siguientes unidades de código:
>
> * 7705
> * 7706
> * 7712
> * 7713  

### <a name="to-create-a-miniform-for-adcs"></a>Para crear un miniformulario para un ADCS

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Miniformularios** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Escriba un código para el miniformulario en el campo **Código**. Opcionalmente, introduzca los valores en el resto de campos.  

    Active el control de alternancia **Iniciar Miniform.** para indicar que el es el primer formulario disponible cuando un usuario inicia sesión.  

4. En la ficha desplegable **Líneas**, defina los campos que aparecen en el miniformulario. El orden en que introduzca las líneas es en el que aparecen en el dispositivo portátil.  

Cuando haya creado un miniformulario, los pasos siguientes son crear las funciones y asociarlas la diversas entradas de teclado.  

### <a name="to-customize-miniform-functions"></a>Para personalizar las funciones del miniformulario

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Miniformularios** y luego elija el enlace relacionado.  
2. Seleccione un miniformulario de la lista y, a continuación, seleccione la acción **Editar**.  
3. Seleccione la acción **Funciones**.  
4. En la lista desplegable de **Cód. función**, seleccione un código que represente la función que desea asociar con el miniformulario. Por ejemplo, puede seleccionar **ESC** para asociar la funcionalidad con la tecla **ESC**.  

## <a name="see-also"></a>Consulte también

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
