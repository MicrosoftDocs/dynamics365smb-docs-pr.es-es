---
title: Configurar procesos financieros
description: Obtenga información sobre las tareas requeridas para configurar las finanzas en su empresa para adaptarse a todas sus necesidades de contabilidad o auditoría.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.date: 08/19/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Configurar las finanzas

Antes de que pueda comenzar a administrar su negocio, debe especificar cómo desea administrar los procesos financieros de la empresa. En primer lugar, debe configurar el elemento básico de los registros de contabilidad de la empresa: el plan de cuentas (COA). A continuación, debe configurar los grupos contables, que se encargan de que el proceso de asignación de cuentas contables predeterminadas a los clientes, proveedores y productos sea más eficaz.

Algunas configuraciones financieras se pueden hacer automáticamente con guías de configuración asistidas, y algunas deben hacerse manualmente. Obtenga más información en [Preparación para hacer negocios](ui-get-ready-business.md). La página **Configuración de contabilidad** especifica cómo gestionar los distintos procesos contables de su empresa. Por ejemplo, utilice esta página para especificar los detalles del redondeo de facturas, el código de divisa de la divisa local, los formatos de dirección y si desea utilizar una divisa alternativa para informes. Obtenga más información en [Descripción de contabilidad y plan de cuentas](finance-general-ledger.md).  

Puede utilizar dimensiones para agregar diferentes tipos de información a cada transacción. Puede configurar las dimensiones básicas de la empresa, por ejemplo, *Proyectos* y *Departamentos*. Más adelante, agregue más dimensiones cuando las necesite. Por ejemplo, puede configurar dimensiones temporales para usarlas durante un período de tiempo limitado, como durante una campaña de ventas. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

La mayoría de las tareas de configuración deben completarse para poder empezar a registrar transacciones financieras, aunque la mayoría de las configuraciones se pueden ajustas en función de las necesidades. Dicho esto, también hay tareas de configuración opcionales. Por ejemplo, solo tiene que configurar registros y consolidaciones de empresas vinculadas si trabaja con varias empresas. Y es posible que otras tareas de configuración, tales como la introducción del período durante el que se permite el registro, se tengan que repetir de forma periódica.  

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
|Ver o editar cuentas de contabilidad en las que se registran todos los movimientos de contabilidad|[Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md)|
| Especifique cómo desea que le paguen los clientes y cómo desea pagar a sus proveedores. |[Configure formas de pago](finance-payment-methods.md) |
| Especifique los términos de pago para administrar las fechas de vencimiento y calcular posibles descuentos en el pago.|[Configurar términos de pago](finance-payment-terms.md) |
| Especifique los grupos contables que asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. |[Configurar los grupos contables de activos](finance-posting-groups.md)|
|Cree informes financieros y defina las categorías de cuentas que determinan el contenido de los gráficos e informes financieros, como los informes Saldo y Extracto de ingresos.|[Preparar Financial Reporting con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)|
|Configure una tolerancia por la que el sistema cierre una factura aunque el pago, incluido el descuento, no cubra totalmente el importe de la factura.|[Trabajar con tolerancias de pago y tolerancias de descuento de pago](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Configure los periodos fiscales. |[Trabajar con periodos contables y ejercicios](finance-accounting-periods-and-fiscal-years.md) |
|Configure términos de la factura que recuerden al cliente que debe pagar.|[Configurar términos y niveles de recordatorios.](finance-setup-reminders.md)|
| Defina cómo informa a las autoridades fiscales de los importes del impuesto de valor añadido (IVA) que ha recaudado sobre las ventas. |[Configurar el impuesto sobre el valor añadido (IVA)](finance-setup-vat.md)|
|Prepárese para gestionar el IVA no realizado en conexión con los métodos contables basados en efectivo.|[Configurar el IVA no realizado para la contabilidad basada en efectivo](finance-setup-unrealized-vat.md)|
|Defina las divisas extranjeras con las que opera o notifica transacciones.|[Configuración de divisas](finance-set-up-currencies.md)|
| Configure sus características de ventas y compras para manejar pagos en divisas extranjeras.|[Permitir la liquidación de movimientos de cliente en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md)
|Defina una o varias divisas adicionales para que los importes se notifiquen automáticamente tanto en divisa local (LCY) como en una divisa de informe adicional en cada movimiento de contabilidad (G/L) y en otros movimientos.|[Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md)|
|Ajuste periódicamente los equivalentes de divisa adicionales para compensar tipos de cambio que fluctúan.|[Actualizar tipos de cambio de divisa](finance-how-update-currencies.md)|
|Defina varias tasas de interés para utilizarlas en diferentes períodos para pagos retrasados en las transacciones comerciales.|[Configurar varios tipos de interés.](finance-how-to-set-up-multiple-interest-rates.md)|
|Haga que los importes se redondeen automáticamente a medida que se crean las facturas.|[Configurar redondeo de factura](finance-set-up-invoice-rounding.md)|
| Agregue nuevas cuentas al plan de cuentas existente. |[Configuración del plan contable](finance-setup-chart-accounts.md) |
| Configure gráficos de inteligencia empresarial (BI) para analizar el flujo de efectivo. |[Configuración del análisis de flujo de efectivo](finance-setup-cash-flow-analyses.md) |
|Active la facturación de un cliente que no está configurado en el sistema.|[Configurar clientes de efectivo](finance-how-to-set-up-cash-customers.md)|
| Configure los informes de intrastat y envíe el informe a una autoridad. | [Configuración y creación de informes Intrastat](finance-how-setup-report-intrastat.md)|
|Asegúrese de que un movimiento de un diario general se asigne entre cuentas diferentes, como la cantidad, el porcentaje o el importe, cuando lo registre en el diario.|[Utilizar claves de asignación en diarios generales](ui-how-use-allocation-keys-general-journals.md)|
|Configure códigos de origen y códigos de auditoría para ayudar a realizar un seguimiento de pistas de auditoría.|[Configuración de códigos de origen y códigos de auditoría para pistas de auditoría](finance-setup-trail-codes.md)|
|Especifique informes predeterminados que se utilizarán para diferentes tipos de documentos.|[Selección de informes en Business Central](across-report-selections.md)|

> [!TIP]
> Según su ubicación geográfica, algunas páginas de Business Central pueden contener campos que no se describen en los productos que están en la lista de arriba porque se aplican a funciones o personalizaciones locales. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Consulte también .

[Finanzas](finance.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
