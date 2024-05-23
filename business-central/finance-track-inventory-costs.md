---
title: Realizar el seguimiento de ajustes de coste de producto
description: Descubra cómo el seguimiento de los ajustes a los costos de los artículos puede ayudarlo a mantener precisos los datos de costos de los artículos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Realizar el seguimiento de ajustes de coste de producto

Es importante mantener los costos de los artículos precisos y acortar el tiempo entre el momento en que se registra una entrada y el momento en que la contabilidad general refleja su costo. Puede realizar un seguimiento del rendimiento de los ajustes de costos para ejecuciones de ajuste y artículos individuales. Si ocurren errores, puede identificar los elementos problemáticos y realizar correcciones. Por ejemplo, puede excluir los elementos de los cálculos para garantizar que los ajustes no se interrumpan para otros elementos. Puede ajustar los costos de artículos individuales o crear lotes de artículos y ajustarlos todos al mismo tiempo.

## Comience a realizar un seguimiento de los ajustes de costos

Empezar es fácil. En la página **Configuración de inventario**, el campo **Registro de ajuste de costos** ofrece algunas opciones:

* **Desactivado** significa que no registra ejecuciones de ajuste de costos.
* **Sólo errores** significa registrar solo las ejecuciones que fallaron.
* **Todo** significa registrar todas las ejecuciones.

> [!NOTE]
> Para minimizar el tamaño del registro, [!INCLUDE [prod_short](includes/prod_short.md)] no registra los ajustes que ocurren automáticamente cuando alguien publica un elemento.

También debe configurar la entrada de la cola de trabajos **Contabilizar costo de inventario en el L/M (1002)**. Esta entrada en la cola de trabajos ajusta automáticamente los costos según un programa. Para obtener más información entradas de cola de trabajo, consulte [Utilice las colas de trabajos para programar tareas](admin-job-queues-schedule-tasks.md).

## Administrar ajustes de costos

Utilice la página **Ajuste de costos de inventario** para administrar y supervisar el proceso de ajuste de costos. Esta página muestra los artículos junto con sus parámetros de cálculo de costes y su estado de ajuste de costes. Puede filtrar la lista para centrarse en elementos que requieren ajuste o que están excluidos del proceso de ajuste de costos.

### Acerca de los lotes de artículos

Puede ejecutar un ajuste de costos para varios artículos agrupándolos en lotes. Los lotes facilitan el ajuste de algunos elementos por separado, por ejemplo, porque tardan más en ajustarse. Los lotes también pueden ayudar a identificar artículos que tienen problemas.

Para crear un lote, en la página **Ajuste de costos de inventario**, realice una de las siguientes acciones:

* Seleccione los elementos de la lista, elija **Ejecutar ajuste de costos** y luego elija **Agregar lote**.
* Para crear un lote y ejecutar el ajuste de costos inmediatamente, seleccione los artículos en la lista, elija **Ejecutar ajuste de costos** y luego elija **Agregar lote y ejecutar**.
* Elija **Ejecutar ajuste de costos**, elija **Lotes de artículos** y luego ingrese un filtro en el campo **Filtro de artículos**.
  
> [!TIP]
> Para crear rápidamente otro lote para todos los artículos que aún no están incluidos en un lote, en la página **Ajuste de costes: lotes de artículos**, elija **Agregar elementos faltantes**.

Cuando finaliza una ejecución de un lote, el lote tiene uno de los siguientes estados en la página **Lotes de artículos**:

* **Éxito**: el ajuste de costes tuvo éxito.
* **Fallido**: si el ajuste de costos falla, [!INCLUDE [prod_short](includes/prod_short.md)] identifica el artículo que causó el error y luego divide el lote actual en dos. Un lote con el artículo problemático y otro con los artículos restantes. Repeticiones de ajuste de costos para el lote con los artículos restantes. Si vuelve a fallar, se repite el proceso. Usted define el número máximo de divisiones en el campo **Máx. de reintentos**. El valor predeterminado para los reintentos es 10, pero puede ingresar un nuevo límite.
* **Tiempo agotado**: si el ajuste de costos para un lote no finaliza dentro del período especificado en el campo **Tiempo de espera (Minutos)** (que va de 1 a 720 minutos), la sesión finaliza y los cambios se revierten. [!INCLUDE [prod_short](includes/prod_short.md)] luego divide el lote actual por la mitad y vuelve a ejecutar el proceso de ajuste de costos para cada mitad. Este proceso continúa hasta que el ajuste de costos sea exitoso o alcance el máximo de reintentos.

> [¡CONSEJO!] Cada lote se ejecuta en una sesión independiente. Para supervisar el progreso, use la acción **Actualizar**.

### Ejecutar ajuste de coste

