---
title: 'Tutorial: Gestión de proyectos con Projects'
description: Este tutorial le presenta las funciones de gestión de programas en trabajos que le permiten programar el uso de los recursos de su empresa y más.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Tutorial: administración de proyectos

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Este tutorial le presenta a las funciones de administración de proyectos. Los proyectos le permiten programar el uso de los recursos de su empresa y realizar un seguimiento de los diversos costes asociados con los recursos de un proyecto específico. Los proyectos implican el consumo de horas de mano de obra, horas de maquinaria, productos de inventario y otros tipos de consumo que es posible que desee controlar a medida que avance un proyecto.  

 En este tutorial, se trata la configuración de un nuevo proyecto, además de las tareas más comunes, como gestión de precios fijos, creación de pagos a plazo, registro de facturas de proyectos y copia de proyectos.  

## Acerca de este tutorial

 En este tutorial, se demuestran las siguientes tareas:  

### Configurar un proyecto

 Con la configuración de la estructura del presupuesto para los proyectos, crear un proyecto es directo. Este tutorial trata los siguientes procedimientos:  

- Configuración de líneas de planificación y líneas de tarea de un proyecto.  
- Creación de precios específicos de proyectos para productos y cuentas.  
- Facturación a partir de un proyecto.  

### Gestión de precios fijos

 Puede gestionar precios fijos y precios de servicios o mercaderías que se acuerdan por adelantado con los clientes. En este tutorial, puede hacer lo siguiente:  

- Ver cómo se determinan los valores de facturas y contratos.  
- Permitir trabajo adicional en el programa que no se ha facturado.  

### Copiar un proyecto

 Esta parte del tutorial se centra en cómo copiar una parte o la totalidad de un proyecto para reducir la introducción manual de datos y mejorar la precisión. Incluye lo siguiente:  

- Copia de parte de un proyecto en un proyecto nuevo.  
- Copia de precios específicos de proyectos.  
- Copia de líneas de planificación.  

### Creación de pagos a plazos

 Cuando un proyecto amplio y caro tiene una larga duración, el cliente suele llegar a un acuerdo con la empresa para pagar a plazos. Este ejemplo muestra cómo configurar pagos a plazo y trata lo siguiente:  

- Creación de pagos a plazo para un proyecto.  
- Facturación de pagos a clientes.  
- Cómo tener en cuenta el uso en un proyecto de pagos a plazo.  

## Roles

 En este tutorial se incluyen tareas para las siguientes funciones:  

- Director de proyectos  
- Miembro del equipo del proyecto  

## Requisitos previos

 Para poder realizar las tareas del tutorial, deberá hacer lo siguiente:  

- Instale la base de datos de demostración CRONUS.
- Cree datos de ejemplo como indican los pasos de la siguiente sección.  

## Historia

Este tutorial se centra en CRONUS, una empresa de diseño y consultoría, que diseña y equipa nuevas infraestructuras, como salas de conferencias y oficinas, con mobiliario, accesorios y unidades de almacenamiento. La mayor parte de su trabajo está orientado a los proyectos. Prakash, un administrador de proyectos de CRONUS utiliza proyectos para obtener un panorama de cada tarea en curso que ha iniciado CRONUS, además de las tareas completadas. Prakash suele ser quien establece acuerdos con los clientes e ingresa al núcleo del proyecto, que son las líneas de tareas y planificación además de los precios [!INCLUDE[prod_short](includes/prod_short.md)]. Prakash observa que crear, mantener y revisar la información es directo. Prakash también considera positiva la forma en que [!INCLUDE[prod_short](includes/prod_short.md)] activa copiar los proyectos y el pago por plazos.

 Tricia, miembro del equipo del proyecto que depende de Prakash, es la responsable de supervisar el día a día del proyecto. Tricia especifica su propio trabajo, así como el trabajo realizado por técnicos en todas las tareas, registra los productos que han utilizado y los costes en los que han incurrido.  

