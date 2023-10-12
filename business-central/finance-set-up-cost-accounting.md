---
title: Configuración de contabilidad de costes
description: 'Antes de empezar a trabajar con la contabilidad de costes, debe realizar la configuración. Cada movimiento de coste debe tener un tipo de coste asignado y un código de centro de coste o un objeto de coste asignado.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1112, 1113, 1122'
ms.date: 06/16/2021
ms.author: bholtorf
---
# Configuración de contabilidad de costes

Antes de empezar a trabajar con la contabilidad de costes, debe realizar tareas de configuración.

## Saldos entre el tipo de coste, centro de coste y objeto de coste

Al configurar la contabilidad de costes, debe asegurarse de que todos los movimientos están asignados a un tipo de coste así como a un centro o un objeto de coste. Indica que cada movimiento de coste debe tener un tipo de coste asignado y un código de centro de coste o un objeto de coste asignado. Esta norma garantiza que cada movimiento de coste aparezca en los centros de coste u objetos de coste, pero nunca en ambas situaciones.  

De esta manera, crea la siguiente ecuación de contabilidad:  

*Saldo tipo coste* = *Saldo centro coste* + *Saldo objeto coste*  

Al imprimir el plan del tipo de coste, el plan de centros de coste y el plan de informes de objetos de coste, puede analizar esta relación.

## Configuración de tipos de coste

El plan de tipos de coste es similar al plan de cuentas de contabilidad general. Puede configurar el plan de tipos de coste de la siguiente forma:  

- Estructure el plan de tipos de coste de manera similar a las cuentas de ingresos del plan de cuentas de contabilidad general. Luego puede transferir el plan de cuentas de contabilidad al plan de tipos de coste. Puede hacer los ajustes necesarios después de la transferencia.  
- Cree el nuevo plan de tipos de coste o agregue nuevos tipos de coste al plan existente de tipos de coste. Debe crear cada tipo de coste nuevo por separado.  

### Para transferir el plan de cuentas de contabilidad al plan de tipos de coste

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan tipos coste** y luego elija el enlace relacionado.  
2. Elija la acción **Traer tipos coste de plan cuentas**. En el cuadro de diálogo, seleccione el botón **Sí** para confirmar la transferencia. La función utiliza el plan de cuentas para crear un plan de tipos de coste.  

    El plan de tipos de coste contendrá todas las cuentas de ingresos en la contabilidad e incluye títulos y subtotales. Puede cambiar el plan de tipos de coste, según sea necesario. Por ejemplo, puede eliminar los tipos de coste existentes duplicados.  

    > [!IMPORTANT]  
    >  La función **Registrar tipos de coste en plan ctas.** actualiza la relación entre el plan de cuentas y el plan de tipos de coste. El campo **Nº** se rellena y comprueba para asegurarse de que cada cuenta contable está relacionada con un solo tipo de coste. La función se ejecuta automáticamente antes de transferir los movimientos de contabilidad a la contabilidad de costes.  

### Configurar nuevos tipos de coste en la página Tipos centros coste

1. Abra la página **Plan tipos coste** en el modo de edición.  
2. Rellene los campos descritos como necesarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Puede configurar y mantener tipos de coste en la página **Ficha tipo de coste** o bien en la página **Plan tipos coste**. En este procedimiento, va a configurar tipos de coste en la página **Plan de tipos de coste**.

3. Una vez creados todos los tipos de coste, elija la acción **Aplicar sangría a tipos coste**. En el cuadro de diálogo, elija el botón **Sí**.  
4. Vincule el nuevo tipo de coste a la cuenta de contabilidad correspondiente.  

    > [!IMPORTANT]  
    >  Si se han escrito definiciones en el campo **Totales** para las cuentas de tipo **Fin-Total** antes de ejecutar la función **Aplicar sangría a tipos coste**, deberá volver a escribir las definiciones más adelante porque la función sobrescribe los valores de todos los campos **Fin-Total**.  

### Para actualizar tipos de coste

1. En la página **Configuración contabilidad costes**, seleccione si desea que el plan de tipos de coste se actualice automáticamente cuando el plan de cuentas se cambia.  
2. En el campo **Alinear cuenta C/G** puede seleccionar de entre las siguientes opciones.  

- **Sin alineación**: no hay cambio aplicable en el plan de tipos de coste cuando se modifica el plan de cuentas.  
- **Automático**: se realiza el cambio correspondiente en el plan de tipos de coste cuando se modifica el plan de cuentas.  
- **Solicitud**: se muestra un mensaje que pregunta si desea realizar a cambio correspondiente en el plan de tipos de coste cuando se realiza un cambio en el plan de cuentas.

## Definición de la relación entre los tipos de coste y las cuentas de contabilidad

La relación entre el tipo de coste y la cuenta de contabilidad se crea en el tipo de coste y en la cuenta de contabilidad.  