Utilice la página **Ajuste de costes de inventario** para realizar ajustes.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Ajuste de costes de inventario**, y luego elija el enlace relacionado.
1. Dependiendo de lo que quiera hacer, use una de las siguientes opciones:

  * Para uno o más artículos inmediatamente, seleccione los artículos en la lista y luego elija **Ejecutar ajuste de costes**.
  * Para lotes, use una de las opciones siguientes:

    * Para crear un lote y ajustar costos inmediatamente, elija los artículos en la lista, elija **Ejecutar ajuste de costos** y después **Agregar lote y ejecutar**.
    * Para ejecutarlo para todos los lotes, elija **Ejecutar ajuste de costos**, **Lotes de artículos** y luego elija **Ejecutar**.
    
    Para obtener más información sobre los lotes, vaya a [Acerca de lotes de artículos](#about-item-batches).

### Explorar detalles del artículo

Utilice el menú **Artículo** para acceder a información sobre ajustes de costos para un artículo seleccionado.

* **Entradas del libro mayor de artículos**: enumera las entradas de artículos para el artículo. La acción **Marcar para ajuste** le permite forzar la repetición del ajuste de costos para artículos directa o indirectamente vinculados a las entradas entrantes que seleccione. Forzar una nueva ejecución puede resultar útil si ejecuciones anteriores generaron costos incorrectos.
* **Entradas de valor**: enumera las entradas de valor para el artículo.
* **Ajuste de costes de Puntos de entrada**: abra la página **Punto de entrada de ajuste de costes medio** , que se utiliza principalmente para calcular el costo promedio. La página muestra combinaciones de artículos, ubicaciones, variantes y fechas de valoración para las cuales se ejecutan, o se deben ejecutar, ajustes de costos.
* **Ajuste de costos de pedidos**: abre el menú **Ajuste de entrada de inventario (Pedido)** , donde ajusta las órdenes de producción y montaje. Muestra que las órdenes están ajustadas o requieren ajuste.

### Ver el resultado

Utilice el menú **Registrar por** para ver el resultado de los ajustes de costos:

* **Ejecutar**: muestra registros de ajuste de costos para cada ejecución. El registro incluye datos sobre el filtro del artículo, el estado (éxito/fallido/tiempo de espera agotado), fecha/hora de inicio y finalización, duración y las diferencias de costos producidas por la ejecución.
* **Artículo**: muestra información detallada sobre el proceso de ajuste del artículo seleccionado.

### Incluir o excluir elementos de los ajustes

Si uno o más elementos fallan, puede excluirlos de la ejecución de ajuste y luego incluirlos en ejecuciones posteriores. En el menú **Funciones** elija una de las siguientes:

* **Excluir artículo del ajuste** e **Incluir artículo en el ajuste**: deshabilite temporalmente y luego vuelva a habilitar el ajuste de costos para un artículo seleccionado. El ajuste de costes continúa manteniendo los costes precisos para otros artículos mientras investiga un problema con un artículo específico.

## Registrar costes ajustados a la contabilidad general

Normalmente, las nuevas entradas de valor se contabilizan en el libro mayor de acuerdo con la programación para la entrada de cola de trabajos **Contabilizar costo de inventario en el libro mayor (1002)**. Sin embargo, puede publicar ajustes en el libro mayor inmediatamente desde la página **Ajuste de costos de inventario**. En el menú **Funciones**, elija **Contabilizar costes de inventario en el Libro Mayor**.

## Solucionar problemas de ajustes de costes

Utilice las siguientes opciones en el menú **Diagnóstico** para solucionar problemas de ejecuciones de ajuste de costos.

* **Exportar datos del artículo**: exporta datos relacionados con el artículo a un archivo de texto. Puede utilizar el archivo para realizar análisis adicionales en un entorno de pruebas o adjuntarlo a una solicitud de soporte al investigar problemas de cálculo de costos.
* **Importar datos del artículo**: importe el archivo de texto exportado previamente nuevamente a la base de datos. Esta acción solo está habilitada en entornos de espacio aislado o empresas de evaluación.
* **Restablecer costo ajustado**: restablece la opción **Costo ajustado** en artículos, órdenes de producción u órdenes de ensamblaje. Esta configuración le permite forzar la repetición del ajuste de costos para ellos.
* **Informe de detección de problemas de costes**: diagnostica problemas de datos típicos que causan errores de cálculo en los costos. Comprueba si los asientos contables de artículos, los asientos de valor, los asientos de aplicación de artículos y los asientos contables de capacidad son correctos.
* **Eliminar datos del artículo**: borre todas las tablas relacionadas con artículos en la base de datos. Esta acción solo está disponible en entornos de espacio aislado o empresas de evaluación.

## Consulte también

[Ajustar costes de productos](inventory-how-adjust-item-costs.md)  
[Detalles de diseño: ajuste de coste](design-details-cost-adjustment.md)  
