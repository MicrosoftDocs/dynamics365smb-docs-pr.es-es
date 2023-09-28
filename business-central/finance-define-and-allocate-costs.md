---
title: Definición y asignación de costes
description: 'Las asignaciones de costes mueven los costes e ingresos entre tipos de coste, centros de coste y objetos de coste. Puede definir tantas asignaciones como necesite.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="defining-and-allocating-costs"></a>Definición y asignación de costes

Las asignaciones de costes mueven los costes e ingresos entre tipos de coste, centros de coste y objetos de coste. Puede definir tantas asignaciones como necesite. Cada asignación consta de:  

- Un origen asignación.  
- Uno o varios destinos de asignación.  

El origen de asignación establece qué costes se deben asignar, y los destinos de asignación determinan dónde se deben asignar los costes. Por ejemplo, un origen de asignación puede ser los costes del tipo de coste Electricidad y Calefacción. Asigna todos los costes de electricidad y calefacción a tres centros de coste: Taller, Producción y Ventas. Estos centros de coste son los destinos de asignación.  

Para cada origen de asignación, puede definir un nivel de asignación, un periodo de validez y una variante como identificador de grupo. Puede utilizar un trabajo por lotes para definir filtros para seleccionar definiciones de asignación y luego ejecutar asignaciones de coste automáticamente.  

Para cada destino de asignación, define una base de asignaciones. La base de la asignaciones puede ser estática o dinámica.  

- Las bases de asignaciones estáticas se basan en un valor definido, por ejemplo los metros cuadrados o una proporción de asignación establecida, como 5:2:4.  
- Las bases de asignaciones dinámicas se basan en valores cambiables, como el número de empleados de un centro de coste o los ingresos de ventas de un objeto de coste en un determinado periodo de tiempo.  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

## <a name="setting-up-allocation-source-and-targets"></a>Configuración del origen de asignación y los destinos

Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. El origen de asignación define qué costes se asignarán. Los destinos de asignación determinan dónde se deben asignar los costes.  

### <a name="to-set-up-cost-allocations"></a>Para configurar asignaciones de coste

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignación de costes** y luego elija el enlace relacionado.  
2. En la página **Asignación costes**, elija la acción **Editar**.  
3. Especifique un identificador para el origen de asignación en el campo **ID**.  
4. Defina un nivel como un número entre 1 y 99 en el campo **Nivel**. El registro de la asignación seguirá el orden de los niveles.  
5. Escriba un tipo de coste para definir qué tipos de coste se asignarán en el campo **Intervalo tipo coste**. Si todos los costes de un tipo de coste se asignan, no se define ningún intervalo.  
6. Especifique un centro de coste junto con los costes que se asignarán en el campo **Código centro coste**.  
7. Especifique un objeto de coste junto con los costes que se asignarán en el campo **Código objeto coste**. Muy a menudo, este campo permanece vacío porque raramente los objetos de coste se asignan a otros objetos de coste.  
8. Especifique un tipo de coste en el campo **Abonar en tipo de coste**. Los costes que asignen se abonarán en el tipo de coste de origen. El registro de haber se registrará en el tipo de coste que se indique aquí.  
9. En la ficha desplegable **Líneas**, define los destinos de asignación. En la primera línea, escriba un tipo de coste en el campo en el campo **Tipo coste destino**. Define a qué tipo de coste se carga la asignación.  
10. En la primera línea, introduzca el primer destino de asignación en el campo **Centro de coste de destino** o el campo **Objeto de coste de destino**. Estos dos campos definen en qué centro de coste u objeto de coste se carga la asignación. Sólo puede rellenar uno de ellos, pero no los dos.  
11. Repita los mismos pasos en la segunda línea para configurar los destinos de asignación adicionales.  
12. Una vez configurado el destino y los orígenes de asignación, elija la acción **Calcular clave de asignación** para calcular los valores compartidos totales.  

> [!NOTE]  
> Seleccione la casilla **Bloqueado** para desactivar la configuración de asignación.

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Configuración de filtros para las bases de la asignación dinámica

El método de asignación dinámica se basa en los valores cambiables. Por ejemplo, el número de empleados de un centro de coste o los productos vendidos de un objeto de coste en un periodo de tiempo determinado. Existen nueve bases predefinidas de asignación y doce rangos de fechas dinámicas. Define distintos filtros basados en la base de asignación.  

### <a name="setting-filters"></a>Configurando filtros

La siguiente tabla muestra qué filtros son posibles para distintas bases de asignación y qué valores son válidos en los campos **Filtro nº** y **Filtro grupo**. Seleccione <kbd>F1</kbd> en el campo **Filtro fecha vto.** para leer descripciones detalladas.  

