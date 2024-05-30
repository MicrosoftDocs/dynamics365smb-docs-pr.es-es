---
title: Conocer el plan de cuentas
description: 'Describe el plan de cuentas, cómo configurarlo y cómo utilizarlo.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/17/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="understanding-the-chart-of-accounts"></a>Conocer el plan de cuentas

Un plan de cuentas (COA) sirve como un directorio completo de cuentas financieras y sus correspondientes números de referencia. Un COA normalmente tiene dos categorías principales de cuentas:

- Cuentas de balance: estas cuentas rastrean los activos, las deudas y el patrimonio neto de su empresa.
- Cuentas del estado de resultados: estas cuentas registran los ingresos de diversas fuentes y también realizan un seguimiento de los gastos.

Las cuentas del balance se clasifican además en tres grupos:

1. Cuentas de activos: estas cuentas rastrean todos los recursos valiosos que posee su empresa.
1. Cuentas de pasivo: registran las deudas de su empresa.
1. Cuentas patrimoniales: representan el valor residual en la empresa tras restar el pasivo del activo.

Las cuentas de ingresos se dividen en dos grupos:

1. Cuentas de ingresos: estas cuentas capturan los ingresos de su empresa de diversas fuentes.
1. Cuentas de gastos: estas cuentas capturan todos los gastos de su empresa.

Utilice el COA para registrar transacciones en la contabilidad general de su organización. Cada cuenta normalmente tiene un identificador (número de cuenta) y un título o encabezado descriptivo, y están codificados sistemáticamente según su tipo de cuenta.

