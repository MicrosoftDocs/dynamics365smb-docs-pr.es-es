---
title: "Tutorial: administración de programas con proyectos | Documentos de Microsoft"
description: "Este tutorial le presenta a las funciones de administración de programas en los trabajos. Los proyectos le permiten programar el uso de los recursos de su empresa y realizar un seguimiento de los diversos costes asociados con los recursos de un proyecto específico. Los proyectos implican el consumo de horas de mano de obra, horas de maquinaria, productos de inventario y otros tipos de consumo que es posible que desee controlar a medida que avance un proyecto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b6a61a9c5d2b8c7b3d197780c580c8bcf957560e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-managing-projects-with-jobs"></a>Tutorial: administración de programas con proyectos
Este tutorial le presenta a las funciones de administración de programas en los trabajos. Los proyectos le permiten programar el uso de los recursos de su empresa y realizar un seguimiento de los diversos costes asociados con los recursos de un proyecto específico. Los proyectos implican el consumo de horas de mano de obra, horas de maquinaria, productos de inventario y otros tipos de consumo que es posible que desee controlar a medida que avance un proyecto.  

 En este tutorial, se trata la configuración de un nuevo proyecto, además de las tareas más comunes, como gestión de precios fijos, creación de pagos a plazo, registro de facturas de proyectos y copia de proyectos.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial  
 En este tutorial, se demuestran las siguientes tareas:  

### <a name="setting-up-a-job"></a>Configuración de un proyecto  
 Con la configuración de la estructura del presupuesto para los trabajos, crear un trabajo es directo. Este tutorial trata los siguientes procedimientos:  

-   Configuración de líneas de planificación y líneas de tarea de un proyecto.  
-   Creación de precios específicos de proyectos para productos y cuentas.  
-   Facturación a partir de un proyecto.  

### <a name="handling-fixed-prices"></a>Gestión de precios fijos  
 En proyectos, puede gestionar precios fijos y precios de servicios o mercaderías que se acuerdan por adelantado con los clientes. En este tutorial, puede hacer lo siguiente:  

-   Ver cómo se determinan los valores de facturas y contratos.  
-   Permitir trabajo adicional en el programa que no se ha facturado.  

### <a name="copying-a-job"></a>Copia de un proyecto  
 Esta parte del tutorial se centra en cómo copiar una parte o la totalidad de un proyecto para reducir la introducción manual de datos y mejorar la precisión. Incluye lo siguiente:  

-   Copia de parte de un proyecto en un proyecto nuevo.  
-   Copia de precios específicos de proyectos.  
-   Copia de líneas de planificación.  

### <a name="making-payment-by-installment"></a>Creación de pagos a plazos  
 Cuando un proyecto amplio y caro tiene una larga duración, el cliente suele llegar a un acuerdo con la empresa para pagar a plazos. Este ejemplo muestra cómo configurar pagos a plazo y trata lo siguiente:  

-   Creación de pagos a plazo para un proyecto.  
-   Facturación de pagos a clientes.  
-   Cómo tener en cuenta el uso en un proyecto de pagos a plazo.  

## <a name="roles"></a>Funciones  
 En este tutorial se incluyen tareas para las siguientes funciones:  

-   Director de proyectos  
-   Miembro del equipo del proyecto  

## <a name="prerequisites"></a>Requisitos previos  
 Para poder realizar las tareas del tutorial, deberá hacer lo siguiente:  

-   Instale la base de datos de demostración CRONUS International Ltd.
-   Cree datos de ejemplo como indican los pasos de la siguiente sección.  

