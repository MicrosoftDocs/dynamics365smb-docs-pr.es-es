---
title: Preguntas más frecuentes de Power BI
description: Obtenga respuestas a algunas preguntas típicas sobre cómo trabajar con Power BI y Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: 939b280e631113d3196f6fbbc90d9bf19b9fc408
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025838"
---
# <a name="power-bi--faq"></a>Preguntas más frecuentes de Power BI

Este artículo responde algunas de las preguntas que pueda tener sobre cómo trabajar con Power BI y [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[General](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Seleccioné un informe para mi área de trabajo en Business Central. Si luego hago cambios en las imágenes del informe en línea, ¿el área de trabajo se actualizará automáticamente a mis cambios?

Sí, porque los informes están incorporados desde Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>¿Están las aplicaciones de Business Central disponibles para Power BI en otros idiomas además del inglés?

Nº Actualmente, estas aplicaciones solo están disponibles en inglés.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Una vez que se publique un informe en mi espacio de trabajo powerbi.com, ¿puedo descargar su pbix? 

Sí. Para más información, vea [Descargar un informe del servicio Power BI a Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>¿Puedo descargar las aplicaciones como archivos pbix? 

Nº Actualmente, no ofrecemos la descarga de archivos pbix para las aplicaciones de Power BI, porque están publicadas en AppSource.

## <a name="license"></a>[Licencias](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>¿Necesito una licencia de Power BI profesional para publicar informes? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nº No es necesaria una licencia profesional para publicar informes. La licencia estándar (gratuita) de Power BI es suficiente. Para obtener más información, consulte [Licencias de Power BI](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>¿Hay algo que no pueda hacer con la licencia gratuita?

No puede compartir informes ni instalar las aplicaciones de Business Central para Power BI. Aparte de eso, la licencia gratuita le permite crear casi todas las variaciones de gráficos e informes.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Si alguien comparte un informe con otra persona, esa persona necesita una licencia profesional para ver el informe. ¿Hay planes para hacer posible esta capacidad con la licencia gratuita?

No tenemos control sobre este requisito. Este requisito lo establece Power BI. Para más información, vea [Compartir paneles e informes de Power BI con compañeros de trabajo y otros](/power-bi/collaborate-share/service-share-dashboards).  

## <a name="designer"></a>[Diseñador](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>¿El conector funciona con páginas API?

Aún no. Pero, a partir de junio de 2021, el nuevo conector de Power BI admitirá tanto los servicios web de Business Central como las páginas API. Para más información, vea [Permitir que el conector de Power BI trabaje con las API de Business Central, en lugar de solo con servicios web](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>¿Es posible elegir el entorno de Business Central obtener datos para Power BI, por ejemplo, como una espacio aislado o un entorno de producción? 

Sí. Se puede elegir fácilmente. Cuando se conecta a Business Central mediante el conector, debe elegir el entorno y el nombre de la empresa.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>¿Puedo combinar datos de varios entornos de producción del mismo inquilino?

Sí. En Power BI, simplemente vuelva a ejecutar la operación de obtención de datos y elija el entorno que desee.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>¿Qué páginas de Business Central tienen la parte del informe de Power BI?  

Actualmente, hay algunas páginas seleccionadas que tienen un cuadro informativo con una parte de **Informes de Power BI** para mostrar un informe. 

En las páginas de lista, la parte de **Informes de Power BI** se filtra para mostrar informes que pertenecen a los datos de la lista. Aquí están las páginas de tipo lista que incluyen la parte **Informes de Power BI**:

|Id. de página|Name|
|-------|----|
|22|Lista de clientes|
|27|Lista de proveedores|
|31|Lista de productos|
|9305|Lista de pedidos de venta|
|9308|Facturas compra|

Aquí hay otras páginas que contienen la parte más grande, no filtrada, de **Informes de Power BI**:

|Id. de página|Name|
|-------|----|
|1156|Detalle de empresas|
|4013|Información de Nube inteligente |
|9006|Área de trabajo de procesador de pedidos|
|9008|Almacén Área de trabajo básica|
|9010|Área de trabajo de planificadores de producción|
|9015|RC de arministrador de proyectos de trabajo|
|9016|Área de trabajo de repartidor de servicios|
|9022|Área de trabajo del administrador de negocio|
|9024|Área de trabajo del administrador de seguridad|
|9026|Gerente de Ventas y relaciones RC|
|9027|Área de trabajo Contable|

> [!TIP]
> No tenemos planes de agregarlo a todas las páginas de lista en este momento. Sin embargo, puede crear una extensión de página sencilla que agregue la parte **Informes de Power BI** parte en un cuadro informativo. Para obtener más información, consulte [Agregar partes de informes de Power BI a páginas](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) en la ayuda para desarrolladores y profesionales de TI.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>¿Hay alguna forma de filtrar un conjunto de datos de Business Central *antes de* meterlo en Power BI, en lugar de aplicar filtros después?

Para filtrar conjuntos de datos más grandes, la forma más sencilla es establecer un filtro en su informe de Power BI, editando directamente la fórmula de Power Query. La mayoría de los filtros que establezca de esta manera se pasarán a Business Central mediante el plegado de consultas. Vea [Actualización incremental para conjuntos de datos](/power-bi/admin/service-premium-incremental-refresh).

Actualmente, no hay forma de configurar un filtro para los datos del servicio web desde Business Central. Si su aplicación necesita establecer un filtro desde Business Central, tendrá que crear una aplicación de Business Central personalizada para este propósito.

<!-- 8 and 9 -->

### <a name="for-embedding-reports-in-business-central-pages-right-now-its-only-possible-to-get-reports-from-my-workspace-in-power-bi-are-there-plans-to-make-it-possible-to-get-them-from-custom-workspaces"></a>Para insertar informes en las páginas de Business Central, ahora solo es posible obtener informes de *Mi espacio de trabajo* en Power BI. ¿Hay planes para que sea posible obtenerlos de espacios de trabajo personalizados?

Sí. Tenemos entre nuestros planes agregar soporte para espacios de trabajo compartidos, pero aún no tenemos una línea de tiempo que ofrecerle.  

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Desde Power BI, además de utilizar una consulta, ¿hay otra forma de obtener datos de las tablas de Business Central que no tienen una página asociada? Por ejemplo, como la tabla *Asignación de valores de atributos de artículos*.

Nº No en este momento.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>¿Las consultas publicadas son más rápidas de usar que las páginas publicadas?

Cuando se trata de servicios web, las consultas publicadas suelen ser más rápidas que las páginas publicadas equivalentes. La razón es que las consultas están optimizadas para leer datos y no contienen desencadenadores costosos como OnAfterGetRecord.

Cuando el nuevo conector esté disponible en junio de 2021, le recomendamos que utilice páginas de API en lugar de consultas publicadas como servicios web.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-developer-have-to-create-a-custom-query"></a>¿Existe alguna forma de que un usuario final cree un servicio web con una columna que esté en una tabla de Business Central, pero no una página? ¿O el desarrollador tendrá que crear una consulta personalizada? 

Aún no. Pero cuando el nuevo conector esté disponible en junio de 2021, un desarrollador puede crear una nueva página de API para cumplir con este requisito. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>¿Puedo conectar Power BI a un servidor de base de datos de solo lectura de Business Central Online? 

Nº Pero tenemos esta característica en nuestra hoja de ruta a largo plazo. 

## <a name="performance"></a>[Rendimiento](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>¿Es más rápido obtener datos usando páginas de API que usando servicios web?

Sí. Nuestras pruebas indican que las páginas de API tienen hasta un 25% más de rendimiento que los servicios web.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>¿Hay planes para tener un espejo en la instancia de Azure SQL Database, al que pueda conectarme directamente?

Nº No en este momento. Solo puede comunicarse con Business Central a través de las API.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>La carga de datos desde los servicios web de Business Central parece lenta. ¿Hay alguna forma de obtener datos directamente de la tabla de la base de datos SQL?

Nº El acceso directo a la base de datos no es posible, pero cambiar a las páginas de API (cuando el nuevo conector esté disponible) será de gran ayuda.

## <a name="advanced"></a>[Avanzado](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>¿Hay planes para que el conector de Power BI admita las funciones de actualización incremental en el servicio de Power BI?

Sí. Está en nuestra hoja de ruta.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Si una solución local de Business Central no tiene acceso a Internet, ¿puedo seguir usando Power BI?
<!-- todo: please explain this one-->

Sí. En este caso, use Power BI Desktop localmente y conéctese a Business Central local. Una vez conectado, puede crear y ver informes, pero no puede publicarlos en el servicio de Power BI. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>¿Existe algún plan para hacer posible la replicación de las bases de datos de Business Central Online para que sean accesibles para consultas SQL de solo lectura? Esta capacidad admitiría la actualización incremental y sería mucho más rápida que las API o los servicios web.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Sí. Tenemos esta característica en nuestra hoja de ruta a largo plazo. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Si uso Azure Data Factory para obtener datos de Business Central y utilizarlos en Power BI, ¿ayudará eso a aumentar el rendimiento? 

Sí. Este escenario avanzado ayudará a Business Central a mantener el rendimiento, porque el acceso a los datos se realizaría a través de Azure Data Factory.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>¿Hay planes para admitir las canalizaciones de implementación de Power BI o una forma de crear canalizaciones de implementación para informes PBI, similar a las extensiones? ¿O tal vez incluso una API sencilla en Business Admin Center? 

Estamos investigando esta función. Power BI ofrece API enriquecidas para controlar la implementación de informes. Para más información, vea [Introducción a las canalizaciones de implementación](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="ive-tried-the-preview-of-the-new-connector-which-will-be-live-in-june-2021-i-see-some-values-like-_x0020_-when-connecting-to-api-v20-what-are-these-values"></a>He probado la vista previa del nuevo conector, que estará disponible en junio de 2021. Veo algunos valores como "_x0020_" al conectar a la API v2.0. ¿Qué son estos valores?

La próxima versión del conector de Power BI permite conectarse a las páginas de la API de Business Central, incluida la API v2.0. Estas páginas incluyen algunos campos basados en [Objetos AL Enum](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Los campos basados en objetos AL Enum deben tener nombres que sean coherentes y siempre iguales, para que los filtros del informe siempre funcionen, sin importar el idioma o el sistema operativo que esté utilizando. Por este motivo, los campos basados en AL Enums no se traducen y se codifican para evitar cualquier carácter especial, incluido el espacio. En particular, siempre que haya una opción vacía en el objeto AL Enum, se codifica como "_x0020_". Siempre puede aplicar una transformación a sus datos en Power BI si desea mostrar algún valor diferente para estos campos, por ejemplo, "Vacío".


---

## <a name="see-also"></a>Consulte también

[Licencia de Power BI](admin-powerbi-setup.md#license)
[Introducción a Business Central y Power BI](admin-powerbi.md)  
[Información general sobre integración de Power BI](admin-powerbi-overview.md)  
[Habilitación de Power BI en Business Central](admin-powerbi-setup.md)  
[Trabajar con informes de Power BI en Business Central](across-working-with-powerbi.md)  
[Trabajar con datos de Business Central en Power BI](across-working-with-business-central-in-powerbi.md)  
[Creación de informes de Power BI para mostrar datos de Business Central](across-how-use-financials-data-source-powerbi.md)    
[Documentación de Power BI](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]