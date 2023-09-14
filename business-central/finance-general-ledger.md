---
title: Descripción de contabilidad y plan de cuentas
description: 'Describe la contabilidad, el plan de cuentas y las categorías de cuentas. Utilice la página Configuración contabilidad para especificar la gestión de asuntos de contabilidad en su empresa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/24/2022
ms.author: bholtorf
---
# Descripción de contabilidad y plan de cuentas

La contabilidad (G/L) almacena sus datos financieros y el plan de cuentas (COA) muestra las cuentas donde se registran todos los movimientos contables. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.

## Configuración de contabilidad y grupos contables

La configuración de la contabilidad es en la base de los procesos financieros porque define cómo se registran los datos. Dos páginas en concreto desempeñan un papel importante en la configuración de sus procesos financieros:  

* La página **Configuración contabilidad**

  En la página **Configuración contabilidad** especifique cómo gestionar determinados asuntos de contabilidad en su empresa, como:  

  * Detalles de redondeo de factura  
  * Formatos de dirección  
  * Informes financieros

  > [!TIP]
  > La página **Configuración de contabilidad:** incluye campos genéricos y campos que son específicos de su país o región. Si no está seguro del significado de un campo, le sugerimos que trabaje con su contable para determinar si es relevante para su organización. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Abra la página [aquí](https://businesscentral.dynamics.com/?page=118)
  
* La página **Configuración grupos contables**

  De manera similar, en la página **Configuración grupos contables**, puede especificar cómo desea configurar las combinaciones generales del negocio y los grupos contables de producto. Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. Rellene una línea por cada combinación de grupo contable de negocio y de producto. Pero también puede abrir cada línea en su propia tarjeta de configuración de registro. Obtenga más información en [Configuraciones de grupos contables](finance-posting-groups.md).  

  > [!TIP]
  > Si no puede ver los campos que está buscando en la página **Configuración grupos contables**, utilice la barra de desplazamiento horizontal situada en la parte inferior de la página para desplazarse hacia la derecha.  

  Abra la página [aquí](https://businesscentral.dynamics.com/?page=314).

## Plan de cuentas

El plan de cuentas muestra todas las cuentas de contabilidad. Desde el plan de cuentas, puede realizar acciones como las siguientes:  

* Ver informes que muestran movimientos de contabilidad y saldos.  
* Cerrar el asiento de regularización.  
* Abrir la ficha de la cuenta de contabilidad general (CG) para agregar o cambiar la configuración.  
* Ver una lista de grupos contables para dicha cuenta.
* Para ver los saldos del Debe y el Haber de una sola cuenta.

Puede agregar, cambiar o eliminar cuentas de contabilidad. Sin embargo, para evitar discrepancias, no puede eliminar una cuenta de contabilidad si sus datos se utilizan en el plan de cuentas. Además, a partir del lanzamiento de versiones 2 de 2022, también puede bloquear la eliminación accidental de cuentas en períodos sensibles. Obtenga más información en la sección [Eliminar cuentas](finance-setup-chart-accounts.md#delete-accounts).  

## Categorías de cuenta

Puede personalizar la estructura de los informes financieros con la asignación de las cuentas de contabilidad a las categorías de cuenta.  

La página **Categorías de cuenta** muestra las categorías y subcategorías, y las cuentas de contabilidad general que se asignó a cada categoría. Puede crear nuevas subcategorías y asignarlas a las cuentas existentes.  

Puede crear un grupo de categorías marcando otras subcategorías debajo de una línea en la página **Categorías de cuenta**. Los grupos de categorías facilitan la obtención de una descripción general, porque cada agrupación muestra un balance total. Por ejemplo, puede crear las subcategorías para distintos tipos de activos y a continuación crear grupos de categorías para los activos fijos y los activos circulantes.  

Puede defnir si los tipos de informes específicos deben incluir las cuentas de cada subcategoría. Las categorías de cuentas ayudan a definir el diseño de sus balances financieros.  

### Ejemplo:

Por ejemplo, el extracto de saldo predeterminado tiene una subcategoría para *Efectivo* en *Activos fijos*. Si desea que el extracto de saldo tenga en cuenta el efectivo pequeño y la cuenta corriente, necesita realizar estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Categorías de cuenta de contabilidad** y luego elija el enlace relacionado.
   1. Alternativamente, [abra la página aquí](https://businesscentral.dynamics.com/?page=790).
2. Seleccione la acción **Editar lista**.
3. Agregue dos subcategorías nuevas: una para el efectivo pequeño y otra para su cuenta corriente:
   1. Seleccione la categoría **Activos circulantes**.
   2. Seleccione la acción **Nuevo**.
   3. Introduzca el nombre de la subcategoría en el campo **Descripción**.
   4. En el campo **Cuentas de mayor en categoría**, seleccione la cuenta de mayor adecuada.
   5. En el campo **Definición de informe adicional**, seleccione la opción **Cuentas de efectivo**.
4. Aplique sangría en la subcategoría **Efectivo**.
   1. Seleccione la subcategoría creada en el paso 3.
   2. Seleccione la acción **Sangría**.
   3. Seleccione la acción **Bajar**.
   4. Elija la acción **Sangrar** para aplicar una sangría bajo la subcategoría **Efectivo**.

Cuando elige la acción **Generar informes financieros**, o la próxima vez que se genere el informe, su estado de cuenta mostrará las siguientes líneas:

* Saldo total en efectivo.
* Líneas con saldos de caja chica y la cuenta corriente.  

> [!NOTE]
> Si crea una cuenta de mayor sin asignar una categoría de cuenta, cuando asigne la cuenta a un grupo contable [!INCLUDE[prod_short](includes/prod_short.md)] asigna automáticamente la categoría de cuenta de la cuenta de mayor inmediatamente encima de la cuenta en su catálogo de cuentas. Sin embargo, para incluir la nueva cuenta en sus informes financieros, debe elegir la acción **Generar informes financieros** sobre la página **Categorías de cuentas del libro mayor**. Como alternativa, puede abrir la página Tarjeta de cuenta del L/M, especificar la categoría de la cuenta y luego volver a generar su informe financiero.

## Obtener una descripción general rápida

La página **Plan de cuentas** muestra las cuentas en una lista jerárquica que ofrece acceso rápido a la información clave de cada cuenta. Sin embargo, la lista es estática y, si tiene muchas cuentas, es posible que deba desplazarse para ver la información de diferentes cuentas. Si solo desea una descripción general rápida de los conceptos básicos, como cambios netos y saldos, la página **Introducción al plan de cuentas** es una alternativa útil. El diseño de columnas en la página ahora es el mismo que encontrará en la página **Catálogo de cuentas** (aunque con menos columnas), por lo que no tendrá que reorientarse. Puede expandir o contraer los niveles jerárquicos para condensar la vista. Para facilitar el cambio entre las páginas, la página **Introducción al plan de cuentas** está disponible en la página del **Plan de cuentas**.

## Acceso para crear y editar cuentas y categorías de cuentas

En una organización pequeña, como la empresa de demostración CRONUS, la mayoría de los usuarios pueden editar el plan de cuentas, excepto los usuarios con una licencia de TEAM MEMBER. Sin embargo, en organizaciones más grandes normalmente los roles de usuario y los permisos limitan el acceso para editar el plan de cuentas. Si es administrador o tiene el rol *Administrador de negocio* o *Contable*, puede controlar los permisos de usuario para dar a las personas adecuadas acceso a las tablas relevantes. Más información en la sección [Para obtener un resumen de los permisos de un usuario](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## Consultar la [formación de Microsoft](/training/modules/business-central-configure-general-ledger-setup/) relacionada

## Consulte también .

[Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
