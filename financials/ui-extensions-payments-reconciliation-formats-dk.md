---
title: "Utilizar la extensión de pagos y conciliaciones (DK) | Documentos de Microsoft"
description: "Esta extensión facilita la exportación de archivos con formato predefinido para cumplir con los requisitos del banco para envíos electrónicos."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 09/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 0718012c9278b337409805d95870d22dac4675ad
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---

# <a name="the-payments-and-reconciliations-dk-extension-for-microsoft-dynamics-for-finance-and-operations-business-edition"></a>La extensión de pagos y conciliaciones (DK) para Microsoft Dynamics for Finance and Operations, Business edition
Realice pagos rápidos y sin errores exportando archivos formateados específicamente para intercambios con su proveedor o banco. Estos archivos aceleran los procesos de pago y conciliación, y eliminan los errores que pueden ocurrir al ingresar manualmente la información en un sitio web de un banco.  
  
Esta extensión admite los formatos de archivo para varios bancos de Dinamarca. Cuando exporta información de pago a un archivo, la extensión empaqueta los datos en el formato que su banco requiere. Por ejemplo, algunos de los formatos son Bankdata-V3, BEC, SDC y FIK, que utilizan muchos bancos diferentes, y algunos que son más especializados para ciertos bancos, por ejemplo, Danske Bank y Nordea. La extensión también incluye algunos formatos para importar y conciliar extractos bancarios.  
  
> [!Note]
> Para utilizar la extensión, es necesario conocer el formato que el banco o proveedor requiere. Algunos bancos o proveedores ofrecen esta información en las páginas web; sin embargo, es posible que deba contactar con su servicio de atención al cliente para obtener la información.  
  
## <a name="supported-bank-formats"></a>Formatos bancarios compatibles
Esta extensión puede liquidar los formatos de archivo siguiente para archivos de pagos:  
  
* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension"></a>Para configurar la extensión
Existen algunos pasos a seguir para empezar.  
  
* Permitir exportaciones de datos de pagos. Para ayudar a proteger sus datos, no se mostrarán.  
* Configurar compra y pagos de manera que no requieran números de documentos externos en las facturas. Si es necesario, puede utilizar el número de referencia para hacer referencia a una factura específica.  
* Especificar la forma de pago de cada proveedor. Las formas de pago definen cómo se pagan las facturas de los proveedores. Por ejemplo, depósito bancario, efectivo, cheque o cuenta.  
* Especifique el tipo de formato que utiliza para cada uno de sus bancos. Por ejemplo, NORDEA, DANSKEBANK, SDC, etc.  
  
Además, debe asignar a los proveedores a un **Grupo contable negocio** y un **Grupo contable proveedor** nacional. La configuración de país/región para el proveedor debe ser Dinamarca (DK). Para obtener más información, consulte [Configurar los grupos contables](finance-posting-groups.md).  
  
### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a>Para permitir que [!INCLUDE[d365fin](includes/d365fin_md.md)] realice exportaciones de datos de pagos
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de pagos** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Editar diario de pagos**, seleccione el proceso **Banco**.  
3. Seleccione la casilla de verificación **Permitir exportación de pagos**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Para especificar una forma de pago de un proveedor
La siguiente tabla muestra las combinaciones de formas de pago FIK y GIRO que [!INCLUDE[d365fin](includes/d365fin_md.md)] admite.

||Tipo 01 | Tipo 04 | Tipo 71 | Tipo 73 |
|----|---|---|---|---|
|¿Número de cuenta de Giro o Número acreedor de FIK? | Número de cuenta de Giro | Número de cuenta de Giro | N.º acreedor de FIK | N.º acreedor de FIK|
|¿Se permiten los mensajes al destinatario? | Sí |No |No | Sí |
|¿Contiene el número de referencia de pago? | No | Sí, 16 dígitos. | Sí, 15 dígitos. | No|

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proveedores** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la ficha, amplíe la pestaña **Pagos**, en el campo **Forma pago** seleccione la forma de pago.  
3. Según de la opción que seleccione, debe rellenar otros campos. Consulte la tabla anterior para obtener una descripción de las combinaciones.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Para especificar el formato que debe utilizar en un banco
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la ficha del banco.  
3. En el campo **Formato de exportación de pagos**, seleccione el formato del archivo de exportación.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Elección de la información de pago de FIK o Giro para facturas de proveedores
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas compra** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el proveedor. Recuerde, debe ser un proveedor danés con una dirección en Dinamarca.
3. Cree una factura. Los campos **Forma pago** y **Número de proveedor** se rellenan según los valores de la ficha de proveedor. Puede cambiarlo si lo desea.
4. En el campo **Referencia de pago**, introduzca el número de 15 dígitos de la factura del proveedor.  
  
    > [!Tip]
    > Tiene que agregar solo los 11 últimos dígitos del número. [!INCLUDE[d365fin](includes/d365fin_md.md)] añadirá cuatro ceros al comienzo del número.  
  
5. Registrar la factura.

## <a name="to-use-the-extension-to-export-payment-data"></a>Para utilizar la extensión para exportar datos de pago
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Proponer diarios de pagos a proveedores**.  
  
    > [!Tip]
    > Si desea exportar únicamente pagos específicos, utilice las opciones para filtrar los datos.  
  
3. Si es necesario, puede agregar filtros para exportar únicamente pagos específicos.  
4. En el campo **Tipo pago por banco**, elija **Pago electrónico**.  
5. Seleccione la acción **Exportar**.  

## <a name="see-also"></a>Consulte también .
[Personalizar Dynamics 365 for [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante extensiones](ui-extensions.md)  
[Creación de movimientos de domiciliación de adeudo directo SEPA y exportación a un archivo bancario](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[Configuración de domiciliaciones de adeudo directo SEPA](finance-how-to-set-up-sepa-direct-debit.md)  
[Registro de recibos de pagos de domiciliación de adeudo directo SEPA](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Cobro de pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  





