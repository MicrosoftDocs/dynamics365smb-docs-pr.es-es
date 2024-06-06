---
title: Acceso a Business Central con licencias de Microsoft 365
description: 'Aprenda cómo los usuarios pueden obtener acceso a los datos de Business Central, por ejemplo en chats y canales de Microsoft Teams, con solo una licencia de Microsoft 365, pero ninguna licencia de Business Central.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: overview
ms.date: 11/22/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Acceso a Business Central con licencias de Microsoft 365

A los usuarios de [!INCLUDE[prod_short](includes/prod_short.md)] se les asigna una licencia de Dynamics 365 Business Central que les permite ver, modificar y actuar sobre sus datos comerciales desde cualquier interfaz de usuario. Para todos los demás empleados de la organización que solo necesitan ver datos ocasionalmente, Business Central ofrece acceso a través de Microsoft 365.  

Cuando una organización tiene una suscripción a Dynamics 365 Business Central y Microsoft 365, los administradores pueden configurar entornos para habilitar el acceso con licencias de Microsoft 365, y elegir exactamente a qué tablas y otros objetos tendrá acceso esta categoría de usuario. Cuando se configura, los empleados que tienen una licencia de Microsoft 365, pero ninguna licencia de [!INCLUDE [prod_short](includes/prod_short.md)] pueden ver los registros de [!INCLUDE [prod_short](includes/prod_short.md)] que se comparten con ellos en chats y canales de Microsoft Teams.

## ¿Por qué habilitar el acceso con licencias de Microsoft 365?  

- Desbloquee datos maestros a los que todos los empleados de la organización deberían tener acceso.

- Capacite a los departamentos que no se ejecutan en [!INCLUDE [prod_short](includes/prod_short.md)] para que se sirvan a sí mismos, accediendo a los datos clave necesarios para realizar con éxito sus tareas, eliminando la necesidad de solicitar continuamente datos de otros.

- Aumente la eficacia de la colaboración para que las tareas y los proyectos que abarcan todos los departamentos se completen a tiempo, al eliminar la fricción que generalmente se asocia con los errores de acceso denegado debido a la licencia.

- Aumente el rendimiento del equipo para que las personas puedan tomar decisiones basadas en datos que incluyan a todos los miembros del grupo, incluso si no trabajan en [!INCLUDE [prod_short](includes/prod_short.md)].

- Cumpla con los objetivos de presupuesto de licencias mediante la asignación de licencias que se ajusten progresivamente a las necesidades de los empleados, con licencias de Microsoft 365 para acceso de solo lectura, licencias de Dynamics 365 Business Central de miembros del equipo para acceso de escritura limitado, y Dynamics 365 Business Central Essentials o Premium para acceso completo de escritura.

- Mejore la seguridad de los datos al reducir la necesidad de pegar fragmentos de pantalla de datos comerciales fuera de los límites de la gobernanza de datos.

## Derechos de uso

Cuando una persona accede a [!INCLUDE [prod_short](includes/prod_short.md)] con una licencia de Microsoft 365, las entidades de licencia dan derecho al usuario a leer (pero no a escribir) datos de [!INCLUDE [prod_short](includes/prod_short.md)] a través de una interfaz de usuario simplificada en Microsoft Teams. Esta sección explica estos derechos de uso y limitaciones que le ayudan a planificar cómo configurar y aprovechar al máximo esta capacidad. Para obtener más información sobre este tipo de licencia en comparación con otras licencias de [!INCLUDE [prod_short](includes/prod_short.md)], consulte la [Guía de licencias de Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).
 
### Acceso de clientes

