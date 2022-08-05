---
title: Configurar la cuenta bancaria del proveedor
description: Aprenda a asociar cuentas bancarias a tarjetas de proveedores en Business Central, incluida la información de contacto, SWIFT y códigos IBAN.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 07/04/2022
ms.author: a-reishima
ms.openlocfilehash: 1839f54de2382ad5b7d8b6b936181e105a56e06b
ms.sourcegitcommit: 5560a49ca4ce85fa12e50ed9e14de6d5cba5f5c3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2022
ms.locfileid: "9144412"
---
# <a name="set-up-vendor-bank-accounts"></a>Configurar cuentas bancarias de proveedor

Así como puede usar la información de la cuenta bancaria en [!INCLUDE [prod_short](includes/prod_short.md)] para realizar un seguimiento de las transacciones bancarias de su empresa, también puede establecer los detalles bancarios de los proveedores. Los datos de la cuenta bancaria del proveedor pueden simplificar los pagos a los proveedores cuando se combinan con la [extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) o la característica [Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md), por ejemplo.

## <a name="add-or-edit-a-vendor-bank-account"></a>Agregar o editar una cuenta bancaria de proveedor

[!INCLUDE [purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

> [!TIP]
> Puede establecer cuentas bancarias de proveedores adicionales en la página **Lista de cuentas bancarias de proveedores**.

## <a name="set-up-a-preferred-vendor-bank-account"></a>Configurar la cuenta de banco preferida del proveedor

Si un proveedor tiene una o más cuentas bancarias y desea establecer una opción preferida para las líneas del diario de pago, siga estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.
2. Abre la ficha del proveedor.
3. En la ficha desplegable **Pagos**, elija la cuenta bancaria del proveedor predeterminado en el campo **Código de cuenta bancaria preferida**.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también .

[Configurar compras](purchasing-setup-purchasing.md)  
[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md)  
[Configurar cuentas bancarias](bank-how-setup-bank-accounts.md)  
[Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
