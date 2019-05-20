---
title: Facturar las reservas en Business Central | Documentos de Microsoft
description: Obtenga información sobre cómo realizar la facturación masiva desde Microsoft Bookings en Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: faa7946dd376dd8e0f89e35cd798a6de45a3248d
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242910"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a>Facturación masiva para Microsoft Bookings en [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si su empresa utiliza la aplicación Bookings en Office 365, puede hacer la facturación masiva para citas. La página **Bookings sin facturar** de [!INCLUDE[d365fin](includes/d365fin_md.md)] ofrece una lista de las reservas completadas de la empresa. En esta página puede seleccionar rápidamente citas que desea facturar y para crear borradores de factura de los servicios prestados.  

## <a name="connect-to-bookings"></a>Conectarse a Bookings
Para conectarse [!INCLUDE[d365fin](includes/d365fin_md.md)] con Bookings, debe especificar su empresa de Bookings, lo que desea sincronizar con Bookings, la frecuencia con que se realizará la sincronización y las plantillas que se usarán. Puede configurar esta información en la página **Configuración de sincronización de Bookings**, que puede iniciar desde la página **Configuración de la sincronización de Exchange**, que puede encontrar mediante [Buscar](ui-search.md).  

Por ejemplo, si desea sincronizar clientes entre Bookings y [!INCLUDE[d365fin](includes/d365fin_md.md)], debe especificar la plantilla predeterminada que se usa para agregar a los clientes nuevos en [!INCLUDE[d365fin](includes/d365fin_md.md)] basándose en los clientes en su empresa de Bookings.  

> [!NOTE]
> La aplicación Bookings está diseñada para reservar citas para clientes individuales en lugar de empresas. La sincronización con [!INCLUDE[d365fin](includes/d365fin_md.md)], por lo tanto, solo sincronizará los contactos del cliente con un Tipo de "Persona". También se requiere una dirección de correo electrónico para que el contacto se sincronice.  

De manera similar, si desea sincronizar los elementos de servicio entre Bookings y [!INCLUDE[d365fin](includes/d365fin_md.md)], debe especificar la plantilla predeterminada que se usará para agregar nuevos elementos de servicio en [!INCLUDE[d365fin](includes/d365fin_md.md)] según los servicios de nuestra compañía de Bookings.  

> [!NOTE]
> Solo los elementos de tipo *Servicio* se sincronizarán entre Bookings y [!INCLUDE[d365fin](includes/d365fin_md.md)]. La plantilla que configuró en la página **Plantillas de configuración** para que se pueda utilizar para la sincronización de elementos debe definir el tipo como *Servicio*.

## <a name="invoice-appointments"></a>Citas de factura
Cuando sea el momento enviar facturas de las reservas completadas, vaya a la página **Bookings sin facturar**. Dependiendo de la frecuencia con que se sincroniza la información, la lista es larga o corta. Puede crear facturas para todas las reservas de la lista o una reserva cada vez. Puede seleccionar una o varias entradas de la lista y facturar solo esas.  

La compatibilidad para facturar citas desde Bookings es más simple que el flujo de trabajo completo para trabajar con ofertas de ventas, pedidos de ventas y facturas de ventas. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md). Puede elegir vender sus servicios utilizando [!INCLUDE[d365fin](includes/d365fin_md.md)] o elegir usar Bookings, en función de sus necesidades empresariales.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/en-us/business/scheduling-and-booking-app)  
