---
title: Creación del informe 340 [ES]
description: Lea sobre cómo crear el informe 340 para las autoridades fiscales en la versión en español de Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/21/2021
ms.author: edupont
ms.openlocfilehash: 72cda0e0ee088853b27a9e3bb48806b61dc4a7ef
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437519"
---
# <a name="create-report-340-in-the-spanish-version"></a>Crear informe 340 en la versión en español
El Informe 340 incluye todas las facturas de compras y ventas que registra una empresa durante un periodo determinado. El informe también incluye los códigos de operación con impuestos y pagos en efectivo relacionados.  

Este informe se genera en un formato que ha aprobado la administración fiscal. Debe presentar este informe en una periodicidad mensual o trimestral, en función del tamaño de la empresa.  

## <a name="to-create-report-340"></a>Para crear el informe 340  

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Modelo 340** y luego elija el enlace relacionado.  
2.  En la ficha desplegable **Opciones** de la página **Modelo 340**, rellene los campos tal y como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ejercicio**|Escriba el año fiscal para el que desea crear la declaración de la operación.|  
    |**Mes**|Seleccione el mes que desea incluir en la declaración.|  
    |**Importe pago mín.**|Escriba el importe que ha recibido en efectivo en la **Cuenta para pagos en efectivo** seleccionada. **Importante:** El campo está diseñado para realizar pagos en efectivo. El importe seleccionado decide la suma de los movimientos de cliente en el informe. Si el importe total facturado para un cliente por año es menor que el importe especificado en el campo, la suma de los movimientos de cliente no se incluye en el informe. Si el importe total facturado para un cliente por año es mayor que el importe especificado en el campo, la suma de los movimientos de cliente se incluye en el informe. Cuando exporte los datos a un archivo de declaración .txt, verá que el campo **Cantidad recibida en efectivo** en el archivo .txt de declaración contiene el importe acumulado de movimientos de clientes en una línea por año.|  
    |**Cuenta para pagos en efectivo**|Seleccione uno o más en cuentas de contabilidad para incluir solo los movimientos que se registran en cuentas de contabilidad filtradas en el informe. **Importante:** El campo está diseñado para realizar pagos en efectivo. Cuando exporte los datos a un archivo de declaración .txt, verá que el campo **Cantidad recibida en efectivo** en el archivo .txt de declaración contiene el valor acumulado para las cuentas seleccionadas. Si no selecciona ninguna cuenta contable, no se crearán líneas del tipo 2 para pagos en efectivo.|  
    |**Nombre contacto**|Introduzca el apellido y el nombre de la compañía que está creando la declaración de operaciones.|  
    |**Número de teléfono**|Introduzca el número de teléfono de la compañía que está creando la declaración de operaciones.|  
    |**Grupos reg. prod. gen. no deduc.**|Seleccione el grupo contable de producto. Los grupos de registro seleccionados se consideran como IVA no deducible.|  
    |**Nº modelo**|Introduzca el número para identificar la declaración de operaciones.|  
    |**Código electrónico**|Especifique el código electrónico que proporciona la administración fiscal.|  
    |**Tipo de medio modelo**|Seleccione el tipo de medio del modelo.|  
    |**Modelo de sustitución**|Seleccione si se trata de una sustitución de una declaración anteriormente registrada.|  
    |**Número de modelo anterior**|Escriba el número de modelo anterior si la opción **Modelo de sustitución** está activada.|  

3.  Seleccione los filtros apropiados y, a continuación, elija el botón **Aceptar**. Se creará el archivo de texto del Informe 340 en la ruta especificada.  

## <a name="to-create-a-modelo-340-report-under-the-cac-regimen"></a>Para crear un informe de Modelo 340 en de régimen CAC  

1.  Realice los pasos del procedimiento anterior.  
2.  Según sea necesario, ajuste y modifique la información del código de operación. Para que el informe pase la validación cuando lo envíe a la administración fiscal, las líneas que tengan un pago no realizado deben actualizarse e incluir un código de operación. Puede cambiar el código de operación de Z o 3 a Z o 1 – 8 solo para los pagos en efectivo.  
3.  Elija el botón **Aceptar**. El informe se exporta a la ubicación de archivo que especifique. El informe solo contiene las líneas de facturas, abonos, liquidados o no, y los pagos que tienen el IVA no realizado.  

    Las facturas se exportarán y contendrán el código de operación Z. Los datos de la colección están en blanco.  

    Los pagos contra una factura se exportarán y contendrán los datos de cobro.  

Si imprime el documento registrado, por ejemplo, una factura de venta registrada, éste incluirá la etiqueta siguiente: **Régimen especial del criterio de caja**.  

## <a name="see-also"></a>Consulte también  
 [Informe 340](report-340.md)   
 [Pagos en efectivo](payments-in-cash.md)   
 [Agencia Tributaria](https://www.agenciatributaria.es/AEAT.internet/en_gb/Inicio.shtml)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]