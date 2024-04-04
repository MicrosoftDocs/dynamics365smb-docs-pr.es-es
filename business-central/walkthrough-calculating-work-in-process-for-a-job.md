---
title: 'Tutorial: cálculo del trabajo en curso para un proyecto'
description: 'Los proyectos implican el consumo de horas de mano de obra, horas de maquinaria, productos de inventario y otros tipos de consumo que se deben controlar a medida que avanza un proyecto.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-calculating-work-in-process-for-a-project"></a>Tutorial: cálculo del trabajo en curso para un proyecto

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Con proyectos, puede programar el uso de los recursos de su empresa y realizar un seguimiento de los diversos costes asociados con el uso de recursos en un proyecto específico. Los proyectos implican el consumo de horas de mano de obra, horas de maquinaria, productos de inventario y otros tipos de consumo que se deben controlar a medida que avanza un proyecto. Si un proyecto se extiende durante un periodo prolongado, es posible que desee transferir estos costes a una cuenta de Trabajo en curso (WIP) en el balance mientras se realiza el proyecto. De este modo, podrá identificar los costes y ventas en las cuentas de regularización cuando sea apropiado.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial

 En este tutorial se ilustran las siguientes tareas:  

-   Cálculo de WIP.  
-   Selección de un método de cálculo de WIP.  
-   Exclusión de parte de un proyecto del WIP.  
-   Registro del WIP en la contabilidad.  
-   Reversión de un registro WIP.  

 Cada paso del proceso calcula el valor y mueve las transacciones del proyecto a la contabilidad. Los pasos de cálculo y registro son independientes, para que pueda revisar los datos y realizar modificaciones antes de registrar en la contabilidad. Por lo tanto, debe asegurarse de que toda la información sea correcta después de ejecutar los trabajos por lotes de cálculos y antes de ejecutar los trabajos por lotes de registro.  

## <a name="roles"></a>Funciones

 En este tutorial se utiliza al miembro del equipo del proyecto (Tricia) como personaje.  

## <a name="prerequisites"></a>Requisitos previos

 Para poder realizar las tareas del tutorial, [!INCLUDE[prod_short](includes/prod_short.md)] debe estar instalado en su ordenador:  

## <a name="story"></a>Historia

 Este tutorial se centra en la empresa CRONUS España S.A., una empresa de diseño y consultoría que diseña y ajusta nuevas infraestructuras, (como salas de conferencias y oficinas) con mobiliario, accesorios y unidades de almacenamiento. La mayor parte del trabajo en CRONUS está orientado al proyecto y Tricia, un miembro del equipo de proyecto, utiliza los trabajos para tener una visión general de cada trabajo en curso que CRONUS ha iniciado y también los trabajos que se han completado. Algunos de los proyectos pueden ser largos y pueden durar varios meses. Tricia puede usar un Cuenta WIP para registrar el trabajo en curso y realizar el seguimiento de los costes del proyecto.  

## <a name="calculating-wip"></a>Cálculo de WIP

 CRONUS ha contratado un proyecto extenso que ahora se ha ampliado a varios periodos de registro. Tricia, un miembro de equipo de proyecto, calcula el trabajo en curso (WIP) para garantizar que el informe financiero de la empresa es preciso.  

 Durante este procedimiento, Tricia selecciona un grupo específico de tareas que se incluye en el cálculo de WIP. En la página **Líneas de tarea proyecto**, Tricia puede especificar estas líneas en la columna **WIP-Total**.  

 La siguiente tabla describe las tres opciones.  

|Campo|Description|  
|-------------------------------------|---------------------------------------|  
|**\<blank\>**|Deje el campo en blanco si la tarea del proyecto es parte de un grupo de tareas.|  
|**Total**|Define el rango o grupo de tareas que se incluyen en el cálculo del WIP y del reconocimiento. En el grupo, cualquier tarea de proyecto con **Tipo tarea proyecto** definido como **Registro** se incluirá en el total WIP, a menos que el campo **Total WIP** se defina como **Excluido**.|  
|**Excluido**|Se aplica sólo a una tarea con el **Tipo tarea proyecto** **Registro**. La tarea no se incluye cuando se calcula el WIP y el reconocimiento.|  

 En el siguiente tutorial, Tricia aplica el método de Valor de coste, su estándar de la empresa, para calcular el WIP. Tricia especifica la parte del trabajo que se incluye en el cálculo de WIP, asignando los valores WIP-Total a diversas líneas de tareas del proyecto.  

