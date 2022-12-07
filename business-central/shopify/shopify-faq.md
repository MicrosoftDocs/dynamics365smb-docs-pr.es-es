---
title: Preguntas frecuentes de detalles técnicos
description: Detalles de implementación relacionados con el Connector for Microsoft Dynamics Shopify.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 534b4aa47820bc3738a8ffc22a02151efef64863
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802908"
---
# <a name="faq-for-technical-details"></a>Preguntas frecuentes de detalles técnicos

Este artículo responde a las preguntas más frecuentes sobre el conector de Shopify.

## <a name="what-is-shopify"></a>¿Qué es Shopify? 

Shopify es un software basado en suscripción que permite a cualquier persona configurar una tienda en línea y vender sus productos. La Shopify plataforma ofrece a los minoristas en línea un conjunto de servicios que incluyen herramientas de pagos, marketing, envío y participación del cliente. 

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector"></a>¿Que es Connector for Microsoft Dynamics Dynamics 365 Business Central Shopify? 

Con el conector de Shopify las empresas pueden vincular su tienda (o tiendas) de Shopify con [!INCLUDE[prod_short](../includes/prod_short.md)] para maximizar la productividad de la empresa. Usando el conector de Shopify, pueden gestionar y ver la información de su negocio y su tienda en línea de Shopify como una unidad. 

### <a name="capabilities"></a>Capacidades

- Soporte para más de una tienda de Shopify
  - Cada tienda tiene su propia configuración, incluida una colección de productos, ubicaciones utilizadas para calcular el inventario y listas de precios.  
- Sincronización bidireccional de artículos o productos
  - El conector sincronizará imágenes, variantes de productos, códigos de barras, números de artículos de proveedores, textos extendidos y etiquetas.  
  - Exportar atributos de producto a Shopify.  
  - Use grupos de precios de clientes seleccionados y descuentos para definir los precios exportados a Shopify.  
  - Decida si los elementos se pueden crear automáticamente o solo permitir actualizaciones de productos existentes.  
- Sincronización de nivel de inventario
  - Elija algunas o todas las ubicaciones disponibles en [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Actualice los niveles de inventario en múltiples ubicaciones en Shopify.  
- Sincronización bidireccional de clientes
  - Clientes de mapa inteligente por teléfono y correo electrónico.  
  - Utilice plantillas específicas del país/región al crear clientes, lo que ayuda a garantizar que la configuración de impuestos sea correcta.  
- Importar pedidos desde Shopify
  - Incluir pedidos creados en varios canales, como la tienda en línea o **Shopify POS**. 
  - Costes de envío, tarjetas de regalo, propinas, métodos de envío y pago, transacciones y riesgo de fraude.  
  - Durante la importación, puede crear automáticamente clientes en [!INCLUDE [prod_short](../includes/prod_short.md)] o decidir gestionar los clientes en Shopify.  
  - Recibir información de pago desde Shopify Payments. 
- Seguimiento de la información de cumplimiento
  - Opcionalmente, elija transferir la información de seguimiento del artículo desde [!INCLUDE [prod_short](../includes/prod_short.md)] a Shopify.  

## <a name="why-did-microsoft-and-shopify-form-this-partnership"></a>¿Por qué Microsoft y Shopify forman esta asociación? 

[!INCLUDE[prod_short](../includes/prod_long.md)] se está asociando con Shopify para ayudar a nuestros clientes a crear una mejor experiencia de compra. Mientas que Shopify ofrece a los comerciantes una solución de comercio fácil de usar, [!INCLUDE[prod_short](../includes/prod_short.md)] ofrece una gestión empresarial integral de los equipos de finanzas, ventas, servicios y operaciones dentro de una única aplicación. La conexión perfecta entre los dos sistemas sincroniza los pedidos, las existencias y la información del cliente para que los comerciantes puedan cumplir con los pedidos más rápido y atender mejor a los clientes.

## <a name="what-microsoft-products-is-the-shopify-connector-available-for"></a>¿Para qué productos de Microsoft está disponible el conector de Shopify?

Esta función está disponible solo para [!INCLUDE[prod_short](../includes/prod_short.md)] en línea, a partir de la versión 20.1. No está disponible para implementaciones locales. La aplicación con Connector for Microsoft Dynamics está preinstalada para nuevos entornos. Las organizaciones con entornos existentes pueden descargar e instalar la aplicación desde AppSource. La organización debe tener una licencia de Business Central y una Shopify licencia para usar Connector for Microsoft Dynamics. Obtenga información sobre países, idiomas y ediciones de [!INCLUDE[prod_short](../includes/prod_short.md)] permitidas en [Conector de Shopify en AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

El conector de Shopify no funciona para [Insertar aplicaciones](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), donde la URL del cliente tenga el formato: `https://[application name].bc.dynamics.com`. 

## <a name="what-support-is-offered-for-the-shopify-connector"></a>¿Qué apoyo se ofrece para el conector de Shopify?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Connector for Microsoft Dynamics Shopify está cubierto por el modelo de soporte actual. Obtenga más información en [Soporte técnico](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (solo en inglés). 

Obtenga ayuda de un consultor que conoce Shopify Connector para [!INCLUDE[prod_short](../includes/prod_short.md)], para cumplir con los requisitos exclusivos específicos de su negocio.
 
Busque en [Servicios de consultoría](https://aka.ms/BCShopifyConsultant).

### <a name="shopify"></a>Shopify

Obtenga ayuda con Shopify empezando con [Centro de Ayuda Shopify General](https://help.shopify.com/) o [Soporte 24/7 para tu tienda como Shopify comerciante](https://help.shopify.com/questions#/). 

También puede explorar [Experts Marketplace](https://experts.shopify.com/) para encontrar a los expertos adecuados que ofrecen servicios para los comerciantes de Shopify.

## <a name="currently-not-supported-features-however-were-tracking-them-and-may-consider-adding-them-in-the-future"></a>Actualmente no se admiten funciones, sin embargo, las estamos rastreando y podemos considerar agregarlas en el futuro:

- Funciones B2B, incluidas empresas, listas de precios de empresas, condiciones de pago
- Mercados
  - Múltiples traducciones de datos maestros. Puede elegir un idioma que se utilizará para exportar la información del producto.
  - Precios por país/región. Una lista de precios está disponible para la moneda seleccionada. La conversión a otras monedas estará a cargo de Shopify.

## <a name="is-the-shopify-connector-extensible"></a>¿Es ampliable el conector de Shopify?

Actualmente, esta aplicación no es extensible con planes para hacerlo extensible en 2023. 

## <a name="is-the-shopify-connector-open-for-contribution"></a>¿Está el conector de Shopify abierto a la contribución?

Sí, esta extensión está abierta a la contribución de la comunidad. Puede encontrar el [código fuente](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) en el repositorio de complementos de aplicaciones de Microsoft AL.


## <a name="see-also"></a>Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
