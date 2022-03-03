---
title: Extensión de migración de datos de QuickBooks Online
description: Describe cómo utilizar la extensión para migrar clientes, proveedores, elementos y cuentas de QuickBooks Online a Business Central.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 06/24/2021
ms.author: bholtorf
ms.openlocfilehash: 235c3050eac4dac983f486f66fe9e837e9594c57
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146051"
---
# <a name="the-quickbooks-online-data-migration-extension"></a>Extensión de migración de datos de QuickBooks Online

Esta extensión se incluye en la guía de configuración asistida **Migración de datos** para ayudarle a migrar datos comerciales importantes de QuickBooks Online a [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, esto es útil cuando su negocio está creciendo y ha decidido actualizar su aplicación de administración de negocios con [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-data-can-i-import-from-quickbooks-online"></a>¿Qué datos puedo importar desde QuickBooks Online?

Puede importar los datos siguientes de QuickBooks Online a [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Clientes
* Proveedores
* Productos
* Plan de cuentas
* Comienzo de la transacción de saldo en el libro mayor
* Cantidad disponible de productos de inventario
* Documentos pendientes para clientes y proveedores, como facturas, abonos y pagos

Migramos únicamente los importes totales de los documentos de ventas y compras. No actualizamos importes pagados parcialmente. Por ejemplo, si un cliente ha pagado 300 de un total de 500 dólares en una factura de venta, migramos la cantidad total de 500. Si ha recibido pagos parciales, debe actualizarlos manualmente, antes o después de migrar los datos. Le recomendamos que aplique las transacciones pendientes antes de migrar, simplemente para facilitar las cosas.

> [!NOTE]  
> No migramos pedidos de compra o venta.

## <a name="before-you-start"></a>Antes de comenzar

Una parte importante del proceso de migración es especificar las cuentas a las que se deben migrar las transacciones. Conviene planificar esta asignación antes de migrar los datos. Por ejemplo, las cuentas en la que registre transacciones de:  

* La venta de productos o servicios a los clientes.
* La compra de productos o servicios a proveedores.  
* Ajustes en el libro mayor.  

[!INCLUDE[prod_short](includes/prod_short.md)] requiere que las cuentas del libro mayor tengan números de cuenta asignados. Asegúrese de que los números de cuenta están asignados a las cuentas de QuickBooks Online.

Si las transacciones en QuickBooks Online tienen impuestos, debe configurar una cuenta de impuestos para sus jurisdicciones fiscales en [!INCLUDE[prod_short](includes/prod_short.md)] antes de poder registrar las transacciones.

## <a name="how-do-i-start-using-the-extension"></a>¿Cómo empiezo a usar la extensión?

Empezar es muy fácil. Únicamente tiene que ejecutar la guía de configuración asistida **Migración de datos**. Instrucciones:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración asistida** y luego elija **Migrar datos empresariales**.
2. Siga las instrucciones en cada paso de la guía de configuración asistida.

## <a name="what-do-i-do-after-i-migrate-data"></a>¿Qué hago después de la migración de datos?

Una vez haya migrado los datos, las transacciones muestran el estado **No registrado**, para que pueda revisarlas y crear ajustes. Para revisar las transacciones, vaya a la página donde están normalmente. Por ejemplo, para revisar facturas de ventas no registradas, vaya a la página **Facturas de ventas**. Para revisar las diario de pagos, vaya a la página **Diario de pagos**.  

Hay algunos pasos que es recomendable que haga:

* Si las transacciones de QuickBooks Online tuvieran importes de descuento o de bonificación, deberá agregar manualmente los importes a las transacciones relacionadas en [!INCLUDE[prod_short](includes/prod_short.md)] antes de registrarlas.
* Si está utilizando el impuesto sobre el valor añadido (IVA), es posible que tenga que agregar un grupo de contable de negocio y un grupo contable de productos a la configuración de grupos contables para poder contabilizar importes de IVA.
* Verifique los saldos iniciales de las cuentas en el libro mayor. QuickBooks Online no almacena el saldo actual de todas las cuentas, por lo que es posible que tenga que corregir los saldos iniciales.

## <a name="see-also"></a>Consulte también

[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]