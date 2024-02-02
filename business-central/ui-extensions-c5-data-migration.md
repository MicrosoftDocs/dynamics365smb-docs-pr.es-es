---
title: Usar la extensión de migración de datos C5 | Microsoft Docs
description: 'Utilice esta extensión para migrar clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'extension, migrate, data, C5, import'
ms.search.form: '1860, 1861, 1862, 1863, 1864, 1867, 1868, 1869, 1874, 1882, 1883, 1884, 1885, 1886, 1888, 1890, 1891, 1892, 1893, 1894, 1898, 1899, 1900, 1901, 1902, 1903, 1904, 1905, 1906'
ms.date: 12/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Extensión de migración de datos de C5

Esta extensión facilita la migración de clientes, proveedores, productos y las cuentas de contabilidad de Microsoft Dynamics C5 2012 a [!INCLUDE[prod_short](includes/prod_short.md)]. También puede migrar los movimientos históricos para cuentas de contabilidad.

> [!NOTE]
> La empresa en [!INCLUDE[prod_short](includes/prod_short.md)] no debe contener ningún dato. Además, después de iniciar una migración, no debe crear clientes, proveedores, artículos ni cuentas hasta que la finalice.

## ¿Qué datos se migran?

Se migran los datos siguientes para cada entidad:

### Clientes

* Contactos  
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

### Proveedores

* Contactos
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

### Productos

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
* L.M. de ensamblado

Si migra cuentas, los datos siguientes también se migrarán:

* Configuración contable inventario
* Configuración grupos contables
* Sección diario producto
* Abra transacciones (movimientos de productos)

> [!NOTE]
> Si hay transacciones abiertas que usan divisas extranjeras, las tasas de cambio para esas divisas también se migran. Otros tipos de cambio no se migran.

### Plan de cuentas

* Dimensiones estándar: departamento, centro de coste, propósito  
* Transacciones históricas de contabilidad  

> [!NOTE]
> Las transacciones históricas de contabilidad se gestionan de un modo un poco diferente. Al migrar datos se establece un parámetro **Periodo actual**. Este parámetro especifica cómo procesar transacciones de contabilidad. Las transacciones después de esta fecha se migran por separado. Las transacciones anteriores a esta fecha se agregan por cuenta y se migran como un único importe. Por ejemplo, supongamos que hay transacciones en 2015, 2016, 2017 y 2018, y especifica el 1 de enero de 2017 en el campo Período actual. Para cada cuenta, los importes de las transacciones del 31 de diciembre de 2106 o anteriores se agregarán en una sola línea de diario general para cada cuenta de contabilidad. Todas las transacciones después de esta fecha se migrarán por separado.

## Requisitos de tamaño del archivo

El tamaño máximo del archivo que puede descargar en [!INCLUDE[prod_short](includes/prod_short.md)] es de 150 MB. Si el archivo que se exporta de C5 es más grande, tenga en cuenta migrar datos en varios archivos. Por ejemplo, exporte uno o dos tipos de entidades de C5, como clientes y proveedores, a un archivo y luego exporte los elementos a otro archivo, y así sucesivamente. Puede importar archivos individualmente en [!INCLUDE[prod_short](includes/prod_short.md)].

## Para migrar datos

Deben realizarse algunos para exportar datos de la C5 e importarlos a [!INCLUDE[prod_short](includes/prod_short.md)]:  

1. En la C5, utilice la función **Base de datos de exportación** para exportar los datos. Envíe la carpeta de exportación a una carpeta comprimida.  
2. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Migración de datos** y luego elige **Migración de datos**.  
3. Complete los pasos de la guía de configuración asistida. Asegúrese de elegir **Importar de Microsoft Dynamics C5 2012** como origen de datos.  

## Ver el estado de la migración

Utilice la página **Información general sobre migración de datos** para controlar el éxito de la migración. La página muestra información como el número de entidades que la migración incluye, el estado de la migración, el número de elementos que se han migrado y si lo han hecho correctamente. También muestra la cantidad de errores, lo que le permite investigar qué salió mal y, cuando es posible, facilita ir a la entidad para solucionar los problemas. Para obtener más información, consulte la siguiente sección de este artículo.  

> [!NOTE]
> Mientras espera los resultados de la migración, debe actualizar la página para mostrarlos.

## Cómo evitar el doble registro

Para ayudar a evitar el registro doble en la contabilidad, se utilizan las siguientes cuentas de saldo para las transacciones abiertas:  

* Para los proveedores, usamos la cuenta de A/P del grupo de publicación del proveedor.  
* Para los clientes, usamos la cuenta de A/R del grupo de publicación del cliente.  
* Para los elementos, creamos una configuración general de contabilización donde la cuenta de ajuste es la cuenta especificada como cuenta de inventario en la configuración de contabilización del inventario.  

## Corrección de errores

Si algo sale mal y se produce un error, el campo **Estado** muestra **Completado con errores** y el campo **Recuento de errores** mostrará cuántos. Para ver una lista de los errores, puede abrir la página **Errores de migración de datos** si elige:  

* El número en el campo **Recuento de errores** de la entidad.  
* La entidad y la acción **Mostrar errores**.  

En la página **Errores de migración de datos**, para corregir un error puede elegir un mensaje de error y seleccionar **Editar registro** para ver los datos migrados de la entidad. Si tiene varios errores a corregir, puede elegir **Corrección masiva de errores** para modificar las entidades de una lista. Aun así, debe abrir registros individuales si el error lo causó una entrada relacionada. Por ejemplo, un proveedor no se migrará si una dirección de correo electrónico a uno de sus contactos tiene un formato no válido.

Después de corregir uno o más errores, puede elegir **Migrar** para migrar solo las entidades que reparó, sin tener que reiniciar por completo la migración.  

> [!TIP]
> Si ha solucionado más de un error, puede usar la función **Seleccionar más** para seleccionar varias líneas para migrar. De forma alternativa, si hay errores que no son importantes para solucionar, puede elegirlos y seleccionar **Omitir selecciones**.

> [!NOTE]
> Si tiene elementos que se incluyen en una lista de materiales, es posible que tenga que migrar más de una vez si el elemento original no se crea antes de las variantes que le hacen referencia. Si primero se crea una variante del elemento, la referencia al elemento original puede provocar un mensaje de error.  

## Comprobar los datos después de la migración

Un modo de comprobar que los datos se han migrado correctamente es mirar las páginas siguientes en la C5 y [!INCLUDE[prod_short](includes/prod_short.md)].

|Microsoft Dynamics C5 2012 | Dynamics 365 Business Central| Trabajo por lotes para utilizar |
|---------------------------|------------------------------|------------------|
|Movimientos de cliente| Diarios generales| CUSTMIGR |
|Movimientos de proveedor| Diarios generales| VENDMIGR|
|Movs. prods.| Diarios de artículos| ITEMMIGR |
|Movimientos de contabilidad| Diarios generales| GLACMIGR |

## Detener la migración de datos

Puede detener la migración de datos con la opción **Detener todas las migraciones**. Si utiliza esta opción, todas las migraciones pendientes también se detendrán.

## Consulte también .

[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
