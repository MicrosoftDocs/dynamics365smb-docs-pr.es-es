---
title: Preguntas frecuentes sobre la asistencia al análisis (versión preliminar)
description: 'Estas preguntas frecuentes brindan información sobre la tecnología de inteligencia artificial utilizada para analizar datos en páginas de Business Central. Incluye las consideraciones clave y detalles sobre cómo se usa la IA, cómo se probó y evaluó, y cualquier limitación específica.'
ms.date: 06/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-analysis-assist-preview"></a>Preguntas frecuentes sobre la asistencia al análisis (versión preliminar)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Estas preguntas frecuentes (P+F) describen el impacto de la característica de asistencia de análisis en [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-analysis-assist"></a>¿Qué es la asistencia de análisis?

La asistencia de análisis es un copiloto que proporciona asistencia para trabajar con el [modo de análisis de datos](analysis-mode.md) en Business Central. El modo de análisis de datos le permite organizar, agregar y resumir datos en páginas y consultas para hacerlos más adecuados para analizar y extraer información significativa. Con la asistencia de análisis, puede crear automáticamente la vista de los datos que desea analizar expresando sus necesidades en un lenguaje simple y natural, como "mostrar proveedores por ubicación ordenados por número de compras". La asistencia de análisis facilita el trabajo con datos sin la necesidad de habilidades técnicas complejas.

## <a name="what-are-capabilities-of-analysis-assist"></a>¿Cuáles son las capacidades de asistencia de análisis?

La asistencia de análisis se basa en las herramientas de desarrollo de Copilot en Business Central. Utiliza Azure OpenAI Service para convertir instrucciones no estructuradas en un diseño estructurado para mostrar datos en el modo de análisis, sin crear, modificar ni actualizar los datos comerciales del cliente.

## <a name="what-is-the-intended-use-of-analysis-assist"></a>¿Cuál es el uso previsto de la asistencia de análisis?

El asistente de análisis ayuda a crear fichas de análisis en el modo de análisis de datos para presentar los datos de forma que resulte más fácil extraer conclusiones. Sin embargo, es importante tener en cuenta que la asistencia de análisis no proporciona información ni conclusiones directas sobre los datos. Es una herramienta que ayuda a los usuarios a organizar y ver sus datos. Depende del usuario extraer información procesable, descubrir tendencias y tomar decisiones informadas para impulsar el valor comercial.

## <a name="how-was-analysis-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>¿Cómo se evaluó la asistencia de análisis? ¿Qué métricas se utilizan para medir el rendimiento?

- La característica se sometió a extensas pruebas basadas en los datos de demostración de [!INCLUDE[prod_short](includes/prod_short.md)] y otros catálogos de productos ficticios. Copilot recibió numerosas indicaciones en las configuraciones regionales en inglés admitidas. Las indicaciones cubrieron una amplia gama de instrucciones de análisis de datos y estilos de expresión de intenciones. Los resultados se evaluaron en función de la precisión, relevancia y seguridad.

- La característica está construida de acuerdo con el Estándar de IA Responsable de Microsoft. [Obtenga más información sobre la IA responsable de Microsoft.](https://aka.ms/RAI)

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>¿Cómo monitorea Microsoft la calidad del contenido generado?

Microsoft cuenta con varios sistemas para garantizar que el contenido generado por Copilot sea de la más alta calidad, detectar abusos y garantizar la seguridad de nuestros clientes y sus datos.

Los usuarios tienen la oportunidad de proporcionar comentarios sobre cada respuesta de Copilot e informar sobre contenido inexacto o inadecuado para ayudar a Microsoft a mejorar esta característica.

- Si encuentra contenido generado inapropiado, infórmelo a Microsoft mediante este formulario de comentarios: [Notificar abuso](https://go.microsoft.com/fwlink/?linkid=2249810)

- Analizamos los comentarios de los usuarios sobre la función y los utilizamos para ayudarnos a mejorar las respuestas.

  Para proporcionar comentarios, utilice el ícono Me gusta (pulgar hacia arriba) o No me gusta (pulgar abajo) en el panel **Copilot** en [!INCLUDE[prod_short](includes/prod_short.md)].

- Microsoft podría deshabilitar las funciones controladas por Copilot para clientes seleccionados si se detecta un abuso de la funcionalidad.

## <a name="what-are-the-limitations-of-analysis-assist-how-can-users-minimize-the-impact-of-the-analysis-assist-limitations-when-using-the-system"></a>¿Cuáles son las limitaciones de la asistencia de análisis? ¿Cómo pueden los usuarios minimizar el impacto de las limitaciones de asistencia de análisis al utilizar el sistema?

- Limitaciones generales de IA:

  Los sistemas de IA son herramientas valiosas, pero no deterministas. Es posible que el contenido que generan no sea exacto. Es importante utilizar su criterio para revisar y verificar las respuestas antes de tomar decisiones que podrían afectar a las partes interesadas, como clientes y socios.

- Idiomas disponibles

   [!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

   La calidad de las respuestas también puede ser inferior si la configuración de idioma para el usuario en Business Central difiere del idioma principal de los datos comerciales en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)].
  
- Limitación geográfica:
  
   La característica está disponible en todos los [países o regiones de Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) admitidos<!-- except for Canada-->. Sin embargo, la característica utiliza Microsoft Azure OpenAI Service, que actualmente está disponible para Business Central en algunas regiones geográficas. Si su entorno está ubicado en un país o región donde el servicio Azure OpenAI no está disponible, los administradores deben permitir que los datos se muevan entre geografías. [Obtenga más información sobre el movimiento de datos de Copilot entre geografías](/dynamics365/business-central/ai-copilot-data-movement).

- Ciertas limitaciones de la industria, el producto y el tema:

  Las organizaciones que operan en algunos ámbitos comerciales, como el médico, el farmacéutico, el jurídico y el de armas, pueden experimentar una menor calidad de servicio.

## <a name="what-data-does-analysis-collect-and-how-is-it-used"></a>¿Qué datos recopila el análisis y cómo se utilizan?

La capacidad de asistencia de análisis recopila los datos mínimos requeridos por Business Central para ofrecer el servicio. Microsoft no utiliza los datos de su empresa, incluido el texto que envía a Copilot, para entrenar los modelos fundamentales en beneficio de otros. Para obtener más información, consulte [Términos de Dynamics 365 para características impulsadas por Azure OpenAI](https://go.microsoft.com/fwlink/?linkid=2236010).

También recopila datos de los comentarios que los usuarios pueden proporcionar usando los iconos Me gusta (pulgar hacia arriba) o No me gusta (pulgar abajo) en la asistencia de análisis de **Copilot**. Los datos son anónimos e incluyen la elección de Me gusta o No me gusta, el motivo de la No me gusta, si se proporciona, y la característica Copilot a la que se aplica el comentario.

## <a name="see-also"></a>Consulte también

[Analizar datos con Copilot (versión preliminar)](analysis-assist.md)
