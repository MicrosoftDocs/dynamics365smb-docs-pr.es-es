---
title: Preguntas más frecuentes de Power BI
description: Obtenga respuestas a algunas preguntas típicas sobre cómo trabajar con Power BI y Business Central.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
---
# Preguntas más frecuentes de Power BI

Este artículo responde algunas de las preguntas que pueda tener sobre cómo trabajar con Power BI y [!INCLUDE [prod_short](includes/prod_short.md)].

## [General](#tab/general)
<!-- 26 -->
### Seleccioné un informe para mi área de trabajo en Business Central. Si luego hago cambios en las imágenes del informe en línea, ¿el área de trabajo se actualizará automáticamente a mis cambios?

Sí, porque los informes están incorporados desde Power BI.

<!-- 3 -->
### ¿Están las aplicaciones de Business Central disponibles para Power BI en otros idiomas además del inglés?

Nº Actualmente, estas aplicaciones solo están disponibles en inglés.

<!-- 24 -->
### Una vez que se publique un informe en mi espacio de trabajo powerbi.com, ¿puedo descargar su pbix? 

Sí. Para más información, vea [Descargar un informe del servicio Power BI a Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### ¿Puedo descargar las aplicaciones como archivos pbix? 

Nº Actualmente, no ofrecemos la descarga de archivos pbix para las aplicaciones de Power BI, porque están publicadas en AppSource.

## [Licencias](#tab/license)

<!-- 14 -->
### ¿Necesito una licencia de Power BI profesional para publicar informes? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nº No es necesaria una licencia profesional para publicar informes. La licencia estándar (gratuita) de Power BI es suficiente. Para obtener más información, consulte [Licencias de Power BI](admin-powerbi-setup.md#license).

<!-- 15 -->
### ¿Hay algo que no pueda hacer con la licencia gratuita?

No puede compartir informes ni instalar las aplicaciones de Business Central para Power BI. Aparte de eso, la licencia gratuita le permite crear casi todas las variaciones de gráficos e informes.

<!-- 16 -->
### Si alguien comparte un informe con otra persona, esa persona necesita una licencia profesional para ver el informe. ¿Hay planes para hacer posible esta capacidad con la licencia gratuita?

No tenemos control sobre este requisito. Este requisito lo establece Power BI. Para más información, vea [Compartir paneles e informes de Power BI con compañeros de trabajo y otros](/power-bi/collaborate-share/service-share-dashboards).  

## [Diseñador](#tab/designer)

<!-- 7 -->
### ¿El conector funciona con páginas API?

Sí. A partir de junio de 2021, el nuevo conector de Power BI admite tanto los servicios web de Business Central como las páginas API. Para más información, vea [Permitir que el conector de Power BI trabaje con las API de Business Central, en lugar de solo con servicios web](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### ¿Puedo crear un informe de Power BI utilizando las API Líneas factura de venta o Líneas de diario?

Los registros de línea más utilizados están disponibles en las [API de Business Central v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/)). Para que pueda utilizarlos para crear informes en Power BI seleccionándolos en el conector de **Dynamics 365 Business Central**. Sin embargo, las API **Líneas** están diseñadas para usarse solo con algunos filtros muy específicos y es posible que no funcionen en su escenario. Es posible que obtenga un error similar a "Debe especificar una identificación o una identificación de documento para obtener las líneas". Para solucionar este problema, siga los siguientes pasos cuando obtenga datos de Business Central para el informe en Power BI Desktop:

1. En lugar de incluir la fuente de datos para la entidad de líneas, agregue la fuente de datos principal. Por ejemplo, agregue **Factura venta** en lugar de **Líneas factura de venta**.
2. Seleccione **Transformar datos** en la barra de acciones de Power BI Desktop.
3. Seleccione la consulta que acaba de agregar, por ejemplo **Facturas venta**.
4. Aplique cualquier filtrado necesario en los registros para reducir la cantidad de registros cargados en su informe.
5. Desplácese hacia la derecha hasta encontrar una columna con el mismo nombre que las líneas, por ejemplo **SalesInvoiceLines**.
6. Seleccione el botón expandir en el encabezado de la columna, junto al nombre de la columna.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Muestra la columna SalesInvoiceLines en Power BI Desktop .":::
<!-- 11 --> 
### ¿Es posible elegir el entorno de Business Central obtener datos para Power BI, por ejemplo, como una espacio aislado o un entorno de producción? 

Sí. Se puede elegir fácilmente. Cuando se conecta a Business Central mediante el conector, debe elegir el entorno y el nombre de la empresa.

<!-- 6 --> 
### ¿Puedo combinar datos de varios entornos de producción del mismo inquilino?

Sí. En Power BI, simplemente vuelva a ejecutar la operación de obtención de datos y elija el entorno que desee.

<!-- 25 -->
### ¿Qué páginas de Business Central tienen la parte del informe de Power BI?  

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
### ¿Hay alguna forma de filtrar un conjunto de datos de Business Central *antes de* meterlo en Power BI, en lugar de aplicar filtros después?

Para filtrar conjuntos de datos más grandes, la forma más sencilla es establecer un filtro en su informe de Power BI, editando directamente la fórmula de Power Query. La mayoría de los filtros que establezca de esta manera se pasarán a Business Central mediante el plegado de consultas. Vea [Actualización incremental para conjuntos de datos](/power-bi/admin/service-premium-incremental-refresh).

Actualmente, no hay forma de configurar un filtro para los datos del servicio web desde Business Central. Si su aplicación necesita establecer un filtro desde Business Central, tendrá que crear una aplicación de Business Central personalizada para este propósito.

<!-- 10 -->
### Desde Power BI, además de utilizar una consulta, ¿hay otra forma de obtener datos de las tablas de Business Central que no tienen una página asociada? Por ejemplo, como la tabla *Asignación de valores de atributos de artículos*.

Nº No en este momento.

<!-- 12 --> 
### ¿Las consultas publicadas son más rápidas de usar que las páginas publicadas?

Cuando se trata de servicios web, las consultas publicadas suelen ser más rápidas que las páginas publicadas equivalentes. La razón es que las consultas están optimizadas para leer datos y no contienen desencadenadores costosos como OnAfterGetRecord.

Los servicios web se basan en páginas o consultas creadas para el acceso desde la Web y, por lo general, no están optimizadas para el acceso desde servicios externos. Incluso aunque el conector de Business Central aún admite la obtención de datos de servicios web, le recomendamos que utilice páginas API en lugar de servicios web siempre que sea posible.

<!-- 13 --> 
### ¿Existe alguna forma de que un usuario final cree un servicio web con una columna que esté en una tabla de Business Central, pero no una página? ¿O el desarrollador tendrá que crear una consulta personalizada? 

Actualmente no hay forma de agregar un nuevo campo a un servicio web. Las páginas API ofrecen total flexibilidad en la estructura de la página, por lo que un desarrollador puede crear una nueva página API para cumplir con este requisito. 

<!-- 28 --> 
### ¿Puedo conectar Power BI a un servidor de base de datos de solo lectura de Business Central Online? 

Esta funcionalidad estará disponible próximamente. A partir de febrero de 2022, los nuevos informes que cree en función de los datos de Business Central Online intentarán conectarse automáticamente a una réplica de la base de datos de solo lectura. Esto hará que sus informes se actualicen más rápido y tendrá menos impacto en el rendimiento si utiliza Business Central mientras se actualiza un informe. Seguimos recomendando, siempre que sea posible, que programe sus informes para que se actualicen fuera del horario laboral habitual.

Si tiene informes antiguos basados en datos de Business Central, no se conectarán a la réplica de la base de datos de solo lectura.

### <a name="databasemods"></a>He probado la versión preliminar del nuevo conector para la actualización de febrero de 2022. Cuando me conecto a mi página personalizada de la API de Business Central, aparece el error "No se puede insertar un registro. La intención de conexión actual es de solo lectura". ¿Cómo puedo solucionarlo?

Con el nuevo conector, los nuevos informes que utilizan datos de Business Central se conectarán a una réplica de solo lectura de la base de datos de Business Central de forma predeterminada. Este cambio traerá una mejora en el rendimiento. Sin embargo, en casos excepcionales, podría causar el error. Este error generalmente ocurre porque su API personalizada está realizando modificaciones en los registros de Business Central mientras Power BI trata de obtener los datos. En particular, ocurre como parte de los desencadenadores AL: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord y OnAfterGetCurrRecord.

Para solucionar este problema obligando al conector Business Central a permitir este comportamiento, consulte [Crear informes de Power BI para mostrar datos de Business Central: solución de problemas](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="perms"></a>¿Cómo cambio o borro la cuenta de usuario que estoy usando actualmente para conectarme a Business Central desde Power BI Desktop?

En Power BI Desktop, realice uno de los siguientes pasos:

1. En el menú Archivo, seleccione **Opciones y configuraciones** > **Configuración de la fuente de datos**.
2. Seleccione **Dynamics Business Central** de la lista, luego seleccione **Borrar permisos** > **Eliminar**.

La próxima vez que se conecte a Business Central para obtener datos, se le pedirá que inicie sesión.

## [Rendimiento](#tab/performance)

<!-- 17 -->

### ¿Es más rápido obtener datos usando páginas de API que usando servicios web?

Sí. Nuestras pruebas indican que las páginas de API tienen hasta un 25% más de rendimiento que los servicios web.

<!-- 18 -->
### ¿Hay planes para tener un espejo en la instancia de Azure SQL Database, al que pueda conectarme directamente?

Nº No en este momento. Solo puede comunicarse con Business Central a través de las API.

<!-- 19 -->
### La carga de datos desde los servicios web de Business Central parece lenta. ¿Hay alguna forma de obtener datos directamente de la tabla de la base de datos SQL?

Nº El acceso directo a la base de datos no es posible, pero cambiar a las páginas de API (cuando el nuevo conector esté disponible) será de gran ayuda.

## [Avanzado](#tab/advanced)
<!-- 1 -->

### ¿Hay planes para que el conector de Power BI admita las funciones de actualización incremental en el servicio de Power BI?

Sí. Está en nuestra hoja de ruta.

<!-- 2 -->
### Si una solución local de Business Central no tiene acceso a Internet, ¿puedo seguir usando Power BI?
<!-- todo: please explain this one-->

Sí. En este caso, use Power BI Desktop localmente y conéctese a Business Central local. Una vez conectado, puede crear y ver informes, pero no puede publicarlos en el servicio de Power BI. 
<!-- 20 -->
### ¿Existe algún plan para hacer posible la replicación de las bases de datos de Business Central Online para que sean accesibles para consultas SQL de solo lectura? Esta capacidad admitiría la actualización incremental y sería mucho más rápida que las API o los servicios web.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Sí. Tenemos esta característica en nuestra hoja de ruta a largo plazo. 

<!-- 21 -->
### Si uso Azure Data Factory para obtener datos de Business Central y utilizarlos en Power BI, ¿ayudará eso a aumentar el rendimiento? 

Sí. Este escenario avanzado ayudará a Business Central a mantener el rendimiento, porque el acceso a los datos se realizaría a través de Azure Data Factory.

<!-- 22 -->
### ¿Hay planes para admitir las canalizaciones de implementación de Power BI o una forma de crear canalizaciones de implementación para informes PBI, similar a las extensiones? ¿O tal vez incluso una API sencilla en Business Admin Center? 

Estamos investigando esta función. Power BI ofrece API enriquecidas para controlar la implementación de informes. Para más información, vea [Introducción a las canalizaciones de implementación](/power-bi/create-reports/deployment-pipelines-overview).

### Cuando obtengo datos de Business Central para usarlos en mis informes de Power BI, veo algunos valores como "_x0020_". ¿Qué son estos valores?

Algunas páginas de API, incluida la mayoría de las páginas de API v2.0, tienen campos basados en [Objetos de enumeración AL](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Los campos basados en objetos de enumeración AL deben tener nombres que sean coherentes y siempre iguales, para que los filtros del informe siempre funcionen, sin importar el idioma o el sistema operativo que esté utilizando. Por este motivo, los campos basados en enumeraciones de AL no se traducen y se codifican para evitar cualquier carácter especial, incluido el espacio. En particular, siempre que haya una opción vacía en el objeto AL Enum, se codifica como "_x0020_". Siempre puede aplicar una transformación a sus datos en Power BI si desea mostrar algún valor diferente para estos campos, por ejemplo, "Vacío".

## Consulte también .

[Licencias de Power BI](admin-powerbi-setup.md#license)  
[Introducción a Business Central y Power BI](admin-powerbi.md)  
[Información general sobre integración de Power BI](admin-powerbi-overview.md)  
[Habilitación de Power BI en Business Central](admin-powerbi-setup.md)  
[Trabajar con informes de Power BI en Business Central](across-working-with-powerbi.md)  
[Trabajar con datos de Business Central en Power BI](across-working-with-business-central-in-powerbi.md)  
[Creación de informes de Power BI para mostrar datos de Business Central](across-how-use-financials-data-source-powerbi.md)  
[Documentación de Power BI](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
