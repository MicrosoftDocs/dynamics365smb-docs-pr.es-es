---
title: 'Informe 340 [ES]'
description: 'Este tema describe el Informe 340, que contiene información sobre facturas e impuestos emitidos o recibidos por su empresa en un período determinado.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Informe 340 en la versión en español
El **Informe 340** contiene información sobre facturas e impuestos emitidos o recibidos por su empresa en un período determinado y se basa en **Fecha de IVA**. El informe se genera en un formato que ha aprobado la administración fiscal. Este informe debe enviarse en el período de liquidación mensual o trimestral de la empresa, según el tamaño de la empresa. Este archivo puede cargarse en el sitio web de la Agencia Tributaria o enviarse en CD-ROM. Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://www.agenciatributaria.es/). Si el número de operaciones es mayor a 1 000 000 el informe se puede enviar electrónicamente.  

## Requisitos de informes para emprendedores y pequeñas empresas  
Los requisitos de presentación de informes para empresarios y pequeñas empresas se modifican para apoyar a las empresas que utilizan los criterios de contabilidad de efectivo (CAC).  

Una empresa puede utilizar el método de contabilidad de efectivo si las ventas del negocio no exceden los 2 millones de euros al año. Hay una excepción a esta regla para una empresa cuyos recibos en efectivo de un único cliente exceden la suma de 100 000 euros.  

En [!INCLUDE[prod_short](../../includes/prod_short.md)], puede configurar grupos de contabilización para la contabilización del IVA en efectivo para compras y ventas.  

 Si se archiva un informe de este régimen, se aplica la etiqueta siguiente a algunos informes de [!INCLUDE[prod_short](../../includes/prod_short.md)]: **Régimen especial del criterio de caja**. Los informes modificados son:  

|Informe|Description|  
|------------|---------------------------------------|  
|Informe 117|Recordatorio|  
|Informe 118|Documento de interés|  
|Informe 205|Confirmación pedido|  
|Informe 206|Ventas - Factura|  
|Informe 207|Ventas - Abono|  
|Informe 405|Pedido compra|  
|Informe 406|Compra – Factura|  
|Informe 407|Compras - Abono|  
|Informe 5900|Pedido servicio|  
|Informe 5911|Servicio - Factura|  
|Informe 5912|Servicio - Abono|  

## Formato de archivo  
El formato de archivo del **informe 340** incluye un registro de deponente y al menos una de las facturas emitidas y facturas recibidas. La información de deponente se obtiene de la tabla **Información empresa** y del formulario de solicitud. Las facturas emitidas se obtienen de las empresas a las que se han vendido mercancías o servicios. La información de cliente se obtiene de la tabla **Cliente**. Las facturas recibidas se obtienen de las empresas a las que se han comprado mercancías o servicios. La información de proveedor se obtiene de la tabla **Proveedor**.  

> [!NOTE]  
>  Si no hay ningún registro de formato, el archivo no se crea y se muestra un mensaje de error.  

## Movimientos incluidos en el informe 340  
Los movimientos incluidos en el **informe 340** deben haberse registrado durante el ejercicio y el periodo que se ha indicado en el formulario de solicitud. Los movimientos que se incluyen en el informe de pagos en efectivo se pueden registrar del año anterior.  

### Negocios  
El **Informe 340** debe incluir los siguientes movimientos:  

- Facturas de ventas y abonos registrados.  
- Facturas de compras y abonos registrados.  
- Facturas de servicios y abonos registrados.  
- Autofacturas y autoabonos.  
- Pagos en efectivo.  

Los movimientos del informe **Libro facturas emitidas** se deben incluir en el informe como facturas emitidas.  

Los movimientos del informe **Libro facturas recibidas** se deben incluir en el informe como facturas recibidas.  

### Empresas pequeñas  
Para las pequeñas empresas y los empresarios que operan bajo los Criterios de contabilidad de efectivo (CAC), el Informe 340 informa de las facturas en virtud del CAC. La factura está marcada con una “Z” para el tipo de la operación. Si la factura está bajo el CAC, se informa de lo siguiente:  

- Método de pago/recibo, es decir, efectivo, cheque, transferencia, etc. Si no se ha producido ningún cobro, este campo estará en blanco en el informe.  
- Importe pago/albarán (completo, parcial)  
- Fechas pagos/albarán  

### Facturas con diferentes porcentajes de IVA o de RE  
Si la factura tiene más de un porcentaje de IVA o de recargo de equivalencia (RE), el informe debe incluir todos los registros con diferentes porcentajes de IVA y RE. Si la factura incluye recargos de equivalencia (RE), se mostrará el porcentaje de RE y el importe de RE sin IVA.  

En todos los registros se mostrará el mismo Id. de factura y número de IVA del cliente.  

## Restricciones del formato de archivo  
Antes de crear el informe **Informe 340**, debe tener en cuenta las siguientes restricciones de formato de archivo:  

- Todos los importes se deben expresar en euros.  
- Todos los importes deben ser positivos. En los campos donde son posibles importes negativos, se indica **N**.  
- Todo el texto deber estar en mayúsculas.  
- Todos los campos alfanuméricos se deben alinear a la izquierda.  
- Todos los campos numéricos deben ir alineados a la derecha.  
- Los caracteres especiales se convierten a caracteres estándar.  
- Si no contienen ningún valor, los campos alfanuméricos se dejarán en blanco y los campos numéricos se rellenarán con ceros.  

## Consulte también  
 [Crear el informe 340](how-to-create-report-340.md)   
 [Pagos en efectivo](payments-in-cash.md)   
 [Funcionalidad local para España](spain-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
