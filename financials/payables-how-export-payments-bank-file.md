---
title: "Exportar pagos de salida a un archivo de pagos electrónicos | Documentos de Microsoft"
description: "Para realizar pagos de proveedor, habilite un servicio de conversión de datos bancarios, exporte un archivo de banco y cargue el archivo en el banco electrónico para transferir los fondos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 3a1a2243c0da6c077cd12388cd38621a6d24b4fb
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="export-payments-to-a-bank-file"></a>Exportar pagos a un archivo bancario
Cuando esté listo para hacer los pagos a los proveedores, o reembolsos a sus empleados, en la ventana **Diario de pagos**, puede exportar un archivo con la información de pago en las líneas del diario. Después, puede cargar el archivo al banco electrónico para procesar las transferencias de dinero relacionadas.

En la versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)], ya está configurado y conectado un proveedor global de servicios de conversión de datos bancarios a cualquier formato de archivo que el banco requiera. En las versiones para Norteamérica, el mismo servicio se puede utilizar para enviar archivos de pagos como transferencia electrónica de fondos (EFT), al menos con un proceso ligeramente distinto. Vea el paso 6 de la sección "Para exportar pagos a un archivo bancario".    

> [!NOTE]  
>   Antes de exportar los archivos de pagos del diario de pagos, debe especificar el formato electrónico de la cuenta bancaria implicada y deberá habilitar el servicio de conversión de datos bancarios. Para obtener más información, vea [Configurar bancos](bank-how-setup-bank-accounts.md) y [Configurar el servicio de conversión de datos bancarios](bank-how-setup-bank-data-conversion-service.md). Además, debe activar la casilla **Permitir exportación de pagos** en la ventana **Secciones diario general**. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  

Use la ventana **Registros de transferencia de crédito** para ver los archivos de pago que han sido exportados del diario de pagos. Desde esta ventana, también puede reexportar los archivos de paso en caso de errores técnicos o cambios en el archivo. No obstante, tenga en cuenta que los archivos EFT exportados no se muestran en esta ventana y no se pueden volver a exportar.  

## <a name="to-export-payments-to-a-bank-file"></a>Para exportar pagos a un archivo bancario
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.
2. Rellene las líneas de diario de pago, por ejemplo, mediante la función **Proponer pagos a proveedores**. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).
3. Rellene los campos de las líneas del diario de pagos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Si utiliza EFT, debe seleccionar **Pago electrónico** o **Pago electrónico-IAT** en el campo **Tipo pago por banco**. Distintos servicios de exportación de archivos y sus formatos requieren valores de configuración diferentes en las ventanas **Ficha banco** y **Ficha banco proveedor**. Estará informado sobre valores de configuración incorrectos o que faltan al intentar exportar el archivo.

4. Cuando haya completado todas las líneas del diario de pagos, elija la acción **Exportar**.
5. En la ventana **Exportar pagos electrónicos**, rellene los campos según sea necesario.

    Los mensajes de error aparecerán en el cuadro informativo **Errores del archivo de pagos**, donde también puede elegir un mensaje de error para ver información detallada. Debe resolver todos los errores para que se pueda exportar el archivo de pagos.

    > [!TIP]  
>   Cuando usa la función del servicio de conversión de datos bancarios, un mensaje de error común indica que el número de la cuenta bancaria no tiene la longitud que el banco requiere. Para evitar o resolver el error, debe eliminar el valor del campo en la ventana **IBAN** de la ventana **Ficha banco** y, a continuación, en el campo **N.º cuenta bancaria** un número de cuenta bancaria en el formato que requiera su banco.

6. En la ventana **Guardar como**, especifique la ubicación a la que se exporta el archivo y, a continuación, seleccione **Guardar**.

    > [!NOTE]  
>   Si utiliza EFT, guarde el formulario de remesa de proveedor resultante como documento de Word o seleccione que se envíe por correo electrónico directamente al proveedor. Los pagos ahora se agregarán a la ventana **Generar archivo EFT** desde donde se pueden generar varias órdenes de pago conjuntas para ahorrar el coste de transmisión. Para obtener más información, vea los pasos siguientes:
7. En la ventana **Diario de pagos**, seleccione la acción **Generar archivo EFT**.

    En la ventana **Generar archivo EFT**, todos los pagos configurados para EFT que haya exportado desde el diario de pagos para un banco especificado pero que no se han generado todavía se muestran en la ficha desplegable **Líneas**.
