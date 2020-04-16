---
title: Configuración de grupos contables | Documentos de Microsoft
description: Resumen de los grupos contables que puede utilizar para ahorrar tiempo y evitar errores al registrar transacciones.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: c4e8f197635606be92584de64b8e81945dae2376
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182953"
---
# <a name="setting-up-posting-groups"></a>Configurar los grupos contables
Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. Ahorran tiempo y ayudan a evitar errores al registrar las transacciones. Los valores de transacción se envían a las cuentas especificadas en el grupo contable de dicha entidad. El único requisito es que tenga un plan de cuentas. Para obtener más información, vea [Configuración del plan de cuentas](finance-setup-chart-accounts.md).  

Los grupos contables tienen tres divisiones:  

* General: defina a quién vende y de quién compra, y lo que vende y compra. También puede combinar grupos para especificar aspectos como las cuentas de regularización para registrar, o usar grupos para filtrar informes.  
* Específico: use documentos de ventas, por ejemplo, en lugar de registrar movimientos directamente en contabilidad. Al crear movimientos de clientes, en contabilidad se crean los movimientos correspondientes.  
* Impuesto: defina los porcentajes de impuestos y los tipos de cálculo que se aplican a quién se vende y de quién se compra, y a lo que vende y compra.

Las tablas siguientes describen los grupos contables con cada división.  

| Grupos contables | Descripción |
| --- | --- |
| Grupos contables negocio |Asigne este grupo a proveedores y clientes para especificar a quién vende y de quién compra. Configúrelos en la página **Grupos contables negocio**. Al hacerlo, piense en cuántos grupos necesita para desglosar las ventas y las compras. Por ejemplo, agrupe clientes y proveedores por área geográfica, o el tipo de negocio. |
| Grupos contables de producto |Asigne este grupo a productos y recursos para especificar lo que vende y lo que compra. Configúrelos en la página **Grupos registro producto gen.**. Al hacerlo, considere el número de grupos que necesitará para desglosar las ventas por producto (productos y recursos) y las compras por producto. Por ejemplo, divida estos grupos por materias primas, mercaderías, recursos, capacidad, etc. |
| Configuraciones grupos contables |Combine grupos contables de negocio y de producto, y seleccione las cuentas en las que se registrarán. Para cada combinación de grupos contables de negocios y productos, puede asignar un conjunto de cuentas de contabilidad. Por ejemplo, esto significa que puede registrar la venta del mismo producto en diferentes cuentas de ventas en la contabilidad porque varios clientes se asignan a diferentes grupos contables de negocio. Configúrelos en la página **Configuración grupos contables**. |

| Grupos contables concretos | Description |
| --- | --- |
| Grupos registro cliente |Defina las cuentas que usará al enviar transacciones de cobros. Si usa existencias y cobros, el grupo contable de negocio general asignado al cliente y el grupo contable de producto general asignado al producto de existencias determinan las cuentas en las que se registran las líneas de pedido de ventas. Consulte "Grupos contables negocio" y "Grupos contables de producto general" en el campo superior **Grupos contables**. Configúrelos en la página **Grupos contables clientes**. |
| Grupos registro proveedor |Defina dónde registrar las transacciones de las cuentas de pagos, las cuentas de servicios y las cuentas de descuentos. Esto es similar a los grupos contables de cliente. Configúrelos en la página **Grupos contables proveedores**. |
| Grupos registro inventario |Defina los grupos de registro de inventario que luego asignará a las cuentas de productos relevantes en la página **Config. registro inventario**. De este modo, al registrar movimientos relativos a un producto, el sistema registrará en la cuenta configurada para la combinación de grupo contable de existencias y almacén asociada al producto. Además, los grupos contables de existencias constituyen una forma ideal de organizar las existencias,de modo que al generar informes, puede dividir los productos por grupo contable. Configúrelos en la página **Grupos contables existencias**. |
| Grupos registro cuenta bancaria |Defina las cuentas de las cuentas bancarias. Por ejemplo, esto puede simplificar los procesos de seguimiento de las transacciones y de conciliación de cuentas bancarias. Configúrelos en la página **Grupos contables bancos**. |
| Grupos contables de activos fijos |Defina las cuentas para diferentes tipos de gastos y costes, como los costes de adquisición, los importes de amortización acumulados, los costes de adquisición en venta/baja, la amortización acumulada en baja, la ganancia en venta/baja, la pérdida en venta/baja, los gastos de mantenimiento y los gastos de amortización. Configúrelos en la página **Grupos registro A/F**. |

| Grupo contable impuesto | Description |
| --- | --- |
| Grupos contables negocio impuesto |Determine cómo calcular y registrar el impuesto de venta para clientes y proveedores. Configúrelos en la página **Grupos contables negocio impuesto**. Al hacerlo, piense en cuántos grupos necesita. Por ejemplo, esto puede depender de factores como la legislación local y si la actividad económica de la empresa es tanto nacional como internacional. |
| Grupos contables productos impuesto |Indique los cálculos de impuesto necesarios para los tipos de productos o recursos que compre o venda. |
| Configuración de registro impuesto |Combine grupos registro IVA negocio y grupos registro IVA producto. Cuando rellene una línea de diario general, línea de compra o línea de venta, examinaremos la combinación para identificar las cuentas que se deben usar. |

## <a name="example-of-linking-posting-groups"></a>Ejemplo de grupos contables de vinculación
A continuación presentamos un ejemplo.  

Estos grupos contables están elegidos en la ficha cliente:  

* Grupo contable de negocio general
* Grupo contable cliente  

Estos grupos contables están elegidos en la ficha producto:  

* Grupo contable de producto general  
* Grupo contable inventario  

Al crear un documento de ventas, el encabezado de ventas usa la información de la ficha cliente y las líneas de ventas usan la información de la ficha producto.  

* El registro de ingresos (comercial) se determina mediante la combinación del grupo contable de negocio general y el grupo contable de producto general.  
* El registro de cobros (balance) se determina mediante el grupo contable de cliente.  
* El registro de existencias (balance) se determina mediante el grupo contable de existencias.  
* El registro del coste de productos vendidos (comercial) se determina mediante la combinación del grupo contable de negocio general y el grupo contable de producto.  

La configuración determina cuándo se realiza el registro. Por ejemplo, el tiempo se ve afectado por el momento en que realiza actividades periódicas, como registrar el coste de inventario o ajustar los movimientos de producto de coste.

## <a name="copying-posting-setup-lines"></a>Copiar líneas de configuración de grupos contables
Cuantos más grupos contables de producto y de negocio tenga, más líneas habrá en la página Configuración grupos contables. Ello podría conllevar la introducción de muchos datos para configurar los grupos contables de la empresa. Si bien puede haber muchas combinaciones distintas de grupos contables de negocio y de producto, las distintas combinaciones podrían crear registros en las mismas cuentas de contabilidad. Para limitar la introducción manual de los datos, copie las cuentas de contabilidad de una línea existente en la página **Configuración grupos contables**.

## <a name="see-also"></a>Consulte también .
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
