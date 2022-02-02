---
title: Trabajar con resúmenes financieros en Excel
description: Obtenga más información sobre cómo puede abrir los estados financieros en Microsoft Excel desde Business Central, para un mejor análisis.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: overview
ms.search.keywords: accountant, accounting, financial report
ms.search.form: 9027
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ec34d0e1898340a3c948d422a24781df44cc1206
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012056"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Análisis de estados financieros en Microsoft Excel

En [!INCLUDE [prod_short](includes/prod_short.md)], puede ver los KPI y obtener resúmenes del estado financiero de la empresa. También puede abrir las listas en Excel y analizar los datos. Además, también puede exportar estados financieros pesados como el balance o la cuenta de resultados a Excel, analizar los datos e imprimir los informes.  

Desde las Áreas de trabajo Administrador de negocio y Contable, puede elegir qué estados financieros desea ver en Excel desde un menú desplegable en la sección Informes de la cinta de opciones. Cuando elige una declaración, se abrirá en Excel o Excel en línea. Un complemento conecta los datos a [!INCLUDE [prod_short](includes/prod_short.md)]. Sin embargo, tiene que iniciar sesión con la misma cuenta que utilice en [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Obtención de panorama y detalles en Excel

En la cinta de opciones, seleccione el informe correspondiente de Excel y deje que se abra para que pueda obtener la visión general que estaba buscando. En esta versión de [!INCLUDE [prod_short](includes/prod_short.md)], proporcionamos los siguientes informes de Excel:

- Balance  
- Balance de ingresos  
- Extracto de flujo de efectivo  
- Extracto de remanentes  
- Antigüedad pagos  
- Antigüedad cobros  

Digamos que desea profundizar en su flujo de efectivo. Desde el Área de trabajo Administrador de negocio o Contable, puede abrir el informe de **Estado de flujo de efectivo** en Excel, pero lo que realmente sucede es que exportamos los datos relevantes y creamos un libro de Excel basado en una plantilla predefinida. Dependiendo de su navegador, se le pedirá que abra o guarde el libro.  

En Excel, ve una pestaña donde los datos se establecen en la primera hoja de cálculo. Todos los datos que se exportaron también están presentes en otras hojas de trabajo en caso de que lo necesite. Puede imprimir el informe de inmediato o puede modificarlo hasta que tenga el panorama y los detalles que desee. Utilice el complemento [!INCLUDE [prod_short](includes/prod_short.md)] de Excel para filtrar y analizar datos.  

### <a name="understanding-the-excel-templates"></a>Conocer las plantillas de Excel

Los informes de Excel predefinidos se basan en los datos de la empresa actual. Por ejemplo, la empresa de demostración ha configurado el plan de cuentas para enumerar tres cuentas de efectivo en *Activos circulantes*: 10100 **Cuenta de cheques**, 10200 **Cuenta de ahorro** y 10300 **inero para gastos menores**. Las cuentas tienen el campo **Subcategoría de cuenta** establecido en *Efectivo* y es su cantidad combinada la que aparece como *Efectivo* en el informe de Excel **Balance**.  

Las hojas adicionales del libro de Excel muestran los datos que hay detrás del informe. Pero para descubrir qué se esconde detrás de las agrupaciones en los informes de Excel, es posible que deba volver a [!INCLUDE [prod_short](includes/prod_short.md)] y aplicar filtros a las listas, por ejemplo.  

## <a name="the-prod_short-excel-add-in"></a>Complemento [!INCLUDE [prod_short](includes/prod_short.md)] de Excel

Su experiencia con [!INCLUDE [prod_short](includes/prod_short.md)] incluye un complemento de Excel. Dependiendo de su suscripción, se iniciará sesión automáticamente o deberá especificar los mismos datos de inicio de sesión que utiliza para [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Ver y editar en Excel desde Business Central](across-work-with-excel.md).  

Con el complemento, puede conseguir nuevos datos de [!INCLUDE [prod_short](includes/prod_short.md)] y puede insertar cambios a [!INCLUDE [prod_short](includes/prod_short.md)]. Sin embargo, la capacidad de insertar datos en la base de datos está desactivada para los informes financieros de Excel a la lista anterior.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Ver y editar en Excel desde Business Central](across-work-with-excel.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]