### <a name="to-calculate-wip"></a>Para calcular WIP

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
2.  En la lista **Proyectos**, seleccione el proyecto **Reno** y, después, seleccione **Editar**. Se abre la ficha de proyecto en modo edición.  

     WIP se puede calcular basándose en Valor coste, Valor venta, Coste ventas, Porcentaje completado o Contrato consumado. En este ejemplo, CRONUS utiliza el método de Valor del coste.  

3.  En la ficha desplegable **Registro**, elija el campo **Método WIP** y seleccione **Valor coste**.  
4.  Seleccione la acción **Líneas de tarea de proyecto** y defina los valores siguientes en el campo **WIP-Total**.  

     La siguiente tabla describe los valores.  

    |Nº tarea proyecto|Campo WIP-Total|  
    |------------------|----------------------|  
    |1130|Excluido|  
    |1190|Total|  
    |1210|Excluido|  
    |1310|Excluido|  

5.  Seleccione la acción **WIP** y, a continuación elija la acción **Calcular WIP**.  
6.  En la página **Calcular WIP proyecto**, puede seleccionar un proyecto para el cual desea calcular WIP. En la ficha desplegable **Proyecto**, seleccione **Deerfield** en el campo **Nº** .  
7.  En el campo **Fecha registro**, introduzca una fecha posterior a la fecha de trabajo.
8.  En el campo **Nº documento**, escriba **1**. Esto crea un documento a la que podrá hacer referencia posteriormente para la trazabilidad.  
9. Elija el botón **Aceptar** para iniciar el trabajo por lotes. Aparece un mensaje. Elija el botón **Aceptar** para continuar. Cierre la página **Líneas tarea proyecto**.  

    > [!NOTE]  
    >  El mensaje indica que hay advertencias asociadas al cálculo del WIP. Revisará las advertencias en el siguiente procedimiento.  

10. En la ficha **Proyecto**, expanda la ficha desplegable **Trabajo en curso y reconocimiento** para ver los valores calculados. También puede ver la **Fecha registro WIP** y los valores que se han registrado en la contabilidad general, si existe.  

 Observe que el valor de **Importe costes reconoc.** es 215,60 en la columna **Para registrar**. Esto refleja los costes totales de dos de los productos en el grupo de las tareas 1110 - 1130 del trabajo. El tercer producto se estableció en **Excluido** y, por lo tanto, no se incluye en el cálculo del WIP.  

### <a name="to-review-wip-warnings"></a>Para revisar las advertencias WIP

1.  Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cabina WIP proyecto** y luego elija el enlace relacionado.  
2.  Seleccione el proyecto **Reno** y, a continuación, seleccione la acción **Mostrar advertencias**.  
3.  En la página **Advertencias WIP proyecto**, revisar la advertencia asociada con el proyecto.  

 Después de finalizar el periodo contable, Tricia debe volver a recalcular el WIP para incluir el trabajo completado hasta este momento.  

### <a name="to-recalculate-wip"></a>Para volver a calcular WIP

1.  En la ficha **Proyecto**, seleccione la acción **Movimientos WIP** para ver el cálculo de WIP.  

     La página **Movs. WIP proyecto** muestra los últimos movimientos de WIP calculados en un proyecto, aún si el WIP todavía no se ha registrado en contabilidad.  

2.  Puede seguir los pasos del procedimiento que explica cómo calcular el WIP para volver a calcular el WIP. Cada vez que se calcula WIP, se crea un movimiento en la página **Movs. WIP proyecto**.  
3.  Cierre la página.  

> [!NOTE]  
>  Solamente se calcula el trabajo en curso y el reconocimiento. No se registra en contabilidad. Para hacerlo, es necesario ejecutar el proceso **Registrar WIP en C/G** después de haber calculado Trabajo en curso y reconocimiento.

## <a name="posting-wip-to-general-ledger"></a>Registro de WIP en contabilidad

 Ahora que Tricia ha calculado el WIP para este proyecto, puede registrarlo en la contabilidad general.  

### <a name="to-post-wip-to-general-ledger"></a>Para registrar un WIP en contabilidad

