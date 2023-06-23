---
title: Asignación de campos para exportar los archivos de pago de banco | Documentos de Microsoft
description: 'Cuando exporta archivos de pago utilizando la extensión AMC Banking 365 Fundamentals, los datos que exporta se exponen al proveedor de servicios.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension" />Asignación de campos al exportar archivos de pago utilizando la extensión AMC Banking 365 Fundamentals
Cuando exporta archivos de pago utilizando la extensión AMC Banking 365 Fundamentals, los datos que exporta se exponen al proveedor de servicios. El proveedor del servicio es responsable de la privacidad de estos datos. Para obtener más información sobre la extensión AMC Banking 365 Fundamentals, consulte [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  Cuando se exportan archivos de pago con la extensión AMC Banking 365 Fundamentals, algunos de los datos empresariales serán visibles para el proveedor del servicio. El proveedor de servicios, AMC Consult A/S, es responsable de la privacidad de estos datos. Para obtener más información, consulte [Directiva de función de AMC](https://go.microsoft.com/fwlink/?LinkId=510158).  

> [!NOTE]
> En la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)], ya está configurado y conectado un proveedor global de servicios de conversión de datos bancarios a cualquier formato de archivo que el banco requiera. En las versiones norteamericanas, el mismo servicio se puede utilizar para enviar archivos de pago como transferencia electrónica de fondos (EFT), por ejemplo, la red de Cámara de Compensación Automatizada (ACH) de uso común, aunque con un proceso ligeramente diferente.

La siguiente tabla enumera los campos en [!INCLUDE[prod_short](includes/prod_short.md)] desde los que puede exportar datos.  

