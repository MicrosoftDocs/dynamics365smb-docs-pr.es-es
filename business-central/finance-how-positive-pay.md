---
title: Exportar archivos de Positive Pay
description: Puede asegurarse de que su banco solo compensa cheques e importes validados mediante la exportación un archivo de Positive Pay que contenga la información de proveedor y pago.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'check, clearing'
ms.search.form: '1231, 1232, 1233, 1234'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="export-a-positive-pay-file"></a>Exportar un archivo de Positive Pay
Para asegurarse de que su banco solo compense los cheques e importes validados, puede exportar un archivo de Positive Pay que contenga la información de proveedor, el número de cheque y el importe de pago, que puede enviar al banco como referencia cuando se procesen pagos.

[!INCLUDE[prod_short](includes/prod_short.md)] se ha preconfigurado para admitir archivos de Positive Pay para Bank of America y City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Para configurar una cuenta bancaria para Positive Pay
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.
2. Abra la ficha del banco para el que desea usar Positive Pay.
3. En el campo **Código de exportación de Positive Pay**, introduzca POSPAYBANK.
4. Cierre la página.

## <a name="to-export-a-positive-pay-file"></a>Para exportar un archivo de Positive Pay
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.
2. Seleccione el banco del que desea exportar un archivo de Positive Pay.
3. Elija la acción **Exportación de Positive Pay**.

    Se abre la página **Exportación de Positive Pay** en la que se presentan los pagos que se han creado para el banco desde la última carga, tal como se muestra en los campos **Fecha de última carga** y **Hora de última carga**.
4. En el campo **Fecha límite de carga**, especifique una fecha de referencia para no incluir pagos anteriores a dicha fecha en el archivo exportado.
5. Seleccione la acción **Exportar**.
6. En la página **Exportar archivo**, seleccione el botón **Guardar** y, a continuación, guarde el archivo en una ubicación adecuada.
7. Cargue el archivo en el sitio del banco electrónico.
8. Anote o copie el número de confirmación que se muestra al cargar el archivo correctamente.

Para ver registros de Positive Pay exportados

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.
2. Seleccione el banco del que desea ver los registros de exportación de Positive Pay.
3. Elija la acción **Movimientos de Positive Pay**.

    En la página **Movimientos de Positive Pay**, puede ver todos los registros de exportación de Positive Pay del banco.
4. En el campo **Número de confirmación**, escriba, por cada registro de salida, el número de confirmación que ha recibido cuando la carga del archivo en el banco es correcta.
5. Para ver las líneas de pago relacionadas, elija la acción **Detalles de movimiento de Positive Pay**.

Para reexportar archivos de Positive Pay

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.
2. Seleccione el banco del que desea reexportar los archivos de Positive Pay.
3. Elija la acción **Movimientos de Positive Pay**.
4. Seleccione la línea del archivo de exportación de Positive Pay que desea reexportar.
5. En la página **Movimientos de Positive Pay**, elija la acción **Reexportar Positive Pay a archivo**.

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
