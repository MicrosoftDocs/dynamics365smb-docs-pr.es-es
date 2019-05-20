---
title: Programar proyectos para que se ejecuten automáticamente | Documentos de Microsoft
description: Las tareas programadas son administradas por la cola de proyecto. Estos proyectos ejecutan informes y codeunits. Puede configurar proyectos para que se ejecuten una vez o de manera periódica.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 1cf5b75bc63acfa07a90cda1d03f45579a0aa51d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1247256"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Uso de colas de proyectos para programar tareas
Las colas de proyectos de [!INCLUDE[d365fin](includes/d365fin_md.md)] permiten a los usuarios programar y ejecutar informes y codeunits específicos. Puede configurar proyectos para que se ejecuten una vez o de manera periódica. Por ejemplo, puede ejecutar el informe de **Vendedor - Estadísticas ventas** de manera semanal, para realizar el seguimiento de ventas por vendedor cada semana, o bien ejecutar la codeunit **Procesar cola de correo electrónico del servicio** diariamente, para asegurarse de que se envían de manera oportuna los mensajes de correo electrónico a los clientes relacionados con sus pedidos de venta.

La página **Entradas de cola de proyectos** enumera todos los proyectos existentes. Si agrega una nueva entrada de cola de proyectos que desee programar, debe especificar información acerca del tipo de objeto que desea ejecutar, por ejemplo, informe o codeunit y nombre y el identificador del objeto que desee ejecutar. También puede agregar parámetros para especificar el comportamiento del movimiento de cola de proyectos. Por ejemplo, puede agregar un parámetro para enviar solo pedidos de venta registrados. Debe disponer de los permisos adecuados para ejecutar el informe o la codeunit en particular; de lo contrario, se devolverá un error al ejecutarse la cola de proyectos.  

Una cola de proyectos puede tener muchos movimientos, que son proyectos que la cola controla y ejecuta. La información del movimiento especifica qué codeunit o informe se ejecuta, cuándo y con qué frecuencia se ejecuta el movimiento, en qué categoría se ejecuta el proyecto y cómo se ejecuta.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Para configurar el registro de fondo con colas de proyecto
Las colas de proyecto son una herramienta eficaz para programar la ejecución de procesos de negocios en segundo plano, como cuando varios usuarios intentan publicar pedidos de ventas, pero solo se puede procesar un pedido a la vez. Alternativamente, puede que desee programar registros para horas en que resulta adecuado para su organización. Por ejemplo, para su empresa puede ser útil ejecutar ciertas rutinas cuando la mayor parte de la introducción de datos del día ha concluido.

Para hacerlo, configure la cola de proyectos para que ejecute varios informes de registro por lotes, como el **Reg. lotes pedidos venta**, el **Reg. lotes facturas ventas**, el **Reg. lotes devoluciones ventas** y el **Reg. lotes abonos venta**. Para obtener más información, vea [Para crear una entrada de cola de proyectos para el registro de pedidos de ventas en segundo plano](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] admite el registro en segundo plano para todos los documentos de ventas, compras y servicios.

El siguiente procedimiento explica cómo configurar el registro en segundo plano de los pedidos de ventas. Los pasos son parecidos para la compra y el servicio.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración ventas y cobros** y luego elija el enlace relacionado.
2. En la página **Configuración de ventas y cobros**, seleccione la casilla de verificación **Registrar con cola de proyectoss**.
3. Para filtrar a las entradas de la cola de proyectoss para el registro de pedidos de ventas, seleccione el campo **Cód. categoría cola proyectos** y, a continuación, seleccione la categoría **REGVEN**.

    Se crea un objeto de cola de proyectoss, codeunit 88 **Registro de ventas a través de cola de proyectoss**. Continúe para habilitarlo en la página **Movs. cola proyecto**.
4. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Movs. cola proyecto** y luego elija el enlace relacionado.
5. En la página **Movs. cola proyecto**, seleccione la acción **Nuevo**.
6. En el campo **Tipo objeto para ejecutar**, seleccione **Codeunit**.  
7. En el campo **Id. objeto para ejecutar**, seleccione 88, **Registro ventas a través de cola de proyectos**.

    Ningún otro campo es relevante para este ejemplo.