## <a name="story"></a>Historia  
Este tutorial se centra en la empresa CRONUS International Ltd., una empresa de diseño y consultoría que diseña y ajusta nuevas infraestructuras, (como salas de conferencias y oficinas) con mobiliario, accesorios y unidades de almacenamiento. La mayor parte de su trabajo está orientado a los proyectos. Prakash es un director de proyectos de CRONUS. Utiliza proyectos para darle un panorama de cada proyecto en curso que CRONUS ha iniciado, además de los proyectos finalizados. Normalmente es uno de los que trata con los clientes e introduce el núcleo del proyecto, que son líneas de tareas y de planificación, además de los precios, en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Observa que crear, mantener y revisar la información es directo. Prakash también considera positiva la forma en que [!INCLUDE[d365fin](includes/d365fin_md.md)] activa copiar los trabajos y el pago por plazos.

 Tricia, miembro del equipo del proyecto que depende de Prakash, es la responsable de supervisar el día a día del proyecto. Ella introduce su propio trabajo además del trabajo realizado por técnicos en cada tarea. Ella registra los productos que han utilizado y los costes en los que han incurrido.  

## <a name="preparing-sample-data"></a>Preparación de datos de ejemplo  
 Para prepararse para este tutorial, deberá añadir a Tricia como un recurso nuevo.  

### <a name="to-prepare-the-sample-data"></a>Para preparar los datos de ejemplo  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recursos** y, a continuación, seleccione el vínculo relacionado.  
2.  Selecione la acción **Nuevo** para crear una nueva ficha de recursos.  
3.  En la ficha desplegable **General**, introduzca la siguiente información:  

    - **Nº**: **Tricia**  
    - **Nombre**: **Tricia**  
    - **Tipo**: **Persona**  

4.  Seleccione el campo **Unidad de medida base** y seleccione la acción **Nuevo** para abrir la ventana **Unidad de medida de recursos**. En el campo **Código**, seleccione **Hora**. Elija el botón **Aceptar**.  
5.  En la ficha desplegable **Facturación**, escriba la siguiente información:  

    -   **Coste unit. directo**: **5**  
    -   **% Coste indirecto**: **4**  
    -   **Coste unitario**: **10**  
    -   **Grupo contable producto**: **Servicios**  
    -   **Grupo registro IVA prod.**: **IVA 25**  

6.  Elija el botón **Aceptar** para guardar los cambios.  

 En el siguiente procedimiento, cree una sección diario proyecto para Tricia para registrar su utilización.  

### <a name="to-create-a-job-journal-batch"></a>Para crear una sección de diario de proyecto  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Diario proyecto**, seleccione el campo **Nombre sección**. Aparecerá la ventana **Secciones diario proyectos**.  
3.  Seleccione la acción **Nuevo**, para crear una línea con la siguiente información:  

    -   **Nombre**: **Tricia**  
    -   **Descripción**: **Tricia**  
    -   **Nos. serie**: **JJNL-GEN**  

4.  Elija el botón **Aceptar** para cerrar todas las ventanas abiertas.  

## <a name="setting-up-a-job"></a>Configuración de un proyecto  
 En este escenario, CRONUS ha ganado un contrato con un cliente, Progressive Home Furnishings, para diseñar una sala de conferencias y un refectorio. El cliente tiene su sede en los Estados Unidos y el proyecto precisa un software especial. El director del proyecto llega a un acuerdo con el cliente y crea un proyecto que cubra el acuerdo.  

### <a name="to-set-up-a-job"></a>Para configurar un proyecto  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  Selecione la acción **Nuevo** para crear una nueva ficha.  
3.  En la ficha desplegable **General**, introduzca la siguiente información:  

    -   **Descripción**: **Asesoramiento en el equipamiento de la sala de conferencias**  
    -   **Factura-a Nº cliente**: **01445544**  

4.  En la ficha desplegable **Registro**, escriba la siguiente información:  

    -   **Estado**: **Pedido**  
    -   **Grupo contable proyecto**: **Equipar**  
    -   **Método WIP**: **Valor coste**  