## Preparación de datos de ejemplo

 Para prepararse para este tutorial, deberá añadir a Tricia como un recurso nuevo.  

### Para preparar los datos de ejemplo  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.  
2. Selecione la acción **Nuevo** para crear una nueva ficha de recursos.  
3. En la ficha desplegable **General**, introduzca la siguiente información:  

    - **Nº**: **Tricia**  
    - **Nombre**: **Tricia**  
    - **Tipo**: **Persona**  

4. Seleccione el campo **Unidad de medida base** y seleccione la acción **Nuevo** para abrir la página **Unidad de medida de recursos**. En el campo **Código**, seleccione **Hora**.  
5. En la ficha desplegable **Facturación**, escriba la siguiente información:  

    - **Coste unit. directo**: **5**  
    - **% Coste indirecto**: **4**  
    - **Coste unitario**: **10**  
    - **Grupo contable producto**: **Servicios**  
    - **Grupo registro IVA prod.**: **IVA 25**  

6. Cierre la página.

En el siguiente procedimiento, cree un lote de diarios de proyecto para Tricia, para contabilizar su uso.  

### Para crear una sección de diario de proyecto  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. En la página **Diario proyecto**, seleccione el campo **Nombre sección**. Aparecerá la página **Secciones diario proyectos**.  
3. Seleccione la acción **Nuevo**, para crear una línea con la siguiente información:  

    - **Nombre**: **Tricia**  
    - **Descripción**: **Tricia**  
    - **Nos. serie**: **JJNL-GEN**  

4. Elija el botón **Aceptar** para guardar los cambios.

## Configurar un proyecto

 En este escenario, CRONUS ha ganado un contrato con un cliente, Progressive Home Furnishings, para diseñar una sala de conferencias y un refectorio. El cliente tiene su sede en los Estados Unidos y el proyecto precisa un software especial. El director del proyecto llega a un acuerdo con el cliente y crea un proyecto que cubra el acuerdo.  

### Para configurar un proyecto  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2. Selecione la acción **Nuevo** para crear una nueva ficha.  
3. En la ficha desplegable **General**, introduzca la siguiente información:  

    - **Descripción**: **Asesoramiento en el equipamiento de la sala de conferencias**  
    - **Factura-a Nº cliente**: **01445544**  

4. En la ficha desplegable **Registro**, escriba la siguiente información:  

    - **Estado**: **Planificación**  
    - **Grupo contable de proyecto**: **Configurando**  
    - **Método WIP**: **Valor coste**  

5. En la ficha desplegable **Duración**, escriba la fecha de hoy en los campos **Fecha inicial** y **Fecha final**. Estas fechas ayudarán a aplicar las conversiones de divisas cuando se facture el proyecto.  
6. En la ficha desplegable **Comercio exterior**, defina el código de divisa en **USD**. Si selecciona USD en el campo **Código divisa factura**, el proyecto se facturará en dólares estadounidenses y se planificará en la divisa local de CRONUS.  

 Puede personalizar el precio para los clientes por cada proyecto, en función de los contratos que ha configurado. En el siguiente procedimiento, el director de proyectos especifica un coste para el tiempo de Tricia, define el precio del software correspondiente y añade en el viaje costes que el cliente ha acordado pagar.  

### Para personalizar los precios  

1. Desde la **Ficha de proyecto**, elija la acción **Recurso**.  
2. En la página **Precios recursos proyecto**, escriba la siguiente información:  

    - **Código**: **Tricia**  
    - **Precio venta**: **20**  

3. Cierre la página.  
4. Elija la acción **Producto**.  
5. En la página **Precios productos proyecto**, escriba la siguiente información y el precio personalizado:  

    1. **Nº producto**: **80201 (Programa gráfico)**  
    2. **Precio venta**: **200**  

6. Cierre la página.  
7. Elija la acción **Cuentas C/G**.  
8. En la página **Precios de la cuenta de proyectos**, introduzca la siguiente información y el coste de viaje, para el que el cliente ha acordado pagar el coste además de un porcentaje del 25% :  

    1. **Cuenta**: **8430 (Viajes)**  
    2. **Factor coste unitario**: **1,25**  

