---
title: Descripción de contabilidad y plan de cuentas
description: Describe la contabilidad, el plan de cuentas y las categorías de cuentas. Utilice la página Configuración contabilidad para especificar la gestión de asuntos de contabilidad en su empresa.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 08/23/2022
ms.author: edupont
ms.openlocfilehash: 1d246e342d286e75da5aacaf1e6a305c5d0559e4
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534648"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Descripción de contabilidad y plan de cuentas

El libro mayor almacena sus datos financieros. El plan contable muestra las cuentas donde se registran los movimientos de contabilidad general. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Configuración de contabilidad y grupos contables

La configuración de la contabilidad es en la base de los procesos financieros porque define cómo se registran los datos. Dos páginas desempeñan un papel importante en la configuración de sus procesos financieros:  

* La página **Configuración contabilidad**

  En la página **Configuración contabilidad** especifique cómo gestionar determinados asuntos de contabilidad en su empresa, como:  

  * Detalles de redondeo de factura  
  * Formatos de dirección  
  * Informes financieros  

  > [!TIP]
  > La página **Configuración de contabilidad:** incluye campos genéricos y campos que son específicos de su país o región. Si no está seguro del significado de un campo, le sugerimos que trabaje con su contable para determinar si es relevante para su organización. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    Abra la página [aquí](https://businesscentral.dynamics.com/?page=118)
* La página **Configuración grupos contables**

    De manera similar, en la página **Configuración grupos contables**, puede especificar cómo desea configurar las combinaciones generales del negocio y los grupos contables de producto. Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. Rellene una línea por cada combinación de grupo contable de negocio y de producto. Pero también puede abrir cada línea en su propia tarjeta de configuración de registro. Para obtener más información, consulte [Configuraciones de grupos de registro](finance-posting-groups.md).  

    > [!TIP]
    > Si no puede ver los campos que está buscando en la página **Configuración grupos contables**, utilice la barra de desplazamiento horizontal situada en la parte inferior de la página para desplazarse hacia la derecha.  

    Abra la página [aquí](https://businesscentral.dynamics.com/?page=314)

## <a name="the-chart-of-accounts"></a>Plan de cuentas

El plan de cuentas muestra todas las cuentas de contabilidad. Desde el plan de cuentas, puede realizar acciones como las siguientes:  

* Ver informes que muestran movimientos de contabilidad y saldos.  
* Cerrar el asiento de regularización.  
* Abrir la ficha de la cuenta de contabilidad general (CG) para agregar o cambiar la configuración.  
* Ver una lista de grupos contables que registran en dicha cuenta.
* Para ver los saldos del Debe y el Haber de una sola cuenta  

Puede agregar, cambiar o eliminar cuentas de contabilidad. Sin embargo, para evitar discrepancias, no puede eliminar una cuenta de contabilidad si sus datos se utilizan en el plan de cuentas. Para evitar errores en períodos sensibles, también puede bloquear la eliminación de cuentas. Para obtener más información, consulte [Eliminar cuentas](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="account-categories"></a>Categorías de cuenta

Puede personalizar la estructura de los informes financieros con la asignación de las cuentas de contabilidad a las categorías de cuenta.  

La página **Categorías de cuenta** muestra las categorías y subcategorías, y las cuentas de contabilidad general que asignó a cada categoría. Puede crear nuevas subcategorías y asignarlas a las cuentas existentes.  

Puede crear un grupo de categorías marcando otras subcategorías debajo de una línea en la página **Categorías de cuenta**. Los grupos de categorías facilitan la obtención de una descripción general, porque cada agrupación muestra un balance total. Por ejemplo, puede crear las subcategorías para distintos tipos de activos y a continuación crear grupos de categorías para los activos fijos y los activos circulantes.  

Puede especificar si las cuentas de cada categoría deben incluirse en los tipos específicos de informes. Las categorías de cuentas ayudan a definir el diseño de sus balances financieros.  

### <a name="example"></a>Ejemplo:

Por ejemplo, el extracto de saldo predeterminado tiene una subcategoría para *Efectivo* en *Activos fijos*. Usted desea que el extracto de saldo tenga en cuenta el efectivo pequeño y la cuenta corriente. Por tanto, sigue estos pasos:  

1. Agregar dos nuevas subcategorías:

    * Una para el efectivo pequeño  
    * Una para su cuenta corriente  
2. Especifique otra definición de informe **Cuentas de efectivo** de estas subcategorías.  
3. Aplique sangría en la subcategoría **Efectivo**.  

La próxima vez que genere esquemas de cuenta, su estado de cuenta mostrará las siguientes líneas:

* Saldo total en efectivo.
* Líneas con saldos de caja chica y la cuenta corriente.  

> [!NOTE]
> Si crea una cuenta de mayor sin asignar una categoría de cuenta, cuando asigne la cuenta a un grupo contable [!INCLUDE[prod_short](includes/prod_short.md)] asigna automáticamente la categoría de cuenta de la cuenta de mayor inmediatamente encima de la cuenta en su catálogo de cuentas. Sin embargo, para incluir la nueva cuenta en sus informes financieros, debe elegir la acción **Generar informes financieros** sobre la página **Categorías de cuentas del libro mayor**. Como alternativa, puede abrir la página Tarjeta de cuenta del L/M, especificar la categoría de la cuenta y luego volver a generar su informe financiero.

## <a name="get-a-quick-overview"></a>Obtener una descripción general rápida

La página **Plan de cuentas** muestra las cuentas en una lista jerárquica que ofrece acceso rápido a la información clave de cada cuenta. Sin embargo, la lista es estática. Si tiene muchas cuentas, es posible que deba desplazarse para ver diferentes cuentas. Si solo desea una descripción general rápida de los conceptos básicos, como cambios netos y saldos, la página **Introducción al plan de cuentas** es una alternativa útil. El diseño de columnas en la página ahora es el mismo que encontrará en la página **Catálogo de cuentas** (aunque con menos columnas), por lo que no tendrá que reorientarse. Puede expandir o contraer los niveles jerárquicos para condensar la vista. Para facilitar el cambio entre las páginas, la página **Introducción al plan de cuentas** está disponible en la página del **Plan de cuentas**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Acceso para crear y editar cuentas y categorías de cuentas

En una organización pequeña, como la empresa de demostración CRONUS, la mayoría de los usuarios pueden editar el plan de cuentas. Excepto usuarios con licencia TEAM MEMBER. Sin embargo, en organizaciones más grandes normalmente los roles de usuario y los permisos limitan el acceso para editar el plan de cuentas. Si es administrador o tiene el rol **Administrador de negocio** o **Contable**, puede controlar los permisos de usuario para dar a las personas adecuadas acceso a las tablas relevantes. Para obtener más información, consulte [Para obtener un resumen de los permisos de un usuario](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/business-central-configure-general-ledger-setup/) relacionada

## <a name="see-also"></a>Consulte también .

[Finanzas](finance.md)  
[Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md)  
[Inteligencia empresarial](bi.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