|**Base**|**Filtro Nº**|**Filtro fecha vto.**|**Filtro centro coste**|**Filtro objeto coste**|**Filtro grupo**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Movimientos de contabilidad|Cuenta|Sí|Sí|Sí|N/D|  
|Movs. pptos. contabilidad|Cuenta|Sí|Sí|Sí|Nombres pptos. contabilidad|  
|Movimientos de tipo de coste|Tipo de coste|Sí|Sí|Sí|N/D|  
|Movs. ppto. costes|Tipo de coste|Sí|Sí|Sí|Nombre ppto.|  
|Nº de empleados|N/D|Sí|Sí|Sí|N/D|  
|Productos vendidos (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable existencias|  
|Productos comprados (cantidad)|Nº producto|Sí|Sí|Sí|Grupo contable existencias|  
|Productos vendidos (importe)|Nº producto|Sí|Sí|Sí|Grupo contable existencias|  
|Productos comprados (importe)|N.º producto|Sí|Sí|Sí|Grupo registro inventario|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Ejemplo 1: definición de asignaciones estáticas basadas en la proporción de asignación

El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4.  

Este tema describe cómo definir tres nuevos objetos de coste de destino de asignación para el centro de coste PROD del origen de asignación mediante la proporción 5:2:4 de asignación establecida. Los tres objetos de coste de destino son ACCESORIOS, PINTURA y COLOCACIONES.  

> [!NOTE]  
> El ejemplo utiliza los datos de demostración en [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Para definir el centro de coste PROD de origen de asignación en la ficha desplegable General

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignación de costes** y luego elija el enlace relacionado.  
2. En la página **Asignación costes**, elija la acción **Nuevo**.  
3. En el campo **ID**, seleccione <kbd>Entrar</kbd> o escriba un Id.  
4. En el campo **Nivel**, introduzca **1**.  
5. Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.  
6. En el campo **Código centro coste**, introduzca **PROD**.  
7. En el campo **Abonar en tipo de coste**, especifique un tipo de coste **9903**.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Para definir los objetos de coste de destino de asignación en la Ficha desplegable Líneas

1. En la primera línea, en el campo **Tipo coste destino**, especifique **9903**.  
2. En la primera línea, en el campo **Objeto de coste de destino**, seleccione **ACCESORIOS**.  
3. En la primera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
4. En la primera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
5. En la primera línea, en el campo **Compartir**, especifique la proporción de asignación **5**.  
6. En la segunda línea, en el campo **Tipo coste destino**, especifique **9903**.  
7. En la segunda línea, en el campo **Objeto de coste de destino**, seleccione **PINTURA**.  
8. En la segunda línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
9. En la segunda línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
10. En la segunda línea, en el campo **Compartir**, especifique la proporción de asignación **2**.  
11. En la tercera línea, en el campo **Tipo coste destino**, especifique **9903**.  
12. En la tercera línea, en el campo **Objeto de coste de destino**, seleccione **COMPLEM**.  
13. En la tercera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
14. En la tercera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
15. En la tercera línea, en el campo **Compartir**, especifique la proporción de asignación **4**.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] calcula automáticamente el campo **Porcentaje** con un porcentaje que depende de las tres relaciones de asignación que se han introducido en el campo **Compartir** para las tres líneas.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Ejemplo 2: definición de asignaciones dinámicas basándose en productos vendidos

Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica. En el ejemplo, se cambia la asignación dinámica de los costes del centro de coste VENTAS para admitir el nuevo EQUIPO TI del objeto de coste. Los paquetes de EQUIPO TI tienen números de producto en el rango de 8904-W a 8924-W. Utiliza las cifras de ventas del año anterior para calcular el reparto. La asignación se registra al tipo de coste de ayuda 9903.  

> [!NOTE]  
> El ejemplo utiliza los datos de demostración en [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Para definir las asignaciones dinámicas basándose en los productos vendidos el año anterior

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Asignación de costes** y luego elija el enlace relacionado.  
2. En la página **Asignación costes**, elija la acción **Nuevo**.  
3. En el campo **ID**, seleccione <kbd>Entrar</kbd> o escriba un Id.  
4. En el campo **Nivel**, introduzca **1**.  
5. Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.  
6. En el campo **Código centro coste**, introduzca **VENTAS**.  
7. En el campo **Abonar en tipo de coste**, especifique un tipo de coste **9903**.  
8. En el campo **Tipo coste destino**, especifique un tipo de coste **9903**.  
9. En el campo **Objeto de coste de destino**, seleccione **Nuevo** para crear un nuevo EQUIPO TI de objeto de coste y rellene los campos según sea necesario. Seleccione **EQUIPO TI**. Deje en blanco el campo **Centro de coste de destino**.  
10. En el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
11. En el campo **Base**, seleccione la base de asignación **Productos vendidos (importe)**.  
12. En el campo **Nº filtro**, especifique **8904-W..8924-W**.  
13. En el campo **Filtro fecha vto.**, especifique **Año anterior**.  
14. Elija la acción **Calcular clave de asignación** para calcular el reparto.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] utiliza las cifras de ventas de ejercicios anteriores para calcular un reparto de 1596,50 DL con el 100 por ciento para los paquetes de EQUIPO TI. Esto significa que todos los productos vendidos el año anterior se asignarán al EQUIPO TI del objeto de coste.

## <a name="see-also"></a>Consulte también .

 [Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)  
 [Transferir y registrar movimientos de coste](finance-transfer-and-post-cost-entries.md)  
 [Contabilidad para costes](finance-manage-cost-accounting.md)  
 [Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)  
 [Acerca de la contabilidad de costes](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
