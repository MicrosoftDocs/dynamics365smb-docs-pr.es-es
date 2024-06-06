---
title: Preguntas frecuentes sobre la asistencia para la conciliación de cuentas bancarias (vista previa) con Copilot
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

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Estas preguntas frecuentes (FAQ) describen el impacto en la IA de la asistencia de Copilot con la conciliación de cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>¿Qué es la asistencia de conciliación bancaria?

La conciliación bancaria es una tarea contable común en la que las organizaciones revisan sus estados de cuenta bancaria para identificar las transacciones que deben registrarse en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, esta tarea se utilizaría para identificar comisiones bancarias periódicas o pequeños gastos de empleados. Esta tarea suele ser un proceso de varios pasos, que comienza con la importación de extractos bancarios a [!INCLUDE[prod_short](includes/prod_short.md)], seguido de comparar transacciones con asientos contables y publicar nuevos asientos contables para reflejar cualquier transacción residual que sus libros contables no conocían anteriormente. Copilot en [!INCLUDE[prod_short](includes/prod_short.md)] reduce el esfuerzo manual al hacer coincidir más transacciones y sugerir cuentas del libro mayor en las que puede publicar. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>¿Cuáles son las capacidades de asistencia para la conciliación bancaria?

Copilot proporciona asistencia impulsada por IA con dos tareas distintas: 

- Cotejo mejorado de transacciones con asientos del libro mayor 

   [!INCLUDE[prod_short](includes/prod_short.md)] ofrece reglas automatizadas que relacionan automáticamente muchas transacciones bancarias con asientos del libro mayor. Sin embargo, estas reglas son inflexibles y a menudo dan como resultado muchas transacciones no coincidentes, cada una de las cuales requiere inspección y comparación manual. Copilot utiliza tecnología de inteligencia artificial para inspeccionar las transacciones restantes e identificar más coincidencias, según fechas, montos y descripciones. Por ejemplo, si un cliente pagó varias facturas como una suma global, Copilot concilia la línea única del extracto bancario con los múltiples asientos del libro mayor de facturas. 
 
- Cuentas contables sugeridas 

   Para las transacciones bancarias residuales que no podían cotejarse con ningún asiento del libro mayor, Copilot usa la tecnología de IA para comparar la descripción de la transacción con los nombres de las cuentas del L/M, sugiriendo la cuenta del L/M más probable en la que contabilizar. Por ejemplo, Copilot podría sugerir que la transacción con la narrativa "Parada de combustible 24" se publiquen en la cuenta "Transporte". 

Copilot no se conecta a su banco para recuperar o enviar transacciones. Esta tarea permanece totalmente bajo su control y es un requisito previo para comenzar a utilizar la asistencia de Copilot, ya sea que esas transacciones se agreguen a [!INCLUDE[prod_short](includes/prod_short.md)] mediante una conexión bancaria digital, importado desde un archivo de extracto bancario o ingresado manualmente. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>¿Cuál es el uso previsto de la asistencia de conciliación bancaria?

La asistencia de conciliación de cuentas bancarias está diseñada para ayudar a identificar nuevas transacciones que los clientes deben contabilizar en [!INCLUDE[prod_short](includes/prod_short.md)], para mejorar la precisión de sus libros de contabilidad. Esta actividad no está destinada a detectar fraudes ni a identificar si los clientes pagaron a tiempo.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>¿Cómo se evaluó la asistencia de conciliación bancaria? ¿Qué métricas se utilizan para medir el rendimiento?

Esta funcionalidad se probó utilizando combinaciones de datos de transacciones bancarias sintéticas y cuentas de mayor y asientos contables similares que cubren las variaciones típicas y los límites de datos para cada campo y en diferentes idiomas. Los datos de prueba representan tanto el uso típico como el uso por parte de malos actores. El rendimiento se midió en comparación con la conciliación manual de los mismos datos. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>¿Cuáles son las limitaciones de la asistencia de conciliación bancaria? ¿Cómo pueden los usuarios minimizar el impacto de las limitaciones de conciliación bancaria al utilizar el sistema?

