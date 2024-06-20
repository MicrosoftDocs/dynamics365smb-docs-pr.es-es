---
title: Análisis ad-hoc en compras
description: Aprenda a usar el modo de análisis de datos para analizar datos en compras.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analyses-in-purchasing"></a>Análisis ad-hoc en compras

Este artículo explica cómo analizar los datos de compra de las páginas de listas y consultas utilizando la característica **Análisis de datos**. Esta característica le permite analizar los datos directamente desde la página, sin tener que ejecutar un informe o abrir otra aplicación, como Excel. El análisis de datos proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Mis proveedores" o "Estadísticas de compras", o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

Utilice las siguientes páginas de lista para análisis ad hoc de procesos de compras:

- [Pedidos de compra](https://businesscentral.dynamics.com/?page=9307)
- [Líns. compra](https://businesscentral.dynamics.com/?page=518)
- [Histórico facturas compra](https://businesscentral.dynamics.com/?page=146)
- [Movs. proveedores](https://businesscentral.dynamics.com/?page=29)
- [Movs. contabilidad](https://businesscentral.dynamics.com/?page=20)

## <a name="ad-hoc-analysis-scenarios-for-purchasing"></a>Escenarios de análisis ad hoc para compras

Utilice la característica **Análisis de datos** para una verificación rápida de hechos y un análisis ad hoc:

- Si no desea ejecutar un informe
- Si no existe un informe para sus necesidades específicas
- Si desea iterar rápidamente para obtener una buena descripción general de una parte de su negocio.

Las siguientes secciones proporcionan ejemplos de escenarios de compras en [!INCLUDE [prod_short](includes/prod_short.md)].

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [Información general de GRNI](#example-goods-received-not-invoiced-grni-overview) | Obtenga una descripción general de los productos recibidos, no facturados (GRNI) de todos los proveedores. | [Líns. compra](https://businesscentral.dynamics.com/?page=518) | **Tipo**, **Imt. Rec. No facturado (LCY)** (filtrar en estos campos), **N.º de proveedor**, **N.º de documento**, **N.º** y **Imt. Rec. No facturado (LCY)** <br><br> **NOTA:** Debe personalizar la página para agregar estos campos. Para obtener más información, vaya a [Personalizar el área de trabajo](ui-personalization-user.md). | 
| [Finance (Proveedores)](#example-finance-accounts-payable) | Vea lo que debe a sus proveedores, quizás desglosado en intervalos de tiempo para saber cuándo vencen los importes. | [Movs. proveedores](https://businesscentral.dynamics.com/?page=29) | **Nombre del proveedor**, **Tipo de documento**, **N.º de documento**, **Año de fecha de vencimiento**, **Mes de fecha de vencimiento** e **Importe restante**. |

## <a name="example-goods-received-not-invoiced-grni-overview"></a>Ejemplo: descripción general de los productos recibidos, no facturados (GRNI)

Para crear una descripción general de productos recibidos, no facturados (GRNI) entre proveedores, siga estos pasos:

1. Abra la página de lista [Pedidos de compra](https://businesscentral.dynamics.com/?page=518).
1. Personalice la página para agregar el campo **Importe recibido no facturado**. Para personalizar la página, elija **Configuración** y luego **Personalizar**.
1. Elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. En el menú **Filtros adicionales** (ubicado debajo del menú **Columnas** a la derecha), establezca los siguientes filtros:
    - **Tipo = Producto**
    - **Imt. Rec. No facturado (LCY) > 0**. 
1. Arrastre el **N.º de proveedor**, **N.º de documento** y el **N.º.** al área **Grupos de filas**. Arrastra los campos en ese orden.
1. Agregue el campo **Amt. Rec. No facturado (LCY)** para incluirlo en la descripción general.
1. Para hacer el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros de análisis**. El menú está a la derecha de la página, justo debajo del menú **Columnas**.
1. Cambie el nombre de su pestaña de análisis a **Productos recibidos, no facturados (GRNI)** o algo que describa este análisis.

## <a name="example-finance-accounts-payable"></a>Ejemplo: Finance (Proveedores)

Para ver lo que debe a sus proveedores, quizás desglosado en intervalos de tiempo para saber cuándo vencen los importes, siga estos pasos:

1. Abre la página de lista [Movimientos de proveedor](https://businesscentral.dynamics.com/?page=29) y active el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Active la opción **Modo dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre los campos **Nombre del proveedor**, **Tipo de documento** y **N.º de documento** al área **Grupos de filas** y luego arrastre el campo **Importe restante** al área **Valores**.
1. Arrastre los campos **Año de fecha de vencimiento** y **Mes de fecha de vencimiento** al área **Etiquetas de columna**. Arrastra los campos en ese orden.
1. Para realizar el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros de análisis** (ubicado debajo del menú **Columnas** de la derecha).
1. Cambie el nombre de su pestaña de análisis a **Antigüedad de pagos por mes** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en la página Movimientos de cliente" lightbox="media/data-analysis-vendor-ledger-entries.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-purchasing"></a>Base de datos para análisis ad hoc de compras

Cuando registra un documento de compra, [!INCLUDE [prod_short](includes/prod_short.md)] actualiza la cuenta del proveedor, la contabilidad, los movimientos de producto y los movimientos de recursos:

- Por cada documento de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. suministrador** y un movimiento de contabilidad en la correspondiente cuenta de pagos. Además, el registro de la compra podría dar como resultado un movimiento del impuesto sobre el valor añadido (IVA) y uno de contabilidad para el importe de descuento.

- Para cada línea de compra, en su caso, se crearán entradas en:
  - Tabla **Mov. producto**, si la línea de compra es de tipo Producto.
  - Tabla **Mov. contabilidad**, si la línea de compra es de tipo Cuenta.
  - Tabla **Movimiento de recurso**, si la línea de compra es de tipo Recurso.
- Además, los documentos de compra siempre se registran en las tablas **Histórico cab. albarán compra** e **Histórico cab. factura compra**.

Obtenga más información, vaya a [Registrar compras](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Consulte también

[Registrar compras](purchasing-how-record-purchases.md#posting-purchases)  
[Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Información general de compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