9. Cierre la página.  

 Los pasos finales en la configuración de un proyecto añaden las tareas del proyecto y las líneas de planificación que forman parte de cada tarea. Las líneas de planificación determinan qué se factura al cliente.  

### Para agregar tareas de proyecto  

1.  En la tarjeta **Proyecto** para el nuevo proyecto, elija la acción **Líneas de tarea del proyecto** .  
2.  La siguiente tabla describe la información que tiene que debería introducir en los campos.  

    |N.º tarea proyecto|Descripción|Tipo tarea proyecto|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Consultoría sobre la equipación de salones|Total inicio|  
    |1010|Reunión de consulta con el cliente|Auxiliar|  
    |nº 1020|Desarrollo|Auxiliar|  
    |1090|Total de consultoría|Fin Total|  

3.  Para indicar que algunas tareas son subcategorías de otras tareas, elija la acción **Indentar tareas proyecto**.  

 Una línea de planificación puede ser uno de los siguientes tipos:  

- **Presupuesto**: añadido a la previsión, pero no facturado.  
- **Facturable**: facturado, pero no añadido a la previsión.  
- **Presupuesto y facturable**: Facturado y añadido a la previsión.  

 En este tutorial, el director de proyectos utiliza **Presupuesto y facturable**. Crean tres líneas de planificación para la tarea 1010, y dos líneas de planificación para la tarea 1020.  

### Para crear líneas de planificación  

1. Seleccione línea 1010 y, a continuación, elija la acción **Líneas de planificación de proyecto**.  

2. Cree líneas de planificación con la siguiente información:  

    | Línea | Tipo de línea | Fecha planif.  | Escriba        | Nº   | Cantidad | Precio unitario |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Presupuesto y facturable | (fecha de hoy) | Recurso | Tricia | 40        |     |
    | 2    | Presupuesto y facturable | (fecha de hoy) | Recurso | Alfredo | 40        |     |
    | 3    | Presupuesto y facturable | (fecha de hoy) | Cuenta | 8430 (viajes) | 2 | 400    |

     Cierre la página. Los totales se actualizan en la página **Líneas tarea proyecto**.  
3. Seleccione línea 1020 y, a continuación, elija la acción **Líneas de planificación de proyecto**. Escriba la siguiente información:  

    | Línea | Tipo de línea | Fecha planif.  | Escriba        | Nº   | Cantidad | Precio unitario |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Presupuesto y facturable | (fecha de hoy) | Recurso | Tricia | 80        |     |
    | 2    | Presupuesto y facturable | (fecha de hoy) | Producto | 80201 (programa gráfico) | 1 |     |

4. Cierre la página. Los totales se actualizan en la página **Líneas tarea proyecto**.  

## Cálculo del uso restante

 Tricia, el miembro del proyecto de equipo, ha estado trabajando en el proyecto durante algún tiempo y desea registrar sus horas y utilización. Tricia no ha trabajado más horas que las acordadas previamente con el cliente. Tricia utiliza el trabajo por lotes **Cálcular el uso restante** para calcular el uso restante para el proyecto en un diario del proyecto. Para cada tarea, el trabajo por lotes calcula la diferencia entre el uso programado de productos, recursos y gastos de contabilidad, y el uso real registrado en los movimientos del proyecto. A continuación, se muestra el uso restante en el diario del proyecto, desde el cual puede registrarlo.  

