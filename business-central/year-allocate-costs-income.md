---
title: Resumen de tareas de asignar costes e ingresos | Documentos de Microsoft
description: Describe las tareas para asignar un movimiento en un diario general a varias cuentas diferentes al registrar el diario.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 60b73b5c29bca5dc85e123f5957c7f3c0917345f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "928775"
---
# <a name="allocate-costs-and-income"></a>Asignar costes e ingresos
Puede asignar un movimiento en un diario general a varias cuentas diferentes al registrar el diario. La asignación se puede realizar según tres métodos distintos:

* Cantidad
* Porcentaje (%)
* Importe

Las funciones de asignación se pueden usar con diarios generales periódicos y en diarios de activos fijos.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Los procedimientos siguientes describen cómo preparar la asignación de costes en un diario general periódico mediante la definición de las claves de asignación. Cuando se definen las claves de asignación, el diario se rellena y se registra como cualquier otro diario general periódico. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).

## <a name="to-set-up-allocation-keys"></a>Para configurar claves de asignación
Puede asignar un movimiento en un diario general periódico a varias cuentas diferentes al registrar el diario. La distribución puede realizarse por cantidad, porcentaje o importe.
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario general periódico** y luego elija el enlace relacionado.
2. Seleccione el campo **Nombre de sección** para abrir la página **Secciones diario general**.
3. Puede modificar las asignaciones en una sección existente de la lista o crear une nueva sección con asignaciones.
   * Para crear un lote nuevo, seleccione la acción **Nuevo** y vaya al paso siguiente.
   * Para cambiar las asignaciones de un diario existente, seleccione el diario y vaya al paso 7.    
4. En el campo **Nombre**, escriba un nombre para la sección, por ejemplo LIMPIEZA. En el campo **Descripción**, escriba una descripción, por ejemplo, Limpieza de diario de gastos.
5. Cuando haya terminado, cierre la página. Aparecerá un nuevo diario periódico vacío.
6. Complete los campos de la línea.
7. Seleccione la acción **Asignaciones**.
8. Agregue una línea para cada asignación. Debe rellenar el campo **% Distribución**, **Cantidad a distribuir** o **Importe**. También debe rellenar el campo **Nº cuenta** y, si distribuye la transacción entre dimensiones globales, los campos de dimensión global.
9. Si escribe un porcentaje en una línea, el importe del campo **Importe** se calculará automáticamente. Estos importes tienen el signo contrario al importe total del campo **Importe** en el diario periódico.
10. Después de introducir las líneas de asignaciones, seleccione **Aceptar** para volver a la página **Diario general periódico**. El campo **Importe asignado (USD)** se rellena y coincide con el campo **Importe**.
11. Registre el diario.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Para modificar una clave de asignación que ya haya sido configurada
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario general periódico** y luego elija el enlace relacionado.
2. En la página **Diario general periódico** (Diarios generales periódicos), seleccione el diario con la distribución.
3. Seleccione la línea con la asignación y, a continuación, seleccione la acción **Asignaciones**.
4. Cambie los campos relevantes y, a continuación, elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)    
[Registrar documentos y diarios](ui-post-documents-journals.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