5.  En la ficha desplegable **Duración**, escriba la fecha de hoy en los campos **Fecha inicial** y **Fecha final**. Estas fechas ayudarán a aplicar las conversiones de divisas cuando se facture el proyecto.  
6.  En la ficha desplegable **Comercio exterior**, defina el código de divisa en **USD**. Si selecciona USD en el campo **Código divisa de factura**, el proyecto se facturará en dólares estadounidenses y se planificará solo en la divisa local de CRONUS.  

 Puede personalizar el precio para los clientes por cada proyecto, en función de los contratos que ha configurado. En el siguiente procedimiento, el director de proyectos especifica un coste para el tiempo de Tricia, define el precio del software correspondiente y añade en el viaje costes que el cliente ha acordado pagar.  

### <a name="to-customize-pricing"></a>Para personalizar los precios  

1.  Desde la ficha de proyecto, elija la acción **Recurso**.  
2.  En la ventana **Precios recursos proyecto**, escriba la siguiente información:  

    -   **Código**: **Tricia**  
    -   **Precio venta**: **20**  

3.  Seleccione el botón **Aceptar** para cerrar la ventana.  
4.  Elija la acción **Producto**.  
5.  En la ventana **Precios productos proyecto**, escriba la siguiente información y el precio personalizado:  

    1.  **Nº producto**: **80201 (Programa gráfico)**  
    2.  **Precio venta**: **200**  

6.  Seleccione el botón **Aceptar** para cerrar la ventana.  
7.  Elija la acción **Cuentas C/G**.  
8.  En la ventana de **precios de la cuenta de proyectos**, introduzca la siguiente información y el coste de viaje, para el que el cliente ha acordado pagar el coste además de un porcentaje del 25% :  

    1.  **Cuenta**: **8430 (Viajes)**  
    2.  **Factor coste unitario**: **1,25**  

9. Elija el botón **Aceptar** para cerrar la ventana.  

 Los pasos finales en la configuración de un trabajo añaden las tareas del trabajo y las líneas de planificación que forman parte de cada tarea. Las líneas de planificación determinan qué se factura al cliente.  

### <a name="to-add-job-tasks"></a>Para agregar tareas de proyecto  

1.  En la ficha **Proyecto** para el nuevo proyecto, seleccione la acción **Líneas de tarea de proyecto** .  
2.  La siguiente tabla describe la información que tiene que debería introducir en los campos.  

    |N.º tarea de trabajo|Description|Tipo de tarea de trabajo|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Consultoría sobre la equipación de salones|Principio-Total|  
    |1010|Reunión de consulta con el cliente|Auxiliar|  
    |nº 1020|Desarrollo|Auxiliar|  
    |1090|Total de consultoría|Fin Total|  

3.  Para indicar que algunas tareas son subcategorías de otras tareas, en la pestaña de **Acciones**, en el grupo de **Funciones**, seleccione **Indentar tareas proyecto**.  

 Una línea de planificación puede ser uno de los siguientes tipos:  

-   **Previsión**: Añadido a la previsión, pero no facturado.  
-   **Contrato**: Facturado, pero no añadido a la previsión.  
-   **Programa y contrato**: Facturado y añadido a la previsión.  

 En este tutorial, el director de proyectos utiliza **Programa y contrato**. Crea tres líneas de planificación para la tarea 1010, y dos líneas de planificación para la tarea 1020.  

### <a name="to-create-planning-lines"></a>Para crear líneas de planificación  

1.  Seleccione línea 1010 y, a continuación, elija la acción **Líneas de planificación de proyecto**. Escriba la siguiente información:  

     **Línea 1**  

    -   **Tipo línea**: **previsión y contrato**  
    -   **Fecha planif.**: **(fecha actual)**  
    -   **Tipo**: **recurso**  
    -   **Nº**: **Tricia**  
    -   **Cantidad**: **40**  

     **Línea 2**  

    -   **Tipo línea**: **Programa y contrato**  
    -   **Fecha planif.**: **(fecha actual)**  
    -   **Tipo**: **recurso**  
    -   **Nº**: **Alfredo**  
    -   **Cantidad**: **40**  

     **Línea 3**  

    -   **Tipo línea**: **previsión y contrato**  
    -   **Fecha planif.**: **(fecha actual)**  
    -   **Tipo**: **cuenta G/L**  
    -   **Nº**: **8430 (viaje)**  
    -   **Cantidad**: **2**  
    -   **Coste unitario**: **400**  

