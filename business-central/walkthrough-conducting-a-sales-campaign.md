---
title: 'Tutorial: realización de una campaña de ventas'
description: Este tutorial brinda una descripción detallada de todas las tareas involucradas en la realización de una campaña de ventas en Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# Tutorial: realización de una campaña de ventas

Una campaña es un tipo de actividad que implica varios contactos. Una importante parte de la configuración de una campaña implica la selección del público objetivo para la misma. Con este fin, en [!INCLUDE[prod_short](includes/prod_short.md)], creará un segmento o grupo de contactos con filtros.  

 Utilice estas funciones en Ventas y Marketing para planificar cuidadosamente las actividades de marketing y para administrar las interacciones con contactos y clientes. Puede crear campañas y configurar segmentos de sus contactos para envíos postales y otros tipos de interacciones con sus clientes y probables clientes.  

 Las funciones Campaña y Segmento con sus procesos automatizados le permitirán planificar, organizar y realizar un seguimiento de sus actividades de marketing. De este modo aumentarán las posibilidades de conseguir nuevos clientes y conservar los actuales.  

## Acerca de este tutorial

 En este tutorial se muestra el proceso para realizar un seguimiento en una feria de muestras y dirigirse a clientes potenciales (contactos) en una campaña de seguimiento.  

 El tutorial presenta la función de administración de campaña y segmento en el departamento de Ventas y Marketing. En este tutorial se ilustran las siguientes tareas:  

- Preparación de los datos.
- Configuración de una campaña.  
- Selección del público objetivo.  
- Extracción de datos.  
- Envío de cartas a contactos.  
- Registro de las respuestas de la campaña.  

## Funciones

 En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:  

- Director de marketing o Director de ventas  
- Empleado de marketing  

## Requisitos previos

 Para poder realizar las tareas del tutorial, deberá instalar [!INCLUDE[prod_short](includes/prod_short.md)]:  

## Historia

 El Director de marketing del Departamento de ventas de CRONUS es responsable de la planificación de campañas y de su ejecución. También toma decisiones sobre en qué ferias de muestras participar y evalúa el progreso de la campaña.  

 El empleado del Departamento de marketing maneja la producción, la distribución y la colocación de material de marketing.  

 La empresa acaba de lanzar un producto denominado el Rome Guest Chair. El producto se ha promocionado recientemente en una fuera de muestras, Office Futurus. Numerosos clientes han expresado un enorme interés en el producto y, como parte de un esfuerzo promocional, a aquellos clientes que compraron Rome Guest Chair durante el periodo de la campaña se les ofreció un precio especial de campaña.  

 Una de las tareas del empleado de marketing después de la feria de muestra es introducir todos los clientes potenciales como contactos.  

 El director de marketing organiza una campaña, crea un segmento que contiene todos los nuevos contactos y finalmente extrae los datos de contacto para seleccionar el público objetivo para la campaña.  

 El empleado ayuda a enviar cartas de agradecimiento a todos los contactos que dejaron sus tarjetas al personal del stand y, finalmente, el director registra todas las respuestas que reciban de los probables clientes.  

## Organización de una campaña

 En cuanto el empleado haya introducido las tarjetas de negocios recibidas en la feria de muestras, el director de marketing organiza una ficha de campaña para administrar las actividades relacionadas.  

### Para configurar una campaña  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Campañas** y luego elija el enlace relacionado.  
2. Seleccione **Nuevo** para crear una nueva campaña. En la ficha de la campaña, seleccione <kbd>Entrar</kbd> para crear un número de la campaña insertado automáticamente.  
3. En el campo **Descripción**, escriba una descripción para la campaña, por ejemplo **Feria de muestras Office Futurus**.  
4. Elegir el campo **Código de estado** y seleccione el código de estado "1-PLAN". 
5. Rellene los campos **Fecha inicial** y **Fecha final** de la campaña como corresponda.  

## Selección del público objetivo

 El director de marketing crea un segmento para seleccionar los contactos con los que desea interactuar.  
 
 Cuando crea un segmento, puede usar una variedad de criterios para seleccionar los contactos que deben ser objetivos para el segmento. Por ejemplo, puede seleccionar personas de contacto que trabajan en una ubicación de cliente o de probable cliente y que son los responsables de compras en sus empresas. Utilice los filtros para añadir los contactos según los criterios que mejor se ajusten a sus propósitos. Por ejemplo, puede elegir filtrar por responsabilidad del cargo de la persona de contacto, la relación empresarial o el sector de la empresa de contacto. Para este tutorial, elija el filtro **Responsabilidad cargo** para seleccionar los contactos.

