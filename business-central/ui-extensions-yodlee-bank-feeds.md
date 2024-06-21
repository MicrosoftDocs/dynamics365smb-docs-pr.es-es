---
title: Conciliación de pagos con la extensión Envestnet Yodlee Bank Feeds
description: 'Describe la extensión Envestnet Yodlee Bank Feeds, que se vincula a las cuentas bancarias para que pueda conciliar pagos rápidamente.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, stream, bank account link'
ms.search.form: '1450, 1451, 1452, 1453, 1454, 1458, 1460,'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Extensión Envestnet Yodlee Bank Feeds

Para conciliar pagos realizados en sus bancos rápidamente, el servicio Envestnet Yodlee Bank Feeds permite vincular su cuenta bancaria del sistema a su cuenta bancaria en línea. Esto significa que el último extracto bancario se introduce manual o automáticamente en el diario de conciliación de pagos, lo que garantiza que siempre procesará sus últimos pagos con el mínimo de errores.

El servicio Envestnet Yodlee Bank Feeds solo se admite en Estados Unidos y Canadá.

> [!NOTE]
> El servicio Envestnet Yodlee Bank Feeds solo se admite en la versión en línea de Business Central. Para utilizar esta funcionalidad local, debe obtener una cuenta de cobrand de Envestnet Yodlee.<br /><br />
> El servicio Envestnet Yodlee Bank Feeds solo se admite en Estados Unidos y Canadá.
> Solo se admiten los bancos que residan en estos países o regiones, aunque los bancos de otros países o regiones puedan aparecer en la ventana de selección de banco de Envestnet Yodlee Bank Feeds en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> Debido a la nueva directiva sobre servicios de pago en Europa (PSD2), después del 14 de septiembre de 2019 ya no podrá importar automáticamente extractos de cuenta de bancos del Reino Unido a [!INCLUDE[prod_short](includes/prod_short.md)]. Estamos analizando la posibilidad de ofrecer esta función nuevamente en el futuro.

El servicio Envestnet Yodlee Bank Feeds proporciona las siguientes ventajas:

* Elimina la necesidad de la entrada manual.
* Actualiza la eficacia y la precisión al realizar la conciliación de pagos.
* Admite un gran número de bancos.
* Permite información actualizada sobre transacciones bancarias en [!INCLUDE[prod_short](includes/prod_short.md)].
* Admite fuentes de banco manuales o automáticas.
* Habilita la externalización de la conciliación de pagos a un contable proporcionando acceso a los extractos bancarios.

## Fuentes de banco disponibles

Puede comprobar si un banco es compatible configurando y conectándose al servicio Envestnet Yodlee Bank Feeds. El banco aparecerá en la lista si es compatible con Envestnet Yodlee.

Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

## Consulte también .

[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Liquidación de pagos automáticamente y conciliación de bancos](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
