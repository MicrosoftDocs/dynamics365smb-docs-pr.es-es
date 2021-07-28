---
title: Descripción de contabilidad y plan de cuentas
description: Describe la contabilidad, el plan de cuentas y las categorías de cuentas. Utilice la página Configuración contabilidad para especificar la gestión de asuntos de contabilidad en su empresa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 8590571283ae810d442d514e6968c1feb9865cd8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "6321119"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a>Descripción de contabilidad y plan de cuentas

La contabilidad almacena sus datos financieros y el plan de cuentas muestra las cuentas donde se registran todos los movimientos contables. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Configuración de contabilidad y grupos contables

La configuración de la contabilidad es en la base de los procesos financieros porque define cómo se registran los datos.  

En la página **Configuración contabilidad** especifique cómo gestionar determinados asuntos de contabilidad en su empresa, como:  

* Detalles de redondeo de factura  
* Formatos de dirección  
* Informes financieros  

De manera similar, en la página **Configuración grupos contables**, puede especificar cómo desea configurar las combinaciones generales del negocio y los grupos contables de producto. Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. Rellene una línea por cada combinación de grupo contable de negocio y de producto. Para obtener más información, consulte [Configuraciones de grupos de registro](finance-posting-groups.md).  

> [!TIP]
> La página **Configuración de contabilidad:** incluye campos genéricos y campos que son específicos de su país o región. Si no está seguro del significado de un campo, le sugerimos que trabaje con su contable para determinar si es relevante para su organización.  

## <a name="the-chart-of-accounts"></a>Plan de cuentas

El plan de cuentas muestra todas las cuentas de contabilidad. Desde el plan de cuentas, puede realizar acciones como las siguientes:  

* Ver informes que muestran movimientos de contabilidad y saldos.  
* Cerrar el asiento de regularización.  
* Abrir la ficha de cuenta para agregar o cambiar la configuración.  
* Ver una lista de grupos contables que registran en dicha cuenta.
* Para ver los saldos del Debe y el Haber de una sola cuenta  

Puede agregar, cambiar o eliminar cuentas de contabilidad. Sin embargo, para evitar discrepancias, no puede eliminar una cuenta de contabilidad si sus datos se utilizan en el plan de cuentas.  

## <a name="account-categories"></a>Categorías de cuenta

Puede personalizar la estructura de los informes financieros con la asignación de las cuentas de contabilidad a las categorías de cuenta.  

La página **Categorías de cuenta** muestra las categorías y subcategorías, y las cuentas que asignó a cada categoría. Puede crear nuevas subcategorías y asignarlas a las cuentas existentes.  

Puede crear un grupo de categorías marcando otras subcategorías debajo de una línea en la página **Categorías de cuenta**. Esto le facilita la obtención de una descripción general, porque cada agrupación muestra un balance total. Por ejemplo, puede crear las subcategorías para distintos tipos de activos y a continuación crear grupos de categorías para los activos fijos y los activos circulantes.  

Puede especificar si las cuentas de cada categoría deben incluirse en los tipos específicos de informes. Las categorías de cuentas ayudan a definir el diseño de sus balances financieros.  

### <a name="example"></a>Ejemplo:

Por ejemplo, el extracto de saldo predeterminado tiene una subcategoría para *Efectivo* en *Activos fijos*. Usted desea que el extracto de saldo tenga en cuenta el efectivo pequeño y la cuenta corriente. Por tanto, sigue estos pasos:  

1. Agregar dos nuevas subcategorías:

    * Una para el efectivo pequeño  
    * Una para su cuenta corriente  
2. Especifique la definición de informe adicional **Cuentas de efectivo** de estas subcategorías.  
3. Aplique sangría en la subcategoría **Efectivo**.  

La próxima vez que genere los esquemas de cuentas, su extracto de saldo mostrará un extracto total de efectivo y dos líneas con extractos para efectivo pequeño y cuenta corriente.  

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Acceso para crear y editar cuentas y categorías de cuentas

En una organización pequeña, como la empresa de demostración CRONUS, la mayoría de los usuarios pueden editar el plan de cuentas, excepto los usuarios con una licencia de TEAM MEMBER. Sin embargo, en organizaciones más grandes, el acceso para editar el plan de cuentas está limitado por roles y permisos. Si es administrador o tiene el rol *Administrador de negocio* o *Contable*, puede verificar los permisos de todos los usuarios para asegurarse de que las personas adecuadas tengan acceso a las tablas relevantes. Para obtener más información, consulte [Para obtener un resumen de los permisos de un usuario](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md)  
[Inteligencia empresarial](bi.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]