---
title: Configurar códigos para pistas de auditoría | Documentos de Microsoft
description: Aprenda sobre las tareas para configurar códigos de origen y códigos de auditoría que puede usar para realizar un seguimiento de pistas de auditoría.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e39de1d4656b272c5c6cf5c01f54d5d6ebeca05b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914219"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Configuración de códigos de origen y códigos de auditoría para pistas de auditoría

Todos los movimientos registrados se asignan automáticamente a un código de origen de forma que pueda realizarse un seguimiento del origen de las transacciones. Si desea asignar a los movimientos un código de origen adicional, utilice códigos de auditoría. Los códigos de auditoría se utilizan para indicar el motivo por el que se ha creado un movimiento. Al configurar códigos de auditoría, puede asignarlos a libros de diarios o a secciones de diarios, así como a líneas de diarios y a documentos individuales.  

Tanto para los códigos fuente como para los códigos de auditoría, use códigos que sean descriptivos y fáciles de recordar. El código debe ser único y puede configurar tantos códigos como desee.

## <a name="define-source-codes"></a>Definir los códigos de origen

A veces querrá saber cómo surge un movimiento determinado, por ejemplo, si procedía del registro de un diario general o de una factura de compra. Un código de origen indica dónde se creó un movimiento. Los movimientos se crean cuando se registran los diarios y facturas, y cuando se ejecutan determinados trabajos por lotes. Cada tipo de registro tiene un código de origen diferente que se asigna cuando se crean entradas individuales.  

El registro de diarios, pedidos, facturas o abonos, así como la ejecución de diversos trabajos por lotes, genera movimientos en los extractos financieros. La página **Configuración códigos origen** contiene varias fichas desplegables, una por cada área de aplicación. Cada ficha desplegable contiene los códigos de origen correspondientes a esa área de aplicación.

Cuando registra o ejecuta un trabajo por lotes, el programa adjunta automáticamente el código de origen correspondiente al movimiento. Por ejemplo, al registrar desde el diario general, el programa codificará el movimiento con la abreviatura *DIAGEN*. Luego puede filtrar la página **Movs. contabilidad** para mostrar qué movimientos se publicaron desde el diario general o desde documentos de ventas, por ejemplo.

### <a name="to-define-source-codes"></a>Para definir códigos de origen

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Configuración códigos origen** y, a continuación, elija el vínculo relacionado.  

2. En la ventana **Configuración del código fuente**, especifique el código fuente relevante para cada tipo de registro y trabajo por lotes.  

Puede cambiar el contenido de un campo más tarde, y ese cambio afectará a futuros registros.

## <a name="change-source-codes"></a>Cambiar códigos de origen

Puede querer cambiar un código de origen. Por ejemplo, quiere modificar el código de origen *GENJNL* a *GNJ*.

### <a name="to-change-source-codes"></a>Para modificar códigos de origen

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Códigos de origen** y, a continuación, elija el vínculo relacionado.

2. En la línea que contiene el código que debe modificarse, seleccione el código en el campo **Código**.

3. Introduzca el nuevo código y, a continuación, elija el botón **Sí**. También puede modificar el contenido del campo **Descripción**.

Todos los nuevos movimientos que se registren posteriormente del diario general tendrán el nuevo código de origen.

## <a name="define-reason-codes"></a>Definir códigos de auditoría

Los códigos de auditoría complementan los código de origen y se utilizan para indicar por qué se creó una entrada. Puede asignar códigos de auditoría en movimientos individuales y puede asignar códigos permanentes a libros de diarios y secciones de diario específicos. Cuando un código de auditoría está vinculado a una línea del diario o a una cabecera de ventas o de compra, se marcan todos los movimientos con el código de auditoria al registrarlos.  

### <a name="to-set-up-reason-codes"></a>Para configurar códigos de auditoría

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Código de auditoría** y, a continuación, elija el vínculo relacionado.

2. En la ventana **Códigos auditoría**, introduzca el primer código en el campo **Código**. En el campo **Descripción**, escriba un texto explicativo.

Repita el procedimiento para cada código que desee utilizar. Puede configurar cualquier número de códigos.

El siguiente procedimiento describe cómo agregar un código de auditoría a un libro del diario, pero se aplican pasos similares para agregar un código de auditoría a una línea del diario o sección del diario.  

### <a name="to-assign-reason-codes-to-journal-templates"></a>Para asignar códigos de auditoría a libros de diarios

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Libro diario general** y, a continuación, elija el vínculo relacionado.

2. En la línea que contiene el libro del diario seleccionado, en el campo **Código de auditoría**, especifique el código relevante.

3. Cierre el libro del diario.

El código de auditoría seleccionado se copiará en las nuevas secciones de diario creadas en este libro del diario. Para asignar códigos de auditoría a libros de diario de otras áreas de aplicación, deberá proceder del mismo modo.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Para usar códigos de auditoría en documentos de compras y ventas

1. Abra el documento de compras correspondiente.

2. En la cabecera de ventas o de compra, escriba el código en el campo **Código de auditoría**.

Al registrar la factura, el código de auditoría se copia en cada movimiento de contabilidad, cliente y proveedor. No puede asignar códigos de auditoría distintos a cada una de las líneas de compra porque todas las líneas se registran como un solo movimiento.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Trabajar con [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