1.  En la lista **Proyectos**, seleccione el proyecto **Reno**.  
2.  Seleccione la acción **WIP** y, a continuación elija la acción **Resgistrar WIP en C/G**.  
3.  En la página **Registrar WIP en C/G proyecto**, en la ficha desplegable **Proyecto**, seleccione **Reno** en **Nº**. .  
4.  En la ficha desplegable **Opciones**, en el campo **Nº documento reversión**, escriba **1**.  
5.  Elija el botón **Aceptar** para registrar WIP a la contabilidad general.  
6.  Elija el botón **Aceptar** para cerrar la página de confirmación.  

     Una vez completado el registro, puede ver la información de registro en la página **Movs.contabilidad WIP**.  

7.  En la lista **Proyectos**, seleccione el proyecto **Reno** y, después, seleccione **Movimientos WIP C/G**.  

     En la página **Movs. C/G WIP proyecto**, compruebe que el WIP se haya registrado en la contabilidad.  

8.  Cierre la página.  
9. Abra la ficha **Proyecto** del proyecto **Reno**.  
10. En la ficha desplegable **Trabajo en curso y reconocimiento**, observe que la columna de **Registrado**, el campo de **Recog. Importe de contabilidad de los costes** ahora está introducido, lo que indica que el WIP se registró en la contabilidad general correctamente.  
11. Elija el botón **Aceptar** para cerrar la ficha.  

## <a name="reversing-a-wip-posting"></a>Reversión de un registro WIP

 Tricia determina que las tareas del proyecto que se excluyeron de cálculo del WIP deben haberse calculado en el WIP. Tricia puede revertir las contabilidades incorrectas sin tener que contabilizar nuevos movimientos de WIP.  

### <a name="to-reverse-a-wip-posting"></a>Para revertir un registro WIP

1.  En la lista **Proyectos**, seleccione el proyecto **Reno**.  
2.  Seleccione la acción **WIP** y, a continuación elija la acción **Resgistrar WIP en C/G**.  
3.  En la página **Registrar WIP en C/G proyecto**, en la ficha desplegable **Proyecto**, seleccione **Reno** en **Nº**. .  
4.  En la ficha desplegable **Opciones**, en el campo **Nº documento reversión**, escriba **1**.  
5.  Especifique la fecha de registro original en el campo **Fecha registro reversión**. Debe ser la misma fecha que la que se usó para calcular el WIP la primera vez.  
6.  Seleccione la casilla **Solo reversión**. De este modo, se revierte el WIP registrado previamente, pero sí se registra el nuevo WIP en la contabilidad.  
7.  Elija el botón **Aceptar** para ejecutar el trabajo por lotes y seleccione el botón **Aceptar** para cerrar la página de confirmación.  
8.  Abra la ficha **Proyecto** para **Reno**.  
9. En la ficha desplegable **Trabajo en curso y reconocimiento**, verifique que no haya movimientos registrados de WIP.  
10. Cierre esta página.  
11. En la lista de **Proyectos**, seleccione el proyecto **Reno**, seleccione la acción **WIP** y, a continuación, elija la acción **Movimientos de contabilidad del WIP**. Los movimientos WIP tienen la casilla **Revertido** activada.  
12. Cierre esta página.  
13. Abra **Líneas tarea proyecto** del proyecto, incluya las partes del proyecto que deben incluirse en el cálculo de WIP y, a continuación, vuelva a calcular y registre el nuevo valor en la contabilidad.  

    > [!NOTE]  
    >  Suponga el WIP calculado y registrado de Tricia para un proyecto con fechas incorrectas. Después del método que se ha discutido anteriormente, Tricia puede revertir los asientos incorrectos, corregir las fechas y volver a la contabilidad general.  

## <a name="next-steps"></a>Pasos siguientes

 Este tutorial le ha enseñado a calcular el trabajo en curso en [!INCLUDE[prod_short](includes/prod_short.md)]. En proyectos más grandes, es posible que resulte útil transferir los costes a una cuenta WIP periódicamente mientras se completa el proyecto. Este tutorial le ha mostrado cómo excluir líneas de tarea de un cálculo. También le muestra cuándo tiene que calcular de nuevo. Y finalmente, este tutorial demuestra la forma de registrar el WIP en la contabilidad general. También se incluye un ejemplo de cómo revertir un WIP que registra la contabilidad general.  

## <a name="see-also"></a>Consulte también

 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
 [Tutorial: administración de programas con proyectos](walkthrough-managing-projects-with-jobs.md)  
 [Comprensión de los métodos WIP](projects-understanding-wip.md)  
 [Controlar el progreso y el rendimiento](projects-how-monitor-progress-performance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
