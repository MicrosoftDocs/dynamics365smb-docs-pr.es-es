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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9b683fa14801c00904c131ada5bcce1f669c9b2a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751010"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-prod_short"></a>Facturación masiva para Microsoft Bookings en [!INCLUDE[prod_short](includes/prod_short.md)]
Si su empresa utiliza la aplicación Bookings en Microsoft 365, puede realizar facturación masiva para citas. La página **Bookings sin facturar** de [!INCLUDE[prod_short](includes/prod_short.md)] ofrece una lista de las reservas completadas de la empresa. En esta página puede seleccionar rápidamente citas que desea facturar y para crear borradores de factura de los servicios prestados.  

## <a name="connect-to-bookings"></a>Conectarse a Bookings
Para conectarse [!INCLUDE[prod_short](includes/prod_short.md)] con Bookings, debe especificar su empresa de Bookings, lo que desea sincronizar con Bookings, la frecuencia con que se realizará la sincronización y las plantillas que se usarán. Puede configurar esta información en la página **Configuración de sincronización de Bookings**, que puede iniciar desde la página **Configuración de la sincronización de Exchange**, que puede encontrar mediante [Buscar](ui-search.md).  

Por ejemplo, si desea sincronizar clientes entre Bookings y [!INCLUDE[prod_short](includes/prod_short.md)], debe especificar la plantilla predeterminada que se usa para agregar a los clientes nuevos en [!INCLUDE[prod_short](includes/prod_short.md)] basándose en los clientes en su empresa de Bookings.  

> [!NOTE]
> La aplicación Bookings está diseñada para reservar citas para clientes individuales en lugar de empresas. La sincronización con [!INCLUDE[prod_short](includes/prod_short.md)], por lo tanto, solo sincronizará los contactos del cliente con un Tipo de "Persona". También se requiere una dirección de correo electrónico para que el contacto se sincronice.  

De manera similar, si desea sincronizar los elementos de servicio entre Bookings y [!INCLUDE[prod_short](includes/prod_short.md)], debe especificar la plantilla predeterminada que se usará para agregar nuevos elementos de servicio en [!INCLUDE[prod_short](includes/prod_short.md)] según los servicios de nuestra compañía de Bookings.  

> [!NOTE]
> Solo los elementos de tipo *Servicio* se sincronizarán entre Bookings y [!INCLUDE[prod_short](includes/prod_short.md)]. La plantilla que configuró en la página **Plantillas de configuración** para que se pueda utilizar para la sincronización de elementos debe definir el tipo como *Servicio*.

## <a name="invoice-appointments"></a>Citas de factura
Cuando sea el momento enviar facturas de las reservas completadas, vaya a la página **Bookings sin facturar**. Dependiendo de la frecuencia con que se sincroniza la información, la lista es larga o corta. Puede crear facturas para todas las reservas de la lista o una reserva cada vez. Puede seleccionar una o varias entradas de la lista y facturar solo esas.  

La compatibilidad para facturar citas desde Bookings es más simple que el flujo de trabajo completo para trabajar con ofertas de ventas, pedidos de ventas y facturas de ventas. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md). Puede elegir vender sus servicios utilizando [!INCLUDE[prod_short](includes/prod_short.md)] o elegir usar Bookings, en función de sus necesidades empresariales.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]