Los usuarios tienen derecho a acceder a los datos de [!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams. La siguiente tabla resume cuáles de los diferentes métodos de acceso al servicio [!INCLUDE [prod_short](includes/prod_short.md)] están permitidos con esta licencia.

|Cliente accediendo al servicio de Business Central |Acceso|
|-|-|
|Aplicación Business Central para Microsoft Teams|![Sí](media/check.png)|
|Cliente web de Business Central |![N.º](media/x-icon.png ) |
|Aplicaciones móviles de Business Central|![N.º](media/x-icon.png )|
|API de Business Central|![N.º](media/x-icon.png )|
|Integraciones de Business Central con otras aplicaciones de Office|![N.º](media/x-icon.png )|
|Business Central integrado en cualquier otra aplicación |![N.º](media/x-icon.png )|

### Acceso a datos

Los usuarios tienen derecho a leer los datos de la tabla, pero no pueden modificar, crear o eliminar registros. La plataforma [!INCLUDE [prod_short](includes/prod_short.md)] evita automáticamente escribir en cualquier tabla de datos.  

### Uso de objetos

El acceso con licencias de Microsoft 365 no restringe a qué objetos o rangos de objetos de Business Central se puede acceder. Los usuarios tienen derecho a acceder a la aplicación base de Microsoft y a cualquier extensión, como personalizaciones y aplicaciones complementarias.

## Interfaz de usuario simplificada

Los usuarios tienen derecho a un conjunto reducido de características y funciones proporcionadas por [!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams. Las siguientes tablas indican las características destacadas. Esta no es una lista exhaustiva y está sujeta a cambios.

Características de la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams:

|Característica  |Disponible|
|-|-|
|Ver tarjetas de [!INCLUDE [prod_short](includes/prod_short.md)]|![Sí](media/check.png)|
|Ver detalles de tarjeta |![Sí](media/check.png) |
|Anclar detalles de tarjeta como pestaña |![Sí](media/check.png)|
|Ver pestañas de [!INCLUDE [prod_short](includes/prod_short.md)]|![Sí](media/check.png)|
|Agregar una pestaña de [!INCLUDE [prod_short](includes/prod_short.md)]|![No_](media/x-icon.png )|
|Buscar contactos profesionales |![No](media/x-icon.png )|
|Pegar y compartir una versión preliminar de vínculo como una tarjeta|![No](media/x-icon.png )|

Funciones del cliente de [!INCLUDE [prod_short](includes/prod_short.md)] integrado en Teams:

|Función |Disponible|Funciones de ejemplo|
|-|-|-|
|Acciones del sistema de manipulación de datos |![N.º](media/x-icon.png )|Editar, crear, eliminar|
|Funciones básicas en listas|![Sí](media/check.png)|Buscar, ordenar, cambiar el diseño|
|Funciones avanzadas en listas|![N.º](media/x-icon.png )|Panel de filtro, vistas|
|Desglose de lista a tarjeta |![Sí](media/check.png)||
|Acceder a datos desde tablas relacionadas|![N.º](media/x-icon.png )|Panel de cuadro informativo, desglose de campo, vistazo, búsqueda |
|Acciones|![N.º](media/x-icon.png )|Barra de acción, menús de acción, acciones de notificación de página|
|Atajos de todo el sistema|![N.º](media/x-icon.png )|Mi configuración, explorador de roles, búsqueda Dígame  |
|Copiar|![Sí](media/check.png)|Copiar filas, copiar valor de campo, copiar vínculo a página|
|Personalización de IU|![N.º](media/x-icon.png )|Personalice| 
|Personalización de alineación|![Sí](media/check.png)|Redimensionar columna, Expandir/Contraer, Mostrar más |
|Compartir datos |![N.º](media/x-icon.png )|Abrir o editar en Excel, compartir con Teams|
|Asistencia al usuario alineado|![Sí](media/check.png) |Información sobre herramientas, vínculos a la documentación|
|Asistencia de usuario avanzada |![N.º](media/x-icon.png )|Sugerencias para la enseñanza de páginas y campos, panel de ayuda|

## Requisitos mínimos

Esta sección describe los requisitos mínimos que debe cumplir su organización para habilitar el acceso con licencias de Microsoft 365 y para que usuarios particulares de Microsoft Teams accedan a los datos de [!INCLUDE [prod_short](includes/prod_short.md)] sin una licencia de [!INCLUDE [prod_short](includes/prod_short.md)].

### Requisitos para habilitar el acceso

- [!INCLUDE [prod_short](includes/prod_short.md)] en línea (SaaS).

- Los entornos deben ser de la plataforma versión 21.1 o posterior.

### Requisitos para que los usuarios individuales accedan a los datos en Teams

- Se debe acceder a los datos mediante la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams. Los usuarios deben tener instalada la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams y deben usar uno de los clientes de Teams compatibles. Para obtener una lista de clientes de Teams compatibles con [!INCLUDE [prod_short](includes/prod_short.md)], consulte [Requisitos mínimos para utilizar Business Central](product-requirements.md#teams).

- Los usuarios deben ser internos de la organización, lo que significa que una identidad de usuario se origina en el mismo inquilino principal donde se implementa [!INCLUDE [prod_short](includes/prod_short.md)] y donde se habilita el acceso. Las identidades externas no son compatibles. [!INCLUDE [prod_short](includes/prod_short.md)] evita automáticamente el acceso a los invitados.

- Los usuarios deben tener asignada una licencia de Microsoft 365 de uno de los siguientes planes.
  
  |Plan compatible|Id. de producto |
  |-|-|
  |Microsoft 365 Business Basic|3b555118-da6a-4418-894f-7df1e2096870|
  |Microsoft 365 Business Standard|f245ecc8-75af-4f8e-b61f-27d8114de5f3|
  |Microsoft 365 Business Premium |cbdc14ab-d96c-4c30-b9f4-6ada7cdc1d46|
  |Microsoft 365 E3 |05e9a617-0261-4cee-bb44-138d3ef5d965 |
  |Microsoft 365 E5|06ebc4ee-1bb5-47dd-8120-11324bc54e06|
  |Microsoft 365 F1|50f60901-3181-4b75-8a2c-4c8e4c1d5a72|
  |Microsoft 365 F3|66b55226-6b4f-492c-910c-a3b7a3c9d993|
  |Office 365 E1|18181a46-0d4e-45cd-891e-60aabd171b4e|
  |Office 365 E2 |6634e0ce-1a9f-428c-a498-f84ec7b8aa2e|
  |Office 365 E3|6fd2c87f-b296-42f0-b197-1e91e994b900|
  |Office 365 E5|c7df2760-2c81-4ef7-b578-5b5392b571df|
  |Office 365 F2|131fd665-5752-4995-a628-bcba5c889745|
  |Office 365 F3|4b585984-651b-448a-9e53-3b10f069cf7f|
  |Microsoft Teams Essentials (Microsoft Entra Identity) |3ab6abff-666f-4424-bfb7-f0bc274ec7bc|
  
  La mayoría de las ofertas basadas en estos planes también son compatibles. Por ejemplo, si se suscribe a Microsoft 365 Business Premium (Precio para personal sin fines de lucro), es una oferta específica para organizaciones sin fines de lucro basada en el plan de Microsoft 365 Business Premium y, por lo tanto, es soportado.

  > [!NOTE]
  > ¿No puede encontrar su plan en la lista? Microsoft busca continuamente comentarios sobre cómo podemos mejorar nuestro servicio y expandir nuestra oferta para que más clientes puedan aprovechar esta capacidad. Comparta su idea sobre qué planes deberíamos admitir a continuación en [https://aka.ms/bcIdeas](https://aka.ms/bcIdeas).

- Los usuarios deben tener asignada una licencia de Microsoft 365 que tenga la aplicación de Microsoft Teams habilitada en la lista de aplicaciones para esa licencia.

  |Aplicaciones admitidas|Id. de plan de servicio|
  |-|-|
  |Microsoft Teams|57ff2da0-773e-42df-b2af-ffb7a2317929 |

- La organización debe tener al menos otro usuario al que se le asigne una licencia de Dynamics 365 Business Central.

## Pasos siguientes

- Obtenga una comprensión del flujo de acceso de los usuarios para ayudar a planificar su enfoque y configuración de Business Central para satisfacer las necesidades comerciales. Consulte [Flujo de acceso de usuarios](admin-access-with-m365-license-flow.md).
- Configure su entorno y usuarios para acceder con licencias de Microsoft 365. Consulte [Configurar el acceso con licencias de Microsoft 365](admin-access-with-m365-license-setup.md).

## Consulte también .

[Integración de Business Central y Microsoft Teams](across-teams-overview.md)  