### Para calcular el uso restante  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. En la página **Diario proyectos**, en el campo **Nombre sección**, abra la lista **Secciones diario proyecto**. Seleccione la sección de diario de proyecto de **Tricia**.  
3. Seleccione la acción **Cálcular uso restante**.  
4. En la página **Cálc. uso restante proyecto**, en la ficha desplegable **Tarea de proyecto**, elija el **N.º de proyecto** y seleccione el número de proyecto correspondiente, normalmente trabajo J00010.  
5. En la ficha desplegable **Opciones**, escriba **J00001** en el campo **Nº documento**. Esto facilitará el futuro seguimiento del registro.  
6. Escriba la fecha de hoy como fecha de registro.  
7. Elija el botón **Aceptar**. De este modo, se generarán las líneas de diario del proyecto derivadas de las líneas de planificación que creó Prakash para el proyecto.  
8. Elija el botón **Aceptar** en la página de confirmación. Las líneas generadas se añaden al diario del proyecto.  
9. Asegúrese de que todos los números del documento son J00001 y, a continuación seleccione la acción **Registrar**. Elija **Sí** para confirmar el registro.  

Ya se han registrado las líneas.  

## Crear y publicar una factura de ventas del proyecto

 A continuación, Tricia puede crear una nueva factura para todo el proyecto o parte de un proyecto. Tricia también puede adjuntar la factura a otra factura del mismo cliente para el mismo proyecto. En este caso, Tricia factura todo el proyecto porque el proyecto ya está terminado.  

### Para crear una factura de ventas del proyecto  

1.  Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione el proyecto que creó anteriormente y luego elija la acción **Crear factura de ventas del proyecto** .  
3.  En la ficha desplegable **Tarea proyecto**, desactive cualquier filtro en **Nº tarea proyecto** para facturar el trabajo. En el **N.º proyecto** seleccione el proyecto relevante.  
4.  En la ficha desplegable **Opciones**, introduzca la fecha de registro y defina si desea crear una factura por tarea o una sola factura para todas las tareas.  
5.  Elija el botón **Aceptar** para crear la factura y seleccione el botón **Aceptar** en la página de confirmación.  

 Después de crear la factura, Tricia puede acceder a ella desde el Área de trabajo **Procesadora de pedidos de ventas**, por ejemplo. 

### Para registrar una nueva factura de ventas  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  
2.  Abra la factura para el nº de cliente 01445544. Puede ver que se ha escrito la información para las líneas de planificación.  
3.  Seleccione la acción **Registrar**. Elija **Sí** para confirmar el registro.  

### Para visualizar la factura registrada  

1.  Abra el proyecto y luego elija la acción **Líneas de planificación del proyecto** .  
2.  Seleccione una de las líneas de planificación que se han facturado y, a continuación, seleccione la acción **Facturas ventas/abono**.
3. En la página **Proyecto Facturas**, elija la acción **Abrir factura de venta/nota de crédito** .  

 Tricia tiene una pregunta sobre los precios, costos y ganancias que son relevantes para este proyecto en particular, por lo que accede a esa información en la página  **Estadísticas** .  

### Para abrir la página Estadísticas  

1.  Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Estadísticas**. Puede revisar información detallada sobre los precios, costos y ganancias del proyecto tanto en moneda local como extranjera.  
3.  Elija el botón **Cerrar** para cerrar la página **Estadísticas del proyecto** .  

## Gestión de precios fijos

 CRONUS se han contratado a las salas de conferencias de instalación. Como director del proyecto, Prakash quiere tener una buena visión general de las tareas requeridas para el proyecto con los costos presupuestados e incurridos asociados para cada tarea. Además, Prakash quiere saber el precio total contratado para el proyecto y el importe facturado hasta este momento. Han llegado a un acuerdo con el cliente sobre el precio fijo del proyecto.  

### Para gestionar precios fijos en proyectos.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2. Seleccione el número de proyecto **Guildford**  y luego elija la acción **Líneas de tarea del proyecto** .  
3. Seleccione la línea 1120 y, en el campo **Presupuesto (coste total)**, haga clic con el botón secundario en el importe y seleccione **Análisis**.  

     Al revisar las líneas de planificación del proyecto, se determina que Prakash también va a necesitar a Tricia durante 30 horas para esta etapa del proyecto. Prakash acuerda un precio fijo con el cliente.  

