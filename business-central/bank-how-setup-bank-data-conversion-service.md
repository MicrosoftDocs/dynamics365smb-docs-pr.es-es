---
title: "Configurar la conversión de datos bancarios | Documentos de Microsoft"
description: Puede configurar cuentas bancarias para realizar un seguimiento de las transacciones e importar o exportar fuentes de bancos, como Yodlee.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 98d7215b4d8ae476fbc550ea0057e6f71a00a5fd
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-bank-data-conversion-service"></a>Configurar el servicio de conversión de datos bancarios
Ya está configurado y listo para habilitar un proveedor global de servicios de conversión de información de pagos a cualquier formato de datos que requiera el banco en [!INCLUDE[d365fin](includes/d365fin_md.md)]. A esto se le denomina en [!INCLUDE[d365fin](includes/d365fin_md.md)] el servicio de conversión de datos bancarios.

Puede exportar líneas de pago desde la ventana **Diario de pagos** a un archivo o una secuencia de datos que, más tarde, puede subir a su cuenta bancaria para procesarlas automáticamente, de manera que no deberá realizar pagos electrónicos de forma por separado. Para obtener más información, vea [Exportar pagos a un archivo bancario](payables-how-export-payments-bank-file.md).

Puede importar archivos de extracto bancario en la ventana **Diario de conciliación de pagos** mediante el servicio de conversión de datos bancarios para convertir un archivo que reciba del banco en una secuencia de datos que [!INCLUDE[d365fin](includes/d365fin_md.md)] pueda importar. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Como alternativa a la importación de extractos bancarios con el servicio de conversión de datos bancarios, puede utilizar el servicio Fuentes de bancos de Envestnet Yodlee. Para obtener más información, vea [Configuración del servicio de fuente de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)

Para importar o exportar archivos bancarios, deberá configurar su propia cuenta bancaria y las de sus proveedores. Para obtener más información, consulte [Configurar cuentas bancarias](bank-how-setup-bank-accounts.md).

> [!NOTE]  
>   El servicio de conversión de datos bancarios puede imponer un límite de número de líneas que se pueden exportar en un archivo. Recibirá un mensaje de error si se supera el límite. Es aconsejable que los archivos de extracto de cuenta no excedan las 1000 líneas, ya que el tiempo de procesado en el servicio de conversión de datos bancarios puede aumentar significativamente.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Para registrar su empresa en el servicio de conversión de datos de banco
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de servicio de conv. de datos del banco** y, a continuación, seleccione el vínculo relacionado.  
2. La ventana **Configuración de servicio de conv. de datos del banco** se abre con tres campos rellenados previamente con las URL correspondientes del proveedor del servicio de conversión de datos de banco en .

    > [!NOTE]  
    >   En la base de datos de demostración de CRONUS International Ltd. se rellenan previamente los campos Nombre de usuario y Contraseña con información de conexión de demostración, los cuales se reemplazarán con la información real de su empresa al registrarse con el servicio de conversión de datos bancarios.
3. En el campo **URL de registro**, seleccione el botón del explorador para abrir la página de inicio de sesión del proveedor de servicios.  
4. En la página de registro del proveedor de servicios del banco, escriba el nombre de usuario y la contraseña correspondientes a la suscripción de su empresa al servicio y, a continuación, complete el proceso de registro tal como indica el proveedor de servicios.

  Su empresa está ahora registrada con el servicio de conversión de datos de banco. Introduzca el nombre de usuario y la contraseña que especificó para el servicio en los campos de configuración relacionados en [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. En la ventana **Configuración de servicio de conv. de datos del banco**, en el campo **Nombre**, introduzca el mismo valor que introdujo como nombre de inicio de sesión en la página del proveedor de servicios en el paso 4.
6. En el campo **Contraseña**, introduzca el mismo valor que introdujo en el campo **Contraseña** en la página del proveedor de servicios en el paso 4.

## <a name="to-encrypt-your-login-information"></a>Para cifrar la información de inicio de sesión
Se recomienda usar esta función para proteger la información de inicio de sesión que se introduce en la ventana **Configuración de servicio de conv. de datos del banco**. Puede cifrar datos en el servidor de [!INCLUDE[d365fin](includes/d365fin_md.md)] generando claves de cifrado nuevas o importando claves existentes que se activarán en la instancia del servidor de [!INCLUDE[d365fin](includes/d365fin_md.md)] que conecta con la base de datos.

1. En la ventana **Configuración de servicio de conv. de datos del banco**, seleccione la acción **Administración del cifrado**.
2. En la ventana **Administración del cifrado de datos**, habilite el cifrado de los datos.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Para ver o actualizar la lista de formatos de datos de banco actualmente compatibles
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de servicio de conv. de datos del banco** y, a continuación, seleccione el vínculo relacionado.
2. En la pestaña **Configuración de servicio de conv. de datos del banco**, seleccione la acción **Nombre banco - Lista conversión de datos** para abrir la lista de nombres de banco que representan los datos de banco que admite el servicio de conversiones.
3. En la página **Nombre banco - Lista conversión de datos**, seleccione la acción **Actualizar lista de nombres de banco**.

Ahora se actualizará la lista de formatos de datos bancarios compatibles con el servicio de conversión de datos bancarios. Esta es la lista de nombres de bancos filtrada por país o región y que se puede seleccionar en el campo **Nombre del banco - Conversión de datos** en la ventana **Ficha de cuenta bancaria**.

> [!NOTE]  
>   La actualización de los formatos de datos bancarios se produce también cuando se selecciona o especifica un valor en el campo **Nombre del banco - Datos de conversión** en la cuenta bancaria.

Se ha registrado en el servicio de conversión de datos de banco. Refleje la información de registro en cada banco que usará el servicio.

## <a name="see-also"></a>Consulte también
[Configurar banca](bank-setup-banking.md)  
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

