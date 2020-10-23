---
title: Configuración de registro de transacciones entre empresas | Documentos de Microsoft
description: Cree sus proveedores y clientes de empresas vinculadas, como los llamados socios de empresas vinculadas, y configure un plan de cuentas de empresas vinculadas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2f85488cd3e3a764d1fd0c60e4d314d4729f03d2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915490"
---
# <a name="set-up-intercompany"></a>Configurar empresa vinculada
Para que una transacción (por ejemplo, una línea del diario de ventas) se envíe de una empresa y se cree automáticamente la transacción correspondiente (por ejemplo, una línea del diario de compras) en la empresa asociada, ambas empresas tiene que acordar el plan de cuentas común y definir las dimensiones que utilizarán en las transacciones entre ambas. El plan de cuentas de empresas vinculadas puede ser, por ejemplo, una versión simplificada del plan de cuentas de la empresa matriz. Cada empresa asigna su plan de cuentas al plan de cuentas de empresas vinculadas compartido y asigna sus dimensiones a las dimensiones de empresas vinculadas.  

También debe configurar un código de socio de empresas vinculadas para cada empresa asociada, que se acuerda entre todas las empresas y, a continuación, asignarlo a las tarjetas de cliente y de proveedor, respectivamente, rellenando el campo **Código de socio de empresas vinculadas**.  

Si va a crear o a recibir líneas de empresas vinculadas con productos, puede utilizar sus propios números de producto o configurar los números de producto de sus socios para cada producto que corresponda, ya sea en el campo **Cód. producto proveedor** o en **Nº producto común** en la ficha del producto. También puede usar la función **Referencia cruzada producto** para asignar los números de producto a las descripciones de los productos de las empresas asociadas, abra la ficha de cada producto y, a continuación, elija la acción **Referencias cruzadas** para configurar las referencias cruzadas entre su descripción de los artículos y la de la empresa asociada. Para obtener más información, vea [Usar referencias cruzadas de producto](inventory-how-use-item-cross-refs.md). 

