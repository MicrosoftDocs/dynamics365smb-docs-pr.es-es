---
title: Crear objetos XMLports basados en esquemas XML | Documentos de Microsoft
description: Utilice los esquemas XML para configurar el marco de intercambio de documentos.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c4b53c6a87148990102ba9eca235cf139a48396e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-xml-schemas-to-prepare-data-exchange-definitions"></a>Procedimiento: Uso de esquemas XML para preparar definiciones de intercambio de datos
Para habilitar la importación y exportación de datos en archivos XML mediante el marco de intercambio de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede usar esquemas XML de los archivos para definir los elementos de datos que desea intercambiar con [!INCLUDE[d365fin](includes/d365fin_md.md)]. Este trabajo se realiza en la ventana **Visor de esquema XML** mediante la carga del archivo de esquema XML, la selección de los elementos de datos pertinentes y la inicialización de una definición de intercambio de datos o un objeto XMLport.  

 Cuando haya definido qué elementos de datos se incluirán según el esquema XML, puede usar la acción **Generar XMLport** a fin de crear el objeto XMLport.  

 También puede utilizar la acción **Generar definición de intercambio de datos** para inicializar una definición de intercambio de datos en los datos seleccionados, que después podrá completar en el marco de intercambio de datos. Esto crea un registro en la ventana **Definiciones de intercambio de registro**, donde se continúa con la definición de qué elementos del archivo se asignan a qué campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Procedimiento: Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

 Este tema incluye los siguientes procedimientos:  

-   Para cargar un archivo de esquema XML  

-   Para seleccionar o borrar nodos en un esquema XML  

-   Para generar una definición de intercambio de datos basada en un esquema XML  

-   Para generar un objeto XMLport para el archivo basado en un esquema XML  

-   Para importar un objeto XMLport en Object Designer  

### <a name="to-load-an-xml-schema-file"></a>Para cargar un archivo de esquema XML  

1.  Asegúrese de que esté disponible el archivo de esquema XML. La extensión de archivo es .xsd.  

2.  En el cuadro **Buscar**, escriba **Esquemas XML** y, a continuación, elija el vínculo relacionado.  

3.  En la pestaña **Inicio**, en el grupo **Nuevo**, seleccione **Nuevo**.  

4.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|[Description]|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Especifique un código para identificar el esquema XML.|  
    |**Descripción**|Especifique una descripción del esquema XML.|  

     El campo **Espacio de nombres de destino** especifica cualquier espacio de nombres del archivo de esquema XML que se ha cargado para la línea.  

5.  En la pestaña **Inicio**, en el grupo **Proceso**, seleccione **Cargar esquema** y seleccione luego el archivo de esquema XML.  

     Cuando se carga el archivo, los demás campos de la línea se rellenan con la información del archivo y se selecciona la casilla **Esquema cargado**.  

    > [!NOTE]  
    >  El árbol del esquema XML cargado está contraído de forma predeterminada. Puede ampliar cada nodo eligiendo el botón **+** en el nodo. Para expandir todos los nodos, seleccione **Expandir todo** en la cinta.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Para seleccionar o borrar nodos en un esquema XML  

1.  En el cuadro **Buscar**, escriba **Visor esquemas XML** y, a continuación, elija el vínculo relacionado.  

2.  Rellene los campos en la cabecera tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Código de esquema XML**|Especifique el archivo de esquema XML que se ha cargado en el paso 5 en la sección “Para cargar un archivo de esquema XML”.|  
    |**N.º XMLport nuevo**|Especifique el número del objeto XMLport que se crea a partir de este esquema de XML cuando elige la acción **Generar XMLport**.|  

     Las líneas ahora se rellenan con nodos que representan todos los elementos del esquema XML. Los nodos de los elementos que son obligatorios según el esquema XML están seleccionados de forma predeterminada.  

