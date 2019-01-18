---
title: "Programar proyectos para que se ejecuten automáticamente | Documentos de Microsoft"
description: "Las tareas programadas son administradas por la cola de proyecto. Estos proyectos ejecutan informes y unidades de código. Puede configurar proyectos para que se ejecuten una vez o de manera periódica."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ad0f99509ff1a191c62dd1c3a6d569c9884ea851
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Uso de colas de proyectos para programar tareas
Las colas de proyectos de [!INCLUDE[d365fin](includes/d365fin_md.md)] permiten a los usuarios programar y ejecutar informes y códigos de unidad específicos. Puede configurar proyectos para que se ejecuten una vez o de manera periódica. Por ejemplo, puede ejecutar el informe de **Vendedor - Estadísticas ventas** de manera semanal, para realizar el seguimiento de ventas por vendedor cada semana, o bien ejecutar la unidad de código **Procesar cola de correo electrónico del servicio** diariamente, para asegurarse de que se envían de manera oportuna los mensajes de correo electrónico a los clientes relacionados con sus pedidos de venta.  

## <a name="add-jobs-to-the-job-queue"></a>Añada los proyectos a la cola de proyectos
La página **Entradas de cola de proyectos** enumera todos los proyectos existentes. Si agrega una nueva entrada de cola de proyectos que desee programar, debe especificar información acerca del tipo de objeto que desea ejecutar, por ejemplo, informe o unidad de código y nombre y el identificador del objeto que desee ejecutar. También puede agregar parámetros para especificar el comportamiento del movimiento de cola de proyectos. Por ejemplo, puede agregar un parámetro para enviar solo pedidos de venta registrados. Debe disponer de los permisos adecuados para ejecutar el informe o la unidad de código en particular; de lo contrario, se devolverá un error al ejecutarse la cola de proyectos.  

Opcionalmente, puede establecer un filtro en el campo **Filtro categoría de la cola de proyecto**. Las categorías de la cola de proyecto se pueden usar para agrupar proyectos en la lista.

[!INCLUDE[d365fin](includes/d365fin_md.md)] ejecutará automáticamente los proyectos según los calendarios especificados para cada entrada de cola de proyecto. También puede iniciar, detener y poner una entrada de cola de proyecto en espera manualmente.

### <a name="log-files"></a>Log Files
Los errores se muestran en la página **Registro de entradas de cola proyecto** a la que se accede de la cinta. También puede solucionar errores de la cola de proyectos. Los datos generados al ejecutar una cola de proyectos se almacenan en la base de datos.  

### <a name="background-posting-with-job-queues"></a>Registro de fondo con colas de proyecto
Las colas de proyectos son un instrumento eficaz para programar la ejecución de procesos de negocio de fondo. Por ejemplo, puede haber un caso en el que varios usuarios intenten registrar pedidos de venta simultáneamente, pero solo se puede procesar un pedido al mismo tiempo. Al configurar la rutina de registro de fondo, puede colocar los registros en una cola para su procesamiento de fondo.  

 Alternativamente, puede que desee programar registros para horas en que resulta adecuado para su organización. Por ejemplo, para su empresa puede ser útil ejecutar ciertas rutinas cuando la mayor parte de la introducción de datos del día ha concluido. Para hacerlo, configure la cola de trabajos para que ejecute varios informes de registro por lotes, como el **Reg. lotes pedidos venta**, el **Reg. lotes facturas ventas** y el **Reg. lotes abonos venta**.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] admite el registro en segundo plano para los siguientes tipos de documento:  

-   Venta: pedido de venta, pedido de devolución, nota de crédito, factura  

-   Compra: pedido de compra, pedido de devolución, nota de crédito, factura  

 Si la cola de proyectos no puede registrar el pedido de venta, cambie el estado a **Error** y el pedido de venta se agregará a la lista de pedidos de venta que el usuario tendrá que administrar.  

> [!NOTE]  
>  Al programa un documento para su registro y el proceso de registro comienza, la rutina de registro se configura automáticamente para tener un tiempo de espera de dos horas si la rutina de registro deja de responder por cualquier motivo.  

