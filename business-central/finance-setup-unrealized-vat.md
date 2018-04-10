---
title: "Configuración el impuesto sobre el valor añadido no realizado | Documentos de Microsoft"
description: "Si utiliza contabilidad basada en efectivo, puede especificar cómo gestionar el IVA no realizado para venta y compras."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5e21330cd7adc97da9023da7b18944a9f0450b8e
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Configurar el IVA no realizado para la contabilidad basada en efectivo
Si utiliza métodos de contabilidad basada en efectivo, puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] para gestionar el IVA no realizado.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Usar las cuentas de contabilidad para el IVA no realizado
Puede elegir que los importes de IVA se calculen y registren en una cuenta temporal al registrar una factura y que, a continuación, se registren en la cuenta correcta y se incluyan en las declaraciones de IVA cuando se registre el pago real de la factura. Antes de poder hacerlo, deberá configurar los grupos de registro de IVA.

Para utilizar cuentas para IVA no realizado, realice los pasos siguientes:
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe") e introduzca **Configuración contabilidad**.
2. En la página **Configuración de contabilidad**, en la ficha desplegable **General**, elija **Mostrar más** y, a continuación, elija la casilla de verificación **IVA no realizado**.
3. Cierre la página.
4. Seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") y especifique **Config. grupos registro IVA**.
5. En la página **Config. grupos registro IVA**, seleccione el grupo de registro de IVA y después seleccione **Editar**.
6. En el campo **Tipo IVA no realizado** elija una opción para especificar cómo se asignan los pagos al importe de la factura (excluyendo el IVA) y el importe del mismo IVA y cómo transferir los importes del IVA desde la cuenta del IVA no realizado a la cuenta de realizado. La siguiente tabla describe las opciones.

| Opción | Descripción |
| --- | --- |
| En blanco | Elija esta opción si no desea utilizar la característica de IVA no realizado. |
| Porcentaje | Los pagos liquidan tanto el IVA como el importe de factura proporcionalmente al porcentaje de pago del importe restante de la factura. El importe del IVA pagado se transfiere de la cuenta del IVA no realizado a la cuenta de IVA realizado. |
| Primero | Los pagos liquidan primero el IVA y después los importes de factura. En este caso, el importe transferido de la cuenta del IVA no realizado a la cuenta del IVA será equivalente al importe del pago hasta que se haya pagado el IVA total. |
| Último | Los pagos liquidan primero el importe de factura y después el IVA. En este caso, no se transferirá ningún importe de la cuenta del IVA no realizado a la cuenta del IVA hasta que se haya pagado el importe total de la factura, excluyendo el IVA. |
| Primero (pagado totalmente) | Los pagos liquidarán primero el impuesto (como en la opción _Primero_), pero el importe no se transferirá a la cuenta del IVA hasta que se haya pagado completamente el importe del IVA. |
| Último (pagado totalmente) | Los pagos liquidarán primero el importe de la factura (como en la opción _Último_), pero el importe no se transferirá a la cuenta del IVA hasta que se haya pagado completamente el importe del IVA. |

6. En el campo **Cta. IVA reper. no realizado**, elija la cuenta de IVA repercutido no realizado.

    > [!NOTE]  
>   El importe de IVA se registrará en esta cuenta y permanecerá hasta que se registre el pago del cliente. A continuación, el importe se transfiere a la cuenta para el IVA repercutido.
7. En el campo **Cta. IVA sopor. no realizado**, introduzca una cuenta de IVA soportado no realizado.

    > [!NOTE]  
    >   El importe de IVA se registrará en esta cuenta y permanecerá hasta que se registre el pago del cliente. A continuación, el importe se transfiere a la cuenta para el IVA soportado.

## <a name="see-also"></a>Consulte también
[Configuración del impuesto sobre el valor añadido](finance-setup-vat.md)

