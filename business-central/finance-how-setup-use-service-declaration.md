---
title: Configurar y utilizar la extensión de declaración de servicio
description: Aprenda a configurar y utilizar las funciones de declaración de servicio (Intrastat para servicios) para informar sobre el comercio de servicios con empresas de otros países de la UE.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, service, declaration,
ms.search.form: 30, 76, 5010, 5022, 5023, 5024, 5800
ms.date: 11/23/2022
ms.author: altotovi
ms.openlocfilehash: 0d5e541e1092b4fa655ab12d5c6d2fa48ff07f9d
ms.sourcegitcommit: bcd3e5dcbb3d839f38f2321b7ef35d4a2ce492c1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806339"
---
# <a name="the-service-declaration-extension"></a>La extensión de la declaración de servicio

En algunos países de la UE, las autoridades exigen que las empresas informen sobre la exportación de servicios a otros países de la UE. La extensión **Declaración de servicio** le permite recopilar información sobre el comercio de servicios en la UE e informar a las autoridades. Aunque se llama **Declaración de servicio**, también puede usarlo como **Intrastat para servicios**. Esta extensión está disponible para todos los países de la UE como una versión W1 y se puede usar tal cual en Bélgica. Para otros países, se requerirá una extensión basada en el país. Si un país solo necesita un formato diferente, puede usar la configuración del informe en el **Marco de intercambio de datos** para cambiar el formato.

## <a name="enable-the-service-declaration-extension"></a>Habilitar la extensión de declaración de servicio

Después de instalar la extensión en su entorno, debe habilitarla.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de características** y luego elija el enlace relacionado.
2. Busque **Característica: habilitar el uso de Declaración de servicio (Intrastat para servicios)** y en el campo **Habilitado para**, seleccione **Todos los usuarios**. Obtenga más información sobre la administración de características en [Habilitar las próximas funciones de antemano](/dynamics365/business-central/dev-itpro/administration/feature-management), en el contenido de la administración.
3. Cuando habilite la función, debe seguir los pasos del proceso de configuración a través del asistente de configuración. La mayoría de los campos están configurados por defecto.
4. Agregue solo **Tipos de transacción de servicio** en el segundo paso eligiendo la opción **Abrir la página de tipos de transacción de servicio para especificar la lista de códigos**.
5. Antes de comenzar, verifique el **Número total de códigos** para comprender cuántos tipos de transacciones de servicios ya se han especificado.
6. Elija **Finalizar** en el último paso para finalizar la configuración.

## <a name="set-up-the-service-declaration-extension"></a>Configurar la extensión de declaración de servicio

Puede configurar la extensión manualmente o mediante un archivo de informes en Definiciones de intercambio de datos.

### <a name="to-set-up-service-declaration-manually"></a>Para configurar la declaración de servicio manualmente

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de declaración de servicios** y luego elija el enlace relacionado.
2. En la ficha desplegable **General**, configure los campos tal como se describe en la tabla siguiente:

    |Campo  |Descripción  |
    |---------|---------|
    |**N.º declaración serie**     | Especifica la serie de números que se usará para asignar ID a nuevos registros.        |
    |**Cargos de producto de informe**  | Especifica si se deben informar los cargos de artículos. Si está habilitado, [!INCLUDE [prod_short](includes/prod_short.md)] comprueba el código de transacción de servicio para los cargos del artículo y los incluye en las declaraciones de servicio.        |
    |**Venta a/Factura a n.º cliente**     | Especifica el cliente que se usará para comparar su código de país con el código de país en la página **Información de la empresa** . Sólo se incluirán en la declaración de servicio los documentos en los que estos dos códigos sean diferentes.<br><br>* **Facturar a.**: utilice el código de país de **Facturar a cliente** <br<br>* **Vender a.**: utilice el código de país de **Vender a cliente**.        |
    |**Compra-a/Pagar a n.º proveedor**  | Especifica qué proveedor se usará para comparar su código de país con el código de país en la página **Información de la empresa** . Sólo se incluirán en la declaración de servicio los documentos en los que estos dos códigos sean diferentes.<br><br> * **Compra a.**: use el código de país de **Compra a proveedor**. <br><br> * **Pagar a.**: utilice el código de país de **Pagar al proveedor**.         |
    |**Código def. intercambio datos**  | Especifica el código definición de intercambio de datos que se usa para generar el archivo exportado para la declaración de servicio.        |
    |**Habilitar CIF/NIF**     |  Especifica si el **CIF/NIF** está habilitado para la declaración de servicio.       |

3. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tipos de transacción de servicio** y luego elija el enlace relacionado.
4. En las líneas, especifique **Códigos** y **Descripciones** para los tipos de transacción de servicio que usará.

### <a name="set-up-a-reporting-file"></a>Configurar un archivo de informe

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la ficha desplegable **General**, describa la definición de intercambio de datos, especificando el tipo de archivo de datos, el separador de columna, las codeunits relacionadas, XMLport y otros campos.
4. En la ficha desplegable **Definiciones de línea**, describa el formato de las líneas en el archivo de datos completando los campos según el campo **Tipo de línea** y donde necesita definir el número de columnas para esta línea.
5. En la ficha desplegable **Definiciones de columna**, complete la línea para cada columna planificada.
6. Elija la acción **Asignación de campos** en la ficha desplegable **Definiciones de línea** para abrir la página **Mapeo de campos**.
7. Cree una nueva entrada y, en la ficha desplegable **General**, elija el **Id. de tabla** adecuado (para la **Línea de declaración de servicio**, elija **5024**) y luego complete los campos así:
   1. En el campo **Índice de clave**, especifique la clave para ordenar los registros de origen antes de la exportación.
   2. Seleccione la **Codeunit de mapeo**.
8. En la ficha desplegable **Mapeo de campos**, agregue las columnas que configuró previamente en la ficha desplegable **Definiciones de columna** y luego agregue lo siguiente:
   1. Especifique el **Id. de campo** para cada una de las columnas.
   2. Especifique la **Regla de transformación** para cada columna según sea necesario. La regla transforma el texto importado en un valor admitido para que se pueda asignar a un campo especificado en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando elige un valor en este campo, el valor exacto se introduce en el campo **Regla de transformación** en la tabla **Búfer asignación campo intercambio datos** y viceversa.
9. Para agrupar entradas en función de las columnas, en la ficha desplegable **Agrupación de campos**, elija los campos que desea usar para agrupar.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] viene con una definición de intercambio de datos preconfigurada para **Declaración de servicio** para todos los países localizados. Obtenga más información acerca de cómo crear una nueva definición de intercambio de datos en [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).

## <a name="other-related-configurations"></a>Otras configuraciones relacionadas

Antes de usar la extensión Declaración de servicio, configure algunos campos para artículos, recursos y cargos de artículos.

### <a name="items"></a>Artículos

Configure la información relacionada con la Declaración de servicio en las páginas de la Tarjeta de artículo:

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Seleccione el elemento que quiere configurar.
3. Expanda la ficha desplegable **Artículo** y rellene los campos siguientes:
   1. En el campo **Tipo**, elija **Servicio**.
   2. En el campo **Código de tipo de transacción de servicio**, especifique el código para un **Tipo de transacción de servicio**.
   3. Si no desea incluir este elemento de servicio en las declaraciones de servicio, elija el campo **Excluir de la declaración de servicio**.

### <a name="resources"></a>Recursos

Configure la información relacionada con la Declaración de servicio en las páginas de la Tarjeta de recurso:

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.
2. Seleccione el recurso que quiere configurar.
3. Expanda la ficha desplegable **General** y rellene los campos siguientes:
   1. En el campo **Código de tipo de transacción de servicio**, especifique el código para un **Tipo de transacción de servicio**.
   2. Si no desea incluir este recurso en las declaraciones de servicio, elija el campo **Excluir de la declaración de servicio**.

### <a name="item-charges"></a>Cargos art.

Configure la información relacionada con la Declaración de servicio para los cargos del artículo:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cargos de producto**, y luego elija el enlace relacionado.
2. Seleccione el cargo del artíciulo que quiere configurar.
3. En el campo **Código de tipo de transacción de servicio**, especifique el código para un **Tipo de transacción de servicio**.
4. Si no desea incluir este carfgo de artículo en las declaraciones de servicio, seleccione el campo **Excluir de la declaración de servicio**.

