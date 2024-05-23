---
title: Trabajar con periodos contables y ejercicios
description: Obtenga información sobre cómo trabajar con períodos contables para definir cuándo empresa elabora los informes de rendimiento financiero.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '100,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Trabajar con periodos contables y años fiscales

Los períodos contables, también conocidos como períodos de información, son períodos de tiempo en los que una empresa u organización informa del rendimiento financiero, por ejemplo, generando su balance de ingresos o su balance. Normalmente, los períodos contables se refieren al ejercicio de la empresa, que puede contener varios períodos contables, como meses o trimestres.

Para muchas empresas, el año fiscal no se alinea con el año calendario, por ejemplo, cuando el año fiscal finaliza el 30 de junio en lugar del 31 de diciembre. En el caso de las empresas de nueva creación, el período fiscal podría incluso ser superior a 12 meses.  

[!INCLUDE[prod_short](includes/prod_short.md)] solo requiere períodos contables si se desea cerrar un balance de ingresos o ejecutar tareas de compresión de datos.

Puede usar periodos contables en informes, como cuando revisa los movimientos registrados en la página **Saldo/Presupuesto**, donde se puede especificar el intervalo de informes. Una de las opciones que puede especificar para crear informes por período contable. También puede crear un informe financiero que compare los resultados de diferentes períodos contables.

## Creación de un nuevo ejercicio

Puede crear períodos contables en bloque, utilizando el proceso **Crear ejercicio** o manualmente.

### Cómo crear períodos contables en bloque

Utilice el proceso **Crear ejercicio** para dividir un ejercicio en periodos de igual duración.  

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") , escriba **Periodos contables** y luego elija el enlace relacionado.  
2. Elija la acción **Crear ejercicio**.
3. En el campo **Fecha inicial**, introduzca la fecha en la que comienza el ejercicio.  
4. En el campo **Nº de periodos** especifique el número de ejercicios económicos en que se dividirá el ejercicio. Puede haber hasta 365 periodos en un año.  
5. En el campo **Longitud período**, introduzca una duración para cada período. Los identificadores de duración incluyen, por ejemplo, 1M para un mes, 1T para un trimestre y 1Y para un año.  
6. Elija **Aceptar**.  

### Cómo crear períodos contables manualmente

Si los períodos contables de su ejercicio tienen duraciones diferentes, como el calendario 4-4-5 utilizado en comercio minorista, puede configurarlo manualmente.  
  
1. Elija el icono ![Buscar página o informe.](media/ui-search/search_small.png "Icono Buscar página o informe") , escriba **Periodos contables** y luego elija el enlace relacionado.  
2. En el campo **Fecha inicial**, introduzca la fecha en la que comienza el ejercicio. El campo **Nombre** mostrará el nombre del mes.  
3. Seleccione la casilla de verificación **Principio ejercicio** para indicar que es el primer periodo del ejercicio. [!INCLUDE[prod_short](includes/prod_short.md)] utilizará este periodo para determinar los periodos para cerrar al final del año.
4. Repita los pasos 2 y 3 con cada periodo restante.  

## Cierre de un ejercicio

Cerrar el ejercicio es una de las tareas para cerrar los libros. Después de cerrar un ejercicio, se seleccionan las casillas **Cerrado** y **Fecha bloqueada** de todos los periodos del ejercicio. No puede volver a abrir un ejercicio ni desmarcar las casillas.

> [!NOTE]  
> Debe tener al menos un ejercicio abierto. Al cerrar un ejercicio, asegúrese de que se ha creado un nuevo ejercicio. Además, tenga en cuenta que después de cerrar un ejercicio, no puede cambiar la fecha de inicio del ejercicio siguiente.

1. Elija el icono ![Buscar página o informe.](media/ui-search/search_small.png "Icono Buscar página o informe") , escriba **Periodos contables** y luego elija el enlace relacionado.  
2. Elija la acción **Cerrar ejercicio**.  

## Registro de movimientos en un ejercicio cerrado

Aunque un ejercicio esté cerrado, todavía podrá registrar en él movimientos de contabilidad. Al hacerlo, los movimientos se marcan como registrados en un ejercicio cerrado y se seleccionará la casilla **Asiento post-cierre**. De forma predeterminada, la casilla no se muestra en la página, pero puede agregarla. Los siguientes pasos son cerrar las cuentas de regularización y transferir los resultados del ejercicio a una cuenta en el balance. Repita estos pasos cada vez que registre movimientos en un ejercicio cerrado.

## Consulte también .

[Cerrar los libros](year-close-books.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Cómo trabajar con informes financieros](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
