---
title: Uso de la extensión AMC Banking 365 Fundamentals | Microsoft Docs
description: Intercambie datos fácilmente con sus bancos mediante la transformación de datos al formato que requieran.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a2147240aac15b805a6f64473b5eb2febb38deac
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757572"
---
# <a name="using-the-amc-banking-365-fundamentals-extension"></a>Uso de la extensión AMC Banking 365 Fundamentals
La extensión AMC Banking 365 Fundamentals hace que sea más fácil y más preciso enviar datos a sus bancos. La extensión conecta [!INCLUDE[prod_short](includes/prod_short.md)] con el servicio AMC Banking 365 Fundamentals para Microsoft Dynamics 365 Business Central, que puede convertir datos bancarios de [!INCLUDE[prod_short](includes/prod_short.md)] a formatos que necesitan más de 600 bancos de todo el mundo. Por ejemplo, esto facilita la transferencia de pagos y créditos a proveedores al introducir los pagos en [!INCLUDE[prod_short](includes/prod_short.md)] y luego cargarlos en su banco. Los formatos también pueden agilizar los procesos de conciliación de banco. Para obtener más información, consulte [AMC Banking para Microsoft Dynamics 365 Business Central](https://amcbanking.com/landing365bc/help).

> [!Note]
> AMC Banking ha creado extensiones adicionales que funcionan con [!INCLUDE[prod_short](includes/prod_short.md)]. Este tema describe solo la extensión Fundamental.

## <a name="using-our-demonstration-account"></a>Mediante nuestra cuenta de demostración
[!INCLUDE[prod_short](includes/prod_short.md)] incluye una cuenta de demostración que le permite probar la extensión AMC Banking 365 Fundamentals. Proporcionamos configuraciones predeterminadas para conectarse a AMC Banking, especificando los bancos para obtener datos de [!INCLUDE[prod_short](includes/prod_short.md)], más algunas definiciones de intercambio de datos. Puede ver la configuración de conexión en la página **Configuración de AMC Banking**. Para los bancos, la extensión aplica valores en los campos **Nombre del banco**, **N.º mensaje transf. créd.**, **Formato de importación de extractos bancarios** y **Formato de exportación de pagos** en las fichas de banco.

Proporcionamos la configuración, pero para probar la extensión, debe ejecutar la guía de configuración asistida para aplicarla. Para ejecutar la guía, en la página **Configuración de AMC Banking**, elija la acción **Configuración asistida**.

> [!Note]
> Existen algunas limitaciones en la cuenta de demostración. Por ejemplo, cuando convierte pagos, el importe en el archivo convertido no coincidirá con el importe real. En cambio, el importe siempre será de cinco unidades de la divisa que utiliza para los pagos.  

## <a name="setting-up-the-extension"></a>Configuración de la extensión
Comenzar a usar la extensión implica solo unos pocos pasos sencillos y una guía de configuración asistida establecerá la conexión y activará la extensión. La guía llevará a cabo acciones como instalar las definiciones de intercambio de datos para configuraciones de exportación/importación de extractos bancarios e iniciar la serie de números utilizada para los mensajes de transferencia de crédito.  

### <a name="to-set-up-the-required-permission-sets"></a>Para configurar los conjuntos de permisos necesarios
Antes de que las personas puedan usar esta extensión, su administrador debe copiar los siguientes conjuntos de permisos, editarlos y luego asignar los nuevos conjuntos de permisos a los usuarios en lugar del original:

* **D365 Basic**
* **D365 Team Member**
* **D365 Read**
* **IntelligentCloudBC**

Para obtener más información, consulte [Para copiar un conjunto de permisos](ui-define-granular-permissions.md#to-copy-a-permission-set).

Para cada nuevo conjunto de permisos, conceda solo el permiso **Leer** para la **Tabla de configuración (20101) de AMC Banking**. Para obtener más información, consulte [Para crear o modificar permisos manualmente](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-connect-the-extension-to-amc-banking"></a>Para conectar la extensión a AMC Banking
1. Obtenga un módulo y un plan de servicio para AMC Banking. Para ello, visite la página [Licencia de AMC](https://license.amcbanking.com/register).
2. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de AMC Banking** y luego elija el enlace relacionado.  
3. En la página **Configuración de AMC Banking**, elija la acción **Configuración asistida**.
4. Complete los pasos de la guía de configuración asistida.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Para conectar bancos a la extensión
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Bancos** y luego elija el enlace relacionado.
2. Abra la ficha del banco que desea conectar al servicio.
3. En el campo **Nombre del banco**, elija el formato que necesita su banco.  

   Los formatos se filtran para mostrar solo aquellos que son relevantes para el país o región que se ha especificado para el banco.
4. En el campo **N.º mensaje transf. créd.**, elija la serie de números que se usará para los mensajes que acompañan a los pagos.
5. En los campos **Formato de importación de extractos bancarios** y **Formato de exportación de pagos**, elija las definiciones de intercambio de datos que necesita su banco.

## <a name="using-the-extension"></a>Uso de la extensión
Para usar esta extensión es solo cuestión de exportar datos en la página **Diarios de pagos** y luego cargarlos en el servicio web de su banco. Para obtener más información, consulte [Realización pagos con la conversión de datos del banco o Transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!Note]
> Debes completar los campos **Código SWIFT** e **IBAN** para cada banco.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Para exportar datos y enviarlos a su banco
> [!CAUTION]  
>  Cuando se exportan datos con la extensión AMC Banking 365 Fundamentals, algunos de los datos empresariales serán visibles para el proveedor del servicio. El proveedor de servicios, AMC Consult A/S, es responsable de la privacidad de estos datos. Para obtener más información, consulte [Directiva de función de AMC](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de pagos** y luego elija el enlace relacionado.
2. Cree las líneas del diario que desea exportar.  

   > [!Note]
   > Para cada línea, recuerde elegir **Pago electronico** en el campo **Tipo pago por banco**.
3. Seleccione la acción **Exportar**.

### <a name="to-import-and-apply-the-converted-file"></a>Para importar y aplicar el archivo convertido
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diario de conciliación de pagos** y luego elija el enlace relacionado.
2. Elija la acción **Importar transacción bancaria** y luego elija el archivo convertido.  

   [!INCLUDE[prod_short](includes/prod_short.md)] creará un nuevo diario de conciliación de pagos que contiene los datos del archivo. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Consulte también
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Introducción](product-get-started.md)