Puede configurar este uso de cola de proyecto en la página **Configuración de ventas y cobros** o **Compras y pagos** , respectivamente. En la ficha desplegable **Registro de fondo** , elija la casilla de verificación **Envío de documentos mediante la cola de proyecto** y rellene la información correspondiente. Aquí también puede utilizar el campo **Código de categoría de cola de proyectos** para ejecutar todas las entradas de la cola de proyecto con ese código. Por ejemplo, puede usar una categotóa **Envío de ventas** que filtra todos los pedidos de venta que coincidan con cualquier cola de proyectos que tenga el mismo código de categoría.  

> [!IMPORTANT]  
>  Si configura un proyecto que va a registrar e imprimir documentos y la impresora muestra un cuadro de diálogo, como una solicitud de credenciales o una advertencia sobre un nivel bajo de tinta de impresora, el documento se registra pero no se imprime. Finalmente, el tiempo de espera del movimiento de cola de proyectos correspondiente se agota y el campo **Estado** se establece **Error**. Por consiguiente, es recomendable no utilizar una configuración de impresora que requiere la interacción con la pantalla de cuadros de diálogo de la impresora junto con el registro en segundo plano.  

## <a name="use-the-my-job-queue-part"></a>Use el apartado de Mi cola proyecto
El apartado **Mi cola proyecto** muestra los movimientos de colas de proyectos que un usuario ha iniciado, pero que aún no han finalizado. Por defecto, el apartado no puede verse, por lo que tiene que agregarlo en el área de trabajo. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).  

En este apartado, puede ver aquellos documentos que se están procesando o que están en la cola para los que se especifica su identificador en el campo **Id. usuario asignado**. La parte le ayuda a realizar un seguimiento de todos los movimientos de cola de proyectos, incluidos los relacionados con el registro en segundo plano. La parte puede indicar en un vistazo si se produjo error en el registro de un documento o si hay errores en un movimiento de cola de proyectos. El apartado también le permite cancelar un registro de documento si no se está ejecutando.  

## <a name="security"></a>Seguridad  
Los movimientos de cola de proyectos se ejecutan según los permisos. Esos permisos deben permitir la ejecución del informe o la unidad de código.  

Cuando una cola de proyecto se activada de forma manual, se ejecuta con las credenciales del usuario. Cuando una cola de proyecto se activa como tarea progamada, se ejecuta con las credenciales de la instancia del servidor. Cuando se ejecuta un proyecto, se ejecuta con las credenciales de la cola de proyecto que lo activa. Sin embargo, el usuario que creó ese movimiento de cola de proyecto también debe tener permisos. Cuando un proyecto se “ejecuta en sesión de usuario” (por ejemplo, en el registro de fondo), se ejecuta con las credenciales del usuario que creó ese proyecto.  

> [!IMPORTANT]  
>  Si utiliza el conjunto de permisos SUPER que se suministran con [!INCLUDE[d365fin](includes/d365fin_md.md)], usted y sus usuarios tienen permisos para ejecutar todos los objetos. En este caso, el acceso para cada usuario se ve limitado sólo por los permisos para los datos.  

## <a name="using-job-queues-effectively"></a>Uso eficaz de las colas de proyectos  
El registro del movimiento de cola de proyectos tiene muchos campos cuya finalidad es incluir parámetros en una unidad de código especificada para ejecutarse con una cola de proyectos. Esto también significa que las unidades de código que se van a ejecutar mediante la cola de proyectos se deben especificar con el registro del movimiento de la cola de proyectos como parámetro en el desencadenador **OnRun**. Esto ayuda a proporcionar un nivel de seguridad adicional, ya que evita que los usuarios ejecuten unidades de código aleatorias mediante la cola de proyectos. Si el usuario debe transmitir parámetros a un informe, la única manera de hacerlo es ajustar la ejecución del informe en una unidad de código, que a continuación analiza los parámetros de entrada y los especifica en el informe antes de ejecutarlo.  

## <a name="see-also"></a>Consulte también  
[Administración](admin-setup-and-administration.md)  
[Configuración de Business Central](setup.md)  

