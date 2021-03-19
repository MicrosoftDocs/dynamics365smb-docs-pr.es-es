---
title: Asignar costos a socios entre empresas | Documentos de Microsoft
description: Descubra cómo la configuración de IVA para clientes y proveedores controla si se calcula el IVA y cómo.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0ebed6a95212fdcf00b54af823684ae139e29638
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388479"
---
# <a name="allocate-costs-to-intercompany-partners"></a>Asignar costos a socios entre empresas
Cuando utiliza contabilizaciones de empresas vinculadas para transferir documentos entre empresas asociadas, las parametrizaciones relacionadas con el IVA (principalmente el grupo de contabilización comercial de IVA) asignadas a las cuentas de cliente o proveedor (asociadas con el socio de empresas vinculadas) controlan si y cómo se calcula y registra el IVA. También puede realizar distribuciones de costos directamente desde una orden de compra a empresas asociadas. Por ejemplo, si registra una factura de compra de un proveedor externo y desea distribuir algunos o todos los costos a uno o más socios de empresas vinculadas.

Puede asignar costos a uno o más socios de empresas vinculadas mediante lo siguiente:

* **Diarios generales intercompañía** - Estos diarios son útiles cuando se compra un servicio. Por ejemplo, cuando una empresa matriz contrata un servicio para instalar sistemas informáticos en dos filiales. La factura se envía a la empresa matriz, pero los costos se asignan a los socios de empresas vinculadas. Para más información, vea [Trabajar con diarios y documentos de empresas vinculadas](intercompany-how-work-documents-journals.md).
* Órdenes de compra y facturas: el uso de documentos de compra es útil cuando las funciones de compra de, por ejemplo, los gastos operativos, se centralizan en una empresa y luego se asignan a los socios de empresas vinculadas.

## <a name="to-allocate-costs-using-an-intercompany-general-journal"></a>Asignar costos mediante un diario general de empresas vinculadas
Para ingresar una línea en un diario general de empresas vinculadas, siga estos pasos. 

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario general de empresas vinculadas** y luego elija el enlace relacionado.
2. Si es necesario, en el campo **Documento externo No.**, ingrese el número de documento en la factura del proveedor.
3. Elija **Factura** en el campo **Tipo documento**.
4. En el campo **Tipo mov.**, elija **Proveedor**.
5. En el campo **Nº cuenta**, elija el proveedor.
6. En el campo **Cantidad**, ingrese un monto negativo igual al monto en la factura.
7. En el campo **Tipo contrapartida**, elija **Cuenta**.
8. En el campo **Cta. contrapartida**, elija la cuenta de contrapartida para usar.
9. Para asignar costos a los socios de empresas vinculadas, siga estos pasos:
   1. Cree una línea nueva.
   2. Deje el campo **Tipo de Documento**, elija la opción que deja el campo en blanco.
   3. En el campo **Documento núm.**, ingrese un número que sea diferente al número del campo **Documento externo No.**. La asignación de costos se considera una transacción diferente.
   4. En el campo **Tipo mov.**, elija **Socio IC**.
   5. En el campo **Cuenta No.**, elija el socio de empresas vinculadas al que asignar el costo.
   6. En el campo **Tipo de cuenta de contrapartida**, elija **Cuenta**.
   7. En el campo **Número de cuenta de saldo**, elija la cuenta de mayor en la que contabilizará el importe que recibe del socio de empresas vinculadas.
   1. En el campo **Cantidad**, ingrese el monto de la factura para asignar al socio de empresas vinculadas.
   1. En el campo **N.º cuenta IC asociada**, elija la cuenta de mayor en la que desea contabilizar el importe para el socio de empresas vinculadas. 
   1. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Repita estos pasos para cada socio de empresas vinculadas que deba compartir el costo.
1. Para contabilizar el documento y asignar los costos, elija **Enviar**.  

## <a name="to-allocate-costs-using-a-purchase-document"></a>Para imputar costos mediante un documento de compra
El siguiente procedimiento describe cómo asignar costos usando una factura de compra. Los pasos son los mismos para pedidos de compra.

> [!NOTE]
> Para completar estos pasos debe personalizar la página **Factura de compra** agregando los campos **Código de socio de IC**, **Socio IC Ref. Tipo** y **Socio de IC**. Para más información, vea [Para comenzar a personalizar una página a través del banner de personalización](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Factura de compra** y luego elija el enlace relacionado.
2. En el campo **Tipo**, elija **Cuenta**.
   
   La cuenta de mayor es la única opción que puede utilizar para asignar costos.  
1. En el campo **N.º**, elija la cuenta de contabilización.
1. En el campo **Código socio IC**, elija el socio de empresas vinculadas al que asignar el costo.
1. En **Tipo referencia socio IC** elija la cuenta de mayor a utilizar para la asignación. Esta cuenta asignará el gasto a una cuenta en el plan de cuentas del socio intercomunicador.
1. En el campo **Cantidad**, especifique el número de unidades que se cobrarán al socio de empresas vinculadas.
1. En el campo **Costo unitario directo excl. IVA (o Incl. IVA)**, ingrese el costo por artículo a cargar al socio de empresas vinculadas.
1. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Para contabilizar la orden de compra, elija **Registrar**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners"></a>Para enviar los costos asignados a socios de empresas vinculadas
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Transacciones sal. IC** y luego elija el enlace relacionado.
2. Elija líneas para enviar y luego elija la acción **Enviar a IC Partner**. 
3. Para asignar los costos, elija la acción **Acciones de línea completa**.

## <a name="calculating-vat-for-cost-distributions"></a>Cálculo del IVA para distribuciones de costos
Cuando usa un documento para distribuir costos a socios de empresas vinculadas, hay dos configuraciones de IVA que debe tener en cuenta: 
* La configuración de la cuenta de mayor para gastos:
   * Si el negocio general o los grupos de contabilización comercial del IVA se configuran en la cuenta de mayor, el cálculo depende de los grupos y los grupos de productos de la línea del documento.
   * Si los grupos contables comerciales generales o comerciales de IVA no se especifican en la cuenta de mayor, el cálculo depende de lo siguiente:
* La configuración del grupo de contabilización en el socio de empresas vinculadas
   * Si el socio de empresas vinculadas está asignado a un número de cliente que no tiene un grupo contable comercial general o comercial de IVA especificado.
   * No hay ningún número de cliente asociado con el socio de empresas vinculadas. Luego, los grupos de contabilización comercial general o comercial de IVA están en blanco y se utiliza la línea en la configuración de contabilización de IVA, que suele ser un grupo en el que se especifica el 0% de IVA.

> [!NOTE]
> Es importante validar tanto la configuración del socio de empresas vinculadas como la configuración de la cuenta de mayor (para la cuenta de gastos utilizada para la distribución de costos) antes de asignar costos a los socios de empresas vinculadas.

## <a name="see-also"></a>Consulte también
[Configurar empresa vinculada](intercompany-how-setup.md)  
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]