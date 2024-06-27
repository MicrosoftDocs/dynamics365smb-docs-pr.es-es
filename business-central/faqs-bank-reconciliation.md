---
title: Preguntas frecuentes sobre la asistencia para la conciliación de cuentas bancarias con Copilot (versión preliminar)
description: 'Estas preguntas frecuentes brindan información sobre la tecnología de inteligencia artificial utilizada para conciliar cuentas bancarias y extractos de Business Central. Incluye las consideraciones clave y detalles sobre cómo se usa la IA, cómo se probó y evaluó, y cualquier limitación específica.'
ms.date: 03/27/2024
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

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Preguntas frecuentes sobre la asistencia para la conciliación de cuentas bancarias con Copilot (versión preliminar)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Estas preguntas frecuentes (FAQ) describen el impacto en la IA de la asistencia de Microsoft Copilot con la conciliación de cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>¿Qué es la asistencia de conciliación bancaria?

La conciliación bancaria es una tarea contable común en la que las organizaciones revisan sus estados de cuenta bancaria para identificar las transacciones que deben registrarse en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, esta tarea se utilizaría para identificar comisiones bancarias periódicas o pequeños gastos de empleados.

La conciliación bancaria suele ser un proceso de varios pasos. Primero, los extractos bancarios se importan a [!INCLUDE[prod_short](includes/prod_short.md)]. A continuación, se cotejan las transacciones con las entradas de contabilidad general. Finalmente, se contabilizan nuevos asientos contables para reflejar cualquier transacción residual que sus libros contables no conocían previamente.

Copilot en [!INCLUDE[prod_short](includes/prod_short.md)] reduce el esfuerzo manual al hacer coincidir más transacciones y sugerir cuentas de contabilidad general (G/L) en las que puede publicar.

## <a name="what-are-the-capabilities-of-bank-reconciliation-assist"></a>¿Cuáles son las capacidades de asistencia para la conciliación bancaria?

Copilot proporciona asistencia impulsada por IA con dos tareas distintas:

- Cotejo mejorado de transacciones con asientos del libro mayor

    [!INCLUDE[prod_short](includes/prod_short.md)] ofrece reglas automatizadas que relacionan automáticamente muchas transacciones bancarias con asientos del libro mayor. Sin embargo, estas reglas son inflexibles y a menudo dan lugar a muchas transacciones sin emparejar, cada una de las cuales requiere una inspección y comparación manuales. Copilot utiliza tecnología de inteligencia artificial para inspeccionar esas transacciones sin coincidencia e identificar más coincidencias, según fechas, montos y descripciones. Por ejemplo, si un cliente pagó varias facturas como una suma global, Copilot concilia la línea única del extracto bancario con los múltiples asientos del libro mayor de facturas.

- Cuentas de L/M sugeridas

    Para las transacciones bancarias residuales que no pueden cotejarse con ningún asiento del libro mayor, Copilot usa la tecnología de IA para comparar la descripción de la transacción con los nombres de las cuentas del L/M, sugiriendo la cuenta del L/M más probable en la que contabilizar. Por ejemplo, si las transacciones no coincidentes tienen la narrativa *Parada de combustible 24*, Copilot podría sugerirle que las contabilice en la cuenta *Transporte*.

Copilot no se conecta a su banco para recuperar o enviar transacciones. Esta tarea permanece totalmente bajo su control. Es un requisito previo para utilizar la asistencia de Copilot, independientemente de si las transacciones se agregan a [!INCLUDE[prod_short](includes/prod_short.md)] mediante una conexión bancaria digital, se importan desde un archivo de extracto bancario o se introducen manualmente.

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>¿Cuál es el uso previsto de la asistencia de conciliación bancaria?

El asistente de conciliación de cuentas bancarias está diseñado para mejorar la exactitud de los libros de contabilidad ayudando a los clientes a identificar las nuevas transacciones que deben contabilizar en [!INCLUDE[prod_short](includes/prod_short.md)]. No está pensada para la detección de fraudes ni para identificar si los clientes pagaron a tiempo.

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>¿Cómo se evaluó la asistencia de conciliación bancaria? ¿Qué métricas se utilizan para medir el rendimiento?

La asistencia de conciliación de cuentas bancarias se probó utilizando combinaciones de datos de transacciones bancarias sintéticas y cuentas de mayor y asientos contables similares que cubren las variaciones típicas y los límites de datos para cada campo y en diferentes idiomas. Los datos de prueba representan tanto el uso típico como el uso por parte de malos actores. El rendimiento se midió en comparación con la conciliación manual de los mismos datos.

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-these-limitations-when-they-use-the-system"></a>¿Cuáles son las limitaciones de la asistencia de conciliación bancaria? ¿Cómo pueden los usuarios minimizar el impacto de estas limitaciones cuando utilizan el sistema?