2.  Elija el botón **Aceptar** para cerrar la ventana. Los totales se actualizan en la ventana de **Líneas tarea proyecto**.  
3.  Seleccione línea 1020 y, a continuación, elija la acción **Líneas de planificación de proyecto**. Escriba la siguiente información:  

     **Línea 1**  

    -   **Tipo de línea**: **previsión y contrato**  
    -   **Fecha planif.**: **(fecha actual)**  
    -   **Tipo**: **recurso**  
    -   **Nº**: **Tricia**  
    -   **Cantidad**: **80**  

     **Línea 2**  

    -   **Tipo línea**: **previsión y contrato**  
    -   **Fecha planif.**: **(fecha actual)**  
    -   **Tipo**: **Producto**  
    -   **Nº**: **80201 (Programa gráfico)**  
    -   **Cantidad**: **1**  

4.  Elija el botón **Aceptar** para cerrar la ventana. Los totales se actualizan en la ventana de **Líneas tarea proyecto**.  

## <a name="calculating-remaining-usage"></a>Cálculo del uso restante  
 Tricia, el miembro del proyecto de equipo, ha estado trabajando en el proyecto durante algún tiempo y desea registrar sus horas y utilización en el proyecto. No ha trabajado más horas que las acordadas previamente con el cliente. Ella utiliza el trabajo por lotes **Cálc. uso restante** para calcular el uso restante para el proyecto en un diario respectivo. Para cada tarea, el trabajo por lotes calcula la diferencia entre el uso programado de productos, recursos y gastos de contabilidad, y el uso real registrado en los movimientos del proyecto. A continuación, se muestra el uso restante en el diario del proyecto, desde el cual puede registrarlo.  

### <a name="to-calculate-remaining-usage"></a>Para calcular el uso restante  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Diario proyectos**, en el campo **Nombre sección**, abra la lista **Secciones diario proyecto**. Seleccione la sección de diario de proyecto de **Tricia**.  
3.  Seleccione la acción **Cálcular uso restante**.  
4.  En la ventana de **Calc. uso restante proyecto**, en la ficha desplegable **Tarea proyecto**, elija el campo de **Nº proyecto** y seleccione el número de proyecto correspondiente, normalmente trabajo J00010.  
5.  En la ficha desplegable **Opciones**, escriba **J00001** en el campo **Nº documento**. Esto facilitará el futuro seguimiento del registro.  
6.  Escriba la fecha de hoy como fecha de registro.  
7.  Elija el botón **Aceptar**. De este modo, se generarán las líneas de diario del proyecto derivadas de las líneas de planificación que creó Prakash para el proyecto.  
8.  Elija el botón **Aceptar** en la ventana de confirmación. Las líneas generadas se añaden al diario del proyecto.  
9. Asegúrese de que todos los números del documento son J00001 y, a continuación seleccione la acción **Registrar**. Elija **Sí** para confirmar el registro.  
10. Ya se han registrado las líneas. Elija el botón **Aceptar** para cerrar las ventanas.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Creación y registro de una factura de ventas de proyecto  
 A continuación, Tricia puede crear una factura nueva para el trabajo completo o para parte de un trabajo. También puede adjuntar la factura a otra factura para el mismo cliente y proyecto. En este caso, puede facturar todo el proyecto, ya que éste ya estará completado.  

