---
title: Asignación de campos al importar archivos CAMT de SEPA | Documentos de Microsoft
description: En los mercados europeos, puede importar los archivos de extractos bancarios en las normas regionales SEPA (zona única de pagos en euros).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e4c3b60bca16e1f1e72e728d02b07ded11cada09
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692589"
---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Asignación de campos al importar archivos CAMT de SEPA
[!INCLUDE[d365fin](includes/d365fin_md.md)] admite los estándares de SEPA (zona única de pagos en euros) regional para importar los extractos de cuenta de SEPA (formato CAMT). Para obtener más información, vea [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

 El estándar CAMT de SEPA en sí presenta variaciones locales. Por lo tanto, es posible que tenga que modificar la configuración de intercambio de datos genérica (representada por el código de **CAMT de SEPA** en la página **Definiciones de intercambio de registro**) para adaptarla a una variación local del estándar. En las tablas siguientes se muestra la asignación de elemento a campo para las tablas 81, 273 y 274 en la implementación CAMT de SEPA en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Para obtener información acerca de cómo crear o ajustar una definición de intercambio de datos, consulte [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>Asignación de datos de CAMT a los campos de la tabla del diario general (81)  

|Ruta de acceso al elemento|Elemento de mensaje|Tipo de datos|Descripción|Identificador de signo de negativo|Nº campo|Nombre de campo|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Importe|Decimal|Importe del dinero del movimiento de efectivo||13|Importe|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Texto|Indica si el movimiento es de débito o de crédito|DBIT|13|Importe|  
|Stmt/Ntry/BookgDt/Dt|Fecha|Fecha|Fecha en que un movimiento se registra en una cuenta de los libros del proveedor de servicios de cuenta||5|Fecha registro|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|Fecha y hora en que un movimiento se registra en una cuenta de los libros del proveedor de servicios de cuenta||5|Fecha registro|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nombre|Texto|Nombre de la parte que debe un importe monetario al (último) acreedor||1221|Información del pagador|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|No estructurado|Texto|Información suministrada para activar el emparejamiento o la conciliación de un movimiento con los productos que el pago pretende liquidar, como facturas comerciales en un sistema de cuentas de cobro no estructuradas.||8|Descripción|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Texto|Información adicional acerca del movimiento.||1222|Información de la transacción|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>Asignación de datos de CAMT a los campos de la tabla de conciliación (273)  

|Ruta de acceso al elemento|Elemento de mensaje|Tipo de datos|Descripción|Identificador de signo de negativo|Nº campo|Nombre de campo|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Fecha|La fecha y hora de creación del mensaje.||3|Fecha extracto|  
|Stmt/Bal/Amt|Importe|Decimal|Importe derivado de los importes liquidados para todos los movimientos de debe y haber.||4|Saldo final extracto|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>Asignación de datos de CAMT a los campos de la tabla de la línea de conciliación (274)  

|Ruta de acceso al elemento|Elemento de mensaje|Tipo de datos|Descripción|Identificador de signo de negativo|Nº campo|Nombre de campo|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Importe|Decimal|Importe del dinero del movimiento de efectivo||7|Importe extracto|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Texto|Indica si el movimiento es de débito o de crédito|DBIT|7|Importe extracto|  
|Stmt/Ntry/BookgDt/Dt|Fecha|Fecha|Fecha en que un movimiento se registra en una cuenta de los libros del proveedor de servicios de cuenta||5|Fecha movimiento|  
|Stmt/Ntry/BookgDt/DtTm|DateTime|DateTime|Fecha y hora en que un movimiento se registra en una cuenta de los libros del proveedor de servicios de cuenta||5|Fecha movimiento|  
|Stmt/Ntry/ValDt/Dt|Fecha|Fecha|Fecha en que los activos están disponibles para el propietario de la cuenta en el caso de un movimiento de haber, o dejan de estar disponibles para el propietario de la cuenta en el cas de un movimiento de debe||12|Fecha valor|  
|Stmt/Ntry/ValDt/DtTm|DateTime|DateTime|Fecha y hora en que los activos están disponibles para el propietario de la cuenta en el caso de un movimiento de haber, o dejan de estar disponibles para el propietario de la cuenta en el cas de un movimiento de debe||12|Fecha valor|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Nombre|Texto|Nombre de la parte que debe un importe monetario al (último) acreedor||15|Información del pagador|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|No estructurado|Texto|Información suministrada para activar el emparejamiento o la conciliación de un movimiento con los productos que el pago pretende liquidar, como facturas comerciales en un sistema de cuentas de cobro no estructuradas.||6|Descripción|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Texto|Información adicional acerca del movimiento.||16|Información de la transacción|  

 Los elementos en el nodo **Ntry** que se importan en [!INCLUDE[d365fin](includes/d365fin_md.md)] pero que no están asignados a ningún campo se almacenan en la tabla **Def. columna intercambio registro**. Los usuarios pueden ver estos elementos desde las páginas **Diario de conciliación de pagos**, **Liquidación de pago** y **Conciliación banco** si eligen la acción **Detalles de línea de extracto bancario**. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).  
## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Uso de la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)   
[Uso de esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Conciliar los pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md)  
