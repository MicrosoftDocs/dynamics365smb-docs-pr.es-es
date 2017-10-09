---
title: "Importar transacciones de nómina | Documentos de Microsoft"
description: "Para administrar los salarios, se importan y registran transacciones financieras desde el proveedor de nóminas a la contabilidad, mediante una extensión de nóminas como Ceridian o Quickbooks."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d53dfb26a3fea663e68a3b558579a59184e9de26
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-import-payroll-transactions"></a>Procedimiento: importar transacciones de nómina
Para contabilizar los pagos de salario y transacciones relacionadas, deberá importar y registrar las transacciones financieras de salario creadas para el proveedor de nóminas al libro mayor. Para hacer esto, primero importe un archivo que recibirá del proveedor de nóminas en la ventana **Diario general**. A continuación asigne las cuentas externas del archivo de nóminas a las cuentas correspondientes. Por último, registre operaciones de nóminas según la asignación de cuentas.

> [!NOTE]  
>   Para utilizar esta funcionalidad, se debe instalar y habilitar la extensión para importar nóminas. Las extensiones Nómina de Ceridian e Importación del archivo de nómina de QuickBooks están preinstaladas en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, consulte [Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante extensiones](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Para importar un archivo de nómina
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diarios generales** y elija el vínculo relacionado.
2. En la sección del diario general correspondiente, elija la acción **Importar transacciones de nómina**. Se abre una guía de configuración asistida.
3. Realice los pasos de la ventana **Importar transacciones de nómina**.

    > [!TIP]  
>   En el paso de la asignación de los registros de nóminas externos a sus cuentas de contabilidad, las asignaciones que cree se recordarán la próxima vez que importe los mismos registros. Esto le ahorrará tiempo al no tener que rellenar manualmente el campo **Número de cuenta** en el diario general cada vez que haya importado transacciones de nóminas periódicas.   

    Cuando elige el botón **Aceptar** en la guía de configuración asistida, la ventana **Diario general** incluye las líneas que representan transacciones que contiene el archivo de nóminas y con las cuentas correspondientes rellenadas previamente en los campos **Cuentas G/L** según las asignaciones que ha creado en la guía.
4. Edite o registre las líneas de diario como cualquier otra transacción de contabilidad. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  

