---
title: "Tutorial: realización de una campaña de ventas | Documentos de Microsoft"
description: "Una campaña es un tipo de actividad que implica varios contactos. Una importante parte de la configuración de una campaña implica la selección del público objetivo para la misma. Con este fin, en Finance and Operations, Business edition, creará un segmento o grupo de contactos con filtros."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e933115531f9adb0296ad8983be00da480f11f25
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Tutorial: realización de una campaña de ventas
Una campaña es un tipo de actividad que implica varios contactos. Una importante parte de la configuración de una campaña implica la selección del público objetivo para la misma. Con este fin, en [!INCLUDE[d365fin](includes/d365fin_md.md)], creará un segmento o grupo de contactos con filtros.  

 Utilice estas funciones en Ventas y Marketing para planificar cuidadosamente las actividades de marketing y para administrar las interacciones con contactos y clientes. Puede crear campañas y configurar segmentos de sus contactos para envíos postales y otros tipos de interacciones con sus clientes y probables clientes.  

 Las funciones Campaña y Segmento con sus procesos automatizados le permitirán planificar, organizar y realizar un seguimiento de sus actividades de marketing. De este modo aumentarán las posibilidades de conseguir nuevos clientes y conservar los actuales.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial  
 En este tutorial se muestra el proceso para realizar un seguimiento en una feria de muestras y dirigirse a clientes potenciales (contactos) en una campaña de seguimiento.  

 El tutorial presenta la función de administración de campaña y segmento en el departamento de Ventas y Marketing. En este tutorial se ilustran las siguientes tareas:  

-   Configuración de una campaña.  
-   Selección del público objetivo.  
-   Extracción de datos.  
-   Envío de cartas a contactos.  
-   Registro de las respuestas de la campaña.  

## <a name="roles"></a>Funciones  
 En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:  

-   Director de marketing o Director de ventas  
-   Empleado de marketing  

