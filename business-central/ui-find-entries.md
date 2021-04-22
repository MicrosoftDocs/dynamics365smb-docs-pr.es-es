---
title: Encontrar entradas | Microsoft Docs
description: Este artículo describe cómo encontrar documentos y entradas que están relacionadas
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5f8ddd7176e69c9d1eb3b8d8ff98c93695d50993
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771166"
---
# <a name="finding-related-entries-for-posted-documents"></a>Búsqueda de entradas relacionadas para documentos registrados 

En este artículo, aprenderá a buscar documentos y entradas que estén relacionados entre sí en función de una información común, como:

- Número de documento o fecha de publicación
- Tipo de contacto comercial, número o número de documento externo
- Número de serie del producto o número de lote

Esta característica es útil para buscar los movimientos originados por ciertas transacciones. Al realizar búsquedas por número de documentos, puede imprimir el resumen desde el informe Listas de documentos.

## <a name="get-started"></a>Introducción

La característica de búsqueda de entradas está disponible en la mayoría de las páginas que muestran documentos publicados o entradas de documentos publicados, tanto para listas como para tarjetas. Por tanto, el primer paso es abrir una de estas páginas. Luego, elija la acción **Buscar entradas** o presione las teclas Alt + G.

La página **Buscar entradas** incluye todos los documentos relacionados y las entradas basadas en el n.º documento y la fecha de registro. La página está dividida en tres secciones:

- La sección superior muestra los campos y las acciones que utiliza para filtrar su búsqueda.
- La sección central muestra documentos relacionados basados en la búsqueda.
- La sección inferior muestra información sobre el documento de origen que se encontró mediante la búsqueda.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Buscar entradas

Puede buscar entradas basándose en información sobre el documento, el contacto comercial o la referencia del producto. Para cambiar la búsqueda, seleccione **Accione**, **Buscar por** y luego una de las siguientes acciones:

|Acción|Descripción|
|------|-----------|
|Buscar por documento|Vea entradas según un n.º documento específico o una fecha de registro.|
|Contacto de negocio |Vea entradas basadas en un tipo de contacto específico, número de contacto, y/o n.º documento externo. Puede introducir información sobre el documento asignado por un proveedor o un cliente. Utilice los campos disponibles para buscar documentos de proveedor mediante el uso de los números que el proveedor ha asignado a los documentos.|
|Referencia a producto|Ver entradas basadas en un número de serie o número de lote. Puede escribir el número de lote o número de serie, o filtrar en el número de lote o número de serie en el que quiera buscar. Esta acción resulta útil para ver dónde se uso un número de seguimiento de producto concreto, de qué proveedor se obtuvo o a qué cliente se vendió.|

Después de hacer una selección, introduzca la información de búsqueda relevante en los campos de la parte superior. Utilice la información de los campos como ayuda. Cuando haya terminado, elija **Buscar** para iniciar la búsqueda. Si cambia cualquiera de los filtros, deberá volver a elegir **Buscar**.

> [!TIP]
> Para ver un par de ejemplos sobre el uso de **Buscar entradas**, consulte [Seguimiento de productos con seguimiento de productos](inventory-how-to-trace-item-tracked-items.md) y [Tutorial: seguimiento de números de lote de serie](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Trabajar con Business Central](ui-work-product.md)  
[Agregar una acción de página al área de trabajo](ui-bookmarks.md)  
[Realizar seguimiento de productos seguidos](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]