---
title: Configuración de grupo contable
description: Resumen de los grupos contables que puede utilizar para ahorrar tiempo y evitar errores al registrar transacciones.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.search.form: 312, 313
ms.date: 01/24/2022
ms.author: bholtorf
ms.openlocfilehash: e44181c8206662b8dee7899a23b49b7f0cb9df57
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381780"
---
# <a name="set-up-posting-groups"></a>Configurar los grupos contables de activos

Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. Ahorran tiempo y ayudan a evitar errores al registrar las transacciones. Los valores de transacción se envían a las cuentas especificadas en el grupo contable de dicha entidad. El único requisito es que tenga un plan de cuentas. Para obtener más información, vea [Configuración del plan de cuentas](finance-setup-chart-accounts.md).  

Los grupos contables tienen tres divisiones:  

* General: defina a quién vende y de quién compra, y lo que vende y compra. También puede combinar grupos para especificar aspectos como las cuentas de regularización para registrar, o usar grupos para filtrar informes.  
* Específico: use documentos de ventas, por ejemplo, en lugar de registrar movimientos directamente en contabilidad. Al crear movimientos de clientes, en contabilidad se crean los movimientos correspondientes.  
* Impuesto: defina los porcentajes de impuestos y los tipos de cálculo que se aplican a quién se vende y de quién se compra, y a lo que vende y compra.

Las secciones siguientes describen los grupos contables con cada división.  

## <a name="general-posting-groups"></a>Grupos contables

La tabla siguiente describe los grupos contables generales.

| Escriba | Descripción |
| --- | --- |
| Grupos contables negocio |Asigne este grupo a proveedores y clientes para especificar a quién vende y de quién compra. Configúrelos en la página **Grupos contables negocio**. Al hacerlo, piense en cuántos grupos necesita para desglosar las ventas y las compras. Por ejemplo, agrupe clientes y proveedores por área geográfica, o el tipo de negocio. |
| Grupos contables de producto |Asigne este grupo a productos y recursos para especificar lo que vende y lo que compra. Configúrelos en la página **Grupos registro producto gen.**. Al hacerlo, considere el número de grupos que necesitará para desglosar las ventas por producto (productos y recursos) y las compras por producto. Por ejemplo, divida estos grupos por materias primas, mercaderías, recursos, capacidad, etc. |
| Configuraciones grupos contables |Combine grupos contables de negocio y de producto, y seleccione las cuentas en las que se registrarán. Para cada combinación de grupos contables de negocios y productos, puede asignar un conjunto de cuentas de contabilidad. Por ejemplo, esto significa que puede registrar la venta del mismo producto en diferentes cuentas de ventas en la contabilidad porque varios clientes se asignan a diferentes grupos contables de negocio. Configúrelos en la página **Configuración grupos contables**. |

## <a name="specific-posting-groups"></a>Grupos contables concretos

La siguiente tabla describe los grupos contables que son específicos de tipos de datos.