## <a name="create-new-service-declaration"></a>Crear una declaración de servicio

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Declaraciones de servicio** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos siguientes en la ficha desplegable **General**:
    1. En el campo **Config. código**, especifique el código de configuración que se utiliza para sugerir líneas y crear archivos. Debe elegir uno como **Declaración de servicio**.
    2. En los campos **Fecha de inicio** y **Fecha de finalización** , especifique las fechas de inicio y finalización del período que se incluirá en el declaración de servicio.
4. Elija la acción **Sugerir líneas** para iniciar un trabajo por lotes que recopila líneas de documentos y completa las líneas de declaración de servicio.

El trabajo por lotes recupera todas las entradas de los documentos de compra y venta aplicables en el período requerido y las agrega en las líneas de declaración de servicio. Pase el cursor sobre los campos en las líneas para leer una breve descripción.

## <a name="modify-a-service-declaration"></a>Modificar una declaración de servicio

Si es necesario, puede modificar las líneas o agregar otras nuevas.

1. En la página **Declaración de servicio**, elija la acción **Nueva línea** en la ficha desplegable **Líneas**.
2. En el campo **Tipo de documento**, elija la opción relacionada con el documento que desea usar.
3. En función del **Tipo de documento**, rellene el campo **Nº documento**.
4. Rellene el resto de campos.

## <a name="overview-the-service-declaration-lines"></a>Información general de las líneas de la declaración de servicio

Después de crear una declaración de servicio, use la acción **Información general** para obtener una descripción general de las líneas de declaración de servicio. Puede agrupar y resumir las líneas de la misma manera que el archivo exportado. Las líneas también se pueden abrir en Excel.

## <a name="report-service-declaration-in-a-file"></a>Informe de declaración de servicio en un archivo

Puede enviar la declaración de servicio como un archivo según los requisitos de las diferentes autoridades locales. Para crear un archivo:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Declaraciones de servicio** y luego elija el enlace relacionado.
2. Elija la declaración de servicio que desea reportar como un archivo.
3. Si todavía no lo ha hecho, rellene el la declaración de servicio manualmente o elija la acción **Proponer líneas**.
4. Elija la acción **Crear archivo**.
5. El archivo de la declaración de servicio se guardará en el formato requerido.

## <a name="other-considerations"></a>Otras consideraciones

Cuando usa la extensión **Declaración de servicio**, hay algunas cosas más que debe considerar. Por ejemplo, es importante que sus grupos cumplan con los requisitos de las autoridades. También es importante que los servicios se incluyan correctamente en los documentos de compra y venta.

### <a name="grouping-lines"></a>Líneas de agrupación

En las líneas de declaración de servicios no existe agrupación por ningún campo. Todas las entradas se copian del documento original como fuente.

La agrupación requerida por las autoridades se proporcionará en el archivo exportado. Debe configurar los grupos en la **Definición de intercambio de datos**, que es totalmente configurable. Más información en [Configurar definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).

### <a name="using-services-in-document-lines"></a>Uso de servicios en líneas de documentos

Cuando crea una factura de compra o venta, encontrará dos campos relacionados con las declaraciones de servicio en sus líneas. Ambos campos se completan con los valores predeterminados de las configuraciones de su artículo, recurso o cargo del artículo.

- **Código de tipo de transacción de servicio**: especifica el código para un Tipo de transacción de servicio.
- **Aplicable para la declaración de servicio**: especifica si un elemento o recurso es aplicable para una declaración de servicio.

Puede cambiar los valores en estos campos, pero si selecciona el campo **Aplicable para declaración de servicio**, debe especificar un valor en la transacción de servicio **Escriba el campo Código**. Si no lo hace, no puede publicar el documento.

Si especifica un valor en el campo **Código de tipo de transacción de servicio** pero no selecciona el campo **Aplicable para declaración de servicio** puede contabilizar el documento, pero la línea no se calculará cuando lo haga.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Consulte también .

[Configurar informes de Intrastat](finance-how-setup-report-intrastat.md)
[Informes de Intrastat en Business Central](finance-how-report-intrastat.md)  
[Gestión financiera](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
