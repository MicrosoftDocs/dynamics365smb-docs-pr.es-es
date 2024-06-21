---
title: Descripción de contabilidad y plan de cuentas
description: 'Describe la contabilidad, el plan de cuentas y las categorías de cuentas. Utilice la página Configuración contabilidad para especificar la gestión de asuntos de contabilidad en su empresa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Descripción de contabilidad y plan de cuentas

La contabilidad (G/L) almacena sus datos financieros y el plan de cuentas (COA) muestra las cuentas donde se registran todos los movimientos contables. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Configuración de contabilidad y grupos contables

La configuración de la contabilidad es en la base de los procesos financieros porque define cómo se registran los datos. Dos páginas en concreto desempeñan un papel importante en la configuración de sus procesos financieros:  

* **Configuración contabilidad**
* **Configuración grupos contables**

### <a name="the-general-ledger-setup-page"></a>La página **Configuración contabilidad**

Use la página **Configuración contabilidad** para especificar cómo gestionar determinados asuntos de contabilidad en su empresa, como:  

* Detalles de redondeo de factura  
* Formatos de dirección  
* Informes financieros

> [!TIP]
> La página **Configuración de contabilidad:** incluye campos genéricos y campos que son específicos de su país o región. Si no está seguro del significado de un campo, le sugerimos que trabaje con su contable para determinar si es relevante para su organización. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Para abrir la página ahora, utilice el siguiente vínculo [Configuración de contabilidad](https://businesscentral.dynamics.com/?page=118).

### <a name="the-general-posting-setup-page"></a>La página **Configuración grupos contables**

Utilice la página **Configuración grupos contables** para configurar combinaciones de grupos contables de negocio y de producto. Los grupos contables asignan entidades como clientes, proveedores, productos, recursos y documentos de venta y compra a cuentas contables. Rellene una línea por cada combinación de grupo contable de negocio y de producto. Pero también puede abrir cada línea en su propia tarjeta de configuración de registro. Obtenga más información en [Configuraciones de grupos contables](finance-posting-groups.md).  

> [!TIP]
> Si no puede ver los campos que está buscando en la página **Configuración grupos contables**, utilice la barra de desplazamiento horizontal situada en la parte inferior de la página para desplazarse hacia la derecha.  

Para abrir la página ahora, utilice el siguiente vínculo [Configuración grupos contables](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Plan de cuentas

La página **Plan de cuentas** muestra todas las cuentas de contabilidad general. Desde el plan de cuentas, puede realizar acciones como las siguientes:  

* Ver informes que muestran movimientos de contabilidad y saldos.  
* Cerrar el asiento de regularización.  
* Abrir la ficha de la cuenta de contabilidad general (CG) para agregar o cambiar la configuración.  
* Ver una lista de grupos contables para dicha cuenta.
* Para ver los saldos del Debe y el Haber de una sola cuenta.

Para obtener más información, vaya a [Conocer el plan de cuentas](finance-chart-of-accounts.md).

## <a name="account-categories"></a>Categorías de cuenta

Puede personalizar la estructura de los informes financieros con la asignación de las cuentas de contabilidad a las categorías de cuenta.  

La página **Categorías de cuenta** muestra las categorías y subcategorías, y las cuentas de contabilidad general que se asignó a cada categoría. Puede crear nuevas subcategorías y asignarlas a las cuentas existentes.  

Puede crear un grupo de categorías marcando otras subcategorías debajo de una línea en la página **Categorías de cuenta**. Los grupos de categorías facilitan la obtención de una descripción general, porque cada agrupación muestra un balance total. Por ejemplo, puede crear las subcategorías para distintos tipos de activos y a continuación crear grupos de categorías para los activos fijos y los activos circulantes.  

Puede defnir si los tipos de informes específicos deben incluir las cuentas de cada subcategoría. Las categorías de cuentas ayudan a definir el diseño de sus balances financieros.  

### <a name="example"></a>Ejemplo:

Por ejemplo, el extracto de saldo predeterminado tiene una subcategoría para *Efectivo* en *Activos fijos*. Si desea que el extracto de saldo tenga en cuenta el efectivo pequeño y la cuenta corriente, siga estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Categorías de cuenta de contabilidad** y luego elija el enlace relacionado.
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
> Si crea una cuenta de mayor sin asignar una categoría de cuenta, cuando asigne la cuenta a un grupo contable [!INCLUDE[prod_short](includes/prod_short.md)] asigna automáticamente la categoría de cuenta de la cuenta de mayor inmediatamente encima de la cuenta en su catálogo de cuentas. Sin embargo, para incluir la nueva cuenta en sus informes financieros, debe elegir la acción **Generar informes financieros** sobre la página **Categorías de cuentas del libro mayor**. Como alternativa, puede abrir la página Ficha cuenta, especificar la categoría de la cuenta y luego volver a generar su informe financiero.

## <a name="access-to-create-and-edit-gl-accounts-and-account-categories"></a>Acceso para crear y editar cuentas de proyecto y categorías de cuentas

En una organización pequeña, como la empresa de demostración CRONUS, la mayoría de los usuarios pueden editar cuentas de proyecto, categorías de cuentas y el plan de cuentas, excepto los usuarios con una licencia de TEAM MEMBER. Sin embargo, en organizaciones más grandes normalmente los roles de usuario y los permisos limitan el acceso para editar esas entidades. Si es administrador o tiene el rol *Administrador de negocio* o *Contable*, puede controlar los permisos de usuario para dar a las personas adecuadas acceso a las tablas relevantes. Para obtener más información, vaya a la sección [Obtener un resumen de los permisos de un usuario](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Utilice dimensiones para simplificar su plan de cuentas

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de venta. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento. Así, en lugar de configurar cuentas de libro mayor separadas para cada departamento y proyecto, puede utilizar las dimensiones como base para el análisis y evitar tener que crear un plan de cuentas complicado.

Para obtener más información sobre dimensiones, vaya a [Configurar dimensiones predeterminadas para clientes, proveedores, y otras cuentas](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## <a name="see-also"></a>Consulte también

[Conocer el plan de cuentas](finance-chart-of-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
