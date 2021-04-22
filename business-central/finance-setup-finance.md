---
title: Configurar los procesos financieros | Documentos de Microsoft
description: Obtenga información sobre las tareas para configurar las finanzas en su empresa para adaptarse a todas sus necesidades de contabilidad o auditoría.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f93eaa38b07a5135aafa22b21253d1e99a8d0406
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788107"
---
# <a name="setting-up-finance"></a>Configurar las finanzas
Antes de que pueda comenzar a administrar su negocio, debe especificar reglas y valores predeterminados sobre cómo desea administrar los procesos financieros para esa empresa. En primer lugar, deberá configurar el elemento básico de los registros de contabilidad de la empresa - el plan de cuentas. A continuación, deberá configurar los grupos contables, que permiten que la asignación de cuentas contables predeterminadas a los clientes, proveedores y productos sea más eficaz.

Algunas configuraciones financieras se pueden hacer automáticamente con guías de configuración asistidas, y algunas deben hacerse manualmente. Para obtener más información, vea [Preparación para hacer negocios](ui-get-ready-business.md).

Puede utilizar dimensiones para agregar diferentes tipos de información a cada transacción. Puede configurar las dimensiones básicas de la empresa, por ejemplo, Proyectos y Departamentos. Posteriormente, puede agregar más dimensiones cuando sea necesario y configurar dimensiones temporales para utilizarlas durante un periodo de tiempo limitado, por ejemplo, en relación con una campaña de ventas. Para obtener más información, consulte [Trabajar con dimensiones](finance-dimensions.md).

En general, las tareas de configuración se deben completar para poder registrar las transacciones financieras, aunque la mayoría de las configuraciones se pueden modificar posteriormente. Algunas de las tareas de configuración son opcionales, por ejemplo, los registros entre empresas vinculadas y las consolidaciones sólo se deben configurar si trabaja con varias empresas. Algunas tareas de configuración tales como la introducción del periodo durante el que se permite el registro puede que se tengan que repetir de forma periódica.  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
| Especifique cómo desea que le paguen los clientes y cómo desea pagar a sus proveedores. |[Configure formas de pago](finance-payment-methods.md) |
| Especifique términos de pago para administrar las fechas de vencimiento y calcular posibles descuentos por pronto pago.|[Configurar términos de pago](finance-payment-terms.md) |
| Especifique los grupos contables que asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. |[Configurar los grupos contables](finance-posting-groups.md)|
|Cree esquemas de cuentas y defina las categorías de cuentas para definir el contenido de los gráficos e informes financieros, como los informes Balance y Balance de ingresos.|[Preparar informes financieros con esquemas de cuentas y categorías de cuentas](bi-how-work-account-schedule.md)|
|Configure una tolerancia por la que el sistema cierre una factura aunque el pago, incluido el descuento, no cubra totalmente el importe de la factura.|[Trabajar con tolerancias de pago y tolerancias de descuento de pago](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Configure los periodos fiscales. |[Trabajar con periodos contables y ejercicios](finance-accounting-periods-and-fiscal-years.md) |
|Configure términos de recordatorio para ayudarlo a cobrar los pagos vencidos.|[Configurar términos y niveles de recordatorios.](finance-setup-reminders.md)|
| Definir cómo se comunican los importes del impuesto de valor añadido que ha recopilado por las ventas a las autoridades fiscales. |[Configurar el impuesto sobre el valor añadido (IVA)](finance-setup-vat.md)|
|Prepárese para gestionar el IVA no realizado en conexión con los métodos contables basados en efectivo.|[Configurar el IVA no realizado para la contabilidad basada en efectivo](finance-setup-unrealized-vat.md)|
| Configure sus características de ventas y compras para manejar pagos en divisas extranjeras.|[Permitir la liquidación de movimientos de cliente en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md)
|Defina una o varias divisas adicionales para que los importes se reporten automáticamente tanto en DL como en una divisa de informe adicional en cada entrada de contabilidad y en otras entradas.|[Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md)|
|Ajuste periódicamente los equivalentes de divisa adicionales para compensar tipos de cambio que fluctúan.|[Actualizar tipos cambio divisa](finance-how-update-currencies.md)|
|Defina varias tasas de interés con el fin de utilizarlas para diferentes períodos de pagos retrasados en las transacciones comerciales.|[Configurar varios tipos de interés.](finance-how-to-set-up-multiple-interest-rates.md)|
|Prepárese para redondear automáticamente los importes de las facturas en el momento en que estas se crean.|[Configurar redondeo de factura](finance-set-up-invoice-rounding.md)|
| Agregue nuevas cuentas al plan de cuentas existente. |[Configuración del plan contable](finance-setup-chart-accounts.md) |
| Configure gráficos de inteligencia empresarial (BI) para analizar el flujo de efectivo. |[Configuración del análisis de flujo de efectivo](finance-setup-cash-flow-analyses.md) |
|Activar la facturación de un cliente que no está configurado en el sistema.|[Configurar clientes de efectivo](finance-how-to-set-up-cash-customers.md)|
| Configurar los informes Intrastat y, enviar el informe a una autoridad | [Configuración y creación de informes Intrastat](finance-how-setup-report-intrastat.md)|
|Asegúrese de que un movimiento de un diario general esté asignado a varias cuentas diferentes al registrar el diario, ya sea cantidad, porcentaje o importe.|[Utilizar claves de asignación en diarios generales](ui-how-use-allocation-keys-general-journals.md)|
|Configurar códigos de origen y códigos de auditoría que puede usar para realizar un seguimiento de pistas de auditoría|[Configuración de códigos de origen y códigos de auditoría para pistas de auditoría](finance-setup-trail-codes.md)|
|Especifique informes predeterminados que se utilizarán para diferentes tipos de documentos.|[Selección de informes en Business Central](across-report-selections.md)|

> [!TIP]
> Según su ubicación geográfica, algunas páginas pueden contener campos que no se describen en los productos que se enumeran aquí, porque se aplican a funciones o personalizaciones locales. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]