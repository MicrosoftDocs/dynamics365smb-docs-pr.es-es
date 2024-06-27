---
title: Usa perfiles para clasificar contactos
description: Lea sobre cómo configurar cuestionarios de perfil para ayudar a clasificar los perfiles de sus contactos comerciales.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'contacts, profiles'
ms.search.form: '5109, 5110'
ms.author: bholtorf
ms.date: 05/20/2022
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Use cuestionarios de perfil para clasificar contactos comerciales

Puede clasificar los contactos con perspectivas de ventas con el fin de identificar los clientes potenciales a los que debe dirigirse la campaña de ventas. Puede configurar los cuestionarios de perfil que desea utilizar en el momento de especificar información de los perfiles de sus contactos. En cada cuestionario, puede configurar distintas preguntas que desee realizar a sus contactos. De esta manera, puede agrupar contactos para que sus campañas tengan más probabilidades de dirigirse a las personas adecuadas en función de los criterios que defina con los cuestionarios.  

Con los cuestionarios adecuados, puede clasificar los distintos clientes potenciales y agruparlos en categorías. Puede utilizar preguntas y respuestas existentes y combinarlas con nuevas preguntas y respuestas para crear un sistema de clasificación propio. Cada respuesta del sistema de clasificación obtendrá un valor de punto y, dependiendo del intervalo que configure para las categorías (*Desde valor* y *Hasta valor*), el sistema de clasificación agrupará los contactos en las categorías definidas. Por ejemplo, clientes *ABC*, proveedores de fidelidad *Alta/baja* o clientes potenciales *Platino/Oro/Plata*.  

Puede ejecutar el cuestionario para que responder de forma automática algunas de las preguntas, según los datos del contacto, cliente o proveedor.  

## Para añadir un cuestionario de perfil

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de cuestionario** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Para añadir preguntas a un cuestionario de perfil

1. Seleccione el cuestionario de perfil correspondiente y, a continuación, elija la acción **Editar config. cuestionario**.  
2. En la primera línea vacía, en el campo **Tipo**, elija **Pregunta** y escriba su pregunta en el campo **Descripción**. Rellene los otros campos de la línea.  

    Opcionalmente, agregue detalles a la pregunta.

    1. Elija la línea con la pregunta y, a continuación, seleccione el menú **Línea** y, a continuación, **Detalles de la pregunta**.  

    2. En la ficha desplegable **Clasificación** de la página **Detalles pregunta perfil**, seleccione **Clasificación contacto autom.**  

    3. En el campo **Campo clasific. contacto**, seleccione la opción **Clasificación**.  

    4. Rellene el campo **% Mín. preguntas respondidas**. El valor predeterminado es **0**.  

        Especifica la cantidad de preguntas que se deben responder para que se calcule esta clasificación.

    5. En la pestaña **Acciones**, en el grupo **Página**, elija **Puntos respuesta**. Introduzca los puntos que desea dar a cada respuesta enumerada en la página **Puntos respuesta**.

        Si desea obtener una información general de los puntos que ha otorgado a cada respuesta, elija la acción **Puntos de respuesta**.

    6. Para ejecutar una actualización, vuelva a la página **Config. cuestionario perfil**. En el menú **Acciones**, en el grupo **Funciones**, seleccione **Actualizar clasificación**.

    En la página **Config. cuestionario perfil**, el número de contactos que cumplen los criterios se muestra en el campo **N.º de contactos**, así como en la **Ficha contacto** de cada contacto.

3. En la siguiente línea vacía, en el campo **Tipo**, elija **Respuesta** y escriba su respuesta en el campo **Descripción**.  
4. En el campo **Prioridad**, seleccione la prioridad. En los campos **Desde valor** y **Hasta valor**, defina un intervalo de punto. Los contactos que reciban puntos en el rango definido obtendrán la respuesta.  

Repita estos pasos para especificar todas las preguntas y respuestas del cuestionario de perfil.

Tras crear un cuestionario, puede usarlo para valorar y clasificar sus contactos. También puede configurar preguntas que se clasifican automáticamente según la información en la ficha de contacto.  

> [!NOTE]
> Si especifica una pregunta que el sistema responde de forma automática, seleccione **Línea** y, a continuación, **Detalles pregunta** para especificar los criterios para responder a la pregunta automáticamente.

## Aplicar cuestionarios a contactos

Puede aplicar sus cuestionarios a contactos manualmente. Solo tiene que abrir la ficha de contacto correspondiente y elegir la acción **Perfil**. Luego, una vez que haya aplicado los cuestionarios que desea aplicar, puede comenzar a utilizar las categorías en sus campañas.  

## la clasificación automática de los contactos

Puede clasificar automáticamente sus contactos según la información de cliente, proveedor y contacto, si configura las preguntas del perfil en la página **Config. cuestionario perfil**.  

> [!NOTE]
> Sólo a los contactos registrados como clientes se les puede asignar una clasificación según los datos de cliente y sólo a los contactos registrados como proveedores se les puede asignar una clasificación según datos de proveedor. La clasificación automática no se actualiza automáticamente. Por lo tanto, quizás desee actualizar los cuestionarios de perfil, después de actualizar los datos del cliente, proveedor o contacto en los que se basa.  

Después de haber configurado las preguntas del perfil automático, si asigna el cuestionario de perfil que contiene esas preguntas a un contacto, [!INCLUDE[prod_short](includes/prod_short.md)] asignará automáticamente las respuestas correctas para ese contacto.  

## Ejemplo

Puede clasificar sus contactos según el volumen de compras que le hagan:

|Respuesta|Se aplica a|
|--- |--- |
|A|contactos que han comprado 500.000 DL o más|
|B|contactos que han comprado de 100.000 DL hasta 499.999 DL|
|U|contactos que han comprado 99.999 DL o menos|

Para ello, rellene los datos de la página **Config. cuestionario perfil** de esta manera:

| Escriba     | Descripción        | Clasificación automática     | Desde valor | Hasta valor |
|----------|--------------------|------------------------------|------------|----------|
| Pregunta | Clasificación ABC | Haga clic para activar el campo |            |          |
| Respuesta   | A                  |                              | 500.000    |          |
| Respuesta   | P                  |                              | 100,000    | 499,999  |
| Respuesta   | U                  |                              |            | 99,999   |

A continuación, rellene los datos de la página **Detalles pregunta perfil** de la siguiente manera:

| Campo                         | Valor         |
|-------------------------------|---------------|
| Campo de clasificación de cliente | Ventas (DL)   |
| Método clasificación         | Valor definido |

Al asignar el cuestionario perfil que contiene esta pregunta a un contacto, la aplicación escribe automáticamente la respuesta adecuada para este contacto en las líneas de perfil de la ficha de contacto.

## Consulte también

[Crear contactos](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]