## <a name="prerequisites"></a>Requisitos previos  
 Para poder realizar las tareas del tutorial, deberá instalar [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

## <a name="story"></a>Historia  
 El Director de marketing del Departamento de ventas de CRONUS es el responsable de la planificación de campañas y de su ejecución. También toma decisiones sobre en qué ferias de muestras participar y evalúa el progreso de la campaña.  

 El empleado del Departamento de marketing maneja la producción, la distribución y la colocación de material de marketing.  

 La empresa acaba de lanzar un producto denominado el Millennium Server. El producto se ha promocionado recientemente en una fuera de muestras, Computer Futurus. Numerosos clientes han expresado un enorme interés en el producto y, como parte de un esfuerzo promocional, a aquellos clientes que compraron Millennium Server durante el periodo de la campaña se les ofreció un precio especial de campaña.  

 Una de las tareas del empleado de marketing después de la feria de muestra es introducir todos los clientes potenciales como contactos.  

 El director de marketing organiza una campaña, crea un segmento que contiene todos los nuevos contactos y finalmente extrae los datos de contacto para seleccionar el público objetivo para la campaña.  

 El empleado ayuda a enviar cartas de agradecimiento a todos los contactos que dejaron sus tarjetas al personal del stand y, finalmente, el director registra todas las respuestas que reciban de los probables clientes.  

## <a name="setting-up-a-campaign"></a>Organización de una campaña  
 En cuanto el empleado haya introducido las tarjetas de negocios recibidas en la feria de muestras, el director de marketing organiza una ficha de campaña para administrar las actividades relacionadas.  

### <a name="to-set-up-a-campaign"></a>Para configurar una campaña  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Campañas** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione **Nuevo** para crear una nueva campaña. En la ficha de la campaña, pulse Entrar para crear un número de la campaña insertado automáticamente.  
3.  En el campo **Descripción**, escriba una descripción para la campaña, por ejemplo **Feria de muestras FUTURUS**.  
4.  Elija el campo **Cód. estado** y seleccione un código de estado de la lista que se abre en la ventana **Estado campaña**.  
5.  Rellene los campos **Fecha inicial** y **Fecha final** de la campaña como corresponda.  

## <a name="selecting-the-target-audience"></a>Selección del público objetivo  
 El director de marketing crea un segmento para seleccionar los contactos con los que desea interactuar.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Para crear un segmento con los contactos relevantes  

1.  Seleccione la acción **Segmentos**.  
2.  Seleccione **Nuevo** para crear un nuevo segmento. En el segmento nuevo, pulse Entrar para tener un número de segmento insertado automáticamente.  
3.  En la ficha desplegable **General**, en el campo **Descripción**, escriba, por ejemplo, **Visitantes de la feria de muestras FUTURUS**.  

     Después de especificar información general acerca del segmento, seleccione los contactos que desee incluir en el segmento.  

     Puede usar diversos criterios para seleccionar contactos, por ejemplo, puede elegir personas de contacto que trabajan en una ubicación del cliente o un cliente potencial que sea responsable de compras en sus empresas.  

     Utilice los filtros para añadir los contactos según los criterios que mejor se ajusten a sus propósitos. Por ejemplo, puede elegir filtrar por responsabilidad del cargo de la persona de contacto, la relación empresarial o el sector de la empresa de contacto. Para este tutorial, elija el filtro **Responsabilidad cargo** para seleccionar los contactos.  

4.  En la ventana **Segmento**, seleccione **Añadir contactos** para abrir el filtro **Añadir contactos**.  
5.  En la ficha desplegable **Responsabilidad cargo**, seleccione el filtro **Compra** como **Cód. cargo contacto** y elija el botón **Aceptar**.  

     La ventana **Segmento** contiene ahora una lista de contactos basada en los filtros que especifique. En la ficha desplegable **General**, en el campo de **Nº líneas**, puede ver de un vistazo el número de contactos que cumplen estos criterios.  

    > [!NOTE]  
    >  Puede guardar los criterios de segmentación para poder usarlos más adelante.

    1.  En la ventana **Segmento**, elija la acción **Segmento** y, a continuación, elija **Guardar criterio**.  
    2.  En la ventana **Guardar criterios segmento**, especifique un código para el segmento. En el campo **Descripción**, escriba una descripción de los criterios del segmento.
    3.  Elija el botón **Aceptar**.  

## <a name="mining-the-data"></a>Extracción de los datos  
 El director de marketing estudia atentamente la lista de contactos segmentada y observa que es demasiado extensa. Decide reducir la lista basándose en clientes probables reales para asegurarse de centrarse en el grupo objetivo correcto. Este proceso de refinar y reducir los datos también se conoce como extracción de datos.  

### <a name="to-remove-contacts-from-the-segment"></a>Para eliminar los contactos del segmento  

1.  En la ventana **Segmento**, haga clic en **Contactos** y, finalmente, haga clic en **Reducir contactos** para abrir la ventana **Eliminar contactos - Reducir**.  
2.  En la ficha desplegable **Relación negocio**, seleccione el filtro **REF** como **Cód. relación negocio** y elija el botón **Aceptar**.  

     La ventana **Segmento** contiene ahora una lista reducida de contactos y, en el campo **Nº líneas**, puede ver el número de contactos que satisface ahora estos nuevos criterios.  

    > [!NOTE]  
    >  Si tuviera que deshacer esta eliminación de un grupo de contactos, puede hacerlo con la función **Volver**. En otras palabras, puede deshacer la última segmentación.  
    >   
    >  En la ventana **Segmento**, elija la acción **Segmento** y, a continuación, elija **Hacia atrás**.  
    >   
    >  Los contactos que acaba de eliminar se añaden de nuevo a la lista de contactos.  

## <a name="linking-a-segment-to-a-campaign"></a>Vinculación de un segmento con una campaña  
 El director de marketing decide que la lista reducida es la lista final de contactos que desea que forme parte de la campaña. Por lo tanto, vincula este segmento a la campaña Feria comercial FUTURUS.  

### <a name="to-link-a-segment-to-the-campaign"></a>Para vincular un segmento a la campaña  

1.  En la ventana **Segmento** , en la ficha desplegable **Campaña**, elija el campo **Nº campaña** ara seleccionar la campaña a la que desee vincular el segmento, por ejemplo, **CP0001**.  
2.  Dado que este segmento es el objetivo de la campaña, seleccione la casilla de verificación **Objetivo campaña**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Enviar cartas y correos electrónicos a los contactos  
 El empleado de marketing ayuda al director de esta área a enviar cartas a los probables clientes para agradecerles por visitar la feria de muestras.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Procedimiento para usar un segmento para enviar una carta a un contacto  

1.  Abra la ficha **Segmento** para los **Visitantes de la feria de muestras FUTURUS**.  
2.  En la ficha desplegable **Interacción**, en el campo **Cód. plantilla interacción**, seleccione la plantilla Carta de negocios, código **NEG**.  
3.  En el campo **Asunto (Genérico)**, escriba el siguiente texto a modo de ejemplo: **Gracias por visitar la feria de muestras**.  

    > [!NOTE]  
    >  Esta plantilla consta de más de un documento adjunto, cada uno de los cuales está escrito en un idioma distinto. Los idiomas del ejemplo comprenden español e inglés.  

4.  Escoja el campo **Cód. idioma (genérico)** para abrir la ventana **Idiomas interacción segmento**. Seleccione un código de idioma y haga clic en el botón **Aceptar**.  
5.  Puede mostrar el documento en el idioma seleccionado. Seleccione la acción **Archivo adjunto** y, a continuación **Abrir**.  

     Para responder al mensaje que solicita permiso para iniciar Word, elija la opción **Permitir para esta sesión de cliente**.  

     De esta manera se abrirá el documento de Word anexo para que pueda examinarlo. También puede aprovechar esta oportunidad para editar y modificar la carta. Cierre Word cuando haya terminado.  

6.  Escriba el asunto de la carta en el campo **Asunto**, en el idioma seleccionado para la plantilla.  
7.  Seleccione la acción **Log**.
8.  Active la casilla **Envía anexos** para imprimir los anexos.  

    1. Seleccione la casilla **Crea segmento seguimiento**.  
    2. Haga clic en el botón **Aceptar** para iniciar el trabajo por lotes **Grabar segmento**.  

9. Se envían los archivos adjuntos. Cuando el proceso haya finalizado, haga clic en el botón **Aceptar** para el mensaje que indica que el segmento se registró.  

     Las cartas se imprimen automáticamente y se registra el segmento. Dado que ya se registró el segmento, este no figura en la lista de segmentos, sino que se mueven a la lista de segmentos registrados. Para ver la lista, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Segmentos archivados** y, a continuación, seleccione el vínculo relacionado.  

10. Una vez registrado el segmento, cada carta se envíe que se registra como interacción, que se puede ver en el registro.  

     Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Movs. log. interacción** y, a continuación, seleccione el vínculo relacionado. Hay un movimiento para cada carta enviada.  

### <a name="to-send-an-email-message-to-a-contact"></a>Procedimiento para enviar un correo electrónico a un contacto  

1.  En la ficha desplegable **Interacción**, en el campo **Cód. plantilla interacción**, seleccione la plantilla Carta de negocios, código **NEG**.  
2.  En el campo **Asunto (Genérico)**, escriba el siguiente texto a modo de ejemplo: **Gracias por visitar la feria de muestras**.  
3.  En el campo **Tipo correspondencia**, seleccione **Correo electrónico**.  
4.  Especifique la configuración de idioma, tal como lo hizo en el procedimiento anterior.  
5.  Seleccione la acción **Log**. Se abre la ventana **Grabar segmento**.  
6.  Seleccione la casilla **Enviar anexos** para enviar los anexos por correo electrónico.  
7.  Seleccione la casilla **Crea segmento seguimiento**.  
8.  Elija el botón **Aceptar**.  

     Las cartas se envían por correo electrónico automáticamente y se registra el segmento. Dado que ya se registró el segmento, este no figura en la lista de segmentos, sino que se guarda en la lista de segmentos registrados. Para ver la lista, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Segmentos archivados** y, a continuación, seleccione el vínculo relacionado.  

## <a name="registering-campaign-responses"></a>Registro de las respuestas de la campaña  
 En el siguiente par de semanas, los probables clientes responden a la carta. El director de marketing desea realizar un seguimiento de las respuestas y registrar estas interacciones.  

 Con este fin, configure un segmento para los contactos que hayan respondido a la carta.  

### <a name="to-register-campaign-responses"></a>Para registrar las respuestas de la campaña  

1.  En la ventana **Segmento**, expanda la ficha desplegable **Interacción**.  
2.  Elija el campo de **Cód. plantilla interacción**.  

     No existe ninguna plantilla de interacciones para registrar las respuestas a las campañas. En consecuencia, cree una plantilla nueva.  

3.  En la ventana **Plantillas de interacción**, elija la acción **Nuevo**.  
4.  En el campo **Código**, escriba **RESP** y, en el campo **Descripción**, escriba **Respuestas de la campaña**.  
5.  Elija el botón **Aceptar**.  
6.  Seleccione esta plantilla de interacción en el campo **Cód. plantilla interacción** y confirme el mensaje que pregunta si desea actualizar las líneas de los segmentos que tengan el mismo Cód. plantilla interacción.  

     Especifique ahora que estos contactos hayan respondido a la campaña:  
7.  En la ficha desplegable **Campaña**, en el campo **Nº campaña** seleccione la campaña.  
8.  Salga del campo **N.º campaña** y confirme el mensaje que le pregunta si desea actualizar las líneas del segmento que tengan el mismo Cód. plantilla interacción.  
9. Seleccione el campo **Respuesta campaña** y confirme el siguiente mensaje.  

     Archive el segmento para asegurarse de registrar las interacciones.  
10. En la ventana **Segmento**, seleccione **Grabar**.  
11. En la ventana **Archivar segmento**, desactive la casilla de verificación **Envía anexos**, elija el botón **Aceptar** y confirme el mensaje que aparece.  

     Después de archivado el segmento, se crea automáticamente un movimiento para la campaña a fin de registrar esta acción en la ventana **Movs. campaña**.  

## <a name="see-also"></a>Consulte también  
[Gestión de relaciones](marketing-relationship-management.md)  
 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

