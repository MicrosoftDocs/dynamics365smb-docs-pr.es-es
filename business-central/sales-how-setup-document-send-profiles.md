---
title: Configurar métodos preferidos para enviar documentos de venta | Documentos de Microsoft
description: Describe cómo configurar el método preferido de cada cliente de enviar documentos de venta, por ejemplo, correo electrónico, PDF, documento electrónico, etc.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8a80d4815e41a1f57f68c5ed9a00042b3fdd76be
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316385"
---
# <a name="set-up-document-sending-profiles"></a>Configurar perfiles de envío de documentos
Puede configurar cada cliente con un método preferido para enviar documentos de venta, de modo que no tenga que seleccionar una opción de envío cada vez que elija la acción **Registrar y enviar**.

En la página **Perfiles de envío de documentos**, puede establecer diferentes perfiles de envío que puede seleccionar del campo **Perfil de envío de documentos** de una ficha de cliente. Puede seleccionar la casilla de verificación **Predeterminado** para especificar que el perfil de envíos de documentos sea el perfil predeterminado para todos los clientes, en que el campo **Perfil de envío de documentos** se rellena con otro perfil de envío.

Cuando elige la acción **Registrar y enviar** en un documento de venta, el cuadro de diálogo **Registrar y enviar confirmación** muestra el perfil de envío usado, tanto el configurado para el cliente como el predeterminado para todos los clientes. En el cuadro de diálogo puede cambiar el perfil de envío para el documento de venta. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Para configurar un perfil de envío de documentos
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Perfiles de envío de documentos** y luego elija el enlace relacionado.
2. En la página **Perfiles de envío de documentos**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Para especificar un perfil de envío en una ficha cliente
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha del cliente para el que desea configurar un perfil de envío.
3. En el campo **Perfil de envío de documentos**, seleccione un perfil que haya configurado como se describe en el procedimiento anterior.

## <a name="see-also"></a>Consulte también
[Configuración de ventas](sales-setup-sales.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
