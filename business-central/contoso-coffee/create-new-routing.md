---
title: Crear una nueva ruta
description: Tutorial para aprender a introducir manualmente toda la información para una nueva ruta en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: deb1ef6ab18cbd6562ae18cc17495fe3e5021db1
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525250"
---
# <a name="walkthrough-create-a-new-routing"></a>Tutorial: Crear una nueva ruta

En este artículo, le guiaremos por los pasos para usar los datos de demostración de Contoso Coffee para configurar manualmente una nueva ruta de producción en [!INCLUDE [prod_short](../includes/prod_short.md)].  

## <a name="scenario"></a>Caso

Oscar, el ingeniero de procesos de Contoso Coffee, decide crear una nueva ruta con el nombre *Nueva ruta de acceso*. Puesto que esta ruta es diferente a cualquier otra ruta de Contoso Coffee, debe introducir manualmente toda la información para la ruta.  

## <a name="steps"></a>Pasos

1. Cree el encabezado de la ruta.  

    1. Elija la ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Rutas** y luego elija el vínculo relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº** |1099|
        |**Descripción** |Nueva ruta de acceso|
2. Cree las líneas de la ruta.

    1. En la ficha desplegable **Líneas**, agrega una nueva línea y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº operación** |10|
        |**Tipo** |Centro trabajo|
        |**Nº** |100|
        |**Tiempo preparación** |nº 20|
        |**Tiempo ejecución** |15|

    2. Agrega una nueva línea y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº operación** |nº 20|
        |**Tipo** |Centro trabajo|
        |**Nº** |200|
        |**Tiempo preparación** |30|
        |**Tiempo ejecución** |5|
3. Certifique la ruta.

    1. En el campo **Estado**, elija *Certificado*.  

La nueva ruta ya está configurada.  

## <a name="see-also"></a>Consulte también .

[Introducción a datos de demostración de Contoso Coffee](contoso-coffee-intro.md)  
