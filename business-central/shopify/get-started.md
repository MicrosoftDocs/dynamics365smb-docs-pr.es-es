---
title: Primeros pasos con el conector para Shopify
description: Primeros pasos al configurar la conexión entre Business Central y Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: e59dd0dcf757fbcf76d4068756adfe7bc9475f54
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361561"
---
# <a name="get-started-with-the-shopify-connector"></a>Comenzar con el conector de Shopify

Conecte su tienda (o tiendas) de Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)] y maximice la productividad de su negocio. Administre y vea información de su negocio y su tienda de Shopify como una unidad. 

El connector de Shopify incluye las siguientes capacidades:

- Soporte para más de una tienda de Shopify  

  - Cada tienda tiene su propia configuración, incluida una colección de productos, ubicaciones utilizadas para calcular el inventario y listas de precios.  
- Sincronización bidireccional de artículos o productos  

  - El conector sincronizará imágenes, variantes de productos, códigos de barras, números de artículos de proveedores, textos extendidos y etiquetas.  
  -    Exportar atributos de producto a Shopify.  
  -    Use grupos de precios de clientes seleccionados y descuentos para definir los precios exportados a Shopify.  
  -    Decida si los elementos se pueden crear automáticamente o solo permitir actualizaciones de productos existentes.  
- Sincronización de nivel de inventario  

  -    Elija algunas o todas las ubicaciones disponibles en [!INCLUDE [prod_short](../includes/prod_short.md)].  
  -    Actualice los niveles de inventario en múltiples ubicaciones en Shopify.  
- Sincronización bidireccional de clientes  

  -    Clientes de mapa inteligente por teléfono y correo electrónico.  
  -    Utilice plantillas específicas del país/región al crear clientes, lo que ayuda a garantizar que la configuración de impuestos sea correcta.  
- Importar pedidos desde Shopify  

  -    Durante la importación, puede crear automáticamente clientes en [!INCLUDE [prod_short](../includes/prod_short.md)] o decidir gestionar los clientes en Shopify.  
  -    Incluir pedidos creados en otros canales, como Shopify POS o Amazon.  
  -    Costes de envío, tarjetas de regalo, propinas, métodos de envío y pago, transacciones y riesgo de fraude.  
  - Recibir información de pago desde Shopify Payments.  
- Fácil seguimiento de la información de cumplimiento  

  -    Opcionalmente, elija escribir la información de seguimiento del artículo desde [!INCLUDE [prod_short](../includes/prod_short.md)] a Shopify.  

Para usar Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], debe a hacer algunas cosas primero. Este artículo sirve como guía para completar la integración de su almacén de Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Requisitos previos para Shopify

Debe tener:

- Una cuenta de Shopify
- Tienda en línea con Shopify

Para crear una cuenta nueva de Shopify o registrarse para una prueba gratuita de 14 días, vaya a [Shopify](https://www.shopify.com/). Para obtener más información sobre cómo crear y personalizar su tienda en línea, consulte [Centro de ayuda de Shopify](https://help.shopify.com/).
  
Se admiten otros canales de venta, por ejemplo, Shopify PDV.

### <a name="recommended-settings"></a>Configuraciones recomendadas

- Desactive **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de [**Finalizar compra**](https://www.shopify.com/admin/settings/checkout) del **Administrador de Shopify**.

Para saber más sobre la configuración de Shopify para escenarios de demostración y prueba, consulte [Escenarios de prueba y formación](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Requisitos previos para Business Central

- Asegúrese de que la aplicación **[Connector de Shopify](https://go.microsoft.com/fwlink/?linkid=2196238)** esté instalada.

La aplicación está preinstalada para todos los nuevos registros y pruebas. Más información sobre como instalar aplicaciones desde el Marketplace, consulte [Instalar y desinstalar extensiones](../ui-extensions-install-uninstall.md#install). Siga los pasos enumerados a continuación si no tiene [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Instalar la aplicación **Dynamics 365 Business Central** para su tienda en línea de Shopify

Por [!INCLUDE[prod_short](../includes/prod_short.md)] existentes, este paso es opcional y se puede omitir.

1. Localizar la aplicación [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) en la [AppStore de Shopify](https://apps.shopify.com/)
2. Seleccione el botón **Agrega aplicación**. Si se le solicita, inicie sesión en su cuenta de Shopify. Seleccione la tienda en línea si tiene más de una.
3. Después de revisar la privacidad y los permisos, seleccione el botón **Instalar aplicación**.
  Puede encontrar y abrir la aplicación instalada **Dynamics 365 Business Central** en la sección **Aplicaciones** de la barra lateral de **administración de Shopify**.
4. Elija **Registrarse ahora** para empezar la prueba de [!INCLUDE[prod_short](../includes/prod_short.md)] o **Iniciar sesión** si ya tiene [!INCLUDE[prod_short](../includes/prod_short.md)]. Se le redirigirá a su [!INCLUDE[prod_short](../includes/prod_short.md)] en [Business Central](https://businesscentral.dynamics.com).
5. Los siguientes pasos deben hacerse en [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Conexión de Business Central a la tienda en línea de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de la búsqueda , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.  
3. En el campo **Código**, escriba el código deseado.  
4. En el campo **URL de Shopify**, escriba la URL de su tienda en línea, que debe conectarse. Utilice el siguiente formato: `https://{shop}.myshopify.com/`.
5. Active la alternancia **Habilitada** y revise y acepte los términos y condiciones.
6. Si se le solicita, inicie sesión en su cuenta de Shopify, revise la privacidad y los permisos, y luego elija el botón **Instalar aplicación**.

Repita los pasos 2 a 6 para todas las tiendas en línea que desee conectar.

### <a name="next-steps"></a>Pasos siguientes

Ahora su tienda en línea está conectada a [!INCLUDE[prod_short](../includes/prod_short.md)]. En los siguientes pasos, definirá cómo y qué sincronizar.

- [Sincronizar elementos](synchronize-items.md)
- [Sincronizar clientes](synchronize-customers.md)
- [Sincronizar pedidos](synchronize-orders.md)

## <a name="see-also"></a>Consulte también

[Escenarios de prueba y formación](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

