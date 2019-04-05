---
title: Migrar datos de Dynamics GP con la extensión de la migración de datos | Documentos de Microsoft
description: Utilice la extensión de migración de datos de Dynamics GP para migrar clientes, proveedores, productos de inventario, cuentas de contabilidad y transacciones de pagos y cobros pendientes desde Dynamics GP a Business Central.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 1441e15785b159f7a8c13ee59c8ebea4c32512dc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805673"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Extensión de la migración de datos de Dynamics GP 
Esta extensión facilita migrar clientes, proveedores, productos de inventario, cuentas de contabilidad y transacciones de pagos y cobros pendientes desde Dynamics GP a [!INCLUDE[prodshort](includes/prodshort.md)]. Si la empresa usa Dynamics GP actualmente, puede exportar los registros correspondientes y después abrir una guía de instalación asistida para agregar los datos a [!INCLUDE[prodshort](includes/prodshort.md)]. La extensión de migración funciona para todas las versiones compatibles de Microsoft Dynamics GP. Para obtener más información, vea [Importar datos empresariales desde otros sistemas financieros](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportar datos desde Dynamics GP
Deberá haber exportado todos los clientes, proveedores, productos de inventario y cuentas de contabilidad existentes, o parte de ellos, mediante la funcionalidad de exportación de datos de Dynamics GP. Al seleccionar los datos para exportar se pueden seleccionar los siguientes tipos:

* Cuenta  
* Cliente  
* Artículo  
* Proveedor  

Cuando se cree el archivo de exportación, tendrá un archivo zip con varios archivos de texto que serán determinados por lo que seleccionó durante el proceso de exportación de datos.  También se generarán archivos txt adicionales que contendrán la información de asistencia necesaria para la configuración dentro de su nueva empresa en [!INCLUDE[prodshort](includes/prodshort.md)].

La extensión de la migración de datos de Dynamics GP asigna automáticamente los datos exportados para que estén a su disposición rápidamente en la nueva empresa de [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="whats-new-in-the-october-2018-release"></a>Novedades en la versión de octubre de 2018

En esta versión, hemos ampliado la cantidad de datos que traemos a [!INCLUDE[prodshort](includes/prodshort.md)] desde Dynamics GP.

En el asistente de migración, ahora puede elegir cómo desea migrar el plan de cuentas de Dynamics GP. Puede migrar el plan de cuentas existente, o puede crear uno nuevo basado en el existente.  

Si elige usar el plan de cuentas existente, las cuentas se configurarán como el segmento de cuenta principal de Dynamics GP y los segmentos adicionales se configurarán como dimensiones dentro de [!INCLUDE[prodshort](includes/prodshort.md)].  

Si elige crear un nuevo plan de cuentas, obtendrá una página de información de cuenta adicional en el asistente para que pueda descargar el libro de trabajo, realizar los cambios pertinentes y luego importarlo de nuevo para cambiar sus cuentas.  

Tendrá que descargar el libro de Excel y asignar un nuevo número de cuenta a cada número de cuenta de la hoja de cálculo de Excel. Es necesario que cada cuenta tenga su propio número, o la migración generará un error. Cuando haya completado la asignación, puede continuar con el asistente de migración e importar el libro de Excel que acaba de actualizar. El asistente validará que cada fila tenga un número de cuenta único y que ninguna fila tenga un número de cuenta nuevo vacío.  

Con el cambio a la asignación del gráfico de opciones de cuenta, también notará un cambio en el tipo de datos que aparecen en el diario general para los números de cuenta.  

- Si elige utilizar los números de cuenta existentes, se incluirá el saldo inicial del segmento principal (nuevo número de cuenta) como un resumen del número de cuenta principal en el momento de la migración.  
- Si elige crear nuevos números de cuenta, traeremos información resumida por el equivalente de dos ejercicios en función de los períodos fiscales que haya configurado en Dynamics GP.

En versiones anteriores de [!INCLUDE[prodshort](includes/prodshort.md)], el asistente migraba una transacción de resumen para el saldo de cliente/proveedor en Dynamics GP. Ahora traemos las transacciones abiertas detalladas para clientes y proveedores en el momento de la migración. ¿Qué significa esto? Si su cliente tiene 3 transacciones pendientes registradas en el módulo de Cobros pendientes, el asistente las importa a [!INCLUDE[prodshort](includes/prodshort.md)] con el importe pendiente como importe del documento. Lo mismo ocurre con el módulo de Pagos pendientes para los proveedores.  

Los artículos de inventario se importan con el método de evaluación de costes que se seleccionó cuando se ejecutó el asistente de configuración de la compañía. A los artículos de servicio se les asigna automáticamente el método de evaluación FIFO. Actualmente traemos la cantidad disponible para los artículos en el momento de la migración.  Esta cantidad se lleva a la ubicación en blanco.  

La última opción que ve en el asistente de migración de datos para Dynamics GP es la capacidad de especificar su opción de publicación. Este valor especifica si desea publicar automáticamente todas las transacciones en los diarios generales tan pronto como la migración traslade los datos a [!INCLUDE[prodshort](includes/prodshort.md)] o si desea publicarlas manualmente para que todas las transacciones se agrupen dentro de la página del diario general para que pueda verificar la información antes de publicarla. Esta opción es visible en la página de opciones del plan de cuentas.


## <a name="see-also"></a>Consulte también
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Personalizar [!INCLUDE[prodshort](includes/prodshort.md)] con extensiones](ui-extensions.md)  
