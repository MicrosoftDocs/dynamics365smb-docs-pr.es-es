---
title: Configurar cuentas bancarias | Documentos de Microsoft
description: Puede conciliar cuentas bancarias con los extractos del banco.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: bcb782b707d4a84ebde9fa24e3c9b448af3dbddb
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-bank-accounts"></a>Configurar bancos
Las cuentas bancarias se utilizan en [!INCLUDE[d365fin](includes/d365fin_md.md)] para hacer un seguimiento de las transacciones bancarias. Los bancos pueden expresarse en la divisa local (DL) o en una extranjera. Cuando haya configurado todos los bancos, puede utilizar también la opción de impresión de cheques.

## <a name="to-set-up-bank-accounts"></a>Para configurar bancos
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Cuentas bancarias** y luego elija el enlace relacionado.
2. En la ventana **Cuentas bancarias**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Para completar el campo **Saldo** con un saldo inicial, debe publicar un movimiento de cuenta bancaria con el importe en cuestión. Puede hacerlo si realiza una conciliación de bancos. Para obtener más información, vea [Conciliar cuentas bancarias por separado](bank-how-reconcile-bank-accounts-separately.md). De forma alternativa, puede implementar el saldo inicial como parte de la creación de datos generales en nuevas compañías mediante la configuración asistida **Migrar datos empresariales**. Para obtener más información, vea [Introducción](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Para configurar la cuenta para la importación o exportación de archivos bancarios
Los campos de la ficha desplegable **Transferencia** en la ventana **Ficha banco** están relacionados con la importación y exportación de archivos o fuentes de banco. Para obtener más información, vea [Configurar el servicio de las fuentes de banco de Envestnet Yodlee](bank-how-setup-bank-data-conversion-service.md) y [Configurar el servicio de conversión de datos bancarios](bank-how-setup-bank-statement-service.md).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Cuentas bancarias** y luego elija el enlace relacionado.
2. Abra la ficha de un banco del que exportará archivos de banco, o al que los importará.
3. En la ficha desplegable **Transferencia**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Distintos servicios de exportación de archivos y sus formatos requieren valores de configuración diferentes en la ventana **Ficha banco**. Estará informado sobre valores de configuración incorrectos o que faltan al intentar exportar el archivo. Leer las descripciones breves de los campos atentamente o consulte los temas relacionados del procedimiento. Por ejemplo, exportar un archivo de pago para la transferencia electrónica de fondos (EFT) de Norteamérica requiere que tanto el campo **Nº último aviso pago** como el campo **Nº tránsito** estén rellenados. Para obtener más información, vea [Exportar pagos a un archivo bancario](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Para configurar cuentas bancarias de proveedor para exportar archivos bancarios
Los campos de la ficha desplegable **Transferencia** en la ventana **Ficha banco proveedor** están relacionados con la exportación de archivos o fuentes de banco. Para obtener más información, vea [Configurar el servicio de conversión de datos bancarios](bank-how-setup-bank-data-conversion-service.md) y [Exportar pagos a un archivo bancario](payables-how-export-payments-bank-file.md).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de un proveedor a cuya cuenta bancaria exportará los archivos bancarios de pagos.
3. Elija la acción **Cuentas bancarias**.
3. En la ficha desplegable **Ficha banco proveedor** de la ventana **Transferencia**, complete los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Consulte también
[Configurar banca](bank-setup-banking.md)  
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

