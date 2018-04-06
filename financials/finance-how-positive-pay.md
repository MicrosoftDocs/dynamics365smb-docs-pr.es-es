---
title: Exportar archivos de Positive Pay | Documentos de Microsoft
description: "Puede asegurarse de que su banco solo compensa cheques e importes validados mediante la exportación un archivo de Positive Pay que contenga la información de proveedor y pago."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57580354c2ea5b63162e1539cf2f97eb9770c50b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="export-a-positive-pay-file"></a>Exportar un archivo de Positive Pay
Para asegurarse de que su banco solo compense los cheques e importes validados, puede exportar un archivo de Positive Pay que contenga la información de proveedor, el número de cheque y el importe de pago, que puede enviar al banco como referencia cuando se procesen pagos.

[!INCLUDE[d365fin](includes/d365fin_md.md)] se ha preconfigurado para admitir archivos de Positive Pay para Bank of America y City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Para configurar una cuenta bancaria para Positive Pay
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Abra la ficha del banco para el que desea usar Positive Pay.
3. En el campo **Código de exportación de Positive Pay**, introduzca POSPAYBANK.
4. Cierre la ventana.

## <a name="to-export-a-positive-pay-file"></a>Para exportar un archivo de Positive Pay
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el banco del que desea exportar un archivo de Positive Pay.
3. Elija la acción **Exportación de Positive Pay**.

    Se abre la ventana **Exportación de Positive Pay** en la que se presentan los pagos que se han creado para el banco desde la última carga, tal como se muestra en los campos **Fecha de última carga** y **Hora de última carga**.
4. En el campo **Fecha límite de carga**, especifique una fecha de referencia para no incluir pagos anteriores a dicha fecha en el archivo exportado.
5. Seleccione la acción **Exportar**.
6. En la ventana **Exportar archivo**, seleccione el botón **Guardar** y, a continuación, guarde el archivo en una ubicación adecuada.
7. Cargue el archivo en el sitio del banco electrónico.
8. Anote o copie el número de confirmación que se muestra al cargar el archivo correctamente.

Para ver registros de Positive Pay exportados

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el banco del que desea ver los registros de exportación de Positive Pay.
3. Elija la acción **Movimientos de Positive Pay**.

    En la ventana **Movimientos de Positive Pay**, puede ver todos los registros de exportación de Positive Pay del banco.
4. En el campo **Número de confirmación**, escriba, por cada registro de salida, el número de confirmación que ha recibido cuando la carga del archivo en el banco es correcta.
5. Para ver las líneas de pago relacionadas, elija la acción **Detalles de movimiento de Positive Pay**.

Para reexportar archivos de Positive Pay

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el banco del que desea reexportar los archivos de Positive Pay.
3. Elija la acción **Movimientos de Positive Pay**.
4. Seleccione la línea del archivo de exportación de Positive Pay que desea reexportar.
5. En la ventana **Movimientos de Positive Pay**, elija la acción **Reexportar Positive Pay a archivo**.

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

