---
title: "Usar claves de asignación en diarios generales | Documentos de Microsoft"
description: "Obtenga infraestructura sobre cómo puede usar las claves de asignación en diarios."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bbacf9b5634d51478dd4d54ac4b587ea9bfaaf99
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-allocation-keys-in-general-journals"></a>Procedimiento: utilizar claves de asignación en diarios generales
Puede asignar un movimiento en un diario general a varias cuentas diferentes al registrar el diario. La distribución puede realizarse por cantidad, porcentaje o importe.

## <a name="to-set-up-allocation-keys"></a>Para configurar claves de asignación
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diario general periódico** y elija el vínculo relacionado.
2. Seleccione el campo **Nombre de sección** para abrir la ventana **Secciones diario general**.
3. Puede modificar las asignaciones en una sección existente de la lista o crear une nueva sección con asignaciones.
   * Para crear un lote nuevo, seleccione la acción **Nuevo** y vaya al paso siguiente.
   * Para cambiar las asignaciones de un diario existente, seleccione el diario y vaya al paso 7.    
4. En el campo **Nombre**, escriba un nombre para la sección, por ejemplo LIMPIEZA. En el campo **Descripción**, escriba una descripción, por ejemplo, Limpieza de diario de gastos.
5. Cuando haya terminado, cierre la ventana. Aparecerá un nuevo diario periódico vacío.
6. Complete los campos de la línea.
7. Seleccione la acción **Asignaciones**.
8. Agregue una línea para cada asignación. Debe rellenar el campo **% Distribución**, **Cantidad a distribuir** o **Importe**. También debe rellenar el campo **Nº cuenta** y, si distribuye la transacción entre dimensiones globales, los campos de dimensión global.
9. Si escribe un porcentaje en una línea, el importe del campo **Importe** se calculará automáticamente. Estos importes tienen el signo contrario al importe total del campo **Importe** en el diario periódico.
10. Después de introducir las líneas de asignaciones, seleccione **Aceptar** para volver a la ventana **Diario general periódico**. El campo **Importe asignado (USD)** se rellena y coincide con el campo **Importe**.
11. Registre el diario.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Para modificar una clave de asignación que ya haya sido configurada
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diario general periódico** y elija el vínculo relacionado.
2. En la ventana **Diario general periódico** (Diarios generales periódicos), seleccione el diario con la distribución.
3. Seleccione la línea con la asignación y, a continuación, seleccione la acción **Asignaciones**.
4. Cambie los campos relevantes y, a continuación, elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

