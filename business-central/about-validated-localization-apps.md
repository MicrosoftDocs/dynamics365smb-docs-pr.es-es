---
title: Desarrollo de aplicaciones de localización validadas
description: Cumpla con los requisitos reglamentarios en Dynamics 365 Business Central como aplicación de localización validada.
author: altotovi
ms.date: 06/04/2024
ms.reviewer: bholtorf
ms.topic: conceptual
ms.author: altotovi
---

# <a name="development-of-validated-localization-apps"></a>Desarrollo de aplicaciones de localización validadas

Este artículo describe los requisitos y pautas para desarrollar una aplicación de localización validada para [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-a-validated-localization-app"></a>¿Qué es una aplicación de localización validada?

[!INCLUDE[prod_short](includes/prod_short.md)] está disponible [a nivel mundial en más de 170 mercados](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json). En un conjunto de mercados, Microsoft trabaja con asociados ISV para localizar [!INCLUDE[prod_short](includes/prod_short.md)] a través de aplicaciones de localización disponibles en [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Para esas regiones, las localizaciones pueden estar disponibles a través del programa de aplicación de localización preferido. El programa de aplicaciones de localización preferidas reconoce aquellas aplicaciones que se crean de acuerdo con las pautas de calidad específicas de Microsoft. Los asociados ISV que cumplan con los requisitos y pautas del programa pueden beneficiarse técnica y comercialmente para atender a sus revendedores y clientes.  

En las siguientes secciones, puede encontrar requisitos y pautas. Puede comunicarse con el equipo del programa si desea participar en este programa y cumplir con los requisitos a continuación comunicándose con nosotros a través del [equipo de localización de Microsoft](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> La iniciativa [!INCLUDE[prod_short](includes/prod_short.md)] Aplicaciones de localización validadas se está implementando actualmente como programa piloto. Los requisitos y beneficios a continuación pueden cambiar según los comentarios de los asociados y clientes.  

Las aplicaciones del programa piloto de localización validado contienen un conjunto de funcionalidades que abordan los requisitos reglamentarios locales que se encuentran dentro de una de las categorías de la siguiente lista.  

- **Requisitos reglamentarios** : funcionalidad local que ayuda a las empresas a cumplir con sus requisitos legales, como informes de impuestos, formatos de facturación electrónica locales, GAAP locales y otros requisitos reglamentarios.
- **Requisito de estándares nacionales**: funcionalidad local que aborda los estándares locales, como formatos de direcciones, formatos bancarios nacionales o interpretaciones locales de estándares globales.
- **Idioma local**: idioma local en la aplicación de localización, pero también para una aplicación base si este idioma no está actualmente en la lista de [idiomas admitidos](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

> [!NOTE]
> Las necesidades del mercado local o los requisitos de la industria no deben incluirse en las aplicaciones de localización preferidas. Si las aplicaciones contienen estas funcionalidades, no se pueden aprobar como aplicaciones de localización validadas.

> [!NOTE]
> La funcionalidad local es beneficiosa para los procesos comerciales de productividad en un país o región y, por lo tanto, agrega valor al negocio, pero no es necesaria desde una perspectiva regulatoria, como formatos bancarios y de pago específicos, informes de gastos, funciones de recursos humanos, nómina y similares, más pequeños o más grandes. y las funciones interesantes deberían aislarse en otras aplicaciones. Si las aplicaciones contienen estas funcionalidades, no se aprueban como aplicaciones de localización validadas.   

## <a name="validated-localization-app-business-requirements"></a>Requisitos comerciales de la aplicación de localización validada

- El proveedor de la aplicación de localización validada cumple con todos los requisitos para ser un proveedor indirecto de CSP.  
- El proveedor de la aplicación de localización validada trae al mercado un mínimo de ofertas en cinco países/regiones, que agrupan Dynamics 365 Business Central con una aplicación de localización validada. 
- El proveedor de la aplicación de localización validada tiene un mínimo de 10 clientes en línea de [!INCLUDE[prod_short](includes/prod_short.md)] con entornos de producción, que utilizan activamente la aplicación de localización validada. 
- El proveedor de la aplicación de localización validada presenta un plan de negocios anualmente al equipo v del programa. Esto incluye actividades planificadas de marketing y preparación para promover la oferta empaquetada con los revendedores indirectos de CSP en los países/regiones aplicables. El plan se puede presentar al inicio de cada trimestre al [Equipo de localización de Microsoft](mailto:d365bcloc@microsoft.com).  
- Las aplicaciones de localización validadas están disponibles para todos los clientes y asociados que quieran beneficiarse de ellas.     
- El proveedor de la aplicación de localización validada participa en flujos de trabajo recurrentes con Microsoft.

## <a name="validated-localization-app-functional-and-technical-requirements"></a>Requisitos funcionales y técnicos de la aplicación de localización validada

### <a name="functionality-requirements"></a>Requisitos de funcionalidad

Además de cumplir los requisitos técnicos para la aplicación de localización preferida, el alcance mínimo viable del producto para la aplicación de localización preferida es:  

- Características normativas regionales   
  - Requisitos legales.   
  - Funciones oficialmente obligatorias. 
  - Características solo horizontales (no específicas de la industria).  
  - Aplicable en la mayoría de negocios.  
  - Dentro del siguiente Blueprint:   
    - Áreas de los cambios legislativos más frecuentes. 
    - Ya rastreado como localización en localizaciones de Microsoft. 
    - Referencias de funciones: rara vez nuevas.  
    - Sin formatos específicos de proveedor/banco, nómina o similares. 
    - No hay características globales si no están creadas por Microsoft. 
- Traducciones: 
  - Traducción de una aplicación de localización a idiomas locales. 
  - Traducción de una aplicación base a idiomas locales, si el idioma aún no se [admite](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Traducción de la documentación de una aplicación de localización a idiomas locales. 
- Aunque ambas son parte de la localización, se recomienda que las características estándar nacionales (parte local) se creen como aplicaciones separadas de las funciones regulatorias locales. 
- Datos de demostración en el idioma local aplicables al mercado específico.   
- Todas las características deben diseñarse para mantener una interfaz de usuario simplificada; tenga en cuenta que están destinadas principalmente al mercado de las PYMES.  
- Evite crear nuevas características si ya existen funcionalidades iguales o similares en la aplicación base, como facturación electrónica, exportaciones de auditoría, funciones de IVA, intercambio de datos y otras donde la mayoría de las funciones son comunes a todos los países/regiones pero existen algunas reglas o formatos comerciales que son extensiones de marcos o formatos globales. En lugar de crear nuevas funciones, amplíe las existentes.  
- Prepare guías de configuración (asistentes) para áreas que son complejas de configurar para ayudar a los usuarios a habilitar, descubrir y tener una buena primera experiencia al usar su aplicación de localización.  
- Los socios deben proporcionar documentación funcional para todos los aspectos de su localización.  

### <a name="technical-requirements"></a>Requisitos técnicos

A continuación encontrará una lista de los requisitos que debe cumplir antes de enviar la aplicación de localización validada como extensión para su validación. Esta lista no cambia la [lista de validación técnica](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) y solo amplía los requisitos a partir de allí.  

- Los proveedores de la aplicación de localización validada deben crear la aplicación de localización validada basada en la aplicación base W1.  
- Los proveedores de aplicaciones de localización validada deben seguir las políticas de soporte y ciclo de vida de Microsoft.   
- La automatización de pruebas obligatoria debe cubrir como mínimo el 80 % del código y todos los procesos empresariales que cambien con la aplicación de localización validada deben estar cubiertos por la automatización de pruebas.  
- Los proveedores de la aplicación de localización validada deben actualizar y/o probar su aplicación de localización validada antes del lanzamiento oficial de la nueva versión (como mínimo con el RC antes de la nueva versión) para confirmar que no hay problemas. 
- Todos los objetos en el código de la aplicación de localización validada deben estar en inglés.   
- Los proveedores de aplicaciones de localización validada deben seguir la política de Microsoft para objetos obsoletos y cambios importantes y mejores prácticas para la obsolescencia del Código AL.  
- Los proveedores de aplicaciones de localización validada deben agregar nuevos eventos si así lo requiere el mercado (otros socios de implementación o clientes) si tiene sentido comercial razonable, siguiendo las políticas y prácticas de Microsoft. De lo contrario, los proveedores de aplicaciones de localización validadas deben responder a dichas consultas con una justificación adecuada de por qué no tiene sentido comercial razonable agregarlas. 
- Los proveedores de aplicaciones de localización validada deben proporcionar escenarios de prueba escritos en inglés y permitir que Microsoft realice pruebas manuales si así lo requiere Microsoft.  
- Si una aplicación de localización validada está ampliando el modelo de datos de [!INCLUDE[prod_short](includes/prod_short.md)] con nuevas tablas y/o campos, el proveedor de la aplicación de localización validada debe configurar la propiedad **DataClassification** correctamente.

> [!NOTE]  
> También puede crear una integración si le resulta beneficioso tener alguna funcionalidad ubicada fuera del entorno de [!INCLUDE[prod_short](includes/prod_short.md)] y en su lugar conectarse a [!INCLUDE[prod_short](includes/prod_short.md)] utilizando, por ejemplo, API o servicios web.

## <a name="see-also"></a>Consulte también

[Validación técnica](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Desarrollo de una solución de localización estándar](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Disponibilidad nacional/regional e idiomas admitidos](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[¿Qué es la funcionalidad local en Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]?](about-localization.md)  
[Disponibilidad internacional de Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Información general sobre cumplimiento](compliance/compliance-overview.md)  
[Disponibilidad geográfica para Dynamics 365](https://dynamics.microsoft.com/en-us/availability-reports/georeport/)  
