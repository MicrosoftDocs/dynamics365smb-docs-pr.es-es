---
title: Exportar los datos de Business Central a Excel | Documentos de Microsoft
description: Puede exportar los informes financieros y los datos de inteligencia empresarial desde Business Central a Excel, o abrir los datos en Excel.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 01/13/2020
ms.author: edupont
ms.openlocfilehash: 1583c17b63df4c4db37eec20ab204ef235d47512
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2020
ms.locfileid: "2952968"
---
# <a name="exporting-your-business-data-to-excel"></a>Exportar los datos de negocio a Excel
Si desea trabajar con sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Excel, puede abrir todas las listas en Excel y trabajar con ellos. De igual forma, si desea cancelar la suscripción de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar los datos a Excel de forma que pueda llevárselos.

## <a name="opening-lists-in-excel"></a>Abrir listas en Excel
Puede abrir los datos en Excel desde cualquier diario, lista u hoja de trabajo. Abra solo la página que desee y, a continuación, elija **Abrir en Excel**. Por ejemplo, abra la lista de clientes (busque **Clientes**) y elija **Abrir en Excel**. El explorador le indicaŕa que abra o guardar el libro de Excel generado.  

> [!NOTE]
> Use esta opción cuando no desee realizar cambios y publicar esos cambios de nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Cada lista incluye varias columnas y la exportación a Excel incluirá algunas columnas que están en la vista actual. Si desea agregar o eliminar columnas antes de abrir la lista en Excel, abra el menú contextual de cualquier columna y después especifique qué columnas que desea ver. Esta lista de columnas es distinta de la mayoría de listas y refleja la estructura de la base de datos donde se almacenan los datos. Si no está seguro del tipo de datos que contiene una determinada columna, puede agregarla a la vista y decidir si desea quitarla de nuevo.  

### <a name="edit-data-in-excel"></a>Editar datos en Excel
Su experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un complemento para Excel para que pueda editar datos en Excel. Para obtener más información, consulte [Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Exportar datos a otros sistemas financieros
Si decida cancelar la suscripción de [!INCLUDE[d365fin](includes/d365fin_md.md)], puede exportar los datos a Excel y llevárselos a su próximo sistema financiero.  

Por supuesto, puede exportar todas las páginas, pero puede que sea más de lo que necesita realmente. Por lo tanto, considere la posibilidad de exportar las páginas esenciales siguientes y recuerde agregar todas las columnas como se ha descrito anteriormente:  

* Plan de cuentas  
* Clientes  
* Proveedores  
* Bancos  
* Productos  

Si también desea todas las transacciones financieras, es una gran cantidad de datos, por lo que la exportación suele tardar varios minutos. Las transacciones financieras se muestran en la página **Movs. contabilidad**.  

Le recomendamos que también considere la posibilidad de exportar los datos de las páginas siguientes:  

* Movs. clientes  
* Movs. proveedores  
* Movs. bancos  
* Movs. productos  
* Configuración grupos contables  
* Grupos contables clientes  
* Grupos contables proveedores  
* Grupos contables producto  
* Grupo contable banco  
* Presupuestos contables  
* Movs. pptos. contabilidad  
* Ofertas venta  
* Facturas venta  
* Facturas compra  
* Contactos  
* Vendedores  

> [!NOTE]  
>   Si ha configurado varias empresas en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe exportar los datos correspondientes de cada empresa.

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Cancelar la suscripción de [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-cancel.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Finanzas](finance.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