### <a name="to-create-a-job-sales-invoice"></a>Para crear una factura de ventas del proyecto  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione el proyecto que ha creado antes y, después, seleccione la acción **Crear factura de venta de proyecto**.  
3.  En la ficha desplegable **Tarea proyecto**, desactive cualquier filtro en **Nº tarea proyecto** para facturar el trabajo. En el campo **Nº proyecto**, seleccione el proyecto correspondiente.  
4.  En la ficha desplegable **Opciones**, introduzca la fecha de registro y defina si desea crear una factura por tarea o una sola factura para todas las tareas.  
5.  Elija el botón **Aceptar** para crear la factura y seleccione el botón **Aceptar** en la ventana de confirmación.  

 Después de que Tricia cree la factura, ella puede acceder a ésta desde **Ventas y Marketing** en **Procesamiento de pedidos** y realizar un procesamiento adicional.  

### <a name="to-post-a-new-sales-invoice"></a>Para registrar una nueva factura de ventas  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas venta** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra la factura para el nº de cliente 01445544. Puede ver que se ha escrito la información para las líneas de planificación.  
3.  Seleccione la acción **Registrar**. Elija **Sí** para confirmar el registro.  

### <a name="to-view-the-posted-invoice"></a>Para visualizar la factura registrada  

1.  Abra el proyecto y, a continuación, elija la acción **Líneas de planificación de proyecto**.  
2.  Seleccione una de las líneas de planificación que se han facturado y, a continuación, seleccione la acción **Facturas ventas/abono**.
3. En la ventana **Facturas de proyecto**, elija la acción **Abrir Facturas venta/Abonos venta**.  

 Tricia tiene una pregunta acerca de los precios, los costes y los beneficios correspondientes a este proyecto en particular; por lo tanto, accede a esa información en la ventana **Estadísticas**.  

### <a name="to-open-the-statistics-window"></a>Para abrir la ventana Estadísticas  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione la acción **Estadísticas**. Puede revisar información detallada acerca de los precios, costes y beneficio bruto del trabajo en las divisas local y extranjera.  
3.  Elija el botón de **Cerrar** para cerrar la ventana de **Estadísticas proyecto**.  

## <a name="handling-fixed-prices"></a>Gestión de precios fijos  
 CRONUS ha sido contratada para configurar dos salas de conferencias. Como director del proyecto, Prakash desea tener un buen panorama de las tareas que requiere el proyecto con los costes presupuestados e incurridos asociados de cada tarea. Además, desea conocer el precio contratado total del proyecto y el importe que se lleva facturado. Ha llegado a un acuerdo con el cliente respecto al precio fijo del proyecto.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>Para gestionar precios fijos en proyectos  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione el número de proyecto **Deco** y, después, seleccione la acción **Líneas de tarea de proyecto**.  
3.  Seleccione la línea 1120 y, en el campo **Previsión (coste total)**, haga clic con el botón secundario en el importe y seleccione **Análisis**.  

     Al revisar las líneas de planificación del proyecto, Prakash determina que también va a necesitar a Tricia durante 30 horas para esta etapa del proyecto. Acuerda un precio fijo con el cliente.  

4.  En la ventana **Líneas de tarea de proyecto**, seleccione la línea 1120 y, a continuación, elija la acción **Líneas de planificación de proyecto**.  
5.  Seleccione **Nuevo**, para crear una línea con la siguiente información:  

    -   **Tipo de línea**: **previsión y contrato**  
    -   **Tipo**: **recurso**  
    -   **Nº**: **Tricia**  
    -   **Cantidad**: **30**  

7.  Elija el botón **Aceptar** para cerrar la ventana.  
8.  En el campo de **Previsión (Coste total)**, haga clic con el botón secundario en el campo y elija **Análisis** otra vez en la ventana de **Líneas tarea proyecto**. Vea los cambios a la programación. Puede ver que se han agregado 30 horas al programa.  
9. Elija el botón **Aceptar** para cerrar las ventanas.  

 Una vez agregada Tricia a la previsión para esta línea de tarea, trabaja 25 horas en el proyecto. Ella introduce estas horas en el diario del proyecto.  

