---
title: Administración de los cambios en el tipo de IVA | Microsoft Docs
description: Aprenda cómo utilizarla la herramienta de cambio del tipo de IVA para Dynamics 365 Business Central.
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.workload: na
ms.search.keywords: VAT, VAT rate, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 7d75cb42b064f8541a1142ef149c9641baa6f69a
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923925"
---
# <a name="managing-vat-rate-changes"></a>Administración de cambios del tipo de IVA

Los tipos de IVA pueden cambiar según la legislación local. Cualquier cambio en el IVA afecta a sus datos en [!INCLUDE[d365fin](includes/d365fin_md.md)] si el tipo de IVA baja, aumenta o se elimina. El IVA está conectado a muchas entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)], como clientes, proveedores, productos, recursos, cargos de producto y cuentas de contabilidad. Los cambios en los tipos de IVA generalmente ocurren en una fecha específica, a partir de la cual deberá haber cambiado la configuración del IVA, los grupos contables, etc. para asegurarse de que se creen nuevos pedidos de ventas y de compras con el nuevo tipo de IVA.

## <a name="changing-vat-rates"></a>Cambio de los tipos de IVA

El enfoque óptimo para administrar un cambio en el tipo de IVA es publicar y cerrar completamente los pedidos abiertos y otros documentos antes de la fecha de cambio del tipo de IVA, para asegurarse de que el cambio no les afecte. Este es el enfoque más claro que le permite iniciar nuevos pedidos y documentos con el nuevo tipo de IVA.

Se sugiere el siguiente enfoque para administrar un cambio en el tipo de IVA

1. Publique y cierre pedidos abiertos, diarios y otros documentos antes de la fecha de cambio. Puede esperar hasta después de la fecha de cambio siempre que no agregue nuevas líneas y asegúrese de que la fecha de vigencia sea anterior a la fecha de cambio.  
2. Cree la nueva configuración del IVA.  
3. Efectúe el cambio del IVA en las entidades (clientes relevantes, proveedores, artículos, etc.).  
4. En la fecha de cambio del tipo de IVA, cree nuevos documentos que utilicen la nueva tasa.  


> [!NOTE]  
> Actualmente estamos actualizando la herramienta de cambio del tipo de IVA. La funcionalidad mencionada a continuación puede no coincidir con la funcionalidad de su entorno. La actualización tendrá lugar antes del 1 de julio de 2020 y no será una actualización mensual regular. En cambio, todos los entornos se actualizarán automáticamente (revisión). Cuando se complete esta actualización, este mensaje ya no aparecerá.  

## <a name="the-vat-rate-change-tool"></a>La herramienta de cambio del tipo de IVA

La herramienta de cambio del tipo de IVA puede ayudar con la conversión de tipos de IVA en datos maestros, diarios y pedidos, hasta cierto punto. Esto es útil si desea convertir el IVA en datos maestros más fácilmente o si tiene pedidos que no puede cerrar antes de la fecha de cambio y se procesarán durante un período de tiempo más largo, superando la fecha de cambio del tipo de IVA. Existen ciertas restricciones y limitaciones en la herramienta de cambio del tipo de IVA que se aplica.

## <a name="understanding-the-vat-rate-conversion-process-and-limitations"></a>Conocer el proceso y limitaciones de la conversión del tipo de IVA

La herramienta de cambio del tipo de IVA realiza conversiones de tipo de IVA para datos maestros, diarios y pedidos en distintas formas. Los datos maestros y los diarios seleccionados se actualizarán por el nuevo grupo de registro del producto general o de IVA. Si un pedido ha sido total o parcialmente enviado, los productos enviados guardarán el grupo de registro de producto general actual o grupo de registro de IVA de producto. Una nueva línea de pedido se creará para los productos no enviados y se actualizará para alinear grupos de registro de producto generales o de IVA nuevos y actuales. Además, se actualizarán según corresponda asignaciones de cargo de producto, platillas de configuración para productos, reservas y la información de seguimiento de producto. 

En las líneas de pedido, el precio unitario se actualizará para todas las líneas de tipo de producto y recurso, si se utilizan precios con IVA incluido para el artículo. Para otros tipos de línea, es posible decidir si el precio unitario se debe actualizar o no.

Existen algunos parámetros que la herramienta no convierte:

* Pedidos de venta o de compra y facturas donde se hayan registrado envíos. Estos documentos se registran con la tasa de IVA actual.  
* Documentos que tienen facturas de prepago registradas. Por ejemplo, ha creado o recibido prepagos en facturas que no se han rellenado antes de utilizar la herramienta de cambio de tasa de IVA. En este caso, habrá una diferencia entre el IVA pendiente y el IVA abonado en los prepagos cuando la factura se completa. La herramienta de cambio de tasa de IVA omitirá estos documentos y tendrá que actualizarlos manualmente.  
* Pedidos de compra o de venta con integración de almacén si se envían o se reciben parcialmente.  
* Envíos directos.
* Pedidos especiales. 
* Pedidos de ensamblado.
* Contratos de servicio.  
* Abonos.
* Devoluciones.
* Precios de productos (datos maestros)
* Precios sobre precios de venta (datos maestros)
* Grupos contables empresariales en clientes y proveedores.

### <a name="to-prepare-vat-rate-change-conversions"></a>Para preparar conversiones de cambio de tasa de IVA

Antes de configurar la herramienta de cambio de tasa de IVA, debe llevar a cabo estos pasos.

* Si mantiene transacciones que utilizan distintas tasas, entonces deben separarse en diferentes grupos creando nuevas cuentas contables por cada tasa o bien utilizando filtros de datos para agrupar transacciones según la tasa.  
* Si crea nuevas cuentas de contabilidad, deberá crear nuevos grupos contables.  
* Para reducir el número de documentos que se convierten, registre tantos documentos como sea posible y reduzca a un mínimo los documentos sin registrar.  
* Copia de seguridad de datos.

### <a name="to-set-up-the-vat-rate-change-tool"></a>Para configurar la herramienta de cambio de tasa de IVA

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conf. cambio tipo IVA** y luego elija el enlace relacionado.  
2. En las fichas desplegables **Datos maestros**, **Diarios** y **Documentos**, elija un valor de grupo contable de la lista de opciones para los campos necesarios. Para cada grupo, puede elegir si desea convertir grupos de registro IVA de producto o grupos de contabilización de productos generales, o convertir ambos valores si están disponibles en el elemento de datos maestros. Para algunas áreas, también puede establecer un filtro para convertir solo un subconjunto de valores, por ejemplo, cuentas. 
3. En la ficha desplegable **Precios IVA incluido**, elija para qué tipos de línea en los pedidos desea actualizar los precios unitarios. Los precios unitarios en las líneas de tipo producto y recurso siempre se actualizarán.

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
> Antes de realizar la conversión de cambio del tipo de IVA, puede probarla. Para hacerlo, siga los pasos siguientes, pero asegúrese de desactivar las casillas de verificación **Realizar conversión** y **Herramienta cambio tasa IVA finalizada**. Durante la conversión de prueba, el campo **Convertido** en la tabla **Mov. registro cambios en tasa IVA** está desactivada y el campo **Fecha conversión** en la tabla **Mov. registro cambios en tasa IVA** está vacío. Después de que la conversión esté completa, elija **Movs. reg. de cambio de tasa de IVA** para ver los resultados de la prueba. Verifique cada movimiento antes de realizar la conversión. Concretamente, verifique las transacciones que utilizan una tasa de IVA antigua.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Conf. cambio tipo IVA** y luego elija el enlace **Conf. cambio tasa IVA**.  
2. Compruebe que haya configurado la conversión del grupo de registro de IVA de producto o la conversión del grupo de registro general de producto.  
3. Elija la casilla de verificación **Realizar conversión**.  

    > [!IMPORTANT]  
    >  Desactive la casilla de verificación **Herramienta cambio tasa IVA finalizada**. La casilla de verificación se selecciona automáticamente cuando la conversión de cambio de tasa de IVA se completa.  

4. Seleccione la acción **Convertir**.  
5. Después de que la conversión esté completa, elija la acción **Movs. reg. de cambio de tasa de IVA** para ver los resultados de la conversión.  

> [!IMPORTANT]  
> Después de la conversión, el campo **Convertido** en la tabla **Mov. registro cambios en tasa IVA** queda seleccionado y el campo **Fecha conversión** en la tabla **Mov. registro cambios en tasa IVA** muestra la fecha de conversión.  

## <a name="see-also"></a>Consulte también

[Configurar el impuesto sobre el valor añadido](finance-setup-vat.md)  
[Configuración del impuesto sobre el valor añadido no realizado](finance-setup-unrealized-vat.md)  
[Crear informes de IVA para la autoridad fiscal](finance-how-report-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Funcionalidad local en Business Central](about-localization.md)  
