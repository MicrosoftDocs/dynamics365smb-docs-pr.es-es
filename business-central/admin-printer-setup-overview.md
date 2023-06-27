---
title: Descripción general de la configuración y administración de la impresora
description: Conozca cuáles son las diferentes oportunidades de impresión en Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 02/10/2023
ms.custom: bap-template
---

# <a name="printer-setup-and-management-overview"></a><a name="printer-setup-and-management-overview"></a>Descripción general de la configuración y administración de la impresora

La impresión de documentos e informes desde [!INCLUDE[prod_short](includes/prod_short.md)] es una tarea importante para los usuarios empresariales. Usted normalmente querrá enviar trabajos de impresión directamente a una de las impresoras de su organización, independientemente del cliente o la aplicación de [!INCLUDE[prod_short](includes/prod_short.md)] que use. Puesto que [!INCLUDE[prod_short](includes/prod_short.md)] Online es un servicio en la nube, no puede llegar directamente a las impresoras locales conectadas a los dispositivos de los usuarios, pero puede conectarlo a impresoras habilitadas para la nube.

## <a name="what-are-your-printer-possibilities-in-business-central"></a><a name="what-are-your-printer-possibilities-in-business-central"></a>¿Cuáles son sus posibilidades de impresión en Business Central?

Para satisfacer sus necesidades de impresión, [!INCLUDE[prod_short](includes/prod_short.md)] ofrece las siguientes características:

|Característica|Descripción|Cliente web| Aplicación móvil|Aplicación para Teams|
|-------|-----------|----------|-----------|--------------|
|Impresión universal|Impresión universal es una solución de gestión de impresoras disponible como servicio en la nube de Microsoft. Con esta característica, puede configurar sus impresoras en Impresión universal y, a continuación, registrarlas para su uso en [!INCLUDE[prod_short](includes/prod_short.md)]. Esta característica requiere una suscripción a Impresión universal y la extensión **Integración de Impresión universal**.|![trabaja en línea.](media/check.png)|![trabaja en línea.](media/check.png)|![trabaja en línea](media/check.png)|
|Impresión por correo electrónico|Esta característica le permite configurar impresoras habilitadas para correo electrónico. [!INCLUDE[prod_short](includes/prod_short.md)] envía los trabajos de impresión a una impresora usando la dirección de correo electrónico de la impresora. Esta característica requiere impresoras habilitadas para correo electrónico y la extensión **Enviar a impresora de correo electrónico**.|![trabaja en línea.](media/check.png)|![trabaja en línea](media/check.png)|![trabaja en línea](media/check.png)|
|Impresión en el navegador|Los trabajos de impresión son gestionados por la funcionalidad de impresión del navegador del usuario. Si no se instala y configura una impresora en la nube o si falla una impresora instalada, la impresión tendrá las opciones de impresión predeterminadas para el navegador. El campo **Impresora** en la página de solicitud de informe mostrará *(Manejado por el navegador)*.|![trabaja en línea](media/check.png)|||

La mayor parte del trabajo para configurar impresoras se puede realizar desde la página **Administración de impresoras** en [!INCLUDE[prod_short](includes/prod_short.md)]. Aunque con las impresoras Universal Print, es posible que también deba trabajar en el centro de administración de Microsoft 365 o en Azure Portal.

> [!IMPORTANT]
> Para Business Central en las instalaciones, Universal Print y Email Print requieren que se use la autenticación de Azure Active Directory (AD) o NavUserPassword.

## <a name="custom-printer-extensions"></a><a name="custom-printer-extensions"></a>Extensiones de impresora personalizadas

[!INCLUDE[prod_short](includes/prod_short.md)] admite otras extensiones de impresora personalizadas que agregan aún más características de impresión. Por lo tanto, si instala extensiones de impresora personalizadas, su aplicación puede incluir características de impresión que no se describen en este artículo.

Si es un desarrollador de AL y desea obtener información sobre cómo crear extensiones de impresora, vaya a [Desarrollo de extensiones de impresora en Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## <a name="next-steps"></a><a name="next-steps"></a>Pasos siguientes

- [Configurar impresoras de Impresión universal](admin-printer-setup-universal-print.md)  
- [Configurar impresoras por correo electrónico](admin-printer-setup-email.md)  
- [Configurar impresoras predeterminadas](ui-specify-printer-selection-reports.md)