### <a name="to-enter-hours-in-the-job-journal"></a>Para especificar horas en el Diario proyectos  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  En una línea nueva, escriba la siguiente información:  

    -   **Tipo línea**: **(en blanco)**  
    -   **Fecha registro**: **(fecha actual)**  
    -   **Nº documento**: **J00002**  
    -   **Nº proyecto**: **Deco**  
    -   **Nº tarea proyecto**: **1120**  
    -   **Tipo**: **recurso**  
    -   **Nº**: **Tricia**  
    -   **Cantidad**: **25**  

3.  Seleccione la acción **Registrar**.  

     Unos días más tarde, Tricia trabaja otras 10 horas en el proyecto. Ya lleva trabajadas 35 horas en total. Como el acuerdo con el cliente es por 30 horas, sólo cinco se cargarán al cliente. Tricia sumará manualmente las cinco horas adicionales que trabajó a la programación.  

4.  En la ventana **Diario de proyecto**, seleccione la acción **Cálc. uso restante**.  
5.  En la ventana **Cálc. uso restante proyecto**, en la ficha desplegable **Opciones**, escriba la siguiente información:  

    -   **Nº documento**: **J00003**  
    -   **Fecha registro**: **(fecha actual)**  

6.  En la ficha desplegable **Tarea proyecto**, escriba la siguiente información:  

    -   **Nº proyecto**: **Deco**  
    -   **Nº tarea proyecto**: **1120**  

     Elija el botón **Aceptar** para ejecutar el cálculo. Existen cinco horas de trabajo que permanecen para Tricia. El campo **Tipo línea** está vacío, lo que indica que sólo falta registrar el uso, puesto que el trabajo ya se ha programado.  

7.  En la opción **Diario proyecto**, cree una línea nueva con la siguiente información. Asegúrese de que ambos números de proyecto son secuenciales con los que ha utilizado ya:  

    -   **Tipo línea**: **Programa**  
    -   **Nº proyecto**: **Deco**  
    -   **Nº tarea proyecto**: **1120**  
    -   **Tipo**: **recurso**  
    -   **Nº**: **Tricia**  
    -   **Cantidad**: **5**  

     Mediante el uso del tipo de línea **Programa**, se actualizan los costes y los precios previstos, pero no se factura al cliente ninguna de las actualizaciones de costes y precios de contrato.  

8.  Seleccione la acción **Registrar**. Seleccione el botón **Aceptar** para cerrar la ventana.  
9. Abra la lista **Proyectos** .  
10. Seleccione el proyecto DECO y, a continuación, elija la acción **Líneas de tarea de proyecto**.  
11. Seleccione la línea 1120 y, en el campo **Previsión (coste total)**, haga clic con el botón secundario en el importe. Elija **Análisis** para ver la información.  

     Los cambios se introducen automáticamente en la línea para el N.º tarea de trabajo 1120 En el coste total del proyecto programado, cinco horas adicionales de trabajo de Tricia se han añadido a la previsión.  

12. Elija el botón **Cerrar** para cerrar la ventana.  
13. Haga clic con el botón secundario en el importe del campo **Contrato (Coste total)** y elija **Análisis** para ver la información.  

     En el precio total del contrato, sólo se han incluido las 30 horas originales contratadas, pues es lo acordado con el cliente.  

## <a name="copying-jobs"></a>Copia de proyectos  
 Prakash ha alcanzado un acuerdo con un cliente, Sellafrio S.L. para equipar 10 salas de conferencias. El acuerdo se parece a un trabajo anterior. Por tanto, ahorrará tiempo si copia ese trabajo anterior.  

 En la ventana **Copiar proyecto**, puede seleccionar las líneas de proyecto y tarea que desea copiar. También puede seleccionar copiar los movimientos del proyecto de origen, con lo cual se crean líneas de planificación basadas en el uso real, o bien copiar las líneas de planificación del proyecto originales, con lo cual se copian las líneas de planificación originales en el nuevo proyecto. A continuación, puede elegir el tipo de línea de planificación o de movimiento que desea incluir, solo seleccione el que sea relevante para este nuevo proyecto. Finalmente, puede seleccionar el proyecto que desea copiar y definir si los precios y las cantidades deben copiarse también.  

