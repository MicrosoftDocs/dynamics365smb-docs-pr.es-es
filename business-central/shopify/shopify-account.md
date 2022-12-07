---
title: Crear y configurar una cuenta de Shopify
description: Aprenda a obtener una cuenta de Shopify para que pueda demostrar el flujo de trabajo para integrar Shopify y Business Central.
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b4449b573307582595ee9949dcb53d5d553ce0f2
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803058"
---
# <a name="create-and-set-up-a-shopify-account"></a>Crear y configurar una cuenta de Shopify

Si está considerando utilizar Shopify como su solución de comercio electrónico y necesita una cuenta Shopify para validar el flujo de trabajo integrado, tiene las siguientes opciones:

- Obtenga una versión de prueba. Este es el punto de partida típico para los usuarios finales.  
- Crear tiendas de desarrollo. Este enfoque es para socios que realizan demostraciones recurrentes, capacitaciones y brindan soporte.

## <a name="trial-end-user"></a>Prueba (usuario final)

Vaya al [sitio web de Shopify](https://www.shopify.com) y use su cuenta de correo electrónico como cuenta de administrador para registrarse para una prueba gratuita. Para obtener más información sobre cómo crear y personalizar su tienda en línea, consulte el [Centro de ayuda de Shopify](https://help.shopify.com/).

En el **Administrador de Shopify** de la tienda creada, aplique la siguiente **Configuración**:

- Desactive **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de [**Finalizar compra**](https://www.shopify.com/admin/settings/checkout) del **Administrador de Shopify**.
- Considere habilitar *Mostrar enlace de inicio de sesión en la tienda y pagar* en la sección **Configuración de la cuenta del cliente** de la configuración de pago.
- Considere seleccionar la opción *Nombre de la empresa - Opcional* en la sección **Información del cliente** de la configuración de pago.
- Habilite la opción **Mostrar opciones de propinas al finalizar la compra** en la sección **Propinas** de la configuración de la finalización de la compra, si planea demostrar propinas
- Activa los pagos de prueba. Tiene dos opciones. Comience yendo a la configuración de [**Pagos**](https://www.shopify.com/admin/settings/payments):  
  1. *(para probar) Bogus Gateway*. Para obtener más información, consulte [Activar Bogus Gateway para realizar pruebas](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* en modo de prueba. Para obtener más información, consulte [Probar Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Seleccione un plan en la configuración de [**Plan**](https://www.shopify.com/admin/settings/plan) para poder probar el proceso de pago.

> [!Important]  
> Para evitar pagos, recuerda cancelar su prueba de Shopify.

## <a name="development-store"></a>Tienda de desarrollo

Comience por unirse al [Programa de socios de Shopify](https://help.shopify.com/partners/about). Luego, use el **panel de socios** para crear la tienda en desarrollo. Más información en [Crear tiendas de desarrollo](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Después de crear la tienda, en el **Administrador de Shopify** de la tienda creada, aplique la siguiente **Configuración**:

- Desactive **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de [**Finalizar compra**](https://www.shopify.com/admin/settings/checkout) del **Administrador de Shopify**.
- Considere habilitar *Mostrar enlace de inicio de sesión en la tienda y pagar* en la sección **Configuración de la cuenta del cliente** de la configuración de pago.
- Considere seleccionar la opción *Nombre de la empresa - Opcional* en la sección **Información del cliente** de la configuración de pago.
- Si tiene previsto demostrar las propinas, habilite la opción **Mostrar opciones de propinas al finalizar la compra** en la sección **Propinas** de la configuración de la finalización de la compra.
- Activa los pagos de prueba. Tiene dos opciones. Comience yendo a la configuración de [**Pagos**](https://www.shopify.com/admin/settings/payments):  
  1. *(para probar) Bogus Gateway*. Para obtener más información, consulte [Activar Bogus Gateway para realizar pruebas](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* en modo de prueba. Obtenga más información en [Probar Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

## <a name="see-also"></a>Consulte también

[Comenzar con el conector Shopify](get-started.md)  
[Tutorial: Configurar y usar el Shopify Connector](walkthrough-setting-up-and-using-shopify.md)