[!INCLUDE[prod_short](includes/prod_short.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.

La composición del plan de cuentas de su empresa es una decisión estratégica tomada por su dirección (o por la normativa específica de cada país o región). Varía según la industria, el modelo comercial y la estructura financiera de su empresa. Por ejemplo, dependiendo de su industria, es posible que tenga cuentas de activos específicas adaptadas a las operaciones y necesidades únicas de su empresa:

* Un negocio minorista podría enfatizar el inventario y las cuentas por cobrar.
* Una empresa de tecnología podría centrarse en activos intangibles como patentes y software.
* Una planta de fabricación rastrearía los activos fijos y los suministros.

## <a name="the-chart-of-accounts-page"></a>Página Plan de cuentas

El plan de cuentas muestra todas las cuentas de contabilidad. Desde el plan de cuentas, puede realizar acciones como las siguientes:  

* Ver informes que muestran movimientos de contabilidad y saldos.  
* Cerrar el asiento de regularización.  
* Abrir la ficha de la cuenta Configuración de contabilidad para agregar o cambiar la configuración.  
* Ver una lista de grupos contables para dicha cuenta.
* Para ver los saldos del Debe y el Haber de una sola cuenta.

Puede agregar, cambiar o eliminar cuentas de contabilidad. Sin embargo, para evitar discrepancias, no puede eliminar una cuenta de contabilidad si sus datos se utilizan en el plan de cuentas. Además, puede bloquear el borrado accidental de cuentas en periodos delicados. Para obtener más información sobre cómo proteger cuentas contra la eliminación, vaya a [Eliminar cuentas](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="the-code-hierarchy-in-gl-accounts"></a>La jerarquía de códigos en cuentas de contabilidad

Las empresas suelen crear una estructura jerárquica en los códigos de cuentas de contabilidad para reflejar su lugar en el plan de cuentas. Por ejemplo, en algunas implementaciones, los códigos de cuenta de contabilidad general que comienzan con **1** denotan cuentas de activos, mientras que los códigos de cuentas de contabilidad general que comienzan con 3 denotan cuentas de patrimonio. En algunas regiones, existen regulaciones locales para el uso de un plan de cuentas estándar. Para ayudar a los usuarios a comprender esta jerarquía sin la necesidad de conocer la estructura del código interno, puede definir encabezados y subtotales en su plan de cuentas que encapsule estas estructuras internas.

## <a name="designing-your-chart-of-accounts"></a>Diseñar su plan de cuentas

Cada línea del plan contable es una cuenta de contabilidad de uno de los tipos:

* Registro (las revistas pueden publicar líneas en estas cuentas)
* Cabecera (define un título general en el plan de cuentas)
* Total (define una fórmula para un subtotal en el plan de cuentas)
* Total inicio (define una cabecera inicial para un subtotal en el plan de cuentas. Todas las líneas subsiguientes hasta una línea de Total final tienen sangría)
* Total final (define un encabezado final para un subtotal y su fórmula en el plan de cuentas. Todas las líneas subsiguientes después de esta línea de Total final anulan la sangría)

Un plan de cuentas minimalista puede consistir únicamente en líneas de cuentas contables. Los otros cuatro tipos se utilizan para definir cómo el plan de cuentas también muestra un estado financiero con encabezados y subtotales. Las cuentas totales se utilizan con frecuencia en los informes financieros.

> [!TIP]
> Si utiliza tipos de cuenta distintos de **Registro** en su plan de cuentas, puede definir diferentes vistas para mostrar las cuentas de contabilización "sin procesar" sin los tipos de cuentas de tipo informe para totalizar. y encabezados. Por ejemplo, Mostrar solo cuentas de registro y Ocultar cuentas bloqueadas.

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Utilice dimensiones para simplificar su plan de cuentas

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de venta. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento. Así, en lugar de configurar cuentas de libro mayor separadas para cada departamento y proyecto, puede utilizar las dimensiones como base para el análisis y evitar tener que crear un plan de cuentas complicado.

Para obtener más información sobre las dimensiones, vaya a [Trabajar con dimensiones](finance-dimensions.md).

## <a name="get-a-quick-overview-of-your-finances"></a>Obtener una descripción general rápida de sus finanzas

La página **Plan de cuentas** muestra las cuentas en una lista jerárquica que ofrece acceso rápido a la información clave de cada cuenta. Sin embargo, la lista es estática y, si tiene muchas cuentas, es posible que deba desplazarse para ver la información de diferentes cuentas. Si solo desea una descripción general rápida de los conceptos básicos, como cambios netos y saldos, la página **Introducción al plan de cuentas** es una alternativa útil. El diseño de columnas en la página es el mismo que el de la página **Catálogo de cuentas** (aunque con menos columnas), por lo que resulta fácil de entender. Puede expandir o contraer los niveles jerárquicos. Para facilitar el cambio entre las páginas, la página **Introducción al plan de cuentas** está disponible en la página del **Plan de cuentas**.

## <a name="access-to-create-and-edit-the-chart-of-accounts"></a>Acceso para crear y editar el plan de cuentas

En una organización pequeña, como la empresa de demostración CRONUS, la mayoría de los usuarios pueden editar el plan de cuentas, excepto los usuarios con una licencia de TEAM MEMBER. Sin embargo, en organizaciones más grandes normalmente los roles de usuario y los permisos limitan el acceso para editar el plan de cuentas. Si es administrador o tiene el rol Administrador de negocio o Contable, puede controlar los permisos de usuario para dar a las personas adecuadas acceso a las tablas relevantes. Para obtener más información, vaya a la sección [Obtener un resumen de los permisos de un usuario](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## <a name="chart-of-accounts-best-practices"></a>Procedimientos recomendados del plan de cuentas

Estos son algunos de los procedimientos recomendados que podría considerar al desarrollar y mantener sus planes de cuentas:

* Redacte el plan de cuentas de su empresa para respaldar las necesidades de informes financieros para que su administración tome decisiones estratégicas.
* Considere comenzar de manera simple con menos cuentas de contabilidad. Siempre puede agregar cuentas más detalladas si es necesario.
* Defina encabezados y subtotales en su plan de cuentas que resumen las estructuras internas en las cuentas de contabilidad.
* Utilice dimensiones para simplificar su plan de cuentas. No tener cuentas de contabilidad específicas para cada producto o departamento.
* Agregue nuevas cuentas de contabilidad a medida que vayan llegando, pero elimine cuentas de su plan de cuentas solo durante el final del período financiero.

## <a name="see-also"></a>Consulte también

[Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md)  
[Comprender la contabilidad general](finance-general-ledger.md)
[Análisis financiero](bi.md)  
[Información general sobre finanzas](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
