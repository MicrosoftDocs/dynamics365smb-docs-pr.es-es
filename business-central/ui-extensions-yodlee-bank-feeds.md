---
title: Conciliación de pagos con la extensión Envestnet Yodlee Bank Feeds | Documentos de Microsoft
description: Describe la extensión Envestnet Yodlee Bank Feeds, que se vincula a las cuentas bancarias para que pueda conciliar pagos rápidamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6089a51a0ef27175988ed0c00fdb353cd3c7e96c
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692949"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Extensión Envestnet Yodlee Bank Feeds
Para conciliar pagos realizados en sus bancos rápidamente, el servicio Envestnet Yodlee Bank Feeds permite vincular su cuenta bancaria del sistema a su cuenta bancaria en línea. Esto significa que el último extracto bancario se introduce manual o automáticamente en el diario de conciliación de pagos, lo que garantiza que siempre procesará sus últimos pagos con el mínimo de errores.

El servicio Envestnet Yodlee Bank Feeds solo se admite en Estados Unidos y Canadá.

> [!NOTE]
> El servicio Envestnet Yodlee Bank Feeds solo se admite en la versión en línea de Business Central. Para utilizar esta funcionalidad local, debe obtener una cuenta de cobrand de Envestnet Yodlee.<br /><br />
> El servicio Envestnet Yodlee Bank Feeds solo se admite en Estados Unidos y Canadá.
> Solo se admiten los bancos que residan en estos países, aunque los bancos de otros países puedan aparecer en la ventana de selección de banco de Envestnet Yodlee Bank Feeds en [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!IMPORTANT]
> Debido a la nueva directiva sobre servicios de pago en Europa (PSD2), después del 14 de septiembre de 2019 ya no podrá importar automáticamente extractos de cuenta de bancos del Reino Unido a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estamos analizando la posibilidad de ofrecer esta función nuevamente en el futuro.

El servicio Envestnet Yodlee Bank Feeds proporciona las siguientes ventajas:

* Elimina la necesidad de la entrada manual.
* Actualiza la eficacia y la precisión al realizar la conciliación de pagos.
* Admite un gran número de bancos.
* Permite información actualizada sobre transacciones bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Admite fuentes de banco manuales o automáticas.
* Habilita la externalización de la conciliación de pagos a un contable proporcionando acceso a los extractos bancarios.

Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Consulte también
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)    
[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