La asistencia para la conciliación de cuentas bancarias funciona mejor cuando los nombres de cuentas del L/M, las descripciones de los asientos del libro mayor y las descripciones de las transacciones bancarias están todos en el mismo idioma. Los idiomas mixtos o el lenguaje mixto de las descripciones de transacciones a menudo resultan en menos coincidencias y sugerencias.

Las cuentas contables sugeridas funcionan mejor en uno de los idiomas admitidos (consulte la siguiente sección para obtener una lista de idiomas). Es posible que los usuarios experimenten menos coincidencias de transacciones y menos cuentas contables sugeridas en otros idiomas.

## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>¿En qué geografías e idiomas está disponible la asistencia de conciliación bancaria?

- Geografías disponibles

  La asistencia de conciliación de cuentas bancarias está disponible en todos los [países o regiones de Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) admitidos. Para que los entornos de clientes ubicados en países o regiones donde el servicio Azure OpenAI no está implementado, los administradores deben dar su consentimiento para permitir el movimiento de datos a través de las fronteras para que [!INCLUDE [prod_short](includes/prod_short.md)] se conecte al servicio Azure OpenAI y para que esta capacidad esté disponible. Obtenga más información sobre el [movimiento de datos de Copilot entre geografías](ai-copilot-data-movement.md).

- Idiomas disponibles

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Para obtener más información sobre el idioma, consulte la pregunta anterior sobre limitaciones.

## <a name="what-is-expected-of-system-users-when-they-operate-bank-account-reconciliation-assist"></a>¿Qué se espera de los usuarios del sistema cuando operan el asistente de conciliación de cuentas bancarias?

### <a name="during-bank-account-reconciliation"></a>Durante una conciliación de cuenta bancaria

Las coincidencias y sugerencias basadas en IA a veces pueden ser incorrectas o incompletas. Los usuarios del asistente de conciliación de cuentas bancarias deben revisar la exactitud de las coincidencias y sugerencias que proporciona Copilot antes de optar por conservarlas. Las coincidencias y sugerencias de Copilot no se guardan en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)] hasta que seleccione el botón **Mantenerlo** y cierre la ventana de Copilot. También puede editar y corregir cualquier coincidencia o sugerencia antes de optar por conservarla.

### <a name="after-bank-account-reconciliation-is-completed"></a>Después de completar la conciliación de cuenta bancaria

Se recomienda que los usuarios también verifiquen la precisión y corrijan cualquier discrepancia después de cerrar la ventana de Copilot. Este proceso debe incluir las siguientes actividades:

- Revise el informe de prueba de conciliación.
- Asegúrese de que su organización cuente con los procesos de revisión y auditoría adecuados.
- Vuelva a abrir cualquier conciliación publicada utilizando la función **Deshacer**.
- Corrija cualquier asiento erróneo en el libro mayor mediante la contabilización inversa de asientos.

## <a name="what-is-expected-of-administrators-and-system-users-when-they-operate-bank-account-reconciliation-assist"></a>¿Qué se espera de los administradores y usuarios del sistema cuando operan la asistencia de conciliación de cuentas bancarias?

Los usuarios del sistema, como contables, tesoreros u otras personas que se dediquen a la contabilidad empresarial, deben revisar siempre la exactitud de las coincidencias y sugerencias que Copilot proporciona antes de optar por mantenerlas. Tras la conciliación con Copilot, recomendamos que estos usuarios revisen el informe de prueba de la conciliación para verificar su exactitud e identificar cualquier discrepancia.

Los administradores deben asegurarse de que se haya concedido acceso a esta capacidad a los usuarios de contabilidad adecuados.

## <a name="is-copilot-the-only-means-of-completing-bank-account-reconciliation"></a>¿Es Copilot el único medio para completar la conciliación de cuentas bancarias?

N.º No, el uso de Copilot es opcional. [!INCLUDE[prod_short](includes/prod_short.md)] ofrece medios tradicionales, sin tecnología de inteligencia artificial, para importar extractos bancarios, ejecutar reglas de comparación predefinidas y aplicar coincidencias y contabilizar manualmente en cuentas contables apropiadas. Tanto el enfoque tradicional como Copilot se pueden utilizar simultáneamente en una organización.

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>¿Cómo doy comentarios sobre el contenido generado por IA?

Cada vez que Copilot le proporcione coincidencias o sugerencias, podrá enviar sus comentarios a Microsoft directamente desde la ventana de Copilot utilizando los controles de me gusta (pulgares arriba) y no me gusta (pulgares abajo). Sus comentarios permanecen anónimos y utilizamos estos datos para mejorar la calidad del servicio.

## <a name="see-also"></a>Consulte también

[Conciliar cuentas bancarias con Copilot (versión preliminar)](bank-reconciliation-with-copilot.md)