|Campo asignado|Campo en tabla|Escritorio|Descripción|  
|------------------|--------------------|-----------|---------------------------------------|  
|N.º acreedor|N.º acreedor|Cuenta bancaria|El identificador asignado a su empresa por el banco para cobrar a los pagos|  
|N.º de cuenta bancaria del remitente|N.º cuenta bancaria/IBAN|Cuenta bancaria|El número de la cuenta bancaria de su empresa (IBAN u otro) que se especifica en la ficha de la cuenta bancaria|  
|Estándar de compensación bancaria del remitente|Estándar de compensación bancaria|Cuenta bancaria|El registro de nombres de bancos nacionales utilizado para la cuenta bancaria del emisor|  
|Código de compensación del banco del remitente|Código de compensación bancaria|Cuenta bancaria|El identificador del banco del remitente en relación con el registro de nombres de bancos utilizado|  
|BIC del banco del remitente|Código SWIFT|Cuenta bancaria|El identificador SWIFT de la cuenta bancaria del emisor.|  
|Divisa de cuenta bancaria del remitente|Cód. divisa|Cuenta bancaria|El código de divisa de la cuenta bancaria del remitente|  
|Nº documento|Nº documento|Línea diario general|El número de documento de la línea de pago|  
|Liq. por nº doc. externo|Liq. por nº doc. externo|Línea diario general|El número de documento externo de la factura o del abono al que se aplica la línea de pago.|  
|Id. del destinatario|Nº cuenta|Línea diario general|El número de cliente o proveedor especificado en la línea de pago|  
|Tipo pago|Conversión de datos del banco - Tipo de pagos|Forma pago|El tipo de transferencia bancaria, como nacional o internacional|  
|Referencia pago|Referencia pago|Línea diario general|La referencia de pago de la línea de pago|  
|Dirección del destinatario|Dirección|Cliente/Proveedor|La dirección del receptor especificada en la ficha de cliente o de proveedor|  
|Ciudad del destinatario|Población|Cliente/Proveedor|La población del receptor especificada en la ficha de cliente o de proveedor|  
|Nombre del destinatario|Nombre|Cliente/Proveedor|El nombre del receptor especificado en la ficha de cliente o de proveedor|  
|Código de país/región del destinatario|Cód. país/región|Cliente/Proveedor|El código de país o región del receptor especificado en la ficha de cliente o de proveedor|  
|Código postal del destinatario|C.P.|Cliente/Proveedor|El código postal del receptor especificado en la ficha de cliente o de proveedor|  
|N.º cta. bancaria destinatario|N.º cuenta bancaria/IBAN|Banco cliente/Banco proveedor|El número de la cuenta bancaria del receptor (IBAN u otro) que se especifica en la ficha de la cuenta bancaria del cliente o del proveedor|  
|Código de compensación del banco del destinatario|Estándar de compensación bancaria|Banco cliente/Banco proveedor|El registro de nombres de bancos nacionales utilizado para la cuenta bancaria del receptor|  
|Est. de compensación del banco del destinatario|Código de compensación bancaria|Banco cliente/Banco proveedor|El identificador de la cuenta bancaria del receptor en relación con el registro de nombres de bancos utilizado|  
|Dirección correo elect. del destinatario|E-Mail|Cliente/Proveedor|La dirección de correo electrónico del destinatario|  
|Mensaje al destinatario 1|Mensaje al destinatario|Línea diario general|El mensaje al receptor especificado en la línea de pago|  
|Importe|Importe|Línea diario general|El importe en la línea de pago|  
|Cód. divisa|Cód. divisa|Línea diario general|El código de divisa en la línea de pago.|  
|Fecha de transferencia|Fecha registro|Línea diario general|La fecha de registro de la línea de pago|  
|Importe factura|Importe inicial|Mov. proveedor/cliente|El importe en el movimiento para el que se liquida el pago.|  
|Fecha factura|Fecha emisión documento|Mov. proveedor/cliente|La fecha de factura en el movimiento para el que se liquida el pago|  
|Dirección del banco del destinatario|Dirección|Banco cliente/Banco proveedor|La dirección de la cuenta bancaria del receptor que se especifica en la ficha de la cuenta bancaria del cliente o del proveedor|  
|La dirección de la cuenta bancaria del receptor que se especifica en la ficha de la cuenta bancaria del cliente o del proveedor|Población|Banco cliente/Banco proveedor|La población de la cuenta bancaria del receptor que se especifica en la ficha de la cuenta bancaria del cliente o del proveedor|  
|Nombre del banco del destinatario|Nombre|Banco cliente/Banco proveedor|El nombre de la cuenta bancaria del receptor que se especifica en la ficha de la cuenta bancaria del cliente o del proveedor|  
|País/región del banco del destinatario|Cód. país/región|Banco cliente/Banco proveedor|El país o la región de la cuenta bancaria del receptor que se especifica en la ficha de la cuenta bancaria del cliente o del proveedor|  
|Código postal del banco destinatario|C.P.|Banco cliente/Banco proveedor|El código postal de la cuenta bancaria del receptor que se especifica en la ficha de la cuenta bancaria del cliente o del proveedor|  
|Dirección del banco del remitente|Dirección|Cuenta bancaria|La dirección de la cuenta bancaria del emisor especificada en la ficha de la cuenta bancaria|  
|Ciudad del banco del remitente|Población|Cuenta bancaria|La población de la cuenta bancaria del emisor especificada en la ficha de la cuenta bancaria|  
|Nombre del banco del remitente|Nombre|Cuenta bancaria|El nombre de la cuenta bancaria del emisor especificada en la ficha de la cuenta bancaria|  
|País/región del banco del remitente|Cód. país/región|Cuenta bancaria|El país o región de la cuenta bancaria del emisor especificada en la ficha de la cuenta bancaria|  
|Código postal del banco del remitente|C.P.|Cuenta bancaria|El código postal de la cuenta bancaria del emisor especificada en la ficha de la cuenta bancaria|  
|Plantilla de libros diario general|Nombre libro diario|Línea diario general|La plantilla de la sección de diario general que se usa para la línea de pago|  
|Nombre sección diario general|Nombre sección diario|Línea diario general|El nombre de la sección de diario general que se usa para la línea de pago|  
|Nombre del banco del remitente - Conv. de datos|Nombre del banco - Conv. de datos|Cuenta bancaria|El nombre de la cuenta bancaria del emisor solicitado por la extensión AMC Banking 365 Fundamentals y especificado en la ficha de la cuenta bancaria|  

## <a name="see-also" />Consulte también
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)
[Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)   
[Realizar pagos con la extensión AMC Banking 365 Fundamentals o transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
