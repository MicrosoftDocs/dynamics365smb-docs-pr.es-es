---
title: Primeros pasos con el conector para Shopify
description: Primeros pasos al configurar la conexión entre Business Central y Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768156"
---
# <a name="get-started-with-the-shopify-connector"></a>Comenzar con el conector de Shopify

[!INCLUDE [prod_short](../includes/prod_short.md)] le da la flexibilidad de conectar su tienda de Shopify (o tiendas) con él para maximizar la productividad de su negocio. Puede administrar y ver información de su negocio y su tienda de Shopify tienda en línea como una unidad usando el conector de Shopify Para usar Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)], necesita seguir algunos pasos. Esta página sirve como guía para completar la integración de su almacén de Shopify con [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Requisitos previos para Shopify

Debe tener:

- Una cuenta de Shopify
- Tienda en línea con Shopify

Para crear una cuenta nueva de Shopify o registrarse para una prueba gratuita de 14 días, vaya a [Shopify](https://www.shopify.com/). Para obtener más información sobre cómo crear y personalizar su tienda en línea, consulte [Centro de ayuda de Shopify](https://help.shopify.com/).
  
- Se admiten otros canales de venta, por ejemplo, Shopify PDV.

### <a name="recommended-settings"></a>Configuraciones recomendadas

- Desactive **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de [**Finalizar compra**](https://www.shopify.com/admin/settings/checkout) del **Administrador de Shopify**.

Para saber más sobre la configuración de Shopify para escenarios de demostración y prueba, consulte [Escenarios de prueba y formación](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Requisitos previos para Business Central

- Asegúrese de que la extensión **Conectar a Shopify para [!INCLUDE[prod_short](../includes/prod_short.md)]** está instalada.

La extensión está preinstalada para todos los nuevos registros y pruebas. Si necesita instalar extensiones desde el Marketplace, visite [Instalación y desinstalación de extensiones](../ui-extensions-install-uninstall.md#install). Siga los pasos enumerados a continuación si no tiene [!INCLUDE[prod_short](../includes/prod_short.md)].
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Conexión de Business Central a la tienda en línea de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de la búsqueda , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.  
3. En el campo **Código**, escriba el código deseado.  
4. En el campo **URL de Shopify**, escriba la URL de su tienda en línea, que debe conectarse.
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