### <a name="to-copy-a-job"></a>Para copiar un proyecto  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  Selecione la acción **Nuevo** para crear un nuevo proyecto. Escriba la siguiente información:  

    -   **Descripción**: **Equipamiento de 10 salas de conferencias**  
    -   **Factura-a Nº cliente**: **20000**  

3.  Seleccione la acción **Copiar tareas de proyecto desde**.  
4.  En la ventana de **Copiar tareas de proyecto**, introduzca lo siguiente:  

    -   **Nº proyecto**: **Deco**  
    -   **Nº tarea proyecto desde**: **1000**  
    -   **Origen**: **Líneas planificación proyecto**  
    -   **Incl. tipo línea planificación**: **Previsión y contrato**  
    -   **Nº tarea proyecto hasta**: **Guildford Equipar 10 salas de conferencias**  
    -   Seleccione los campos **Copiar dimensiones** y **Copiar cantidad**.  

5.  Elija el botón **Aceptar** para copiar el proyecto y, a continuación, seleccione el botón **Aceptar** para cerrar la ventana de confirmación.  

     Comparando los precios, las líneas de tareas de proyectos y las líneas de planificación del proyecto para los dos proyectos, puede ver que la información se copió correctamente.  

## <a name="making-payments-by-installments"></a>Creación de pagos a plazos  
 CRONUS acaba de iniciar un proyecto grande de un año de duración. Dado que requiere la dedicación de numerosos recursos, el director del proyecto configura el contrato de manera que el cliente pague parte del precio por adelantado, parte cuando el proyecto vaya por la mitad y el último pago tras su finalización.  

### <a name="to-set-up-a-new-account"></a>Para configurar una cuenta nueva  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Plan de cuentas**, seleccione la acción **Nuevo** para crear una ficha nueva.  
3.  En la ficha **Cuenta nueva**, escriba la siguiente información:  

    -   **Nº**: **6630**  
    -   **Nombre**: **Pago proyecto**  

4.  En la ficha desplegable **Registro**, en el campo **Grupo contable producto**, seleccione **VARIOS**. Elija el botón **Aceptar** para cerrar la ventana.  
5.  En la ventana de **Plan de cuentas**, seleccione **Nº 6630 de pago del proyecto** y, a continuación, seleccione la acción **Incidente en plan de cuentas**. Seleccione **Sí** para confirmar.  

 Los siguientes procedimientos muestran cómo crear un proyecto nuevo, establece las tarifas y, a continuación, el pago a plazos configurado. En las líneas de tareas del proyecto, puede crear líneas específicas dedicadas al pago a plazos. Todo el trabajo finalizado del proyecto que se agregue a la previsión se escribirá en las líneas de uso. Para cada línea de tarea de pago en las líneas de planificación, el tipo de línea es Contrato, lo que significa que se va a facturar al cliente. Añada una nueva línea para la entrada del pago. En la línea de tarea de uso, puede escribir la información para los productos y recursos utilizados en este proyecto, lo cual aumentará la previsión, como horas de empleado y productos usados en el proyecto.  

### <a name="to-make-a-payment-by-installment"></a>Para crear un pago a plazos  

1.  Cree un proyecto nuevo.  
2.  En la nueva ficha **Proyecto**, rellene la siguiente información:  

    -   **Descripción**: **Redecoración del área de recepción**  
    -   **Factura-a Nº cliente**: **30000**  
    -   **Grupo contable proyecto**: **Equipar**  
    -   **Método WIP**: **Valor coste**  

3.  En la ficha de proyecto, elija la acción **Recurso**. Escriba la siguiente información:  

    -   **Código**: **Tricia**  
    -   **Precio venta**: **10**  

     Seleccione el botón **Aceptar** para cerrar la ventana.  