- El campo **Intervalo cuenta C/G** en la tabla **Tipo coste** establece qué cuentas de contabilidad pertenecen a un tipo de coste.  
- El campo **Nº tipo coste** en el plan de cuentas establece a qué tipo de coste pertenece una cuenta de contabilidad.  

Estos dos campos se rellenan automáticamente cuando utiliza la función **Obtener tipos coste de plan ctas.**  

### Relación entre las cuentas de contabilidad y los tipos de coste

Existe una relación n:1 entre las cuentas de contabilidad y los tipos de coste Varias cuentas de contabilidad pueden pertenecer a un tipo de coste, pero cada cuenta de contabilidad pertenece a sólo un tipo de coste. La siguiente tabla describe los detalles de la relación.  

|Relaciones|**Intervalo cuenta CG**|**Nº tipo coste**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Una cuenta de contabilidad para cada tipo de coste|Cuentas contables|Un tipo de coste|  
|Varias cuentas de contabilidad para un tipo de coste|Intervalo de cuenta de contabilidad, por ejemplo, 7110..7193 para cada cuenta de contabilidad|Para cada cuenta de contabilidad del intervalo, existe únicamente un tipo de coste|  
|Tipos de coste sin las cuentas de contabilidad correspondientes|\<Empty\>||  
|Cuentas de contabilidad cuyos movimientos no se transferirán||\<Empty\>|  

### Tipos de coste sin una relación con la contabilidad

Un tipo de coste puede no tener una relación con las cuentas contables si una de las siguientes condiciones es verdadera:  

- Las cuentas para la contabilidad operativa, como Calc. intereses y amortización, sólo toman costes de la contabilidad operativa.  
- Los tipos de coste de ayuda, como los tipos de coste 9901, 9902 y 9903, en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)], se utilizan como cuentas de crédito y débito para asignaciones.  
- La cuenta de ayuda, 9920 en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)], contiene las acumulaciones reales que muestran la diferencia entre los costes y el gasto de contabilidad.

## Configuración de centros de coste

Los centros de coste son departamentos que son responsables de los costes y de los ingresos. El plan de centros de coste es similar a la información de dimensión de contabilidad. Puede configurar el plan de centros de coste de la siguiente forma:  

- Transfiera los valores de dimensión en la contabilidad al plan de centros de coste. Puede hacer los ajustes necesarios después de la transferencia.  
- Cree un nuevo plan de centro de coste que es independiente de la contabilidad o agregue un nuevo centro de coste a un plan existente de centro de coste. Debe crear cada centro de coste por separado.  

### Para transferir los valores de dimensión en la contabilidad al plan de centros de coste