8. Elija la acción **Establecer estado en Preparado**.
9. Para verificar que la cola de proyectos funciona como se esperaba, registre un pedido de venta. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
10. Revise si el pedido de ventas se publicó correctamente en la página **Movs. registro cola proyecto**. Para obtener más información, consulte [Para ver el estado o los errores en la cola de proyectos](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Si también desea que los documentos de ventas se impriman cuando se registren, seleccione la casilla de verificación **Registrar e imprimir con cola de proyectoss** en la página **Configuración de ventas y cobros**.  

> [!IMPORTANT]  
> Si configura un proyecto que va a registrar e imprimir documentos y la impresora muestra un cuadro de diálogo, como una solicitud de credenciales o una advertencia sobre un nivel bajo de tinta de impresora, el documento se registra pero no se imprime. Finalmente, el tiempo de espera del movimiento de cola de proyectos correspondiente se agota y el campo **Estado** se establece **Error**. Por consiguiente, es recomendable no utilizar una configuración de impresora que requiere la interacción con la pantalla de cuadros de diálogo de la impresora junto con el registro en segundo plano.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Para crear un movimiento de la cola de proyectos para el registro por lotes de pedidos de ventas
El siguiente procedimiento muestra cómo configurar el informe **Reg. lotes pedidos venta** para que se registren automáticamente los pedidos de ventas lanzados a las 4:00 en días hábiles.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Movs. cola proyecto** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **Tipo objeto para ejecutar**, seleccione **Informe**.  
4. En el campo **Id. objeto para ejecutar**, seleccione 296, **Reg. lotes pedidos venta**.
5. Seleccione la casilla **Página de solicitud de informe**.
6. En la página de solicitud **Reg. lotes pedidos venta**, defina qué se incluye durante el registro automático de pedidos de ventas y luego elija el botón **Aceptar**.
7. Seleccione todas las casillas de verificación desde **Ejecutar los lunes** hasta **Ejecutar los viernes**.
8. En el campo **Hora de inicio**, introduzca 4:00.
9. Elija la acción **Establecer estado en Preparado**.

Los pedidos de venta que están listos para registrarse se registrarán cada día de la semana a las 4:00.

> [!NOTE]
> Si la cola de proyectos no puede registrar el pedido de venta, cambie el estado a **Error** y el pedido de venta se agregará a la lista de pedidos de venta que el usuario debe administrar manualmente. Para obtener más información, consulte [Para ver el estado o los errores en la cola de proyectos](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Después de configurar y ejecutar las colas de proyectos, el estado puede cambiar de la siguiente manera en cada período recurrente:

* **Esperar**  
* **Preparado**  
* **En proceso**  
* **Error**  
* **Terminada**  

Después de que un proyecto haya finalizado correctamente, se elimina de la lista de movimientos de la cola de proyectos a menos que sea un proyecto periódico. Si es un proyecto periódico, el campo **Hora inicial más próxima** se ajusta para mostrar la próxima vez que se espera que el proyecto se ejecute.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Para ver el estado o los errores en la cola de proyectos
Los datos que se generan cuando se ejecuta una cola de proyectos se almacenan en la base de datos, para que pueda solucionar los errores de la cola de proyectos.

### <a name="to-view-status-for-any-job"></a>Para ver el estado de un proyecto
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Movs. cola proyecto** y luego elija el enlace relacionado.
2. En la página **Movs. cola proyectos**, seleccione un movimiento de la cola de proyectos y luego elija la acción **Registrar movs**.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Para ver el estado de un documento de compra o de venta
1. Desde el documento que ha intentado registrar con la cola de proyectos, seleccione el campo **Estado de la cola de proyectos**, que contendrá **Error**.
2. Revise el mensaje de error y corrija el problema.

## <a name="the-my-job-queue-part"></a>El apartado de Mi cola proyecto
El apartado **Mi cola proyecto** del Área de trabajo muestra los movimientos de colas de proyectos que se han iniciado, pero que aún no han finalizado. Por defecto, el apartado no puede verse, por lo que tiene que agregarlo en el área de trabajo. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).  

Este apartado muestra los documentos con su ID en el campo **Id. usuario asignado** que se están procesando o están en cola, incluidos los relacionados con el registro en segundo plano. La parte puede indicar en un vistazo si se produjo error en el registro de un documento o si hay errores en un movimiento de cola de proyectos. El apartado también le permite cancelar un registro de documento si no se está ejecutando.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Procedimiento para ver un error del apartado Mi la cola de proyectos
1. En un movimiento con el estado **Error**, elija la acción **Mostrar error**.
2. Revise el mensaje de error y corrija el problema.

## <a name="security"></a>Seguridad  
Los movimientos de cola de proyectos se ejecutan según los permisos. Esos permisos deben permitir la ejecución del informe o la codeunit.  

Cuando una cola de proyecto se activada de forma manual, se ejecuta con las credenciales del usuario. Cuando una cola de proyecto se activa como tarea progamada, se ejecuta con las credenciales de la instancia del servidor. Cuando se ejecuta un proyecto, se ejecuta con las credenciales de la cola de proyecto que lo activa. Sin embargo, el usuario que creó ese movimiento de cola de proyecto también debe tener permisos. Cuando un proyecto se “ejecuta en sesión de usuario” (por ejemplo, en el registro de fondo), se ejecuta con las credenciales del usuario que creó ese proyecto.  

> [!IMPORTANT]  
>  Si utiliza el conjunto de permisos SUPER que se suministran con [!INCLUDE[d365fin](includes/d365fin_md.md)], usted y sus usuarios tienen permisos para ejecutar todos los objetos. En este caso, el acceso para cada usuario se ve limitado sólo por los permisos para los datos.  

## <a name="using-job-queues-effectively"></a>Uso eficaz de las colas de proyectos  
El registro del movimiento de cola de proyectos tiene muchos campos cuya finalidad es incluir parámetros en una codeunit especificada para ejecutarse con una cola de proyectos. Esto también significa que las codeunits que se van a ejecutar mediante la cola de proyectos se deben especificar con el registro del movimiento de la cola de proyectos como parámetro en el desencadenador **OnRun**. Esto ayuda a proporcionar un nivel de seguridad adicional, ya que evita que los usuarios ejecuten codeunits aleatorias mediante la cola de proyectos. Si el usuario debe transmitir parámetros a un informe, la única manera de hacerlo es ajustar la ejecución del informe en una codeunit, que a continuación analiza los parámetros de entrada y los especifica en el informe antes de ejecutarlo.  

## <a name="see-also"></a>Consulte también  
[Administración](admin-setup-and-administration.md)  
[Configuración de Business Central](setup.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