### Para crear un segmento con los contactos relevantes  

1. Elija la acción **Navegar** y luego elija la acción **Segmentos**.  
2. Seleccione **Nuevo** para crear un nuevo segmento. En el segmento nuevo, seleccione **Entrar** para tener un número de segmento insertado automáticamente.  
3. En la ficha desplegable **General**, en el campo **Descripción**, escriba, por ejemplo, *Visitantes de la feria de muestras Office Futurus*.
4. Elija, la acción **Añadir contactos** para abrir el filtro **Añadir contactos**.  
5. Desplácese hacia abajo hasta la ficha desplegable **Cargo contacto**, seleccione el filtro **Compra** como **Cód. cargo contacto** y elija el botón **Aceptar**.  

La página **Segmento** contiene ahora una lista de contactos basada en los filtros que especifique. En la ficha desplegable **General**, en el campo de **Nº líneas**, puede ver de un vistazo el número de contactos que cumplen estos criterios.  

> [!NOTE]  
> Puede guardar los criterios de segmentación para poder usarlos más adelante.

### Para guardar sus criterios de segmentación

1. En la página **Segmento**, seleccione **Acciones**.
2. Elija **Funciones**, después **Segmento** y, luego, elija la acción **Guardar criterio**.  
3. En la página **Guardar criterios segmento**, especifique un código para el segmento. En el campo **Descripción**, escriba una descripción de los criterios del segmento.
4. Elija el botón **Aceptar**.  

## Extracción de los datos

 El director de marketing estudia atentamente la lista de contactos segmentada y observa que es demasiado extensa. Decide reducir la lista basándose en clientes probables reales para asegurarse de centrarse en el grupo objetivo correcto. Este proceso de refinar y reducir los datos también se conoce como extracción de datos.  

### Para eliminar los contactos del segmento  

1. En la página **Segmento**, seleccione **Acciones**.
2. En la barra de menú de abajo, elija **Funciones**, **Contactos** y **Reducir contactos**.  

  Se abre el cuadro de diálogo **Eliminar contactos - Reducir**.  
4. En la ficha desplegable **Relación negocio contacto**, seleccione el filtro **CLIE** como **Cód. relación negocio** y elija el botón **Aceptar**.

 La página **Segmento** contiene ahora una lista reducida de contactos y, en el campo **Nº líneas**, puede ver el número de contactos que satisface ahora estos nuevos criterios.  

 > [!NOTE]  
 > Si tuviera que deshacer esta eliminación de un grupo de contactos, puede hacerlo con la función **Volver**. En otras palabras, puede deshacer la última segmentación.  

### Para recuperar los contactos eliminados

1. En la página **Segmento**, seleccione la acción **Segmento**.
2. Seleccione la acción **Volver**.

Los contactos que acaba de eliminar se añaden de nuevo a la lista de contactos.

## Vinculación de un segmento con una campaña

El director de marketing decide que la lista reducida es la lista final de contactos que desea que forme parte de la campaña. Por lo tanto, vincula este segmento a la campaña Feria comercial FUTURUS.  

### Para vincular un segmento a la campaña  

1. En la página **Segmento**, en la ficha desplegable **Campaña**, elija el campo **Nº campaña** ara seleccionar la campaña a la que desee vincular el segmento, por ejemplo, **CP0001**.
2. Seleccione **Sí**.  
3. Dado que este segmento es el objetivo de la campaña, seleccione la casilla de verificación **Objetivo campaña** y elija **Sí**.  

## Enviar cartas y correos electrónicos a los contactos

 El empleado de marketing ayuda al director de esta área a enviar cartas a los probables clientes para agradecerles por visitar la feria de muestras.

### Procedimiento para usar un segmento para enviar una carta a un contacto  

> [!NOTE]  
> En este procedimiento, debe adjuntar un documento de Word. Puede agregar archivos adjuntos en cualquier idioma.

> [!NOTE]  
> Si es necesario, haga clic en el icono **Lápiz de edición** para abrir la página en modo de edición.

