---
title: Asignar documentos electrónicos a líneas de pedido de compra con Copilot
description: Obtenga información sobre cómo utilizar Copilot para asignar documentos electrónicos a líneas de órdenes de compra.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 02/23/2024
ms.custom: bap-template
---

# <a name="map-e-documents-to-purchase-order-lines-with-copilot-preview"></a>Asignar documentos electrónicos a líneas de pedido de compra con Copilot (versión preliminar)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

A medida que los procesos de adquisiciones se vuelven más digitales, la función de documentos electrónicos en Business Central desempeña un papel clave en la automatización de la recepción y el procesamiento de facturas de proveedores. Copilot puede ayudar en este proceso mejorando la asignación y la correspondencia de las facturas de los proveedores con las órdenes de compra. Esto reduce las tareas que consumen mucho tiempo y que normalmente incluirían búsquedas, consultas e introducción de datos exhaustivas. El beneficio se ve agravado por el hecho de que las facturas de los proveedores a menudo no se relacionan exactamente con los pedidos de compra, en cuyo caso Copilot está mejor posicionado para identificar los pedidos de compra correspondientes. Las capacidades de comparación mejoradas benefician particularmente a las organizaciones pequeñas y medianas que necesitan un seguimiento eficiente de documentos para líneas de órdenes de compra. Copilot es el asistente de trabajo con tecnología de IA que impulsa la creatividad y mejora la productividad de los usuarios de Business Central.

> [!IMPORTANT]
> - Esta es una característica de Vista previa lista para producción para entornos de producción y sandbox en cualquier localización de país o región, con excepción de Canadá.
> - Las vistas previas listas para producción están sujetas a términos de uso complementarios. Más información: [Términos de uso complementarios para la vista previa de Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)
> - El contenido generado por IA puede ser incorrecto.

En la versión inicial de la aplicación **documento electrónico**, introdujimos escenarios fundamentales para documentos electrónicos para todo el proceso de ventas. Sin embargo, existe la necesidad de mejoras y automatización en el manejo de los documentos recibidos, especialmente en el contexto de los procesos de compra. Copilot perfecciona la forma de gestionar los documentos electrónicos en el proceso de compra, especialmente con respecto a las órdenes de compra. El marco de documentos electrónicos le permite especificar el tipo de documento de compra que creará para cada proveedor cuando reciba facturas electrónicas de ellos. Anteriormente, la única opción era crear una factura de compra, ya sea como documento o como diario del libro mayor.

Ahora puede actualizar una orden de compra existente en Business Central con la información recibida en la factura electrónica.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->


## <a name="identify-purchase-orders"></a>Identificar pedidos compra

Primero, puede identificar los pedidos de compra que puede corresponder automáticamente.

## <a name="map-lines"></a>Asignar líneas

Copilot le ayuda a hacer coincidir automáticamente líneas de facturas electrónicas con líneas de órdenes de compra y ofrece inteligencia de comparación adicional para mejorar las coincidencias.

Después de compararlos y asignarlos, Business Central actualiza la orden de compra coincidente con la información de recibo relevante para garantizar que se reciban las cantidades correctas en las líneas de pedido.

## <a name="see-also"></a>Consulte también

[Información general de documentos electrónicos](finance-edocuments-overview.md)  
[Usar documentos electrónicos en ventas y compras](finance-how-use-edocuments.md)  
[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)  
[Preguntas frecuentes para IA responsable para asistencia de conciliación bancaria](faqs-bank-reconciliation.md)  
