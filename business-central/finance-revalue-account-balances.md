---
title: Revalorizar saldos de contabilidad general
description: Aprenda a revalorizarlos saldos de contabilidad general antes de producir sus estados financieros.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# <a name="revalue-general-ledger-account-balances"></a>Revalorizar saldos de contabilidad general

Si utiliza cuentas de contabilidad general (CG) para registrar partidas del balance en divisas extranjeras, debe revalorizar los saldos de las cuentas antes de generar estados financieros. Los tipos de cambio de divisas cambian con frecuencia y la revalorización ayuda a que sus estados financieros sean más precisos.

## <a name="set-up-revaluations"></a>Configurar revalorizaciones

Usted configura cada cuenta que desea incluir en las revalorizaciones en la página **Ficha cuenta**. Puede seleccionar si desea contabilizar ajustes de revalorización en cuentas de pérdidas/ganancias realizadas o no realizadas. La contabilización de ganancias y pérdidas durante un ajuste del tipo de cambio de moneda sigue la rutina de contabilización normal. Por ejemplo, lo hace para cada configuración en la página  **Divisas**. Para obtener más información sobre los ajustes del tipo de cambio, vaya a [Actualizar tipos de cambio de divisa](finance-how-update-currencies.md).

Para minimizar errores, en el campo **Registro divisa origen**, puede configurar una validación para las divisas que desea permitir que se contabilicen en cuentas de contabilidad individuales:

* Todas divisas (en blanco)
* Varias divisas
* Misma divisa
* Divisa local

## <a name="run-a-revaluation"></a>Ejecutar una revalorización

Para revalorizar los importes en divisa extranjera en moneda local para los saldos de cuentas del contabilidad, en la página **Plan de cuentas**, use la acción **Revalorización divisa contable** para iniciar un trabajo por lotes. El trabajo por lotes crea entradas de ajuste en el diario que seleccione. Cuando registra las entradas, ajusta el saldo en moneda local (ML) de la cuenta. Los saldos de cuentas de contabilidad que siempre se muestran en ML ahora reflejan cambios en las monedas en las que se registraron los asientos. Esta revalorización le permite producir un estado financiero más preciso con menos esfuerzo.

Si utiliza una moneda de informe adicional (DA), los asientos de revaluación del contabilidad tienen un importe DA. El importe solo corresponde al importe ML en estas entradas, no al saldo DA en la cuenta de contabilidad. Si ajusta las tasas DA después de registrar los ajustes, ejecute el ajuste del tipo de cambio de moneda una vez más para ajustar todas las entradas de contabilidad.

> [!IMPORTANT]
> Es posible que la revaloración de la cuenta de contabilidad no cumpla con todos los requisitos para los registros de transacciones y activos que necesitan revalorización. Por ejemplo, para instrumentos financieros, valores, activos arrendados, o si los utiliza para volúmenes específicos o grandes de transacciones o activos. Le recomendamos que analice con su auditor si puede utilizar la función y, de ser así, cómo debe utilizarla. Por ejemplo, si permite que se mezclen monedas para una cuenta o si necesita mantener una cuenta separada para cada activo del que desea realizar un seguimiento.

> [!NOTE]
> La revalorización no brinda la posibilidad de aplicar o cancelar asientos, como se puede hacer con los asientos contables de clientes y proveedores. Los ajustes se realizan según el saldo por moneda.

## <a name="revaluate-accounts-vs-customer-and-vendor-exchange-rate-adjustments"></a>Revalorizar cuentas versus ajustes de tipo de cambio de clientes y proveedores

La revalorización simplifica la tarea de ajustar los saldos de las cuentas de contabilidad general. La característica revaloriza el saldo por divisa por cuenta de contabilidad de manera muy similar a como lo hace para los ajustes en las cuentas de contabilidad que están vinculadas a cuentas bancarias. Si utiliza una cuenta de contabilidad para realizar un seguimiento de varios activos, considere utilizar una cuenta de proveedor o de cliente.

> [!NOTE]
> Es posible que la revaloración de la cuenta de contabilidad no cumpla con todos los requisitos para los registros de transacciones y activos que necesitan revalorización. Por ejemplo, para instrumentos financieros, valores, activos arrendados, o si los utiliza para volúmenes específicos o grandes de transacciones o activos. Le recomendamos que analice con su auditor si puede utilizar la función y, de ser así, cómo debe utilizarla. Por ejemplo, si permite que se mezclen monedas para una cuenta o si necesita mantener una cuenta separada para cada activo del que desea realizar un seguimiento.

Los siguientes ejemplos ilustran la diferencia entre usar una cuenta de contabilidad y usar una cuenta de proveedor para rastrear el saldo de dos activos monetarios que usan una divisa extranjera.

**Usar una cuenta de contabilidad** Si está utilizando una cuenta de contabilidad para realizar un seguimiento de varios activos (por ejemplo, préstamos o activos fijos) en la misma divisa o transacciones parciales individuales para el mismo activo pero aún en la misma divisa, la revaluación de contabilidad realiza una entrada por revalorización de la moneda. Esto significa que no puede realizar un seguimiento de los ajustes relacionados con activos individuales o transacciones individuales para el mismo activo.

**Usar una cuenta de proveedor** Si configura varios activos como proveedores y les contabiliza transacciones, ya sea en la misma divisa o en diferentes divisas, obtendrá un ajuste por divisa y por proveedor. O, si activa el conmutador **Publicación por entrada** en la entrada de la cola de trabajo **Ajustar el tipo de cambio de moneda**, obtendrá una entrada de ajuste para cada entrada separada del libro de contabilidad de proveedores.

Esta diferencia es importante cuando evalúa si la revaloración de contabilidad es la característica adecuada para sus necesidades de informes.

> [!TIP]
> Le recomendamos que pregunte a su contable o auditor qué tipo de cuenta es mejor para su negocio. Además, podría haber una aplicación para [!INCLUDE [prod_short](includes/prod_short.md)] en [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) que es perfecta para sus escenarios comerciales.

## <a name="see-also"></a>Consulte también

[Revisar importes en cuentas del libro mayor](finance-review-accounts.md)  
[Descripción de contabilidad y plan de cuentas](finance-general-ledger.md)  