1. Abra la ficha **Segmento** para los **Visitantes de la feria de muestras FUTURUS**.  
2. En la ficha desplegable **Interacción**, en el campo **Cód. plantilla interacción**, seleccione la plantilla Carta de negocios, código **NEG.** y seleccione **Sí**.
3. Escoja el campo **Cód. idioma (genérico)** para abrir la página **Idiomas interacción segmento**. Seleccione un **Código de idioma** y haga clic en el botón **Aceptar**.
4. Asegúrese de que **Tipo correspondencia (predeterminado)** está establecido en **Copia impresa**.
5. En el campo **Archivo adjunto**, seleccione el cuadro de diálogo de **Puntos suspensivos**. Esto abre el cuadro de diálogo Importar archivo adjunto.
    1. Seleccione el botón **Elegir** para elegir su archivo.
    1. Busque el archivo y seleccione el botón **Abrir** botón para adjuntarlo.
6. En el campo **Asunto (Genérico)**, escriba el siguiente texto a modo de ejemplo: **Gracias por visitar la feria de muestras**. Seleccione la tecla <kbd>tabulador</kbd> para salir del campo y seleccione el botón **Sí**.
7. Deslice **Envía docs. Word como anexo** la posición de activado y seleccione el botón **Sí**.
8. Seleccione la acción **Registrar**. En la ventana emergente Registrar segmento, habilite **Crear segmento seguimiento**
9. Haga clic en el botón **Aceptar** para iniciar el trabajo por lotes **Registrar segmento**.  

Se envían los archivos adjuntos. Cuando el proceso haya finalizado, haga clic en el botón **Aceptar** para el mensaje que indica que el segmento se registró.  

 Las cartas se imprimen automáticamente y se registra el segmento. Dado que ya se registró el segmento, este no figura en la lista de segmentos, sino que se mueven a la lista de segmentos registrados. Para ver esa lista, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Segmentos archivados** y, a continuación, elija el vínculo relacionado.  

Una vez registrado el segmento, cada carta se envíe que se registra como interacción, que se puede ver en el registro.  

Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movs. log. interacción** y luego elija el enlace relacionado. Hay un movimiento para cada carta enviada.  

### Procedimiento para enviar un correo electrónico a un contacto  

1. En la ficha desplegable **Interacción**, en el campo **Cód. plantilla interacción**, seleccione la plantilla Carta de negocios, código **NEG**.  
2. En el campo **Asunto (Genérico)**, escriba el siguiente texto a modo de ejemplo: **Gracias por visitar la feria de muestras**.  
3. En el campo **Tipo correspondencia**, seleccione **Correo electrónico**.  
4. Especifique la configuración de idioma y adjunte un documento de Word, como en el procedimiento anterior.  
5. Seleccione la acción **Log**. Se abre la página **Grabar segmento**.  
6. Seleccione la casilla **Enviar anexos** para enviar los anexos por correo electrónico.  
7. Seleccione la casilla **Crea segmento seguimiento**.  
8. Elija el botón **Aceptar**.  

 Las cartas se envían por correo electrónico automáticamente y se registra el segmento. Dado que ya se registró el segmento, este no figura en la lista de segmentos, sino que se guarda en la lista de segmentos registrados. Para ver esa lista, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Segmentos archivados** y, a continuación, elija el vínculo relacionado.  

## Registro de las respuestas de la campaña

 En el siguiente par de semanas, los probables clientes responden a la carta. El director de marketing desea realizar un seguimiento de las respuestas y registrar estas interacciones.  

 Con este fin, configure un segmento para los contactos que hayan respondido a la carta.  

### Para registrar las respuestas de la campaña  

1. En la página **Segmento**, en la ficha desplegable **Interacción**, elija el campo **Cód. plantilla interacción**.  

 No existe ninguna plantilla de interacciones para registrar las respuestas a las campañas. En consecuencia, cree una plantilla nueva.  

2. En el menú desplegable **Plantillas de interacción**, elija la acción **Nuevo**.  
3. En el campo **Código**, escriba **RESP** y, en el campo **Descripción**, escriba **Respuestas de la campaña**.  
4. Elija el botón **Aceptar**.
5. Elija **Sí** para confirmar que desea aplicar este código de plantilla de interacción a todas las líneas de segmento.
6. En la ficha desplegable **Campaña**, seleccione el campo **Respuesta campaña**. Elija **Sí** para confirmar el mensaje *Ha modificado la respuesta de la campaña*.  
7. En la página **Segmento**, seleccione **Grabar**.  
8. En la página **Registrar segmento**, borre la casilla de verificación **Enviar archivos adjuntos**. Posteriormente, elija el botón **Aceptar** para confirmar que se ha registrado el segmento.  
  
## Consulte también  
[Gestión de relaciones](marketing-relationship-management.md)  
 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
