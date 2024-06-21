---
title: Contabilidad y auditoría
description: Este artículo proporciona información que le ayudará a usar Microsoft Dynamics 365 Business Central para realizar correctamente la contabilidad y las auditorías de su empresa.
author: altotovi
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'accounting, bookkeeping'
ms.search.form: '16, 39, 108'
ms.date: 03/14/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Contabilidad y auditoría

La contabilidad es una función crítica en cualquier solución de planificación de recursos empresariales (ERP), y también en la mayoría de las empresas. La contabilidad representa el proceso de registrar y catalogar las transacciones financieras de una empresa, y luego recuperar, medir, resumir y presentar los resultados mediante el uso de diferentes informes que a menudo exige la legislación local. El objetivo principal de este proceso es ayudar a la gerencia de la empresa a comprender las finanzas del negocio y medir los resultados de las actividades económicas de la empresa.

La auditoría es una parte del proceso contable e implica el registro regular de todas las transacciones financieras de una empresa. [!INCLUDE[prod_short](includes/prod_short.md)] es un sistema ERP que incluye herramientas integradas para facilitar la auditoría en el sistema. Muchas acciones se pueden hacer manualmente.

Este artículo proporciona un resumen de los procesos de auditoría, incluidas las reglas, los procedimientos y otras pautas en [!INCLUDE[prod_short](includes/prod_short.md)]. El contenido de este artículo está destinado a ayudar a los contables y auditores a completar su trabajo diario en este sistema ERP. Para obtener ayuda adicional, se incorpora un asistente basado en contexto en [!INCLUDE[prod_short](includes/prod_short.md)]. Este asistente contiene vínculos a información relacionada con la página actual e instrucciones para trabajar con el proceso correspondiente. Para acceder a él, seleccione el botón [**Ayuda**](product-help-and-support.md) en la esquina superior derecha para abrir el panel **Ayuda** . A continuación, utilice los vínculos en las secciones **Acerca de esta tarea o página** y **Recursos relacionados de Microsoft Learn**.

El siguiente vídeo presenta algunas de las capacidades clave para la contabilidad y las auditorías.

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.