Si va a realizar transacciones de ventas entre empresas vinculadas que incluyan recursos, debe rellenar el campo **Nº cuenta compra IC asociada** en la ficha de cada recurso que proceda. Es el número de la cuenta de empresas vinculadas en la empresa asociada en la que se registrará la cantidad correspondiente a este recurso. Para obtener más información, consulte [Configurar recursos](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Establecer empresas para transacciones entre empresa vinculadas
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.  
2. En la página **Información de la empresa**, rellene los campos **Código de socio de empresas vinculadas**, **Tipo de bandeja de entrada de las empresas vinculadas** y **Detalles de bandeja de entrada de las empresas vinculadas**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Para establecer socios de empresas vinculadas
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Socios de empresas vinculadas** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Socios de empresas vinculadas**, rellene los campos según sea necesario.

> [!NOTE]
> En [!INCLUDE[d365fin](includes/d365fin_md.md)] online, no puede utilizar ubicaciones de archivos para transferir transacciones a sus socios porque [!INCLUDE[d365fin](includes/d365fin_md.md)] no tiene acceso a su red local. Por tanto, si elige **Ubicación del archivo** en el campo **Tipo de transferencia**, el campo **Ruta de la carpeta** no está disponible. En su lugar, el archivo se descargará a la carpeta Descargas de su computadora. Luego envía el archivo a alguien de la empresa asociada, por ejemplo, por correo electrónico. Para un proceso más directo, le recomendamos que elija **Email** en lugar.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Para configurar proveedores y clientes de empresas vinculadas
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. De forma alternativa, acceda al proveedor desde el campo **N.º proveedor** en la página **Proveedor empresas vinculadas**.
3. Abra la ficha de un proveedor que sea un socio de empresa vinculada. Para obtener más información, vea [Registrar nuevos proveedores](purchasing-how-register-new-vendors.md).
4. En el campo **Socio de empresa vinculada**, seleccione el código de socio de empresas vinculadas correspondiente.
5. Repita los pasos 1 a 4 para los clientes.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Para configurar los planes de cuentas de las empresas vinculadas
Para que un grupo de empresas vinculadas pueda realizar transacciones entre ellas, deben aprobar un plan de cuentas para utilizarlo como referencia común. Debe ponerse de acuerdo con las empresas asociadas en cuanto a los números de cuenta que todos utilizarán al crear transacciones entre empresas vinculadas. Por ejemplo, la empresa matriz del grupo puede crear una versión simplificada de su propio plan de cuentas, exportar este plan de cuentas de empresas vinculadas desde su base de datos a un archivo XML y distribuirlo al resto de empresas del grupo.  

Si su empresa es la empresa asociada y se encarga de definir el plan de cuentas de las empresas vinculadas que utilizará el grupo como referencia común, siga el procedimiento [Configurar la definición de las empresas vinculadas](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Si su empresa es una empresa subsidiaria y ha recibido un archivo XML que contiene el plan de cuentas común de las empresas vinculadas, siga el procedimiento [Para importar el plan de cuentas de empresas vinculadas:](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Configurar la definición de las empresas vinculadas
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas de empresas vinculadas** y luego elija el enlace relacionado.
2. En la página **Plan de cuentas de empresas vinculadas**, introduzca cada cuenta en una línea en la página.  
3. Si su plan de cuentas de empresas vinculadas va a ser idéntico o similar al suyo habitual, puede rellenar la página automáticamente mediante la acción **Copiar de Plan de cuentas**. Puede editar las líneas nuevas si es necesario.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Para exportar el plan de cuentas de empresas vinculadas:
Para permitir que sus socios de empresas vinculadas importen el plan de cuentas definido, debe exportarlo a un archivo.      
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas de empresas vinculadas** y luego elija el enlace relacionado.
2. En la página **Plan de cuentas de empresas vinculadas**, seleccione la acción **Exportar** y, a continuación, el botón **Guardar**.
3. Indique el nombre y la ubicación que desea utilizar para guardar el archivo XML y seleccione **Guardar**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Para importar el plan de cuentas de empresas vinculadas  
Cuando existe un archivo para el plan de cuentas de empresas vinculadas definido, los socios de las empresas vinculadas pueden importarlo para asegurarse de que tienen las mismas cuentas.  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas de empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Plan de cuentas de empresas vinculadas**, seleccione la acción **Importar**.  
3. Seleccione el nombre y la ubicación del archivo XML y elija el botón **Abrir**.  

La página **Plan de cuentas IC** se rellena con las líneas de cuentas nuevas o modificadas según el plan de cuentas de empresas vinculadas en el archivo. Las líneas existentes, no relacionadas en la página permanecen sin cambios.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Para asignar el plan de cuentas de empresas vinculadas al plan de cuentas de la empresa propia  
Cuando ha definido o importado el plan de cuentas de empresas vinculadas que su empresa y las empresas vinculadas asociadas han acordado utilizar, debe asociar cada una de las cuentas de empresas vinculadas a una de las cuentas de su empresa. En la página **Plan de cuentas IC**, puede especificar cómo se transformarán las cuentas de empresas vinculadas, en transacciones entrantes, en cuentas del plan de cuentas de su empresa.

Si las cuentas del plan de cuentas de empresas vinculadas tiene los mismos números de cuenta que las correspondientes del plan de cuentas, puede asignar las cuentas automáticamente.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas de empresas vinculadas** y luego elija el enlace relacionado.  
2. Seleccione las líneas que desea asignar automáticamente y seleccione la acción **Asignar a cuenta con igual n.º**.  
3. Para las cuentas de empresas vinculadas que no se asignan automáticamente, rellene el campo **N.º de cuenta de asignación** .  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Para configurar cuentas de contabilidad de socios de empresas vinculadas predeterminadas  
Cuando crea una línea de venta o de compra de empresas vinculadas para enviarla como transacción saliente, introducirá una cuenta del plan de cuentas de empresas vinculadas como cuenta predeterminada en la que se registra el importe en la empresa asociada. En la página **Plan de cuentas**, para las cuentas que utiliza a menudo en líneas de diario de ventas o compras salientes, puede especificar una cuenta genérica de empresa vinculada asociada. Por ejemplo, para su cuenta de clientes, puede introducir las cuentas de proveedores correspondientes desde el plan de cuentas de empresas vinculadas.  

Ahora, cuando introduzca una cuenta contable en el campo **Cta. contrapartida** en una línea de empresas vinculadas con **Socio de empresas vinculadas** en el campo **Tipo de cuenta** el campo **Cuentas genéricas de empresas vinculadas asociadas** se rellenará automáticamente.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. En la línea de una cuenta que se utiliza para transacciones entre empresas vinculadas, en el campo **Cuentas genéricas de empresas vinculadas asociadas**, ingrese la cuenta de contabilidad general entre empresas vinculadas que su socio registrará cuando registre en la cuenta de contabilidad en la línea.  
3. Repita el paso 2 para cada cuenta que introduzca a menudo en el campo **Cta. contrapartida** en un diario o documento de empresas vinculadas.

## <a name="to-set-up-intercompany-dimensions"></a>Para configurar registros entre empresas vinculadas
Si usted y las empresas vinculadas asociadas desean intercambiar transacciones que estén relacionadas con dimensiones, debe estar de acuerdo en las dimensiones que todos usarán. Por ejemplo, la empresa matriz del grupo puede crear una versión simplificada de su propio grupo de dimensiones, exportar estas dimensiones de empresas vinculadas a un archivo XML y distribuirlas al resto de empresas del grupo. Cada una de las subsidiarias importará el archivo XML en la página **Dimensiones de empresas vinculadas** y asignará las dimensiones de las empresas vinculadas a las de su propia página **dimensiones**.  

Si su empresa es la empresa asociada y se encarga de definir el conjunto de dimensiones de las empresas vinculadas que utilizará el grupo como referencia común, siga el procedimiento [Definir las dimensiones de empresas vinculadas](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Si su empresa es una empresa subsidiaria y ha recibido un archivo XML que contiene las dimensiones de las empresas vinculadas que utilizará el grupo como referencia común, siga el procedimiento [Importar las dimensiones de empresas vinculadas](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Definir las dimensiones de empresas vinculadas
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Dimensiones de empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Dimensiones de empresas vinculadas**, introduzca cada dimensión en una línea de la página.

    Si las dimensiones de empresas vinculadas va a ser idénticas o similares a las de su empresa, puede rellenar la página automáticamente mediante la función **Copiar de Dimensiones** y, a continuación, modificar las líneas resultantes.  
3. Para exportar las empresas vinculadas a un archivo XML para distribuirlo entre sus socios, elija la acción **Exportar**.  
4. Indique el nombre y la ubicación que desea utilizar para guardar el archivo XML y seleccione **Guardar**.  

### <a name="to-import-the-intercompany-dimensions"></a>Importar las dimensiones de empresas vinculadas  
Cuando existe un archivo para las dimensiones de empresas vinculadas definido, los socios de las empresas vinculadas pueden importarlo para asegurarse de que tienen las mismas dimensiones.  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Dimensiones de empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Dimensiones de empresas vinculadas**, seleccione la acción **Importar**.  
3. Especifique el nombre y la ubicación del archivo XML y elija el botón **Abrir**.  

Se han importado las líneas de las páginas **Dimensiones de empresas vinculadas** y **Valores de dimensión de empresas vinculadas**.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Para asignar dimensiones de empresas vinculadas a las dimensiones de su empresa
Cuando haya definido o importado las dimensiones que su empresa y las empresas vinculadas asociadas han acordado utilizar, debe asociar cada una de las dimensiones de empresas vinculadas a una de las dimensiones de su empresa, y a la inversa. En la página **Dimensiones de empresas vinculadas**, puede especificar cómo se transformarán las dimensiones de las empresas vinculadas en transacciones entrantes, en dimensiones de la lista de dimensiones de su propia empresa. En la página **Dimensiones**, puede especificar cómo se transformarán sus dimensiones en dimensiones de empresas vinculadas, en transacciones salientes.

Si alguna de las dimensiones de empresas vinculadas tiene el mismo código que las dimensiones correspondientes de la lista de dimensiones de su empresa, puede dejar que la aplicación realice automáticamente las asignaciones y, a continuación, puede asignar las cuentas automáticamente.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Dimensiones de empresas vinculadas** y luego elija el enlace relacionado.
2. Abra la página **Dimensiones de empresas vinculadas**, seleccione las líneas que desea asignar automáticamente y elija la acción **Asignar a dim. con igual código**.
3. Para cada dimensión de empresas vinculadas que no se asocia automáticamente, rellene el campo **Código dimensión de asignación**.

    Puede que tenga que agregar el campo a su vista. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).
4. Seleccione la acción **Valores de dimensiones de empresas vinculadas**.
5. En la página **Valores de dimensiones de empresas vinculadas**, rellene el campo **Código valor dimens. asig.**

    Proceda a asignar las dimensiones a las dimensiones de empresas vinculadas realizando pasos similares.
6. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Dimensiones** y, a continuación, elija el enlace relacionado.
7. Abra la página **Dimensiones**, seleccione las líneas que desea asignar automáticamente y elija la acción **Asignar a dim. IC con igual código**.
8. Para cada dimensión de empresas vinculadas que no se asocia automáticamente, rellene el campo **Código valor dimens. IC asig.**.
9. Seleccione la acción **Valores de dimensión**.
10. En la página **Valores de dimensiones**, rellene el campo **Código valor dimens. IC asig.**

## <a name="see-also"></a>Consulte también
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