4. En la página **Líneas de tarea de proyecto**, seleccione la línea 1120 y, a continuación, elija la acción **Líneas de planificación de proyecto**. Cree una línea de planificación con la siguiente información:  

    | Línea | Tipo de línea | Escriba        | Nº   | Cantidad |
    |------|-----------|-------------|-------|----------|
    | 1    | Presupuesto y facturable  | Recurso | Tricia | 30 |

     Cierre la página.  
5. En el campo de **Presupuesto (coste total)**, haga clic con el botón secundario en el campo y elija **Análisis** otra vez en la página **Líneas tarea proyecto**. Vea los cambios a la programación. Puede ver que se han agregado 30 horas al programa.  
6. Cierre las páginas.  

Después de ser agregada al cronograma para esta línea de tareas, Tricia trabaja 25 horas en el proyecto y ingresa estas horas en el diario del proyecto.  

### Para especificar horas en el Diario proyectos  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos** y luego elija el enlace relacionado.  
2. En una línea nueva, escriba la siguiente información:  

    - **Tipo línea**: **(en blanco)**  
    - **Fecha registro**: **(fecha actual)**  
    - **Nº documento**: **J00002**  
    - **Nº proyecto**: **Guildford**  
    - **N.º tarea proyecto**: **1120**  
    - **Tipo**: **recurso**  
    - **Nº**: **Tricia**  
    - **Cantidad**: **25**  

3. Seleccione la acción **Registrar**.  

     Unos días después, Tricia trabaja otras 10 horas en el trabajo y ahora ha trabajado 35 horas en total. Como el acuerdo con el cliente es por 30 horas, sólo cinco se cargarán al cliente. Tricia sumará manualmente las cinco horas adicionales que trabajó a la programación.  

4. En la página **Diario de proyecto**, seleccione la acción **Cálc. uso restante**.  
5. En la página **Cálc. uso restante proyecto**, en la ficha desplegable **Opciones**, escriba la siguiente información:  

    - **Nº documento**: **J00003**  
    - **Fecha registro**: **(fecha actual)**  

6. En la ficha desplegable **Tarea proyecto**, escriba la siguiente información:  

    - **Nº proyecto**: **Guildford**  
    - **N.º tarea proyecto**: **1120**  

7. Elija el botón **Aceptar** para ejecutar el cálculo.

    Existen cinco horas de trabajo que permanecen para Tricia. El campo **Tipo línea** está vacío, lo que indica que sólo falta registrar el uso, puesto que el trabajo ya se ha programado.  

8. En la opción **Diario proyecto**, cree una línea nueva con la siguiente información. Asegúrate de que ambos números de proyecto sean secuenciales con los que ya has utilizado:  

    - **Tipo de línea**: **Presupuesto**  
    - **Nº proyecto**: **Guildford**  
    - **N.º tarea proyecto**: **1120**  
    - **Tipo**: **recurso**  
    - **Nº**: **Tricia**  
    - **Cantidad**: **5**  

     Mediante el uso del tipo de línea **Presupuesto**, se actualizan los costes y los precios previstos, pero no se factura al cliente ninguna de las actualizaciones de costes y precios de contrato.  

9. Seleccione la acción **Registrar**. Elija el botón **Aceptar** para cerrar la página.  
10. Abra la lista **Proyectos** .  
11. Seleccione el trabajo DECO y, a continuación, en la sección **Líneas tarea proyecto**, seleccione la línea 1120 y en el campo **Presupuesto (coste total)**, haga clic con el botón derecho en el importe. Elija **Análisis** para ver la información.  

     Los cambios se introducen automáticamente en la línea para el N.º tarea de proyecto 1120 En el coste total del proyecto programado, cinco horas adicionales de trabajo de Tricia se han añadido a la previsión.  

12. Elija el botón **Cerrar** para cerrar la página.  
13. Haga clic con el botón secundario en el importe del campo **Contrato (Coste total)** y elija **Análisis** para ver la información.  

En el precio total del contrato, sólo se han incluido las 30 horas originales contratadas, pues es lo acordado con el cliente.  

## Copiar proyectos

