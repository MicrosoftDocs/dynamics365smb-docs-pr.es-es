---
title: Facturar las reservas en Business Central
description: Este tema explica cómo aprender a realizar la facturación masiva desde Microsoft Bookings en Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Facturación masiva para Microsoft Bookings en [!INCLUDE[prod_short](includes/prod_short.md)]

Si su empresa utiliza la aplicación Bookings en Microsoft 365, puede hacer la facturación masiva para citas. La página **Reservas no facturadas** de [!INCLUDE[prod_short](includes/prod_short.md)] ofrece una lista de las reservas completadas de la empresa. En esta página puede seleccionar rápidamente citas que desea facturar y para crear borradores de factura de los servicios prestados.  

## Conectarse a Bookings

Para conectarse [!INCLUDE[prod_short](includes/prod_short.md)] con Bookings, debe especificar su empresa de Bookings, lo que desea sincronizar con Bookings, la frecuencia con que se realizará la sincronización y las plantillas que se usarán. Puede configurar esta información en la página **Configuración de sincronización de Bookings**, que puede iniciar desde la página **Configuración de la sincronización de Exchange**, que puede encontrar mediante [Buscar](ui-search.md).  

Por ejemplo, si desea sincronizar clientes entre Bookings y [!INCLUDE[prod_short](includes/prod_short.md)], debe especificar la plantilla predeterminada que se usa para agregar a los clientes nuevos en [!INCLUDE[prod_short](includes/prod_short.md)] basándose en los clientes en su empresa de Bookings.  

> [!NOTE]
> La aplicación Bookings está diseñada para reservar citas para clientes individuales en lugar de empresas. La sincronización con [!INCLUDE[prod_short](includes/prod_short.md)], por tanto, solo sincronizará los contactos del cliente con un Tipo de *Persona*. También se requiere una dirección de correo electrónico para que el contacto se sincronice.  

De manera similar, si desea sincronizar los elementos de servicio entre Bookings y [!INCLUDE[prod_short](includes/prod_short.md)], debe especificar la plantilla predeterminada que se usará para agregar nuevos elementos de servicio en [!INCLUDE[prod_short](includes/prod_short.md)] según los servicios de nuestra compañía de Bookings.  

> [!NOTE]
> Solo los elementos de tipo *Servicio* se sincronizarán entre Bookings y [!INCLUDE[prod_short](includes/prod_short.md)]. La plantilla que configuró en la página **Plantillas de configuración** para que se pueda utilizar para la sincronización de elementos debe definir el tipo como *Servicio*.

## Citas de factura

Cuando sea el momento de enviar facturas de las reservas completadas, vaya a la página **Reservas no facturadas**. Dependiendo de la frecuencia con que se sincroniza la información, la lista es larga o corta. Puede crear facturas para todas las reservas de la lista o una reserva cada vez. Puede seleccionar una o varias entradas de la lista y facturar solo esas.  

La compatibilidad para facturar citas desde Bookings es más simple que el flujo de trabajo completo para trabajar con ofertas de ventas, pedidos de ventas y facturas de ventas. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md). Puede elegir vender sus servicios utilizando [!INCLUDE[prod_short](includes/prod_short.md)] o elegir usar Bookings, en función de sus necesidades empresariales.  

> [!NOTE]
> En mayo de 2022, hemos detectado un problema en la integración con Bookings. Actualmente, la sincronización de Bookings con [!INCLUDE [prod_short](includes/prod_short.md)] requiere la asociación manual de las facturas con los clientes en [!INCLUDE [prod_short](includes/prod_short.md)].

## Consulte también

[Finanzas](finance.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]