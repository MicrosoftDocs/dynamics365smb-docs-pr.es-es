---
title: Crear objetos XMLports basados en esquemas XML | Documentos de Microsoft
description: Utilice los esquemas XML para configurar el marco de intercambio de documentos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0d028206d1e17c7a1093cf2b93da02894909deb5
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554451"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>Uso de esquemas XML para preparar definiciones de intercambio de datos
Para habilitar la importación y exportación de datos en archivos XML mediante el marco de intercambio de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede usar esquemas XML de los archivos para definir los elementos de datos que desea intercambiar con [!INCLUDE[d365fin](includes/d365fin_md.md)]. Este trabajo se realiza en la página **Visor de esquema XML** mediante la carga del archivo de esquema XML, la selección de los elementos de datos pertinentes y la inicialización de una definición de intercambio de datos o un objeto XMLport.  

 Cuando haya definido qué elementos de datos se incluirán según el esquema XML, puede usar la acción **Generar XMLport** a fin de crear el objeto XMLport.  

 También puede utilizar la acción **Generar definición de intercambio de datos** para inicializar una definición de intercambio de datos en los datos seleccionados, que después podrá completar en el marco de intercambio de datos. Esto crea un registro en la página **Definiciones de intercambio de registro**, donde se continúa con la definición de qué elementos del archivo se asignan a qué campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

 Este tema incluye los siguientes procedimientos:  

-   Para cargar un archivo de esquema XML  

-   Para seleccionar o borrar nodos en un esquema XML  

-   Para generar una definición de intercambio de datos basada en un esquema XML  

-   Para generar un objeto XMLport para el archivo basado en un esquema XML  

-   Para importar un objeto XMLport en Object Designer  

### <a name="to-load-an-xml-schema-file"></a>Para cargar un archivo de esquema XML  

1.  Asegúrese de que esté disponible el archivo de esquema XML. La extensión de archivo es .xsd.  

2.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.  

3.  Seleccione la acción **Nuevo**.  

4.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Especifique un código para identificar el esquema XML.|  
    |**Descripción**|Especifique una descripción del esquema XML.|  

     El campo **Espacio de nombres de destino** especifica cualquier espacio de nombres del archivo de esquema XML que se ha cargado para la línea.  

5.  Elija la acción **Cargar esquema** y luego seleccione el archivo de esquema XML.  

     Cuando se carga el archivo, los demás campos de la línea se rellenan con la información del archivo y se selecciona la casilla **Esquema cargado**.  

    > [!NOTE]  
    >  El árbol del esquema XML cargado está contraído de forma predeterminada. Puede ampliar cada nodo eligiendo el botón **+** en el nodo. Para expandir todos los nodos, seleccione **Expandir todo** en la cinta.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Para seleccionar o borrar nodos en un esquema XML  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Visor esquemas XML** y luego elija el enlace relacionado.  

2.  Rellene los campos en la cabecera tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Código de esquema XML**|Especifique el archivo de esquema XML que se ha cargado en el paso 5 en la sección “Para cargar un archivo de esquema XML”.|  
    |**Nuevo nº de XMLport**|Especifique el número del objeto XMLport que se crea a partir de este esquema de XML cuando elige la acción **Generar XMLport**.|  

     Las líneas ahora se rellenan con nodos que representan todos los elementos del esquema XML. Los nodos de los elementos que son obligatorios según el esquema XML están seleccionados de forma predeterminada.  

3.  En la primera línea, en la columna **Nombre de nodo**, expanda el nodo **Documento** y, a continuación expanda gradualmente los nodos subyacentes que desea revisar.  

     También puede hacer clic con el botón secundario en un nodo y elegir **Expandir todo**.  

4.  Elija cualquiera de las acciones siguientes para cambiar los nodos que se muestran.  

    |**Acción**|Descripción|  
    |----------------|---------------------------------------|  
    |**Mostrar todos**|Se muestran todos los nodos.|  
    |**Ocultar elementos opcionales**|Solo se muestran los nodos que representan elementos que son obligatorios según el esquema XML. Estos nodos normalmente se indican mediante un **1** en el campo **MinOccurs**.<br /><br /> Elija **Mostrar todos** para revertir la vista.|  
    |**Ocultar elementos no seleccionados**|Solo se muestran los nodos donde está seleccionada la casilla **Seleccionado**.<br /><br /> Elija **Mostrar todos** para revertir la vista.|  

5.  Seleccione la acción **Editar**.  

6.  En la casilla **Seleccionado**, especifique para cada nodo si desea que el elemento se admita en la definición de intercambio de datos para el archivo bancario SEPA relacionado.  

    > [!NOTE]  
    >  Al seleccionar un nodo secundario obligatorio, también se seleccionan todos los nodos principales por encima de él.  

7.  Elija la acción **Seleccionar todos los elementos obligatorios** para reelegir todos los nodos que representen elementos obligatorios según el esquema XML.  

8.  Elija la acción **Anular selección** para borrar todas las selecciones.  

     El campo **Opción** especifica que el nodo tiene dos o más nodos de hermano que funcionan como opciones.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Para generar una definición de intercambio de datos basada en un esquema XML  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.  

2.  Seleccione el esquema XML relevante y luego elija la acción **Abrir Visor de esquema XML**.  

3.  Asegúrese de que estén seleccionados los nodos correspondientes. Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".  

4.  En la página **Visor de esquemas XML**, elija la acción **Generar definición de intercambio de datos**.  

 Se crea una definición de intercambio de datos en la página **Definiciones de intercambio de registro**, que se puede completar especificando qué elementos del archivo de banco SEPA se corresponden con los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
>  También puede utilizar la función **Obtener estructura de archivo** desde la página **Definiciones de intercambio de registro**, la cual utiliza la funcionalidad de la página **Visor esquemas XML** para prellenar la ficha desplegable **Definiciones de columna**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Para generar un objeto XMLport basado en un esquema XML  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.  

2.  Seleccione el esquema XML relevante y luego elija la acción **Abrir Visor de esquema XML**.  

3.  En el campo **N.º XMLport nuevo** especifique el número que recibirá el nuevo objeto XMLport cuando se genere.  

4.  Asegúrese de que estén seleccionados los nodos correspondientes. Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".  

5.  Elija la acción **Generar XMLport** y, a continuación, guarde el objeto como un archivo .txt en un almacén adecuado.  

6. Importe el nuevo XMLport en el entorno de desarrollo de [!INCLUDE[d365fin](includes/d365fin_md.md)] y compílelo.

## <a name="see-also"></a>Consulte también  
[Configurar definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md)   
[Exportar pagos a un archivo bancario](payables-how-export-payments-bank-file.md)   
[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)   
[Acerca del marco de intercambio de datos](across-about-the-data-exchange-framework.md)
