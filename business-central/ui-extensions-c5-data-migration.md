---
title: "Usar la extensión de migración de datos C5 | Documentos de Microsoft"
description: "Utilice esta extensión para migrar clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: es-es
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a>Extensión de la migración de datos de C5 para Business Central
Esta extensión facilita la migración de clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a [!INCLUDE[d365fin](includes/d365fin_md.md)]. También puede migrar los movimientos históricos para cuentas de contabilidad.

> [!Note]
> La empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)] no debe contener ningún dato. Además, después de iniciar una migración, no debe crear clientes, proveedores, artículos ni cuentas hasta que la finalice.

## <a name="what-data-is-migrated"></a>¿Qué datos se migran?
Se migran los datos siguientes para cada entidad:

**Clientes**
* Lugar
* País
* Dimensiones de cliente (departamento, centro, propósito)
* Condiciones de envío
* Vendedor
* Condiciones de pago
* Forma pago
* Grupo precio cliente
* Descuento de la factura del cliente

Si migra cuentas, los datos siguientes también se migrarán:

* Configuración contable cliente
* Lote diario general
* Transacciones abiertas (movimientos de cliente)

**Proveedores**
* Lugar
* País
* Dimensiones de proveedor (departamento, centro, propósito)
* Descuento en factura
* Condiciones de envío
* Comprador
* Condiciones de pago
* Forma pago
* Descuento de factura del proveedor

Si migra cuentas, los datos siguientes también se migrarán:

* Configuración contable proveedor
* Lote diario general
* Abra transacciones (movimientos de proveedores)

**Productos**
* Lugar
* País
* Dimensiones de producto (departamento, centro, propósito)
* Descuentos línea de ventas
* Grupos descuento cliente
* Grupos descuento productos
* Precio venta
* Código arancelario
* Unidades de medida
* Código seguimiento producto
* Grupo precio cliente

Si migra cuentas, los datos siguientes también se migrarán:

* Configuración contable inventario
* Configuración grupos contables
* Sección diario producto
* Abra transacciones (movimientos de productos)

> [!Note]
> Si hay transacciones abiertas que usan divisas extranjeras, las tasas de cambio para esas divisas también se migran. Otros tipos de cambio no se migran.

**Plan de cuentas**  
* Dimensiones estándar: departamento, centro de coste, propósito  
* Transacciones históricas de contabilidad  

> [!Note]
> Las transacciones históricas de contabilidad se gestionan de un modo un poco diferente. Al migrar datos se establece un parámetro **Periodo actual**. Este parámetro especifica cómo procesar transacciones de contabilidad. Las transacciones después de esta fecha se migran por separado. Las transacciones anteriores a esta fecha se agregan por cuenta y se migran como un único importe. Por ejemplo, supongamos que hay transacciones en 2015, 2016, 2017 y 2018, y especifica el 1 de enero de 2017 en el campo Período actual. Para cada cuenta, los importes de las transacciones del 31 de diciembre de 2016 o anteriores se agregarán en una sola línea de diario general para cada cuenta de contabilidad. Todas las transacciones después de esta fecha se migrarán por separado.

## <a name="to-migrate-data"></a>Para migrar datos
Deben realizarse algunos para exportar datos de la C5 e importarlos a [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. En la C5, utilice la función **Base de datos de exportación** para exportar los datos. Envíe la carpeta de exportación a una carpeta comprimida.  
2. En [!INCLUDE[d365fin](includes/d365fin_md.md)], seleccione el ícono ![Buscar página o informe](media/ui-search/search_small.png "Buscar página o informe"), introduzca **Migración de datos** y, a continuación, seleccione **Migración de datos**.  
3. Complete los pasos de la guía de configuración asistida. Asegúrese de elegir **Importar de Microsoft Dynamcis C5 2012** como origen de datos.  

> [!Note]
> Las empresas a menudo agregan campos para personalizar la C5 para su línea de negocio específica. [!INCLUDE[d365fin](includes/d365fin_md.md)] no migra datos de campos personalizados. Además, la migración dará error si tiene más de 10 campos personalizados.

## <a name="viewing-the-status-of-the-migration"></a>Ver el estado de la migración
Utilice la página **Información general sobre migración de datos** para controlar el éxito de la migración. La página muestra información como el número de entidades que la migración incluirá, el estado de la migración, el número de elementos que se han migrado y si lo han hecho correctamente. También muestra la cantidad de errores, lo que le permite investigar qué salió mal y, cuando es posible, facilita ir a la entidad para solucionar los problemas. Para obtener más información, consulte la siguiente sección de este tema.  

> [!Note]
> Mientras espera los resultados de la migración, debe actualizar la página para mostrarlos.

## <a name="how-to-avoid-double-posting"></a>Cómo evitar el doble registro
Para ayudar a evitar el registro doble en la contabilidad, se utilizan las siguientes cuentas de saldo para las transacciones abiertas:  
  
* Para los proveedores, usamos la cuenta de A/P del grupo de publicación del proveedor.  
* Para los clientes, usamos la cuenta de A/R del grupo de publicación del cliente.  
* Para los elementos, creamos una configuración general de contabilización donde la cuenta de ajuste es la cuenta especificada como cuenta de inventario en la configuración de contabilización del inventario.  

## <a name="correcting-errors"></a>Corrección de errores
Si algo sale mal y se produce un error, el campo **Estado** mostrará **Completado con errores** y el campo **Recuento de errores** mostrará cuántos. Para ver una lista de los errores, puede abrir la página **Errores de migración de datos** si elige:  

* El número en el campo **Recuento de errores** de la entidad.  
* La entidad y la acción **Mostrar errores**.  

En la página **Errores de migración de datos**, para corregir un error puede elegir un mensaje de error y seleccionar **Editar registro** para abrir una página que muestre los datos migrados de la entidad. Después de corregir uno o más errores, puede elegir **Migrar** para migrar solo las entidades que reparó, sin tener que reiniciar por completo la migración.  

> [!Tip]
> Si ha solucionado más de un error, puede usar la función **Seleccionar más** para seleccionar varias líneas para migrar. De forma alternativa, si hay errores que no son importantes para solucionar, puede elegirlos y seleccionar **Omitir selecciones**.

> [!Note]
> Si tiene elementos que se incluyen en una lista de materiales, es posible que tenga que migrar más de una vez si el elemento original no se crea antes de las variantes que le hacen referencia. Si primero se crea una variante del elemento, la referencia al elemento original puede provocar un mensaje de error.  

## <a name="verifying-data-after-migrating"></a>Comprobar datos después de migrar
Un modo de comprobar que los datos se han migrado correctamente es mirar las páginas siguientes en la C5 y [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]| Trabajo por lotes para utilizar |
|-----|-----|-----|
|Movimientos de cliente| Diarios generales| CUSTMIGR |
|Movimientos de proveedor| Diarios generales| VENDMIGR|
|Movs. prods.| Diarios de productos| ITEMMIGR |
|Movimientos de contabilidad| Diarios generales| GLACMIGR |

## <a name="stopping-data-migration"></a>Detener la migración de datos
Puede detener la migración de datos con la opción **Detener todas las migraciones**. Si utiliza esta opción, todas las migraciones pendientes también se detendrán.

## <a name="see-also"></a>Consulte también
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)  
[Introducción](product-get-started.md) 

