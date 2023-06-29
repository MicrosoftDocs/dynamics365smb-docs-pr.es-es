---
title: Clasificar confidencialidad de datos
description: Debe especificar qué tipo de datos almacena sobre las personas para que pueda responder a las solicitudes de los asuntos de datos.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.search.form: 1752
ms.date: 06/14/2021
---

# <a name="classifying-data-sensitivity-fields"></a><a name="classifying-data-sensitivity-fields"></a><a name="classifying-data-sensitivity-fields"></a>Clasificar campos de confidencialidad de datos
Para clasificar los campos que contienen datos confidenciales o personales, un socio de Microsoft puede establecer la propiedad ```DataClassification``` en los campos. Esto requiere acceso a las tablas de la base de datos, ya sea a través del entorno de desarrollo o ejecutando un script de Windows PowerShell. Para obtener más información, consulte [Clasificar datos](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data).  

Como cliente, puede agregar un segundo nivel de clasificación especificando los niveles de confidencialidad para los datos que almacena en campos estándar y personalizados. La clasificación de la confidencialidad de los datos ayuda a garantizar que sepa dónde guarda los datos personales en su sistema y facilita la respuesta a las solicitudes de los interesados. Por ejemplo, si un contacto o cliente le pide que exporte sus datos personales. Para obtener más información, vea [Respuesta a las solicitudes de datos personales](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Microsoft proporciona esta característica de Clasificación de confidencialidad de datos como una cuestión de conveniencia solamente. Es su responsabilidad clasificar los datos de manera apropiada y cumplir con las leyes y normativas que le sean aplicables. Microsoft se exime de toda responsabilidad respecto de cualquier reclamo relacionado con su clasificación de los datos.  

En la tabla siguiente se describen niveles de confidencialidad de datos que puede asignar.

|Confidencialidad|Description|
|----|----|
|Confidencial | Información sobre el origen racial o étnico de un sujeto de datos, opiniones políticas, creencias religiosas, participación en sindicatos, salud física o mental, sexualidad o detalles sobre delitos. |
|Personal | Información que se puede utilizar para identificar un sujeto de datos, ya sea directamente o en combinación con otros datos o información.|
|Confidencial | Los datos comerciales que utiliza para fines de contabilidad u otros fines comerciales, y no desea exponer a otras entidades. Por ejemplo, movimientos contables.|
|Normal | Datos generales que no pertenecen a ninguna otra categoría.|

## <a name="how-do-i-classify-my-data"></a><a name="how-do-i-classify-my-data"></a><a name="how-do-i-classify-my-data"></a>¿Cómo clasifico mis datos?

Clasificar la confidencialidad de muchos campos uno a uno llevaría mucho tiempo. Para ayudar a acelerar el proceso, proporcionamos herramientas que puede usar para clasificar en bloque la confidencialidad de los campos y luego ajustar las clasificaciones para campos específicos. Puede encontrar herramientas en la hoja de trabajo Clasificación de datos, que está disponible en el área de trabajo Administración de usuarios, grupos de usuarios y permisos. Es necesario ser administrador del sistema para usar la hoja de trabajo.

> [!Important]
> Cuando abra la hoja de trabajo Clasificación de datos por primera vez, estará vacía. Debe ejecutar la guía Clasificación de datos para generar la lista de campos. Para iniciar la guía, elija la acción **Configurar clasificaciones de datos**.

Por ejemplo, la hoja de trabajo Clasificación de datos le permite hacer cosas como:  

* Usar la guía de clasificación de datos para exportar sus campos a una hoja de cálculo de Excel donde puede clasificarlos en bloque. Usar la hoja de cálculo de Excel es particularmente útil si colabora con un socio de Microsoft. Después de actualizar la hoja de trabajo, puede usar la guía para importar y aplicar las clasificaciones. También puede utilizar la guía para ordenar campos manualmente.  
* Elija un campo y luego filtre la lista para buscar campos similares que probablemente pertenezcan a la misma clasificación que el campo en el que basó la búsqueda.  
* Investigar un campo por su contenido.  

> [!Tip]
> Hemos definido clasificaciones de confidencialidad de muestra para las tablas y campos en la empresa de demostración Cronus. Puede utilizar las clasificaciones como inspiración cuando ordene sus propias tablas y campos.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Clasificar datos](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