4.  En la ficha **Proyecto**, elija la acción **Líneas de tarea de proyecto**.  

     La siguiente tabla describe las líneas que creará.  

    |Línea|N.º tarea de trabajo|Description|Tipo de tarea de trabajo|  
    |----------|------------------|---------------------------------------|-------------------|  
    |0|1000|Pago del Pago inicial|Registro|  
    |2|2000|Uso|Auxiliar|  
    |3|3000|Pago - Intermedio|Auxiliar|  
    |4|4000|Pago - Finalización|Registro|  

5.  En la ventana **Líneas de tarea de proyecto**, seleccione la tarea 1000 y, a continuación, elija la acción **Líneas de planificación de proyecto**.  
6.  Cree una línea de planificación con la siguiente información:  

    -   **Tipo línea**: **Contrato**  
    -   **Fecha planif.**:  **(fecha actual)**  
    -   **Tipo**: **cuenta G/L**  
    -   **Nº**: **6630**  
    -   **Cantidad**: **1**  
    -   **Precio venta**: **5000**  

     Elija el botón **Aceptar** para cerrar la ventana.  

7.  En la ventana de **Líneas tarea proyecto**, seleccione **tarea 2000**y abra sus **Líneas de planificación de proyecto**.  

     La siguiente tabla describe las líneas de planificación que creará.  

    |Línea|Tipo de línea|Fecha planif.|Escriba|Nº|Cantidad|  
    |----------|---------------|-------------------|----------|---------|--------------|  
    |1|Programa|(fecha de hoy)|Recurso|Tricia|120|  
    |2|Programa|(fecha de hoy)|Producto|70104|10|  

     Elija el botón **Aceptar** para cerrar la ventana. En la ventana **Líneas tarea proyecto**, podrá ver que se han actualizado los importes del programa.  

8.  En la ventana **Líneas tarea proyecto**, seleccione **tarea 3000**.  
9. Cree una línea de planificación con la siguiente información:  

    -   **Tipo línea**: **Contrato**  
    -   **Fecha de la planificación**: **una fecha futura**  
    -   **Tipo**: **cuenta G/L**  
    -   **Nº**: **6630**  
    -   **Cantidad**: **1**  
    -   **Precio venta**: **5000**  

     Elija el botón **Aceptar** para cerrar la ventana.  

10. Crear un movimiento de línea similar de planificación de la tarea 4000 del proyecto.  

 Ahora que se han especificado las líneas de tarea y de planificación, Prakash crea una factura para el primer pago. Lo hace desde las líneas de tarea del proyecto para asegurarse de que la factura sólo contenga las líneas del primer pago. Puede abrir el pedido de venta desde las líneas de planificación o desde las líneas de tarea.  

### <a name="to-create-an-invoice"></a>Para crear una factura  

1.  En la ventana **Líneas de tarea de proyecto**, seleccione la línea 1000 y, a continuación, elija la acción **Crear factura de ventas**.  
2.  En la ventana de **Crear factura venta**, establezca la fecha de hoy como la fecha de registro, especifique **Por la tarea** y elija el botón de **Aceptar** para crear una factura con la información predeterminada. Elija el botón **Aceptar** para cerrar la ventana de confirmación.  
3.  Elija la acción **Crear factura/abono de venta**. En la factura de venta, puede ver que sólo se incluye en la factura el pago de entrada. Ahora puede enviarlo al cliente como acordaron.  

## <a name="next-steps"></a>Pasos siguientes  
 Este tutorial le ha llevado por algunos de los pasos básicos de trabajo con los proyectos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ha aprendido acerca de cómo crear un trabajo nuevo, cómo copiar un trabajo y cómo administrar los pagos. Además, ha visto una demostración de cómo seguir las horas y crear las facturas.  

## <a name="see-also"></a>Consulte también  
 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)   
 [Configurar la administración de proyectos](projects-setup-projects.md)   
 [Cómo usar recursos](projects-how-use-resources.md)   
 [Cómo supervisar el progreso y el rendimiento](projects-how-monitor-progress-performance.md)   
 [Facturación de proyectos](projects-how-invoice-jobs.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

