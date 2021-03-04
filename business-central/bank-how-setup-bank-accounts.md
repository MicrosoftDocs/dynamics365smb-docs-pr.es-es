---
title: Configurar cuentas bancarias | Documentos de Microsoft
description: Puede conciliar cuentas bancarias con los extractos del banco.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1684f12858a33234f51d7847b50ea15aa1d7b230
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755297"
---
# <a name="set-up-bank-accounts"></a>Configurar bancos
Las cuentas bancarias se utilizan en [!INCLUDE[prod_short](includes/prod_short.md)] para hacer un seguimiento de las transacciones bancarias. Los bancos pueden expresarse en la divisa local (DL) o en una extranjera. Cuando haya configurado todos los bancos, puede utilizar también la opción de impresión de cheques.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

## <a name="to-set-up-bank-accounts"></a>Para configurar bancos
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.
2. En la página **Cuentas bancarias**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Para completar el campo **Saldo** con un saldo inicial, debe publicar un movimiento de cuenta bancaria con el importe en cuestión. Puede hacerlo si realiza una conciliación de bancos. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md). De forma alternativa, puede implementar el saldo inicial como parte de la creación de datos generales en nuevas compañías mediante la guía de configuración asistida **Migrar datos empresariales**. Para obtener más información, vea [Introducción](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Para configurar la cuenta para la importación o exportación de archivos bancarios
Los campos de la ficha desplegable **Transferencia** en la página **Ficha banco** están relacionados con la importación y exportación de archivos o fuentes de banco. Para obtener más información, vea [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) y [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.
2. Abra la ficha de un banco del que exportará archivos de banco, o al que los importará.
3. En la ficha desplegable **Transferencia**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Distintos servicios de exportación de archivos y sus formatos requieren valores de configuración diferentes en la página **Ficha banco**. Estará informado sobre valores de configuración incorrectos o que faltan al intentar exportar el archivo. Leer las descripciones breves de los campos atentamente o consulte los temas relacionados del procedimiento. Por ejemplo, exportar un archivo de pago para la transferencia electrónica de fondos (EFT) de Norteamérica requiere que tanto el campo **Nº último aviso pago** como el campo **Nº tránsito** estén rellenados. Para obtener más información, vea [Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Para configurar cuentas bancarias de proveedor para exportar archivos bancarios

Los campos de la ficha desplegable **Transferencia** en la página **Ficha banco proveedor** están relacionados con la exportación de archivos o fuentes de banco. Para obtener más información, vea [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) y [Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de un proveedor a cuya cuenta bancaria exportará los archivos bancarios de pagos.
3. Elija la acción **Cuentas bancarias**.
4. Desde la **Lista de cuentas bancarias de proveedores**, elija la cuenta bancaria relevante o agregue una nueva cuenta bancaria.  
5. En la página **Ficha banco proveedor** de la ventana **Transferencia**, complete los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Consulte también

[Configurar banca](bank-setup-banking.md)  
[Configurar los grupos contables](finance-posting-groups.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]