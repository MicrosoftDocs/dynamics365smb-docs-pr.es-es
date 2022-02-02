---
title: La extensión Archivo de datos
description: El archivo de datos crea una copia de seguridad de bajo costo de sus registros.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 630
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 4070ff5658ad4aa976c181a3df377155080f1e3b
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012082"
---
# <a name="the-data-archive-extension"></a>La extensión Archivo de datos
Con el tiempo, su empresa acumulará una cantidad sustancial de datos y, como administrador, probablemente sea una buena idea tener una estrategia para archivar datos. Tener muchos datos puede ralentizar las cosas, por ejemplo, puede llevar un poco más de tiempo generar informes o incluso bloquear registros. Además, grandes cantidades de datos pueden generar mayores costos de almacenamiento.

La extensión Archivo de datos proporciona un marco básico para archivar y realizar copias de seguridad de los datos como parte de la compresión por fechas. Cuando utiliza compresión por fechas, las entradas relacionadas se consolidan en una sola entrada y los originales se eliminan. Para más información, vea [Comprimir datos con compresión por fechas](admin-manage-documents.md#compress-data-with-date-compression). Sin embargo, puede ser útil conservar esos datos, por lo que en lugar de eliminarlos, puede archivarlos para su uso posterior.

## <a name="start-archiving-data"></a>Iniciar el archivo de datos
La extensión está preinstalada y disponible en la **Administración de extensiones**, por lo que no necesita hacer nada para comenzar. La extensión también está disponible en Microsoft AppSource. 

Sus archivos de datos se enumeran en la página **Lista de archivo de datos**. Cada archivo puede contener datos de varias tablas y puede contener hasta 10.000 registros. Si hay más de 10.000 registros en una tabla, se creará un segundo archivo para los 10.000 registros siguientes, y así sucesivamente. Por ejemplo, si archiva 10.100 entradas de contabilidad, Business Central crea un archivo "Entrada de contabilidad" para las primeras 10.000 entradas y luego un segundo archivo para las 100 entradas restantes. 

Después de archivar los datos, puede explorarlos usando Microsoft Excel o como archivo CSV.

* Si usa la opción de Excel, el libro de trabajo contendrá una hoja de cálculo para cada tabla del archivo de datos.
* Si usa la opción CSV, obtendrá un archivo ZIP con un archivo CSV para cada tabla del archivo de datos.

> [!TIP]
> Las opciones Excel y CSV facilitan el uso de otra aplicación o servicio para mover los datos a otra ubicación, como Azure Blob Storage, o una herramienta de análisis, como Microsoft Power BI.

Los siguientes trabajos por lotes utilizan las extensiones Archivo de datos para compresión por fechas.

|Trabajos por lotes  |
|---------|
|Compresión por fechas Movimientos de presupuesto de productos |
|Comprimir fechas movs. banco |
|Comprimir fechas movs. cliente |
|A/F Comprimir fechas movs. |
|Comprimir fechas movs. cont. |
|Comprimir fechas movs. seguro |
|Comprimir fechas movs. mnto. |
|Comprimir fechas movs. mnto. |
|Comprimir fechas mov. recurso |
|Comprimir fechas movs. IVA |
|Comprimir fechas movs. prov. |
|Compr. por fechas movs. almacén Movimientos |
|Compresión por fechas Movs. pptos. contabilidad |

Para comenzar a archivar datos cuando ejecuta uno de los trabajos por lotes, active el botón de alternancia **Archivar movs. borrados**.

## <a name="storage-considerations"></a>Consideraciones sobre el almacenamiento
Los datos archivados se almacenan en la tabla **Medios de suscriptor**. Esta tabla no se incluye cuando se calcula el tamaño de la base de datos, de acuerdo con los términos de su licencia. En cambio, cuenta como almacenamiento de archivos. Sin embargo, le recomendamos que exporte archivos antiguos a, por ejemplo, un archivo CSV y luego elimine los registros del archivo antiguo.

## <a name="see-also"></a>Consulte también
[Administrar almacenamiento eliminando documentos o comprimiendo datos](admin-manage-documents.md)
