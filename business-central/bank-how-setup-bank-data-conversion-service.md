---
title: Configurar la conversión de datos bancarios
description: 'Puede configurar cuentas bancarias para realizar un seguimiento de las transacciones e importar o exportar fuentes de bancos, como Yodlee.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, AMC Banking 365 Fundamentals extension, funds transfer'
ms.search.form: '304, 20106, 20105, 20100, 20101, 20107, 20109'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Configurar la extensión AMC Banking 365 Fundamentals
Ya está configurado y listo para habilitar un proveedor global de servicios de conversión de información de pagos a cualquier formato de datos que requiera el banco en [!INCLUDE[prod_short](includes/prod_short.md)]. Esto se menciona en [!INCLUDE[prod_short](includes/prod_short.md)] como la extensión AMC Banking 365 Fundamentals.

Puede exportar líneas de pago desde la página **Diario de pagos** a un archivo o una secuencia de datos que, más tarde, puede subir a su cuenta bancaria para procesarlas automáticamente, de manera que no deberá realizar pagos electrónicos de forma por separado. Para obtener más información, vea [Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Puede importar archivos de extracto bancario en la página **Diario de conciliación de pagos** mediante la extensión AMC Banking 365 Fundamentals para convertir un archivo que reciba del banco en una secuencia de datos que [!INCLUDE[prod_short](includes/prod_short.md)] pueda importar. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Como alternativa a la importación de extractos bancarios con la extensión AMC Banking 365 Fundamentals puede usar el servicio Envestnet Yodlee Bank Feeds. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

Para importar o exportar archivos bancarios, deberá configurar su propia cuenta bancaria y las de sus proveedores. Para obtener más información, consulte [Configurar cuentas bancarias](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> La extensión AMC Banking 365 Fundamentals puede imponer un límite de número de líneas que se pueden exportar en un archivo. Recibirá un mensaje de error si se supera el límite. Es aconsejable que los archivos de extracto de cuenta no excedan las 1000 líneas, ya que el tiempo de procesado en la extensión AMC Banking 365 Fundamentals puede aumentar significativamente.

## Para inscribir a su empresa en la extensión AMC Banking 365 Fundamentals
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de servicio de conv. de datos del banco** y luego elija el enlace relacionado.  
2. La página **Configuración de servicio de conv. de datos del banco** se abre con tres campos rellenados previamente con las URL correspondientes del proveedor de la extensión AMC Banking 365 Fundamentals.

    > [!NOTE]  
    >   En la base de datos de demostración de CRONUS España S.A. se rellenan previamente los campos Nombre de usuario y Contraseña con información de conexión de demostración, los cuales se reemplazarán con la información real de su empresa al registrarse con la extensión AMC Banking 365 Fundamentals.
3. En el campo **URL de registro**, seleccione el botón del explorador para abrir la página de inicio de sesión del proveedor de servicios.  
4. En la página de registro del proveedor de servicios del banco, escriba el nombre de usuario y la contraseña correspondientes a la suscripción de su empresa al servicio y, a continuación, complete el proceso de registro tal como indica el proveedor de servicios.

    Su compañía ya está inscrita para la extensión AMC Banking 365 Fundamentals. Introduzca el nombre de usuario y la contraseña que especificó para el servicio en los campos de configuración relacionados en [!INCLUDE[prod_short](includes/prod_short.md)].

5. En la página **Configuración de servicio de conv. de datos del banco**, en el campo **Nombre**, introduzca el mismo valor que introdujo como nombre de inicio de sesión en la página del proveedor de servicios en el paso 4.
6. En el campo **Contraseña**, introduzca el mismo valor que introdujo en el campo **Contraseña** en la página del proveedor de servicios en el paso 4.

> [!NOTE]  
> Los datos de inicio de sesión se cifran automáticamente.

## Para ver o actualizar la lista de formatos de datos de banco actualmente compatibles
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de servicio de conv. de datos del banco** y luego elija el enlace relacionado.
2. En la página **Configuración de servicio de conv. de datos del banco**, seleccione la acción **Nombre banco - Lista conversión de datos** para abrir la lista de nombres de banco que representan los datos de banco que admite el servicio de conversiones.
3. En la página **Nombre banco - Lista conversión de datos**, seleccione la acción **Actualizar lista de nombres de banco**.

Ahora se actualizará la lista de formatos de datos bancarios compatibles con la extensión AMC Banking 365 Fundamentals. Esta es la lista de nombres de bancos filtrada por país o región y que se puede seleccionar en el campo **Nombre del banco - Conversión de datos** en la página **Ficha de cuenta bancaria**.

> [!NOTE]  
>   La actualización de los formatos de datos bancarios se produce también cuando se selecciona o especifica un valor en el campo **Nombre del banco - Datos de conversión** en la cuenta bancaria.

Ya se ha inscrito para la extensión AMC Banking 365 Fundamentals. Refleje la información de registro en cada banco que usará el servicio.

## Consulte también
[Configurar banca](bank-setup-banking.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]