---
title: Utilizar claves de asignación en diarios generales
description: Puede asignar un movimiento en un diario general a varias cuentas diferentes al registrar el diario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.search.form: '283, 284'
ms.date: 06/29/2021
ms.author: bholtorf
---
# Utilizar claves de asignación en diarios generales
Puede asignar un movimiento en un diario general a varias cuentas diferentes al registrar el diario. La distribución puede realizarse por cantidad, porcentaje o importe.

## Para configurar claves de asignación
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario general periódico** y luego elija el enlace relacionado.
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

## Para modificar una clave de asignación que ya haya sido configurada
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario general periódico** y luego elija el enlace relacionado.
2. En la página **Diario general periódico** (Diarios generales periódicos), seleccione el diario con la distribución.
3. Seleccione la línea con la asignación y, a continuación, seleccione la acción **Asignaciones**.
4. Cambie los campos relevantes y, a continuación, elija el botón **Aceptar**.

## Consulte también
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Registrar documentos y diarios](ui-post-documents-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]