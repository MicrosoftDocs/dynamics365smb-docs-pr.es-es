---
title: Crear una nueva L.M. de producción y una versión de L.M.
description: Tutorial para aprender a agregar otra cafetera a la línea de productos de Contoso Coffee en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---
# Tutorial: Crear una nueva L.M. de producción y una versión de L.M.

En este artículo, le guiaremos por los pasos para usar los datos de demostración de Contoso Coffee para trabajar con listas de materiales (L.M) en procesos de producción.  

## Caso

Contoso Coffee ha decidido agregar otra cafetera a su línea de producto: **SP-SCM1008 Airpot Lite**. Esta cafetera es idéntica al artículo existente **SP-SCM1009 Airpot**, excepto que no incluye la placa de calentamiento, **SP-BOM1104**. En un paso separado, la luz de encendido/apagado, **SP-BOM1106** se elimina para una versión de la L.M. de Airpot Lite.

Oscar, el ingeniero de procesos de Contoso Coffee, debe configurar una nueva L.M. de producción para definir los requisitos de componentes iniciales para Airpot Lite. Óscar debe entonces configurar una nueva versión de L.M., con una fecha de inicio del 1 de julio, para alinearse con los planes del lanzamiento de otra edición.

## Pasos

1. Cree una nueva L.M. de producción para Airpot Lite.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **L.M. de producción** y, a continuación, elija el vínculo relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº** |SP-SCM1008|
        |**Descripción** |Airpot Lite|
        |**Cód. unidad medida**|UDS  |

2. Copie los componentes de la L.M. de producción **SP-SCM1009**.

    1. Elija la acción **Copiar L.M.**.

    2. En la página **L.M. de producción**, elija la línea **SP-SCM1009, Airpot** y luego el botón **Aceptar**.

3. Modifique los componentes para la nueva L.M. de producción como se describe en el escenario.

    1. En la ficha desplegable **Líneas**, seleccione la línea para el artículo **SP-BOM1104** y luego elija la acción **Eliminar línea**.  

4. Certifique la nueva L.M.  

    1. En el campo **Estado**, elija *Certificado*.  

5. Cree una versión de L.M. de producción para Airpot Lite.

    1. Seleccione la acción **Versiones**.

    2. En la página **Lista versiones L.M. produc.**, elija la acción **Nuevo** y, a continuación, rellene los campos de cuenta tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Cód. versiones** |02|
        |**Descripción** |Airpot Lite, v2|
        |**Cód. unidad medida**|UDS  |  
        |**Fecha inicial**|1 de julio  |  

6. Copie las líneas de componentes de la L.M. de producción en la nueva versión de L.M.

    1. Elija la acción **Copiar L.M.** y luego el botón **Sí** para copiar los componentes de la L.M. de producción original.

7. Quite el artículo **SP-BOM1106, luz de encendido/apagado** de los componentes de la versión.

8. Certifique la nueva versión de L.M.

    1. En el campo **Estado**, elija *Certificado*.  

    2. Cierre la versión de L.M.

La nueva cafetera ahora está configurada como una L.M. de producción con una versión.  

## Consulte también .

[Introducción a datos de demostración de Contoso Coffee](../contoso-coffee-intro.md)  