1. Configure una dimensión para que sea la dimensión del centro de coste en la página **Actualizar dimensiones contabilidad costes**. Sólo los valores de esta dimensión se transfieren.  
2. Elija el icono ![Bombilla que abre la función Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan centros coste** y luego elija el enlace relacionado.  
3. En la pestaña **Acciones**, en el grupo **Funciones**, seleccione **Traer centros de coste de dimensión** para transferir los valores de dimensión al plan de centros de coste. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión centro coste** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de centros de coste. No puede definir una sincronización del plan de centros de coste a los valores de dimensión de la contabilidad.  

El plan de centros de coste contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

### Crear nuevos centros de coste en la página Plan centros coste

Puede configurar y mantener centros de coste en la ficha **Ficha centro de coste** o bien en la página **Plan centros coste**. En este procedimiento, va a configurar centros de coste en la página **Plan de centros de coste**.  

1. Abra la página **Plan centros coste** en el modo de edición.  
2. En el campo **Código**, introduzca el código del centro de coste. Todos los centros de coste deben disponer de un código.  
3. En el campo **Nombre**, introduzca el nombre del centro de coste.  
4. Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del centro de coste.  

    - Para los centros de coste de la línea **Total** debe rellenar el campo **Totales**. Utilice el operador **or**, que es una línea vertical (**&#124;**) para establecer rangos de centros de coste.  
    - Para centros de coste del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Aplicar sangría.  
5. Rellene los campos **Orden clasificación** y **Subtipo de coste** .  
6. Seleccione la siguiente línea vacía para crear un centro de coste nuevo y, a continuación, repita del paso 2 al 5.  
7. Cuando haya configurado todos los centros de coste, elija la acción **Aplicar sangría a centros coste**. Elija el botón **Sí**.  

> [!IMPORTANT]  
> Si ha introducido definiciones en los campos **Totales** para los centros de coste de **Total-final** antes de ejecutar la función Aplicar sangría, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.

## Configuración de objetos de coste

Los objetos de coste son proyectos, productos o servicios de una empresa. El plan de objetos de coste es similar a la información de dimensión de contabilidad. Puede configurar el plan de objetos de coste de la siguiente forma:  

* Transfiera los valores de dimensión en la contabilidad al plan de objetos de coste. Puede hacer los ajustes necesarios después de la transferencia.  
* Cree un plan del objeto de coste que es independiente de la contabilidad o agregue un objeto de coste nuevo a un plan existente de objetos de coste. Debe crear cada objeto de coste por separado.  

### Para transferir valores de dimensión de la contabilidad al plan de objetos de coste

1.  Configurar una dimensión para que sea la dimensión del objeto de coste en la página **Actualizar dimensiones CA**. Sólo los valores de esta dimensión se transfieren.  
2.  Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan objetos coste** y luego elija el enlace relacionado.  
3.  Elija la acción **Traer objetos coste de dimensión** para transferir los valores de dimensión al plan de objetos de coste. La función transfiere los valores de dimensión que definió en el paso 1.  

    > [!NOTE]  
    >  Puede configurar el campo **Alinear dimensión objeto coste** para definir una sincronización unidireccional de los valores de dimensión de la contabilidad al plan de objetos de coste. No puede definir una sincronización del plan de objetos de coste a los valores de dimensión de la contabilidad.  

El plan de objetos de coste contendrá ahora todos los valores de dimensión especificados desde la contabilidad e incluirá títulos y subtotales.  

### Crear nuevos objetos de coste en la página Plan objetos coste

Puede configurar y mantener objetos de coste en la ficha **Plan objeto de coste** o bien en la página **Plan objetos coste**. En este procedimiento, va a configurar objetos de coste en la página **Plan de objetos de coste**.  

1.  Abra la página **Plan objetos coste** en el modo de edición.  
2.  En el campo **Código**, introduzca el código del objeto de coste. Todos los objetos de coste deben disponer de un código.  
3.  En el campo **Nombre**, introduzca el nombre del objeto de coste.  
4.  Seleccione la flecha desplegable del campo **Tipo línea** para especificar la finalidad del objeto de coste.  

    * Para los objetos de coste de la línea **Total** debe rellenar el campo **Total desde/a**. Utilice el operador **or**, que es una línea vertical (**&#124;**), para establecer rangos de objetos de coste.  
    * Para objetos de coste del tipo de línea **Total final**, este campo se rellena automáticamente cuando utiliza la función Aplicar sangría.  
5.  Rellene el campo **Orden clasificación**.  
6.  Seleccione la siguiente línea vacía para crear un objeto de coste nuevo y, a continuación, repita del paso 2 al 5.  
7.  Cuando haya configurado todos los objetos de coste, elija la acción **Aplicar sangría a objetos coste**. Elija el botón **Sí**.  

> [!IMPORTANT]  
>  Si ha introducido definiciones en los campos **Total desde/a** para los objetos de coste de **Total final** antes de ejecutar la función Aplicar sangría, deberá volver a introducirlas. La función sobrescribe los valores de todos los campos de **Total final**.

## Definición de centros de coste y de objetos de coste para el plan de cuentas

Puede transferir automáticamente los movimientos de gastos y de ingresos de la contabilidad a la contabilidad de costes para cada registro de contabilidad o con un trabajo por lotes. Cuando lleva a cabo la transferencia, [!INCLUDE[prod_short](includes/prod_short.md)] transfiere sólo los movimientos ya vinculados a un centro o un objeto de coste. Para establecer una transferencia significativa, debe asegurarse de que los centros de coste y los objetos de coste están definidos correctamente.  

### Definición de los valores de dimensión predeterminados para cuentas de contabilidad

Para cada cuenta de contabilidad, puede definir valores de dimensión predeterminados de la tabla **Dimensión predeterminada**. El siguiente ejemplo muestra cómo definir que siempre debe haber un centro de coste de DEPARTAMENTO, pero nunca un objeto de coste de PROYECTO al registrar en una cuenta de contabilidad.  

|**Cód. dimensión**|**Registro valor**|  
|------------------------------------------|-----------------------------------------|  
|Departamento|Código obligatorio|  
|Programa|Sin código|  

### Definición de valores de dimensión para costes generales y costes directos

 Puede transferir costes generales a un centro de coste y costes directos a un objeto de coste. La siguiente tabla muestra la combinación óptima de valores de configuración de dimensión.  

|Transferir a|Registro del centro de coste|Registro del objeto de coste|  
|-----------------|-------------------------|-------------------------|  
|Centro coste|Código obligatorio|Sin código|  
|Objeto coste|Sin código|Código obligatorio|  

> [!NOTE]  
>  Para garantizar que el centro de coste y el objeto de coste predefinidos que configuró en la contabilidad sean transportados automáticamente a la contabilidad de costes, seleccione la casilla **Comprobar registros C/G** en la página Configuración contabilidad costes.

## Consulte también .

[Contabilidad de costes](finance-manage-cost-accounting.md)  
[Transferir y registrar movimientos de coste](finance-transfer-and-post-cost-entries.md)  
[Definición y asignación de costes](finance-define-and-allocate-costs.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