8. Seleccione la acción **Generar archivo EFT** para exportar un archivo para todos los pagos de EFT.
9. En la ventana **Guardar como**, especifique la ubicación a la que se exporta el archivo y, a continuación, seleccione **Guardar**.

El archivo del pago de banco se exporta a la ubicación que se especifique y puede empezar a cargarlo en la cuenta bancaria electrónica y hacer los pagos en sí. A continuación, podrá registrar las líneas de diario de pagos exportadas.

## <a name="to-export-payments-that-represent-customer-refunds"></a>Para exportar pagos que representan reembolsos de cliente
A continuación se describe un solución para exportar pagos electrónicos de reembolso.

> [!CAUTION]  
>   Las líneas de diario de pagos resultantes no se pueden registrar, borrar o anular.
1. Configure el cliente como proveedor. Asígnele el nombre "Cliente X para reembolsos", por ejemplo. Para obtener más información, vea [Registrar nuevos proveedores](purchasing-how-register-new-vendors.md).
2. En la línea del diario de pagos del cliente, configure el campo **Tipo de cta.** en **Cliente** y el campo **Tipo documento** en **Reembolso**.
3. Lleve a cabo los pasos normales para la exportación de pagos como se describe en "Para exportar pagos a un archivo bancario".

## <a name="to-plan-when-to-post-exported-payments"></a>Para planificar cuando registrar los pagos exportados
Si no desea registrar una línea de diario de pagos para un pago exportado, por ejemplo porque se está esperando confirmación de que la transacción ha sido procesada por el banco, puede eliminar solo la línea del diario. Cuando se crea posteriormente una línea de diario de pagos para pagar el importe pendiente en la factura, el campo **Importe total exportado** muestra qué parte del importe del pago se ha exportado ya. También puede encontrar información detallada acerca del total exportado seleccionando el botón **Movimientos de reg. de transferencia de crédito** para ver detalles acerca de los archivos de pago exportados.

Si hace un seguimiento de un proceso en el que no registra pagos hasta que haya confirmado que se han procesado en el banco, puede controlarlo de dos formas.

* En un diario de pagos con líneas de pago propuestas, puede ordenar tanto por la columna **Exportado a archivo de pagos** como por la columna **Importe total exportado** y después eliminar las propuestas de pago de las facturas pendientes para las que ya se han realizado los pagos y no desea realizar ninguno más.
* En la ventana **Proponer pagos a proveedores**, donde puede especificar qué pagos desea insertar en el diario de pagos, puede seleccionar la casilla **Omitir pagos exportados** si no desea insertar líneas de diario para pagos que ya se hayan exportado.

Para ver información acerca de pagos exportados, seleccione la acción **Historial de exportación de pagos**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Para reexportar pagos a un archivo bancario
Puede volver a exportar los archivos de pago desde la ventana **Registros de transferencia de crédito**. Antes de eliminar o registrar líneas de diario de pagos, también puede volver a exportar el archivo de pago desde la ventana **Diario de pagos** simplemente exportándolo de nuevo. Si ha eliminado o registrado las líneas de diario de pagos tras exportarlas, solo puede volver a exportar el mismo archivo de pago desde la ventana **Registros de transferencia de crédito**. Seleccione la línea para el lote de transferencias de crédito que desee volver a exportar y, a continuación, use la acción **Reexportar pagos al archivo**.

> [!NOTE]  
>   Los archivos EFT exportados no se muestran en la ventana **Registros de transferencia de crédito** y no se pueden volver a exportar.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registros de transferencia de crédito** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione una exportación de pago que desee reexportar y, a continuación, elija la acción **Reexportar pago a archivo**.

## <a name="see-also"></a>Consulte también
[Pagos](payables-manage-payables.md)  
[Configurar compras](purchasing-setup-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