Prakash ha alcanzado un acuerdo con un cliente, Sellafrio S.L. para equipar 10 salas de conferencias. El acuerdo se parece a un proyecto anterior. Por lo tanto, le ahorrará tiempo copiar ese proyecto anterior.  

En la página **Copiar proyecto**, puede seleccionar el proyecto y las líneas de tarea que desea copiar. También puede seleccionar copiar los asientos del libro mayor del proyecto de origen, lo que crea líneas de planificación basadas en el uso real, o puede copiar las líneas de planificación del proyecto de origen, lo que copia las líneas de planificación originales en el nuevo proyecto. Luego puede elegir qué línea de planificación o tipo de línea de movimiento contable desea incluir, seleccionando solo lo que sea relevante para este nuevo proyecto. Finalmente, puede seleccionar el proyecto que desea copiar y definir si también se deben copiar los precios y las cantidades.  

### Para copiar un proyecto  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y, a continuación, elija el vínculo relacionado.  
2. Elija la acción **Nuevo** para crear un nuevo proyecto. Escriba la siguiente información:  

    - **Descripción**: **Equipamiento de 10 salas de conferencias**  
    - **Factura-a Nº cliente**: **20000**  

3. Seleccione la acción **Copiar tareas de proyecto desde**.  
4. En la página **Copiar tareas de proyecto**, introduzca lo siguiente:  

    - **Nº proyecto**: **Guildford**  
    - **N.º tarea proyecto desde**: **1000**  
    - **Origen**: **Líneas planificación proyecto**  
    - **Incl. tipo línea planificación**: **Presupuesto + Facturable**  
    - **Nº tarea proyecto hasta**: **GuildfordSetting 10 salas de conferencias**  
    - Seleccione los campos **Copiar dimensiones** y **Copiar cantidad**.  

5. Elija el botón **Aceptar** para copiar el proyecto y luego elija el botón **Aceptar** para cerrar la página de confirmación.  

Al comparar precios, líneas de tareas de proyecto y líneas de planificación de proyecto para los dos proyectos, puede ver que la información se copió correctamente.  

## Creación de pagos a plazos

CRONUS acaba de iniciar un proyecto grande de un año de duración. Dado que requiere la dedicación de numerosos recursos, el director del proyecto configura el contrato de manera que el cliente pague parte del precio por adelantado, parte cuando el proyecto vaya por la mitad y el último pago tras su finalización.  

### Para configurar una cuenta nueva  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. En la página **Plan de cuentas**, seleccione la acción **Nuevo** para crear una ficha nueva.  
3. En la ficha **Cuenta nueva**, escriba la siguiente información:  

    - **Nº**: **40255**  
    - **Nombre**: **Pago del proyecto**  

4. En la ficha desplegable **Registro**, en el campo **Grupo contable producto**, seleccione **Servicios**. Cierre la página.  
5. En la página **Plan de cuentas**, seleccione **Nº 40255 de pago del proyecto** y, a continuación, seleccione la acción **Incidente en plan de cuentas**. Seleccione **Sí** para confirmar.  

Los siguientes procedimientos muestran cómo crear un nuevo proyecto, establecer precios y luego configurar el pago a plazos. En las líneas de tareas del proyecto, puede crear líneas específicas dedicadas al pago a plazos. Todo el trabajo completado en el proyecto que se agrega al cronograma se ingresará en las líneas de uso. Para cada línea de tarea de pago en las líneas de planificación, el tipo de línea es **Facturable**, lo que significa que se va a facturar al cliente. Añada una nueva línea para la entrada del pago. En la línea de tarea de uso, puede ingresar la información de los elementos y recursos que se han utilizado en este proyecto, lo que aumentará el cronograma, como las horas de los empleados y los elementos utilizados en el proyecto.  

### Para crear un pago a plazos  