3.  En la primera línea, en la columna **Nombre de nodo**, expanda el nodo **Documento** y, a continuación expanda gradualmente los nodos subyacentes que desea revisar.  

     También puede hacer clic con el botón secundario en un nodo y elegir **Expandir todo**.  

4.  En la pestaña **Inicio**, en el grupo **Ver**, seleccione cualquiera de las acciones siguientes para cambiar los nodos que se muestran.  

    |**Acción**|Description|  
    |----------------|---------------------------------------|  
    |**Mostrar todos**|Se muestran todos los nodos.|  
    |**Ocultar elementos opcionales**|Solo se muestran los nodos que representan elementos que son obligatorios según el esquema XML. Estos nodos normalmente se indican mediante un **1** en el campo **MinOccurs**.<br /><br /> Elija **Mostrar todos** para revertir la vista.|  
    |**Ocultar elementos no seleccionados**|Solo se muestran los nodos donde está seleccionada la casilla **Seleccionado**.<br /><br /> Elija **Mostrar todos** para revertir la vista.|  

5.  En la pestaña **Inicio**, en el grupo **Administrar**, elija **Editar**.  

6.  En la casilla **Seleccionado**, especifique para cada nodo si desea que el elemento se admita en la definición de intercambio de datos para el archivo bancario SEPA relacionado.  

    > [!NOTE]  
    >  Al seleccionar un nodo secundario obligatorio, también se seleccionan todos los nodos principales por encima de él.  

7.  Elija la acción **Seleccionar todos los elementos obligatorios** para reelegir todos los nodos que representen elementos obligatorios según el esquema XML.  

8.  Elija la acción **Anular selección** para borrar todas las selecciones.  

     El campo **Opción** especifica que el nodo tiene dos o más nodos de hermano que funcionan como opciones.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Para generar una definición de intercambio de datos basada en un esquema XML  

1.  En el cuadro **Buscar**, escriba **Esquemas XML** y, a continuación, elija el vínculo relacionado.  

2.  Seleccione el esquema XML y, a continuación, en la pestaña **Inicio**, en el grupo **Procesar**, elija **Abrir Visor de esquema XML**.  

3.  Asegúrese de que estén seleccionados los nodos correspondientes. Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".  

4.  En la ventana **Visor de esquema XML**, en la pestaña **Inicio**, en el grupo **Procesar**, seleccione **Generar definición de intercambio de datos**.  

 Se crea una definición de intercambio de datos en la ventana **Definiciones de intercambio de registro**, que se puede completar especificando qué elementos del archivo de banco SEPA se corresponden con los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Procedimiento: Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  También puede utilizar la función **Obtener estructura de archivo** desde la ventana **Definiciones de intercambio de registro**, la cual utiliza la funcionalidad de la ventana **Visor esquemas XML** para prellenar la ficha desplegable **Definiciones de columna**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Para generar un objeto XMLport basado en un esquema XML  

1.  En el cuadro **Buscar**, escriba **Esquemas XML** y, a continuación, elija el vínculo relacionado.  

2.  Seleccione el esquema XML y, a continuación, en la pestaña **Inicio**, en el grupo **Procesar**, elija **Abrir Visor de esquema XML**.  

3.  En el campo **N.º XMLport nuevo** especifique el número que recibirá el nuevo objeto XMLport cuando se genere.  

4.  Asegúrese de que estén seleccionados los nodos correspondientes. Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".  

5.  En la pestaña **Inicio**, en el grupo **Procesar**, seleccione **Generar XMLport** y, a continuación, guarde el objeto como un archivo .txt en una ubicación adecuada.  

6. Importe el nuevo XMLport en el entorno de desarrollo de [!INCLUDE[d365fin](includes/d365fin_md.md)] y compílelo.

## <a name="see-also"></a>Consulte también  
[Procedimiento: Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md)   
[Exportación de pagos a un archivo de banco](payables-how-export-payments-bank-file.md)   
[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
[Acerca del marco de intercambio de datos](across-about-the-data-exchange-framework.md)

