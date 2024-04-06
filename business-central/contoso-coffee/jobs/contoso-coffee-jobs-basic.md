---
title: Tutorial de trabajos básicos
description: Este artículo lo guía a través de varios procesos centrales en la gestión de proyectos.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-of-basic-jobs"></a>Tutorial de trabajos básicos

Este tutorial demuestra varios procesos principales:

- Agregar tareas de trabajo a trabajos
- Registrar el tiempo y los gastos de material de un trabajo
- Facturar un trabajo

## <a name="adding-a-project-task"></a>Agregar una tarea de trabajo a un trabajo

### <a name="scenario"></a>Escenario

Simon, el director del proyecto, quiere registrar el tiempo invertido en a educar al cliente sobre el uso de productos de máquinas de café expreso para una tarea separada del trabajo de instalación de una máquina comercial en el sitio.

### <a name="steps"></a>Pasos

1. Crear la tarea de trabajo  

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
    2. Seleccione el trabajo *J00010*.
    3. En el área **Tareas**, elija la acción **Nueva línea**.  Introduzca los siguientes valores:
 
    |N.º tarea de proyecto|Descripción|Tipo de tarea de trabajo|
    |------------|-----------|-------------|  
    |220|Formación del cliente|Registro|

2. Sangría a Tareas proy
   1. En el área Tareas, busque la acción **Sangría de tareas de trabajo**
   2. Confirme que desea aplicar sangría a las tareas seleccionando **Sí**.

### <a name="results"></a>Resultados

 - Ahora se pueden registrar el tiempo y los gastos en la nueva tarea de trabajo

## <a name="record-time-and-material-expenses-to-a-project"></a>Registrar el tiempo y los gastos de material de un trabajo

### <a name="scenario-1"></a>Escenario

Edgin, el técnico que instala la máquina, necesita registrar en el trabajo su tiempo y los materiales utilizados durante la instalación para la facturación.  Ya agregó los viajes y los materiales, y ahora necesita agregar tiempo para enseñar al personal cómo usar la máquina.

### <a name="steps-1"></a>Pasos

1. Crear líneas de diario de proyectos adicionales

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de proyectos**, y luego elija el enlace relacionado.  
    2. Seleccione el lote *CONTOSO*.  Verá varias líneas de tipos de recursos y elementos, que reflejan el tiempo (para el técnico y el vehículo) y los materiales (la máquina y los suministros) utilizados.
    3. Cree una línea nueva. Introduzca los siguientes valores:
 
    |N.º proyecto|N.º tarea de proyecto|Tipo|N.º|Descripción|Cantidad|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Recurso|EDGIN|Formación del cliente|1|

2. Registrar el tiempo y el gasto
   1. Seleccione la acción **Registrar**
   2. Confirme que desea publicar las líneas seleccionando **Sí**.

### <a name="results-1"></a>Resultados

 - Se crearán asientos del Libro mayor de trabajos y Asientos del Libro mayor de recursos de tipo *Uso*
 - Se crearán asientos del libro mayor de artículos para ajustar negativamente el inventario
 - En la Ficha de Trabajo, los Costos y Precios en el área de Tareas reflejarán los nuevos saldos pendientes de facturar
 - En la tarjeta de trabajo, el cuadro informativo Detalles del trabajo reflejará los totales de los precios

## <a name="creating-a-sales-invoice-for-a-project"></a>Creación de una factura de venta para un trabajo

### <a name="scenario-2"></a>Escenario
Simon necesita crear y publicar una factura para enviarla al cliente con el tiempo y los gastos del trabajo.

### <a name="steps-2"></a>Pasos
1. Crear la factura de ventas

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyectos** y luego elija el enlace relacionado.  
    2. En la lista de Trabajos, elija la acción **Crear factura de venta de trabajo**.
    3. Establezca el filtro **N.º de trabajo** en *J00010*.
    4. Elija **Aceptar** para generar la factura de ventas.  Recibirá una confirmación de cuantas facturas se generan

2. Registrar la factura del tiempo y el gasto
   1. Elija el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  
   2. Seleccione la última factura para abrirla y revisarla.
   3. Seleccione la acción **Registrar**.

### <a name="results-2"></a>Resultados

 - Se crearán asientos del Libro mayor de trabajos y Asientos del Libro mayor de recursos de tipo *Ventas*
 - En la Ficha de Trabajo, los Costos y Precios en el área de Tareas reflejarán los nuevos saldos facturados
 - En la tarjeta de trabajo, el cuadro informativo Detalles del trabajo reflejará los precios en la sección precio facturado