1. Permite crear un proyecto nuevo.  
2. En la nueva tarjeta **Proyecto**, complete la siguiente información:  

    - **Descripción**: **Redecoración del área de recepción**  
    - **Factura-a Nº cliente**: **30000**  
    - **Grupo contable de proyecto**: **Configurando**  
    - **Método WIP**: **Valor coste**  

3. En la ficha de proyecto, elija la acción **Precios** y, a continuación, la acción **Recurso**. Escriba la siguiente información:  

    - **Código**: **Tricia**  
    - **Precio venta**: **10**  

     Cierre la página.  

4. En la tarjeta **Proyecto**, en la sección **Tareas**, agregue líneas de tareas del proyecto como se describe en la siguiente tabla:  

    | Línea | N.º tarea proyecto | Descripción          | Tipo tarea proyecto |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Pago del Pago inicial | Registro       |
    | 2    | 2000         | Uso                | Registro       |
    | 3    | 3000         | Pago - Intermedio     | Registro       |
    | 4    | 4000         | Pago - Finalización | Registro       |

5. Elija la tarea 1000 y, a continuación, la acción **Líneas de planificación de proyecto**.  

6. Cree una línea de planificación con la siguiente información:  

    | Línea | Tipo de línea | Fecha planif.  | Escriba        | Nº   | Cantidad | Precio unitario |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Facturable  | (fecha de hoy) | Cuenta | 40255 | 1        | 5000       |

     Cierre la página.  

7. Elija la tarea 2000 y, a continuación, la acción **Líneas de planificación de proyecto**.  

8. Cree una línea de planificación con la siguiente información:

    | Línea | Tipo de línea | Fecha planif.  | Escriba     | Nº    | Cantidad |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Presupuesto    | (fecha de hoy) | Recurso | Tricia | 120      |
    | 2    | Ppto    | (fecha de hoy) | Artículo     | 70104  | 10       |

     Cierre la página. En la página **Líneas tarea proyecto**, podrá ver que se han actualizado los importes del programa.  

9. Elija la tarea 32 000 y, a continuación, la acción **Líneas de planificación de proyecto**.  

10. Cree una línea de planificación con la siguiente información:

    | Línea | Tipo de línea | Fecha planif.   | Escriba        | Nº   | Cantidad | Precio unitario |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Facturable  | (una fecha futura) | Cuenta | 40255 | 1        | 5000       |

     Cierre la página.  

11. Crear un movimiento de línea similar de planificación de la tarea 4000 del proyecto.  

 Ahora que se han especificado las líneas de tarea y de planificación, Prakash crea una factura para el primer pago. Prakash lo hace desde las líneas de tarea del proyecto, para asegurarse de que la factura sólo contenga las líneas del primer pago. Puede abrir el pedido de venta desde las líneas de planificación o desde las líneas de tarea.  

### Para crear una factura  

1.  En la página **Líneas de tarea de proyecto**, seleccione la línea 1000 y, a continuación, elija la acción **Crear factura de ventas**.  
2.  En la página **Crear factura venta**, establezca la fecha de hoy como la fecha de registro, especifique **Por la tarea** y elija el botón **Aceptar** para crear una factura con la información predeterminada. Elija el botón **Aceptar** para cerrar la página de confirmación.  
3.  Elija la acción **Crear factura/abono de venta**. En la factura de venta, puede ver que sólo se incluye en la factura el pago de entrada. Ahora puede enviarlo al cliente como acordaron.  

## Pasos siguientes

 Este tutorial le ha guiado a través de algunos de los pasos básicos para trabajar con proyectos en [!INCLUDE[prod_short](includes/prod_short.md)]. Ha aprendido cómo crear un nuevo proyecto, cómo copiar un proyecto y cómo manejar los pagos. Además, ha visto una demostración de cómo seguir las horas y crear las facturas.  

## Consulte también .

 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
 [Configurar la administración de proyectos](projects-setup-projects.md)  
 [Usar recursos](projects-how-use-resources.md)  
 [Controlar el progreso y el rendimiento](projects-how-monitor-progress-performance.md)  
 [Facturar proyectos](projects-how-invoice-jobs.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
