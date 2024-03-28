---
title: Business Central para organizaciones internacionales y de sitios múltiples | Microsoft Docs
description: Business Central proporciona capacidades que admiten un modelo de negocio de de concentrador y radios.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Business Central para organizaciones internacionales y de sitios múltiples
Las organizaciones que tienen varios sitios a menudo utilizan un modelo de negocio de centro y radios en el que una empresa matriz, o la sede central, gestiona las operaciones generales del negocio, mientras que cada sitio funciona como una entidad única e independiente. Los sitios a menudo están distribuidos geográficamente y tienen diferentes necesidades para compartir información con la empresa matriz. Además, los sitios no suelen necesitar el mismo nivel de complejidad y, a menudo, carecen de los recursos para mantener un sistema grande.

[!INCLUDE[prod_short](includes/prod_short.md)] ofrece a las pequeñas y medianas empresas una solución de gestión empresarial que es fácil de usar y mantener con un bajo costo de propiedad.

Este artículo presenta algunas de las formas en que [!INCLUDE[prod_short](includes/prod_short.md)] soporta un modelo de negocio de concentrador y radios.

## Integración de la empresa matriz y los sitios

[!INCLUDE[prod_short](includes/prod_short.md)] puede integrarse con el sistema de contabilidad de la empresa matriz mientras satisface las diferentes necesidades de los diferentes sitios, independientemente del tamaño, la ubicación o el tipo de negocio.

El siguiente diagrama es un ejemplo de diferentes sitios integrados con una empresa matriz.

![Descripción del diagrama generada automáticamente.](media/multisite-headquarter-sites.png)

## Satisfacer las necesidades de los sitios nacionales e internacionales

Las necesidades comerciales de los sitios a menudo difieren según el sector, los métodos comerciales o su relación con la empresa matriz. [!INCLUDE[prod_short](includes/prod_short.md)] se puede adaptar y ampliar fácilmente para diversos tipos de empresas y lugares. Microsoft AppSource ofrece una gran cantidad de aplicaciones de Microsoft y nuestros socios, y los socios pueden implementar rápidamente [!INCLUDE[prod_short](includes/prod_short.md)] con una interrupción mínima de las operaciones diarias.

Para organizaciones multinacionales, [!INCLUDE[prod_short](includes/prod_short.md)] soporta los requisitos legales locales y las prácticas comerciales.

* Para las versiones en línea, hay más de [40 versiones de países y regiones localizadas](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) que puede instalar como extensiones desde Microsoft AppSource.  
* Para versiones locales, están disponibles [versiones de país o región](/azure/architecture/solution-ideas/articles/business-central) como versiones localizadas por Microsoft o como localizaciones complementarias llevadas por socios.

Una red de más de 4 000 socios de Microsoft en todo el mundo proporciona experiencia local.

