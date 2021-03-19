---
title: Extensión de migración de QuickBooks | Microsoft Docs
description: Describe cómo utilizar la extensión para importar clientes, proveedores, elementos y cuentas de QuickBooks Desktop a Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 990aabaaccbf32a5cbd95c09527657757e5182cb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391429"
---
# <a name="the-quickbooks-data-migration-extension"></a>Extensión de la migración de datos de QuickBooks

Esta extensión facilita la migración de clientes, proveedores, productos y cuentas de QuickBooks a [!INCLUDE[prod_short](includes/prod_short.md)]. Si la empresa usa QuickBooks actualmente, puede exportar la información correspondiente y después abrir una guía de instalación asistida para cargar los datos en [!INCLUDE[prod_short](includes/prod_short.md)].  
Para obtener más información, vea [Importar datos empresariales desde otros sistemas financieros](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Datos de QuickBooks Desktop

Puede importar los datos siguientes desde QuickBooks Online a Business Central:

- Clientes  
- Proveedores  
- Productos  
- Plan de cuentas  
- Comienzo de la transacción de saldo en el libro mayor  
- Cantidad disponible de productos de inventario  
- Documentos pendientes para clientes y proveedores, como facturas, abonos y pagos  

Migramos únicamente los importes totales de los documentos de ventas y compras. No actualizamos importes pagados parcialmente. Por ejemplo, si un cliente ha pagado 300 de un total de 500 dólares en una factura de venta, migramos la cantidad total de 500. Si ha recibido pagos parciales, debe actualizarlos manualmente, antes o después de migrar los datos. Le recomendamos que aplique las transacciones pendientes antes de migrar, simplemente para facilitar las cosas.

> [!NOTE]
> No migramos pedidos de compra o venta.

## <a name="before-you-start"></a>Antes de comenzar

Una parte importante del proceso de migración es especificar las cuentas a las que se deben migrar las transacciones. Conviene planificar esta asignación antes de migrar los datos. Por ejemplo, las cuentas en la que registre transacciones de:

- La venta de productos o servicios a los clientes  
- La compra de productos o servicios a proveedores  
- Ajustes en el libro mayor  

Business Central requiere que las cuentas del libro mayor tengan números de cuenta asignados. Asegúrese de que los números de cuenta están asignados a las cuentas de QuickBooks.
Si las transacciones en QuickBooks tienen impuestos, debe configurar una cuenta de impuestos para sus jurisdicciones fiscales en Business Central antes de poder registrar las transacciones.

Para extraer sus datos de la aplicación QuickBooks Desktop necesitará descargar la herramienta Microsoft Data Exporter Tool.  Las instrucciones de la herramienta se encuentran en el Asistente para la migración de los datos de [!INCLUDE[prod_short](includes/prod_short.md)]. La herramienta se conectará a su aplicación QuickBooks y exportará los datos correspondientes a un archivo .zip.  

> [!NOTE]
> La herramienta de exportador de datos actualmente solo funciona en QuickBooks 2017 y 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Buscar la extensión de la migración de datos de QuickBooks

La extensión de la migración de datos de QuickBooks está instalada y lista como parte integrada de la guía de configuración asistida de la migración de datos. Si está preparado para empezar ahora y ha exportado sus datos de QuickBooks, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración asistida** y, a continuación, haga clic el vínculo relacionado. Seleccione **Migrar los datos empresariales** y, a continuación, siga los pasos en la guía.  

## <a name="what-do-i-do-after-i-migrate-data"></a>¿Qué hago después de la migración de datos?

Una vez haya migrado los datos, las transacciones muestran el estado No registrado, para que pueda revisarlas y crear ajustes. Para revisar las transacciones, vaya a la página donde están normalmente. Por ejemplo, para revisar facturas de ventas no registradas, vaya a la página Facturas de ventas. Para revisar las diario de pagos, vaya a la página Diario de pagos.
Hay algunas acciones concretas que debe realizar: si las transacciones de QuickBooks tenían importes de descuento o bonificación, debe agregar manualmente los importes a las transacciones relacionadas en Business Central antes de registrarlas.
Si está utilizando el impuesto sobre el valor añadido (IVA), es posible que tenga que agregar un grupo de contable de negocio y un grupo contable de productos a la configuración de grupos contables para poder contabilizar importes de IVA.
Verifique los saldos iniciales de las cuentas en el libro mayor. QuickBooks no almacena el saldo actual de todas las cuentas, por lo que es posible que tenga que corregir los saldos iniciales.

## <a name="see-also"></a>Consulte también

[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]