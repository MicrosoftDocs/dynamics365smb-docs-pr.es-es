---
title: Configurar el plan de cuentas (contiene vídeo)
description: El plan de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros. Puede cambiar las cuentas predeterminadas en el plan de cuentas y puede agregar nuevas cuentas.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: 57dadabe2e96654a919127f17fcc6391786eb90f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533622"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Configurar o cambiar el plan de cuentas

El plan de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.
Sin embargo, puede cambiar las cuentas predeterminadas y puede agregar nuevas cuentas.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Agregar o cambiar cuentas

Desde el plan de cuentas, puede abrir cada cuenta de contabilidad y agregar o cambiar la configuración. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Si es necesario, puede utilizar más de una línea para un nombre de cuenta de contabilidad. En la página **Ficha cuenta**, en el grupo **Cuenta**, elija **Textos adicionales** y luego complete una o más líneas con el texto que se va a copiar y el nombre de la cuenta.  

Para cuentas del tipo **Total**, deberá completar el campo **Sumatorio**. Para las cuentas **Fin Total**, éste lo rellena automáticamente la función Aplicar sangría. Una vez que haya configurado todas las cuentas, elija la acción **Proceso** y luego elija **Test plan de cuentas**.  

> [!IMPORTANT]
> Si ha escrito definiciones en los campos **Sumatorio** referentes a las cuentas **Fin-Total** antes de ejecutar la función Indentar, deberá volver a escribirlas, ya que esta función sobrescribe los valores de todos los campos **Fin-Total**.

## <a name="delete-accounts"></a>Eliminar cuentas

Puede eliminar una cuenta contable. Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:  

* El saldo de la cuenta debe ser cero.  
* El campo **Permite borrar ctas. anteriores a** se debe configurar en la página **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.  
* Si se selecciona el campo **Chequear uso ctas. cont.** en la página **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.  

[!INCLUDE[prod_short](includes/prod_short.md)] impedirá que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el plan de cuentas.  

## <a name="block-deletion-of-gl-accounts"></a>Bloquear eliminación de cuentas de contabilidad

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

El lanzamiento de versiones 2 de 2022 introduce una protección adicional contra la eliminación accidental de cuentas contabilidad, incluso en los escenarios en los que se cumplen los criterios.  

Un nuevo campo, **Bloquear eliminación de cuentas de contabilidad**, se agrega a la página **Configuración de contabilidad**. El campo actúa como una validación adicional cuando un usuario intenta eliminar una cuenta donde hay movimientos contables posteriores a la fecha especificada en el campo **Comprobar eliminación de cuenta después de**.

Cuando el campo **Bloquear eliminación de cuentas de contabilidad** se establece en *Sí*, no puede eliminar cuentas que tengan movimientos después de la fecha en el campo **Comprobar eliminación de cuenta después de**. Para eliminar esta cuenta, un usuario con acceso a la página **Configuración de contabilidad** debe establecer primero este campo en *No*. La cuenta se puede eliminar.  

Recomendamos establecer el campo **Bloquear eliminación de cuentas de contabilidad** en *Sí*. También le recomendamos que siempre tengas una fecha fijada en el campo **Comprobar eliminación de cuenta después de**, como el tiempo que debe almacenar sus datos financieros.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/chart-accounts-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a>Consulte también

[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Trabajar con esquemas de cuentas](bi-how-work-account-schedule.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cerrar cuentas de regularización en la versión francesa](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Imprimir balances de ingresos en la versión australiana](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Imprimir balances de ingresos en la versión neozelandesa](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Configuración y asiento de la regularización en la versión en español](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Efectuar el test y la validación del plan de cuentas en la versión en español](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