| **Requisito de negocio** | **Cómo lo soporta Business Central** | **Más información** |
|-------------------------|-------------------------|-------------------------|
| Adapte el sistema a la empresa. | Disfrute de un sistema que se diseñó desde el principio para empresas medianas. | [Información general](https://dynamics.microsoft.com/business-central/overview/) |
| Abordar las prácticas regulatorias y locales. | Cumpla con los requisitos legales y las prácticas comerciales locales. | [Funcionalidad local](about-localization.md) |
| Acceda a múltiples empresas desde una sola página. | Obtenga acceso rápido a cualquier empresa de Business Central de su organización. | [Hub de empresas](ui-extensions-company-hub.md) |
| Maneje múltiples idiomas y divisas. | La compatibilidad con varios idiomas y monedas ayuda a satisfacer las necesidades locales. | [Capacidades multilingües](about-locale-language.md)<br></br>[Capacidades multidivisa](finance-how-setup-additional-currencies.md) |


## Consolidar datos financieros

Una faceta fundamental del modelo de negocio de concentrador y radios es la capacidad de la empresa matriz y los sitios para intercambiar datos financieros, incluso cuando la empresa matriz y los sitios utilizan diferentes sistemas, estructuras contables, idiomas y divisas.

| **Requisito de negocio** | **Cómo lo soporta Business Central** | **Más información** |
|-------------------------|-------------------------|-------------------------|
| Consolidar datos financieros de sitios. | Consolide los estados financieros de los sitios, independientemente de si ejecutan Business Central u otra aplicación, en una única entidad comercial (empresa). | [Consolidar los datos financieros de varias empresas](finance-consolidated-company-reporting.md) |
| Integre estructuras contables. | Transfiera datos de consolidación de diferentes estructuras contables a la suya. Formato de archivo incorporado para F&O (disponible con el segundo lanzamiento de 2020) | [Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)<br></br>[Preparar las cuentas de contabilidad para la consolidación](finance-consolidated-company-reporting-setup.md#glacc) |
| Realice transacciones en varias divisas. | Ayude a garantizar que los estados financieros en diferentes divisas sean precisos y utilicen tipos de cambio correctos. | [Actualizar tipos de cambio de divisa](finance-how-update-currencies.md) |

## Comparta Business Insight con el análisis integrado

Alinee la organización con sus objetivos comerciales proporcionando un conocimiento común de la realidad actual. La analítica integrada puede ayudar a las personas a basar sus decisiones en el mismo conjunto de hechos.

| **Requisito de negocio** | **Cómo lo soporta Business Central** | **Más información** |
|-------------------------|-------------------------|-------------------------|
| Comparta conocimientos con sitios sin un amplio soporte de TI. | Cree KPI y paneles de inteligencia empresarial en Power BI basados en sus datos. | [Trabajar con datos de Business Central en Power BI](across-working-with-business-central-in-powerbi.md) |
| Desarrolle informes financieros personalizados. | Genere informes financieros basados en parámetros. | [Inteligencia empresarial](bi.md) |
| Póngase en línea con los hechos. | Genere, vea y comparta informes con partes interesadas internas y externas. | [Informes financieros](finance-reports.md) |
| Analizar datos en Excel. | Busque hechos, resuelva problemas y realice análisis ad hoc en Microsoft Excel. | [Analizar estados financieros en Excel](finance-analyze-excel.md) |


## Intercambio de datos mediante API y XMLports

Las API y XMLports simplifican el proceso de conectar instancias de [!INCLUDE[prod_short](includes/prod_short.md)], incluidos los que se han personalizado para cada sitio.

| **Requisito de negocio** | **Cómo lo soporta Business Central** | **Más información** |
|-------------------------|-------------------------|-------------------------|
| Conecte versiones personalizadas entre los sitios y la empresa matriz. | Las páginas de API pueden exponer cualquier representación de una entidad, incluidas sus personalizaciones. | [Habilitación de las API para Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Versiones y seguridad. | Las API utilizan ODataV4, que proporciona control de versiones, webhooks y seguimiento de cambios. | [Seguridad y protección](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Registrar e importar documentos XML. | Las unidades de código pueden exponerse como acciones independientes para admitir la publicación y la ingestión de documentos XML. Para procesar documentos XML, se pueden aplicar XMLports. Las acciones independientes también pueden generar un documento XML o JSON. | [Objetos XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Facilite el mantenimiento mediante el intercambio electrónico de datos. | Se puede agregar una solución de intercambio electrónico de datos para que sirva como una capa de integración entre la empresa matriz y los sitios. | [Marco de intercambio de datos](across-about-the-data-exchange-framework.md) |
| Intercambie datos entre diferentes sistemas. | Use XMLports para crear documentos XML, que luego se pueden intercambiar entre una empresa matriz que usa un sistema y sitios que usan Business Central. | [Información general de XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Organice intercambios de datos complejos. | Utilice una combinación de XMLports con Business Central y Microsoft BizTalk Server para satisfacer las necesidades únicas de sus sitios.</br>Para necesidades complejas, utilice una solución de intercambio electrónico de datos basada en BizTalk Server y Commerce Gateway en Business Central, con XMLports. | [Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md) |
| Conectarse a soluciones y servicios de terceros. | Las API establecen una conexión punto a punto entre Business Central y soluciones y servicios de terceros. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## Promover una cadena de suministro interempresas eficiente

Los sitios a menudo necesitan acceso a la cadena de suministro y la capacidad de administrar ciertos aspectos de la misma. Por ejemplo, los sitios pueden usar el mismo proveedor, pero administrar sus activos y ubicaciones físicas por separado.

| **Requisito de negocio** | **Cómo lo soporta Business Central** | **Más información** |
|-------------------------|-------------------------|-------------------------|
| Trate las transacciones entre divisiones como transacciones normales de compra y venta. | Utilice los registros entre empresas para crear documentos de ventas y compras y entradas de movimientos de contabilidad para flujos de trabajo completos y para más de una empresa a la vez, para eliminar la entrada de datos duplicada. | [Gestión de transacciones entre empresas](intercompany-manage.md) |
| Utilice procesos sin papel. | Evite el costo de enviar, recibir e imprimir documentos. | [Documentos entrantes](across-income-documents.md)<br><br> [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md) |

## Responda rápidamente a las nuevas condiciones comerciales

La empresa matriz debe poder reaccionar rápidamente a los cambios comerciales en cada sitio. En combinación con Power Automate, [!INCLUDE[prod_short](includes/prod_short.md)], puede servir como un mecanismo de alerta temprana.

![Captura de pantalla de una publicación en las redes sociales de descripción generada automáticamente.](media/multisite-apps.png)

| **Requisito de negocio** | **Cómo lo soporta Business Central** | **Más información** |
|-------------------------|-------------------------|-------------------------|
| Genere automáticamente alertas por correo electrónico. | Configure alertas en Power Automate que generarán correos electrónicos para informarle sobre las condiciones comerciales críticas en los sitios o socios de la cadena de suministro. | [Business Central y Power BI](admin-powerbi.md) |
| Utilice alertas estándar o personalizadas. | Utilice 12 plantillas diferentes incluidas para Business Central o configure sus propias alertas para adaptarse a su negocio. | [Usar Business Central en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md) |

## Consulte también
[Administración de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
