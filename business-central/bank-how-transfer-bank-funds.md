---
title: Transferir fondos bancarios
description: 'Puede transferir importes de una cuenta bancaria a otra, con divisas distintas, registrando la transacción en el diario general.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 04/29/2021
ms.author: bholtorf
---
# <a name="transfer-bank-funds"></a>Transferir fondos bancarios

En ocasiones es necesario transferir un importe desde un banco en [!INCLUDE[prod_short](includes/prod_short.md)] a otro. Para hacerlo, debe registrar la transacción en la página **Diario general**. La tarea varía en función de si los bancos usan la misma divisa o distintas divisas.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Para registrar transferencias entre bancos con el mismo código de divisa

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario general**, y luego elija el enlace relacionado.
2. En una línea de diario, rellene los campos **Fecha registro** y **Nº documento**.
3. En el campo **Tipo mov**, seleccione **Banco**.
4. En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.
5. En el campo **Importe**, introduzca el importe que quiere transferir.

    A continuación, debe especificar la cuenta de contrapartida. Si no puede ver los campos relevantes, elija la acción **Mostrar más columnas** para ver todos los campos disponibles.
6. En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.
7. En el campo **Cta. contrapartida**, seleccione la cuenta a la que quiere transferir los fondos.
8. Registre el diario.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Para registrar transferencias entre bancos con códigos de divisa distintos

Para transferir fondos entre cuentas bancarias que usan distintas divisas, debe registrar dos líneas de diario general.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario general**, y luego elija el enlace relacionado.
2. Cree dos líneas de diario y rellene los campos **Fecha de registro** y **N.º de documento**.
3. En la primera línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.
4. En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.
5. En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria, con o sin signo menos.

    > [!TIP]
    > Una cantidad sin signo es un débito y una cantidad con signo menos es un crédito.

    > [!NOTE]
    > Algunas empresas prefieren realizar transferencias entre cuentas en líneas de diario separadas. Otras empresas prefieren publicar todo en una línea de diario utilizando una cuenta de contrapartida. Consulte con su experto local si no está seguro de qué hacer.
    >
    > Si su empresa prefiere utilizar una cuenta de contrapartida, establezca el campo **Tipo de cuenta de contrapartida** en **Banco** y establezca el **N.º de cuenta de contrapartida** en el banco al que desea transferir los fondos. Luego continúe con el paso 9 o 10.
    >
    > Si su empresa prefiere utilizar una línea de diario separada, continúe con el siguiente paso.
6. En la segunda línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.
7. En el campo **N.º cuenta**, seleccione la cuenta a la que quiere transferir los fondos.
8. En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria, con o sin signo menos.

    > [!TIP]
    > Una cantidad sin signo es un débito y una cantidad con signo menos es un crédito.
9. Si los tipos de cambio usados en el diario son diferentes a los contenidos en la página **Tipos de cambio de divisa**, introduzca una nueva línea del diario para el beneficio o la pérdida del tipo de cambio.  

    1. Especifique **Cuenta** en el campo **Tipo mov**.  

    2. Especifique el número de cuenta para la pérdida o ganancia de tipo de campo en el campo **Nº cuenta**.  

    3. Introduzca el beneficio o la pérdida del tipo de cambio en el campo **Importe**, con o sin signo menos.

    > [!TIP]
    > Una cantidad sin signo es un débito y una cantidad con signo menos es un crédito.
10. Registre el diario.

## <a name="see-also"></a>Consulte también

[Conciliar bancos](bank-manage-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