| Tarea | Artículo |
|------|---------|
| Vea o edite las cuentas de contabilidad en las que se registran todos los movimientos de contabilidad. | [Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md) |
| Especifique cómo desea que le paguen los clientes y cómo desea pagar a sus proveedores. | [Configurar formas de pago](finance-payment-methods.md) |
| Especifique los términos de pago para administrar las fechas de vencimiento y calcular posibles descuentos en el pago. | [Configurar términos de pago](finance-payment-terms.md) |
| Especifique los grupos contables que asignan entidades (como clientes, proveedores, productos, recursos y documentos de venta y compra) a cuentas contables. | [Configurar grupos de registro](finance-posting-groups.md)|
| Cree informes financieros y defina las categorías de cuentas que determinan el contenido de los gráficos e informes financieros, como los informes **Saldo** y **Extracto de ingresos**. | [Preparar Financial Reporting con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)|
| Configure una tolerancia que el sistema use para cerrar una factura aunque el pago, incluido el descuento, no cubra totalmente el importe de la factura. | [Trabajar con tolerancias de pago y tolerancias de descuentos de pago](finance-payment-tolerance-and-payment-discount-tolerance.md) |
| Configure los periodos fiscales. | [Trabajar con periodos contables y ejercicios](finance-accounting-periods-and-fiscal-years.md) |
| Configure términos de la factura que recuerden al cliente que debe pagar. | [Configurar términos, niveles y textos de recordatorios.](finance-setup-reminders.md)|
| Defina cómo informa a las autoridades fiscales de los importes del impuesto de valor añadido (IVA) que ha recaudado sobre las ventas. | [Configurar impuesto sobre valor añadido (IVA)](finance-setup-vat.md) |
| Determine cómo va a gestionar el IVA no realizado en conexión con los métodos contables basados en efectivo. | [Configurar el IVA no realizado para la contabilidad basada en efectivo](finance-setup-unrealized-vat.md) |
| Defina las divisas extranjeras con las que opera o notifica transacciones. | [Configuración de divisas](finance-set-up-currencies.md) |
| Configure sus características de ventas y compras para manejar pagos en divisas extranjeras. | [Permitir la liquidación de movimientos en distintas divisas](finance-how-enable-application-ledger-entries-different-currencies.md) |
| Defina una o varias divisas adicionales para que los importes se notifiquen automáticamente tanto en divisa local (LCY) como en una divisa de informe adicional en cada movimiento de contabilidad y en otros movimientos. | [Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md) |
| Ajuste periódicamente los equivalentes de divisa adicionales para compensar tipos de cambio que fluctúan. | [Actualizar tipos de cambio de divisa](finance-how-update-currencies.md)|
| Defina varias tasas de interés para diferentes períodos de pagos retrasados en las transacciones comerciales. | [Configurar múltiples tipos de interés](finance-how-to-set-up-multiple-interest-rates.md) |
| Haga que los importes se redondeen automáticamente a medida que se crean las facturas. | [Configurar redondeo de factura](finance-set-up-invoice-rounding.md) |
| Agregue nuevas cuentas al plan de cuentas existente (COA). | [Configuración del plan contable](finance-setup-chart-accounts.md) |
| Configure gráficos de inteligencia empresarial (BI) para analizar el flujo de efectivo. | [Configuración del análisis de flujo de efectivo](finance-setup-cash-flow-analyses.md) |
| Permita que se creen facturas para los clientes que no están en el sistema. | [Configurar clientes de efectivo](finance-how-to-set-up-cash-customers.md) |
| Configure los informes de intrastat y envíe el informe a una autoridad. | [Configuración y creación de informes Intrastat](finance-how-setup-report-intrastat.md) |
| Asegúrese de que un movimiento de un diario general se asigne entre cuentas diferentes, como la cantidad, el porcentaje o el importe, cuando lo registre en el diario. | [Utilizar claves de asignación en diarios generales](ui-how-use-allocation-keys-general-journals.md) |
| Configure códigos de origen y códigos de auditoría para realizar un seguimiento de pistas de auditoría. | [Configuración de códigos de origen y códigos de auditoría para pistas de auditoría](finance-setup-trail-codes.md) |
| Especifique los informes predeterminados que se utilizarán para diferentes tipos de documentos. | [Selección de informes en Business Central](across-report-selections.md) |
| Liquide pagos entrantes, concilie cuentas bancarias durante la liquidación de pagos y recopile saldos pendientes. | [Administrar cobros](receivables-manage-receivables.md) |
| Efectúe pagos, liquide pagos salientes y trabaje con cheques. | [Administrar pagos](payables-manage-payables.md) |
| Pida a sus clientes que envíen el pago antes del envío, o envíe el pago a sus proveedores antes de que realicen el envío. | [Facturación de prepagos](finance-invoice-prepayments.md) |
| Concilie y transfiera fondos entre cuentas bancarias. | [Conciliar bancos](bank-manage-bank-accounts.md) |
| Configure los socios de empresas vinculadas y procese transacciones, manual o automáticamente, entre las entidades jurídicas dentro de la misma empresa. | [Gestión de transacciones entre empresas vinculadas](intercompany-manage.md) |
| Analice los costes de administrar su empresa asignando costes reales y presupuestados de operaciones, departamentos, productos y proyectos a los centros de costes. | [Contabilidad para costes](finance-manage-cost-accounting.md) |
| Administre los costes de inventario y fabricación, y notifique costes y concílielos con la contabilidad. | [Gestión de costes de inventario](finance-manage-inventory-costs.md) |
| Administre y reporte entradas y salidas de efectivo. | [Información general del flujo de efectivo]( finance-cash-flow-overview.md) |
| Supervise el flujo de efectivo de entrada y salida de su empresa. | [Analizar los flujos de efectivo de la empresa](finance-analyze-cash-flow.md) |
| Siga un proceso de extremo a extremo que use los informes financieros para hacer pronósticos de flujo de efectivo. | [Elaboración de previsiones del flujo de efectivo con informes financieros](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Obtenga información sobre la contabilidad general y los planes de cuentas. | [Descripción de contabilidad y plan de cuentas](finance-general-ledger.md) |
| Combine movimientos de contabilidad de varias empresas en una empresa consolidada virtual para el análisis financiero. | [Consolidar los datos financieros de varias empresas](finance-consolidated-company-reporting.md)|
| Agregue dimensiones para la inteligencia empresarial más completa. | [Trabajar con dimensiones](finance-dimensions.md) |
| Cree presupuestos contables para prever diferentes actividades financieras y asigne dimensiones para fines de inteligencia empresarial. | [Crear presupuestos contables](finance-how-create-budgets.md) |
| Registre los ingresos y los gastos directamente en la contabilidad sin registrar documentos empresariales dedicados. | [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md) |
| Revierta movimientos para deshacer registros de valor en el diario general o registros de cantidad en documentos de compra y ventas. | [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md) |
| Asignar un movimiento en un diario general a varias cuentas al registrar el diario. | [Asignar costes e ingresos](year-allocate-costs-income.md) |
| Asigne costes adicionales, como el flete o los gastos de manipulación física que se producen durante las operaciones comerciales, a los productos relacionados. El coste se refleja en la valoración del inventario. | [Usar los cargos de productos a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md) |
| Registre gastos de los empleados por actividades relacionadas con el trabajo y realice reembolsos directamente en las cuentas bancarias de los empleados. | [Registrar y reembolsar los costes de los empleados](finance-how-record-reimburse-employee-expenses.md) |
| Asigne ingresos y gastos a periodos diferentes a los de la fecha en que se registraron las transacciones. | [Fraccionar ingresos y gastos](finance-how-defer-revenue-expenses.md) |
| Conozca las opciones disponibles para enviar facturas de suscripción automáticamente a clientes y registre ingresos periódicos. | [Trabajar con ingresos recurrentes](finance-recurring-invoicing.md) |
| Use divisas adicionales y actualice automáticamente los tipos de cambio. | [Actualizar tipos de cambio de divisa](finance-how-update-currencies.md) |
| Importe transacciones de salario del proveedor de nóminas en el libro mayor. | [Importar transacciones de nómina](finance-how-import-payroll-transactions.md) |
| Calcule el IVA en las transacciones de ventas y compras para que pueda informar de los importes a las autoridades fiscales. | [Trabajar con el IVA por ventas y compras](finance-work-with-vat.md) |
| Prepare un informe que genere una lista del IVA de las ventas y envíelo a las autoridades fiscales de la Unión Europea (UE). | [Crear informes de IVA para las autoridades fiscales](finance-how-report-vat.md) |
| Convierta manualmente los contratos de servicio para cambiar el tipo de IVA. | [Convertir contratos de servicio que incluyen importes de IVA](service-how-to-convert-service-contracts.md) |
| Trabaje con extractos financieros y resúmenes en Microsoft Excel. | [Análisis de estados financieros en Excel](finance-analyze-excel.md) |
| Use el Área de trabajo contable, interactúe con un contable externo y utilice el hub de empresa para administrar las cuentas de varios clientes. | [Experiencias contables en Business Central](finance-accounting.md) |
| Configure informes de Intrastat para proporcionar comercio con otros miembros de la UE de acuerdo con la legislación local. | [Configurar informes de Intrastat]( finance-how-setup-report-intrastat.md) |
| Rellene, valide y envíe el informe Intrastat. | [ Trabajar con informes de Intrastat]( finance-how-report-intrastat.md) |
| Configure, rellene, valide y envíe el informe de declaración de servicio para los servicios comerciales en toda la UE. | [ Configure y utilice la declaración de servicio]( finance-how-setup-use-service-declaration.md) |
| Crear activos fijos, asignar métodos de amortización, registrar adquisiciones, valores residuales e imprimir listas de activos fijos. | [Activos fijos adquiridos](fa-how-acquire.md) |
| Registrar visitas de servicio y registrar y monitorizar costes de mantenimiento. | [Mantener activos fijos](fa-how-maintain.md) |
| Actualizar información de seguros, registrar costes en pólizas de seguros, modificar la cobertura del seguro, ver estadísticas de seguros y listar pólizas de seguros. | [Aseguramiento de activos fijos](fa-how-insure.md) |
| Reclasifique activos fijos, transfiera activos fijos a distintas ubicaciones, divida o combine activos. | [Transferir, dividir o combinar activos fijos.](fa-how-trans-split-combine.md) |
| Ajuste el valor de los activos fijos, registre apreciación y transacciones de depreciación. | [Revalorizar activos fijos](fa-how-revalue.md) |
| Registre y calcule la amortización y analícela en informes de activos fijos. | [Depreciar o amortizar activos fijos](fa-how-depreciate-amortize.md) |
| Registrar transacciones de venta/baja, ver movimientos de venta/baja y registrar ventas/bajas parciales. | [Cancelar o retirar activos fijos](fa-how-dispose-retire.md) |
| Gestionar presupuestos de activos fijos, costes, ventas/bajas y amortización. | [Administrar presupuestos para activos fijos.](fa-how-manage-budgets.md) |
| Configure usuarios de flujo de trabajo de aprobación, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo. Para crear nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación. | [Configurar flujos de trabajo de aprobación](across-set-up-workflows.md) |
| Habilite flujos de trabajo de aprobación, actúe al recibir notificaciones de flujos de trabajo, (por ejemplo, la solicitud y la aprobación de un paso de flujo de trabajo) y archive y elimine flujos de trabajo. | [Usar flujos de trabajo de aprobación](across-use-workflows.md) |
| Ver importes reales comparados con importes presupuestados para todas las cuentas y durante varios periodos. | [Analizar importes reales frente a importes presupuestados](bi-how-analyze-actual-versus-budget.md) |
| Crear nuevos informes financieros para definir los balances financieros para elaborar informes o para mostrar como gráficos. | [Preparar informes financieros con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md) |
| Analice el rendimiento financiero configurando indicadores clave de rendimiento (KPI) basados en informes financieros y publíquelos como servicios web. Los KPI de informes financieros publicados se pueden ver en un sitio web o importar a Excel usando los servicios Web de OData. | [Configurar y publicar un servicio web KPI basado en informes financieros](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Configurar vistas para analizar datos usando dimensiones. | [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md) |
| Crear nuevos informes de análisis para ventas, compras y existencias, así como configurar plantillas de análisis. | [Crear informes de análisis](bi-how-create-analysis-views-reports.md) |
| Habilite la información financiera global por medio de las organizaciones internacionales de contabilidad el estándar de lenguaje de informes de negocio extensible (XBRL). | [Crear informes con XBRL](bi-create-reports-with-xbrl.md) |
| Cambie la intención de acceso a la base de datos en informes, páginas de tipo API y consultas para ayudar a reducir la carga y mejorar el rendimiento. | [Administrar intento de acceso a bases de datos](admin-data-access-intent.md) |

## Consulte también .

[Configurar las finanzas](finance-setup-finance.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Cerrar periodos fiscales](year-close-years-periods.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Importar datos de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