La asistencia para la conciliación de cuentas bancarias funciona mejor cuando los nombres de cuentas del L/M, las descripciones de los asientos del libro mayor y las descripciones de las transacciones bancarias están todos en el mismo idioma. Los idiomas mixtos o el lenguaje mixto de las descripciones de transacciones a menudo resultan en menos coincidencias y sugerencias. 

Las cuentas contables sugeridas funcionan mejor en inglés. Si bien esta función se puede utilizar en cualquiera de los idiomas disponibles de [!INCLUDE[prod_short](includes/prod_short.md)], los usuarios pueden experimentar menos coincidencias de transacciones y menos cuentas contables sugeridas en otros idiomas. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>¿En qué geografías e idiomas está disponible la asistencia de conciliación bancaria?

Esta capacidad está disponible para cualquier entorno, localización de país/región y en cualquier idioma de usuario. Para entornos de clientes ubicados en países o regiones donde el servicio Azure OpenAI no está implementado, los administradores primero deben dar su consentimiento para permitir el movimiento de datos a través de las fronteras para que [!INCLUDE[prod_short](includes/prod_short.md)] se conecte al servicio Azure OpenAI y para que esta capacidad esté disponible. 

Para obtener más información sobre el idioma, consulte la pregunta anterior sobre limitaciones.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>¿Qué se espera de los usuarios finales cuando operan la asistencia de conciliación de cuentas bancarias?

### <a name="while-using-bank-account-reconciliation"></a>Al usar la conciliación de cuenta bancaria

Las coincidencias y sugerencias basadas en IA a veces pueden ser incorrectas o incompletas. Los usuarios de la asistencia de conciliación de cuentas bancarias deben revisar la exactitud de las coincidencias y sugerencias proporcionadas por Copilot antes de optar por conservarlas. Las coincidencias y sugerencias de Copilot no se guardan en la base de datos [!INCLUDE[prod_short](includes/prod_short.md)] hasta que elijas el botón Conservar y salgas de la ventana de Copilot. También puede editar y corregir cualquier coincidencia o sugerencia antes de optar por conservarla. 

### <a name="after-completing-bank-account-reconciliation"></a>Después de completar la conciliación de cuenta bancaria

Se recomienda que los usuarios también verifiquen la precisión y corrijan cualquier discrepancia después de salir de la ventana de Copilot, incluidas las siguientes actividades: 

- Revise el informe de prueba de conciliación. 
- Asegúrese de que su organización cuente con los procesos de revisión y auditoría adecuados. 
- Vuelva a abrir cualquier conciliación publicada utilizando la función Deshacer. 
- Corrija cualquier asiento erróneo en el libro mayor mediante la contabilización inversa de asientos. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>¿Qué se espera de los administradores y usuarios finales cuando operan la asistencia de conciliación de cuentas bancarias?

Los usuarios finales, como contadores, tesoreros u otras personas que trabajan en la contabilidad empresarial, siempre deben revisar la exactitud de las coincidencias y sugerencias proporcionadas por Copilot antes de optar por conservarlas. Después de conciliar con Copilot, recomendamos revisar el informe de prueba de conciliación para verificar la precisión e identificar cualquier discrepancia. 

Los administradores deben asegurarse de que se haya concedido acceso a esta capacidad a los usuarios de contabilidad adecuados. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>¿Es Copilot el único medio para completar la conciliación de cuentas bancarias?

No, el uso de Copilot es opcional. [!INCLUDE[prod_short](includes/prod_short.md)] ofrece medios tradicionales, sin tecnología de inteligencia artificial, para importar extractos bancarios, ejecutar reglas de comparación predefinidas y aplicar coincidencias y contabilizar manualmente en cuentas contables apropiadas. Tanto el enfoque tradicional como Copilot se pueden utilizar simultáneamente dentro de una organización. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>¿Cómo doy comentarios sobre el contenido generado por IA?

Cada vez que Copilot proporciona coincidencias o sugerencias, puede proporcionar comentarios a Microsoft directamente desde la ventana de Copilot, utilizando los controles Me gusta y No me gusta. Sus comentarios permanecen anónimos y utilizamos estos datos para mejorar la calidad del servicio.


## <a name="see-also"></a>Consulte también .

[Conciliar cuentas bancarias con la asistencia de conciliación bancaria (vista previa)](bank-reconciliation-with-copilot.md)
