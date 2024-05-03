---
title: Configuración de activos fijos (FA)
description: 'Obtenga información sobre la secuencia de tareas que debe realizar para configurar activos fijos, como maquinaria o edificios.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5607,'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Configurar activos fijos

Antes de trabajar con activos fijos (FA), debe definir algunos parámetros:  

* Cómo se amortizan los activos fijos.  
* Cómo se registran los costes de adquisición, las amortizaciones y otros valores en la contabilidad general.  
* Opcionalmente, cómo registrar seguros y mantenimiento de activos fijos.

Las secciones de este artículo enlazan con más información sobre cómo configurar activos fijos. Una vez finalizada la configuración, puede comenzar a trabajar con activos fijos. Para obtener más información, vea [Usar activos fijos](fa-manage.md).  

> [!NOTE]  
> Puede registrar transacciones de activos en las páginas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna. Los artículos de ayuda para activos fijos solo describen cómo utilizar la página **A/F Diario general**.  

Cuando habilite una actividad de activo fijo en la sección **Integración contabilidad** de la página **Ficha libro amortización**, utilice la página **A/F Diario general** para registrar las transacciones de la actividad.

## Tareas de configuración necesarias

La siguiente tabla contiene una secuencia de tareas para configurar activos fijos y vínculos a artículos relacionados.

| Para | Vea |
|---|---|
| Configurar las cuentas predeterminadas, las claves de asignación, las plantillas y las secciones del diario utilizadas para registrar los activos fijos, y configurar las clases y subclases de activos fijos como, por ejemplo, Tangible e Intangible. |[Configurar información general de activos fijos](fa-how-setup-general.md) |
| Crear libros de amortización y definir varios métodos de amortización, integrarlos con el libro mayor y permitir la duplicación de movimientos en varios libros de amortización. |[Configurar amortización de activos fijos](fa-how-setup-depreciation.md) |

## Tareas de configuración opcionales (seguro, mantenimiento y métodos de amortización definidos por el usuario)

La siguiente tabla contiene una secuencia de tareas opcionales para configurar los activos fijos, como los seguros, el mantenimiento y los métodos de amortización, así como enlaces a artículos relacionados. 

| Para | Vea |
|---|---|
| Activar el seguro de activos fijos, configurar la información del seguro, una ficha de seguro por póliza y preparar los diarios para registrar los costes del seguro. |[Configure el seguro de los activos fijos](fa-how-setup-insurance.md) |
| Activar el mantenimiento de activos fijos, configurar la información general de mantenimiento, configurar el mantenimiento de las cuentas de registro y definir los tipos de trabajo de mantenimiento. |[Configurar el mantenimiento de activos fijos](fa-how-setup-maintenance.md) |
| Obtenga información sobre cómo aplicar métodos de amortización. |[Configurar métodos de amortización definidos por usuario](fa-how-setup-user-defined-depreciation-method.md) |

## Consulte también

[Información general de los activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
