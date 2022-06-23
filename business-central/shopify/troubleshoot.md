---
title: Solución de problemas de Shopify y sincronización de Business Central
description: Descubra qué hacer si algo falla durante la sincronización de datos entre Shopify y Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ff2e4aca52f479e461dab0d9d0f0ce4958d19353
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808873"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Solución de problemas de Shopify y sincronización de Business Central

Es posible encontrarse con situaciones en las que necesite solucionar problemas. Esta página define los pasos para solucionar algunos escenarios comunes que pueden surgir.

## <a name="logs"></a>Registros

Si falla una tarea de sincronización, puede activar el registro habilitando la alternancia **Habilitar registro** en la **Ficha de tienda de Shopify**. Active manualmente la tarea de sincronización y revise los registros.

1. Vaya al icono de búsqueda ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer"). , escriba **Movimientos de registro de Shopify** y luego elija el vínculo relacionado.
2. Seleccione el movimiento de registro relacionado y abra la ventana **Movimiento de registro de Shopify**.
3. Revise la solicitud, el código de estado y la descripción, y la respuesta.

Recuerde desactivar el registro para evitar un impacto negativo en el rendimiento y un aumento en el tamaño de la base de datos.

Desde la ventana **Movimientos de registro de Shopify**, puede desencadenar la eliminación de todas las entradas de registro o las que tengan más de siete días.

## <a name="data-capture"></a>Captura de datos

Sin importar los ajustes de **Registro activado**, algunas respuestas de Shopify siempre se registran para que pueda inspeccionarlas o descargarlas usando la ventana **Lista de captura de datos**.

Elija la acción **Datos de Shopify recuperados** en una de las siguientes páginas:

- **Pedido de Shopify**
- **Cumplimento de pedido de Shopify**
- **Gastos de envío de pedido de Shopify**
- **Transacciones de pedido de Shopify**
- **Pagos de Shopify**
- **Transacciones de pago de Shopify**
- **Transacciones de Shopify**

## <a name="reset-sync"></a>Restablecer sincronización

Para un rendimiento óptimo, el conector importa solo clientes, productos y pedidos creados o modificados desde la última sincronización. En la **Ficha de tienda de Shopify**, hay funciones disponibles para cambiar la fecha y hora de la última sincronización o restablecerla por completo. Esta función garantiza que cuando se ejecuta la sincronización, se sincronizan todos los datos y no solo los cambios desde la última sincronización.

Esta función solo se aplica a las sincronizaciones de Shopify para [!INCLUDE[prod_short](../includes/prod_short.md)] y puede ser útil si necesita restaurar datos eliminados, como productos, clientes o pedidos eliminados.

## <a name="update-the-access-token"></a>Actualizar el token de acceso

Si [!INCLUDE[prod_short](../includes/prod_short.md)] no puede conectarse a su cuenta de Shopify, intente restablecer el token de acceso.

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea conseguir el token de acceoso para abrir la página **Tarjeta de tienda de Shopify**.
3. Elegir la acción **Solicitar acceso**.
4. Si se le solicita, inicie sesión en su cuenta de Shopify.

## <a name="see-also"></a>Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