|Escriba | Descripción |
| --- | --- |
| Grupos registro cliente |Defina las cuentas que usará al enviar transacciones de cobros. Si usa existencias y cobros, el grupo contable de negocio general asignado al cliente y el grupo contable de producto general asignado al producto de existencias determinan las cuentas en las que se registran las líneas de pedido de ventas. Consulte *Grupos contables negocio* y *Grupos contables de producto general* en la sección [Grupos contables generales](#general-posting-groups). Configúrelos en la página **Grupos contables clientes**. |
| Grupos registro proveedor |Defina dónde registrar las transacciones de las cuentas de pagos, las cuentas de servicios y las cuentas de descuentos. Esto es similar a los grupos contables de cliente. Configúrelos en la página **Grupos contables proveedores**. |
| Grupos registro inventario |Defina los grupos de registro de inventario que luego asignará a las cuentas de productos relevantes en la página **Config. registro inventario**. De este modo, al registrar movimientos relativos a un producto, el sistema registrará en la cuenta configurada para la combinación de grupo contable de existencias y almacén asociada al producto. Además, los grupos contables de existencias constituyen una forma ideal de organizar las existencias,de modo que al generar informes, puede dividir los productos por grupo contable. Configúrelos en la página **Grupos contables existencias**. |
| Grupos registro cuenta bancaria |Define las cuentas contables en las que se publican las entradas de la cuenta de banco. Por ejemplo, esto puede simplificar los procesos de seguimiento de las transacciones y de conciliación de cuentas bancarias. Configúrelos en la página **Grupos contables bancos**. Recomendamos que estas cuentas de mayor tengan el campo **Publicación directa** campo establecido en *No*. |
| Grupos contables de activos fijos |Defina las cuentas para diferentes tipos de gastos y costes, como los costes de adquisición, los importes de amortización acumulados, los costes de adquisición en venta/baja, la amortización acumulada en baja, la ganancia en venta/baja, la pérdida en venta/baja, los gastos de mantenimiento y los gastos de amortización. Configúrelos en la página **Grupos registro A/F**. |

## <a name="tax-posting-groups"></a>Grupos contables de impuestos

La tabla siguiente describe los grupos contables relacionados con los impuestos.

| Escriba | Descripción |
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

## <a name="set-up-posting-groups-on-the-go"></a>Configurar grupos contables sobre la marcha

Para que los usuarios comiencen más rápido, [!INCLUDE[prod_short](includes/prod_short.md)] ofrece asistencia a través de notificaciones de cuentas de contabilidad general que falten en varias configuraciones de grupos contables en documentos. Para recibir estas notificaciones, asegúrese de que la notificación **Cuenta C/G que falta en grupo de registro o configuración** está seleccionada en la página **Mis notificaciones**, a la que puede acceder desde el campo **Cambiar cuándo recibo notificaciones** en la página **Mi configuración**.  

De esta manera, cuando trabaje en un documento que usa un grupo contable o una configuración a la que le falta una cuenta de contabilidad general requerida, recibirá una notificación. Elija el vínculo en la notificación para abrir una página donde puede realizar los cambios relevantes, siempre que tenga permiso para hacerlo.  

> [!NOTE]
> Para llevarlo directamente al grupo contable o configuración al que le falta una cuenta de contabilidad general, [!INCLUDE[prod_short](includes/prod_short.md)] creará una configuración o grupo contable que servirá como marcador. Los grupos contables y las configuraciones son una forma para que el contable controle cómo se registran los movimientos en la contabilidad general, por lo que es posible que la creación al momento de grupos contables y configuraciones no esté permitida en su organización.  
> 
> En ese caso, desactive la notificación **Cuenta C/G que falta en grupo de registro o configuración** y, a continuación, trabaje con su contable para realizar los cambios relevantes en el grupo contable, la configuración o su documento. Este es un paso importante, porque una vez que se contabilizan los documentos, los grupos contables o configuraciones incorrectamente utilizados no se pueden eliminar porque se han creado movimientos de contabilidad general para ellos. 

## <a name="troubleshooting-posting-group-errors"></a>Solución de problemas de errores de grupos de publicación

Los grupos de publicación son uno de los conceptos más avanzados para configurar en [!INCLUDE[prod_short](includes/prod_short.md)]. Si no están configurados correctamente, pueden ocurrir errores al registrar documentos o líneas de diario. Por ejemplo, estos errores generalmente se deben a un error en cómo se asignan las cuentas de contabilidad o en cómo se combinan los grupos de registro.

Cuando algo anda mal, [!INCLUDE[prod_short](includes/prod_short.md)] mostrará la página **Mensajes de error**. La página **Mensajes de error** puede facilitar la identificación y resolución del problema. La página ofrece una descripción del error que señala la configuración del grupo de publicación que necesita atención. Por ejemplo, el mensaje podría ser "A la cuenta de prepago de ventas le falta una configuración de registro general". También hay un enlace para abrir la página que es la fuente del problema para que pueda resolverlo rápidamente.  

> [!NOTE]
> El manejo de errores descrito anteriormente no está disponible en diarios de artículos, recursos, empleados y activos fijos, ni para cuentas de contabilidad agregadas en versiones locales de grupos de registro.

## <a name="see-also"></a>Consulte también .
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
