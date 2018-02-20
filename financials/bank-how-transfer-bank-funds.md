---
title: Transferir fondos bancarios | Documentos de Microsoft
description: "Puede transferir importes de una cuenta bancaria a otra, con divisas distintas, registrando la transacción en el diario general."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d3bd448ef67f742794e3a162bd828e38366775bb
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="transfer-bank-funds"></a>Transferir fondos bancarios
En ocasiones es necesario transferir un importe desde una cuenta bancaria a otra. Para hacerlo, debe registrar una transacción en el diario general. La tarea varía en función de si los bancos usan la misma divisa o distintas divisas.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Para registrar transferencias entre bancos con el mismo código de divisa
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario general** y, a continuación, seleccione el vínculo relacionado.
2. En una línea de diario, rellene los campos **Fecha registro** y **Nº documento**.
3. En el campo **Tipo mov**, seleccione **Banco**.
4. En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.
5. En el campo **Importe**, introduzca el importe que quiere transferir.
6. En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.
7. En el campo **Cta. contrapartida**, seleccione la cuenta a la que quiere transferir los fondos.
8. Registre el diario.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Para registrar transferencias entre bancos con códigos de divisa distintos
Para transferir fondos entre cuentas bancarias que usan distintas divisas, debe registrar dos líneas de diario general.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario general** y, a continuación, seleccione el vínculo relacionado.
2. Cree dos líneas de diario y rellene los campos **Fecha de registro** y **N.º de documento**.
3. En la primera línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.
4. En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.
5. En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria. Escriba los importes de crédito con un signo menos. Escriba los importes de débito sin el signo menos.
6. En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.
7. En el campo **Cta. contrapartida**, seleccione la cuenta a la que quiere transferir los fondos.
8. En la segunda línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.
9. En el campo **N.º cuenta**, seleccione la cuenta a la que quiere transferir los fondos.
10. En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria. Escriba los importes de crédito con un signo menos. Escriba los importes de débito sin el signo menos.
11. En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.  
12. En el campo **Cta. contrapartida**, seleccione la cuenta desde la que quiere transferir los fondos.

    > [!NOTE]  
>   Si los tipos de cambio usados en el diario son diferentes a los contenidos en la ventana **Tipos de cambio de divisa**, introduzca una tercera línea para las diferencias positivas o negativas del cambio. Especifique **Cuenta** en el campo **Tipo mov**. Especifique el número de cuenta para la pérdida o ganancia de tipo de campo en el campo **Nº cuenta**. Introduzca la diferencia positiva o negativa del tipo de cambio en el campo **Importe** con o sin el signo menos para los créditos y los débitos respectivamente.
13. Registre el diario.

## <a name="see-also"></a>Consulte también
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

