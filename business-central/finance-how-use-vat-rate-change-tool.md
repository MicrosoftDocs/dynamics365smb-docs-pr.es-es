---
title: Usar la herramienta de cambio de tipo de IVA | Documentos de Microsoft
description: Usar la herramienta de cambio de tipo de IVA
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu
ms.openlocfilehash: 76c6f8902e9661f4f4dbbbf70487a53bf286edb2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183169"
---
# <a name="use-the-vat-rate-change-tool"></a>Usar la herramienta de cambio de tipo de IVA

## <a name="understanding-the-vat-rate-conversion-process"></a>Conocer el proceso de conversión de tasa de IVA  
La herramienta de cambio de tasa de IVA realiza conversiones de tasa de IVA para datos maestros, diarios y pedidos en distintas formas. Los datos maestros y los diarios seleccionados se actualizarán por el nuevo grupo de registro del producto general o de IVA. Si un pedido ha sido total o parcialmente enviado, los productos enviados guardarán el grupo de registro de producto general actual o grupo de registro de IVA de producto. Una nueva línea de pedido se creará para los productos no enviados y se actualizará para alinear grupos de registro de producto generales o de IVA nuevos y actuales. Además, se actualizarán según corresponda asignaciones de cargo de producto, reservas y la información de seguimiento de producto.  

Existen algunos parámetros que la herramienta no convierte:

* Pedidos de venta o de compra y facturas donde se hayan registrado envíos. Estos documentos se registran con la tasa de IVA actual.  
* Documentos que tienen facturas de prepago registradas. Por ejemplo, ha creado o recibido prepagos en facturas que no se han rellenado antes de utilizar la herramienta de cambio de tasa de IVA. En este caso, habrá una diferencia entre el IVA pendiente y el IVA abonado en los prepagos cuando la factura se completa. La herramienta de cambio de tasa de IVA omitirá estos documentos y tendrá que actualizarlos manualmente.  
* Envíos directos o pedidos especiales.  
* Pedidos de compra o de venta con integración de almacén si se envían o se reciben parcialmente.  
* Contratos de servicio.  

### <a name="to-prepare-vat-rate-change-conversions"></a>Para preparar conversiones de cambio de tasa de IVA  
Antes de configurar la herramienta de cambio de tasa de IVA, debe llevar a cabo estos pasos.

* Si mantiene transacciones que utilizan distintas tasas, entonces deben separarse en diferentes grupos creando nuevas cuentas contables por cada tasa o bien utilizando filtros de datos para agrupar transacciones según la tasa.  
* Si crea nuevas cuentas de contabilidad, deberá crear nuevos grupos contables.  
* Para reducir el número de documentos que se convierten, registre tantos documentos como sea posible y reduzca a un mínimo los documentos sin registrar.  
* Copia de seguridad de datos.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Para configurar la herramienta de cambio de tasa de IVA  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conf. cambio tipo IVA** y luego elija el enlace relacionado.  
2. En las fichas desplegables **Datos maestros**, **Diarios** y **Documentos**, elija un valor de grupo contable de la lista de opciones para los campos necesarios. Para cada grupo, puede elegir si desea convertir grupos de registro IVA de producto o grupos de contabilización de productos generales, o convertir ambos valores si están disponibles en el elemento de datos maestros. Para algunas áreas, también puede establecer un filtro para convertir solo un subconjunto de valores, por ejemplo, cuentas. 

### <a name="to-set-up-product-posting-group-conversion"></a>Para configurar una conversión grupos de registro de producto  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conf. cambio tipo IVA** y luego elija el enlace relacionado.  
2. En la página **Conf. cambio tasa IVA**, elija la acción **Conv. gr. contable producto IVA** o **Conv. gr. contable producto general**.  
3. En el campo **Código origen**, especifique el grupo de registro actual.  
4. En el campo **Código destino**, especifique el nuevo grupo de registro.  

### <a name="to-perform-vat-rate-change-conversion"></a>Para realizar la conversión de cambio de tasa de IVA  
Utiliza la herramienta de cambio de tasa de IVA para gestionar los cambios en la tasa estándar de IVA. Realiza las conversiones de IVA y grupo contable para cambiar las tasas de IVA y mantener informes de IVA precisos. Dependiendo de la configuración, se realizan los siguientes cambios:  

* Se convierten los grupos de registro generales y de IVA.  
* Los cambios se implementan en cuentas de contabilidad, clientes, proveedores, documentos pendientes, líneas de diario, etc.  

> [!IMPORTANT]  
>  Antes de realizar la conversión de cambio del tipo de IVA, puede probarla. Para hacerlo, siga los pasos siguientes, pero asegúrese de desactivar las casillas de verificación **Realizar conversión** y **Herramienta cambio tasa IVA finalizada**. Durante la conversión de prueba, el campo **Convertido** en la tabla **Mov. registro cambios en tasa IVA** está desactivada y el campo **Fecha conversión** en la tabla **Mov. registro cambios en tasa IVA** está vacío. Después de que la conversión esté completa, elija **Movs. reg. de cambio de tasa de IVA** para ver los resultados de la prueba. Verifique cada movimiento antes de realizar la conversión. Concretamente, verifique las transacciones que utilizan una tasa de IVA antigua.     

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conf. cambio tipo IVA** y luego elija el enlace **Conf. cambio tasa IVA**.  
2. Compruebe que haya configurado la conversión del grupo de registro de IVA de producto o la conversión del grupo de registro general de producto.  
3. Elija la casilla de verificación **Realizar conversión**.  

    > [!IMPORTANT]  
    >  Desactive la casilla de verificación **Herramienta cambio tasa IVA finalizada**. La casilla de verificación se selecciona automáticamente cuando la conversión de cambio de tasa de IVA se completa.  

4. Seleccione la acción **Convertir**.  
5. Después de que la conversión esté completa, elija la acción **Movs. reg. de cambio de tasa de IVA** para ver los resultados de la conversión.  

> [!IMPORTANT]  
>  Después de la conversión, el campo **Convertido** en la tabla **Mov. registro cambios en tasa IVA** queda seleccionado y el campo **Fecha conversión** en la tabla **Mov. registro cambios en tasa IVA** muestra la fecha de conversión.  
## <a name="see-also"></a>Consulte también  
[Configurar el impuesto sobre el valor añadido](finance-setup-vat.md)  
[Configuración del impuesto sobre el valor añadido no realizado](finance-setup-unrealized-vat.md)      
[Crear informes de IVA para la autoridad fiscal](finance-how-report-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Funcionalidad local en Business Central](about-localization.md)
