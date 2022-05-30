---
title: Configurar el impuesto sobre el valor añadido
description: Asegúrese de que calcula, registra y crea informes correctamente del IVA de las ventas y las compras. Es recomendable que use la guía de configuración asistida para configurar el IVA.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 1877, 470, 471, 472
ms.date: 04/12/2022
ms.author: bholtorf
ms.openlocfilehash: 98a190594dbd2b37f949bdc51e7f810dd739b769
ms.sourcegitcommit: 4853614c85beb347091c5c4c1ea8d974dec887fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740316"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido

Los consumidores y las empresas pagan el impuesto sobre el valor añadido (IVA) cuando compran mercancías o servicios. El importe de IVA a pagar puede variar, dependiendo de varios factores. En [!INCLUDE[prod_short](includes/prod_short.md)], puede configurar el IVA para especificar las tasas que se usarán para calcular los importes de impuesto a partir de los siguientes parámetros:

* A quién vende  
* A quién compra  
* Qué vende  
* Qué compra  

Puede configurar los cálculos de IVA de forma manual, pero puede ser difícil y largo. Para que sea fácil, proporcionamos una guía de configuración asistida denominada **Configuración de IVA** que le ayudará con los pasos. Es recomendable que use la guía de configuración asistida para configurar el IVA.

> [!NOTE]  
> Puede usar la guía únicamente si ha creado una mi empresa, y no haya registrado transacciones que incluyen IVA. De lo contrario, sería muy sencillo usar tasas de IVA distintas por error, y crear informes relacionados con IVA inexactos.  

Si desea configurar cálculos del IVA, o solo desea obtener información acerca de cada paso, este artículo contiene descripciones de cada paso.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Usar la guía de configuración asistida Configuración de IVA para configurar el IVA (recomendado)

Es recomendable que use la guía de configuración asistida Configuración de IVA para configurar el IVA en [!INCLUDE[prod_short](includes/prod_short.md)].

Para iniciar la guía de configuración asistida, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración asistida**.  
2. Escoger **Configurar IVA** y completa los pasos.
3. Cuando haya completado la configuración asistida, visite la página **Configuración de registro de IVA** y verifique si debe completar campos adicionales de acuerdo con los requisitos locales de su versión de [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Funciones locales en Business Central](about-localization.md)  

### <a name="check-the-vat-posting-setup"></a>Comprobar la configuración de registro de IVA

Para ayudarle a empezar rápido, [!INCLUDE [prod_short](includes/prod_short.md)] le mostrará notificaciones si le faltan cuentas de contabilidad general (CG) en grupos contables o configuraciones de registro, como la página **Configuración de registro de IVA**. Puede activar o desactivar este tipo de notificación utilizando la notificación *Cuentas contables que faltan en grupo de registro o configuración* en la página **Mis notificaciones**. Solo tiene que ir a la página **Mi configuración** y luego elegir *Cambiar cuándo recibo notificaciones.* .  

Si elige esta notificación, [!INCLUDE [prod_short](includes/prod_short.md)] crea automáticamente esas configuraciones de registro en función de los grupos de registro en el documento o diario en el que esté trabajando actualmente.  

En este punto, puede completar las cuentas de contabilidad general que falten. Más adelante, cuando redefina aún más la configuración, es posible que se dé cuenta de que esta configuración era errónea. [!INCLUDE [prod_short](includes/prod_short.md)] no permite la eliminación de la configuración de registro de IVA y la configuración de registro general cuando se crean entradas basadas en dichas configuraciones. A partir del primer lanzamiento de versiones de 2022, puede usar el campo **Bloqueado** en la página **Configuración de registro de IVA** para evitar que los usuarios utilicen por error una configuración que ya no es pertinente para los nuevos registros.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Configurar números CIF/NIF para su país o región

Para ayudar a garantizar que las personas introduzcan números CIF/NIF válidos, puede definir formatos que se usan en los países o regiones con los que mantiene relaciones comerciales. [!INCLUDE[prod_short](includes/prod_short.md)] mostrará un mensaje de error cuando alguien cometa un error o utilice un formato que sea incorrecto para el país o región.

Para configurar números CIF/NIF, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Países/Regiones**.
2. Elija el país o región y después elija la acción **Formatos CIF/NIF**.
3. En el campo **Formatos**, puede definir el formato introduciendo uno o varios de los siguientes caracteres:  

* **#** Requiere un número de un solo dígito.  
* **@** Requiere una letra. Este formato no distingue entre mayúsculas y minúsculas.  
* **?** Permite cualquier carácter.  

    > [!Tip]
    > Puede usar otros caracteres siempre que estén presentes en el formato de país o región. Por ejemplo, si necesita incluir un punto o un guión entre conjuntos de números, puede definir el formato como ##.####.### or @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Configuración de grupos de registro de IVA de negocio

El grupo de registro de IVA de negocio debería representar los mercados en los que trabaje con clientes y proveedores, y definir cómo calcular y registrar el IVA en cada mercado. Ejemplos de grupos de registro de IVA de negocio son **Nacional** y **Unión Europea (EU)**.  

Use códigos fáciles de recordar y que describan el grupo de registro de negocio, como **UE**, **No UE** o **Nacional**. El código debe ser único. Puede configurar tantos códigos como desee, pero no puede aparecer el mismo código más de una vez en una tabla.

Para configurar un grupo de registro de IVA de negocio, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupo de registro de IVA de negocio** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

Para configurar grupos de registro de IVA de negocio predeterminados deberá vincularlos a grupos contables de negocio. [!INCLUDE[prod_short](includes/prod_short.md)]asigna automáticamente el grupo de registro de IVA de negocio cuando asigne el grupo de registro de negocio relevante a un cliente, proveedor o cuenta contable.

## <a name="set-up-vat-product-posting-groups"></a>Configurar grupos de registro de IVA de producto

Los grupos de registro de IVA de producto representan los productos y los recursos que compra o vende, y determinan cómo se calcula y se registra el IVA en función del tipo de producto o que se adquiera o se venda.  
Conviene utilizar códigos que sean fáciles de recordar y que describan el tipo, como **SIN IVA** o **Cero**, **IVA10** o **Reducido** para el IVA del 10 % e **IVA25** o **Estándar** para el 25 %.

Para configurar un grupo de registro de IVA de negocio, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de registro IVA de producto** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Combinar grupos de registro de IVA en configuraciones de registro de IVA

[!INCLUDE[prod_short](includes/prod_short.md)] calcula los importes de IVA de ventas y compras en función de las configuraciones de registro de IVA, que son combinaciones de grupos de registro de IVA de negocio y de producto. En cada combinación puede especificar el porcentaje de IVA, el tipo de cálculo del IVA y las cuentas de contabilidad para el registro del IVA de ventas, compras y los cargos invertidos. También puede especificar si el IVA se vuelve a calcular cuando se aplica o se recibe un descuento.  

Configure tambas combinaciones como necesite. Si desea agrupar las combinaciones de configuración de registro de IVA con atributos parecidos, puede definir un **identificador de IVA** para cada grupo y asignarlo a los miembros del grupo.

Para combinar las configuraciones de registro de IVA, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 5.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Asignar los grupos de registro de IVA de forma predeterminada a varias entidades

Si desea aplicar los mismos grupos de registro de IVA a varias entidades, puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que lo haga de forma predeterminada. Existen un par de formas de hacer esto:

* Puede asignar los grupos de registro de IVA de negocio a los grupos de registro de negocio generales, o plantillas de cliente o proveedor
* Puede asignar los grupos de registro de IVA de negocio a grupos de registro de producto generales  

El grupo de registro de IVA de negocio o de producto se asigna cuando elige un grupo de registro de IVA de negocio o de producto para un cliente, un proveedor, un producto o un recurso.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Asignar grupos de registro de IVA a cuentas, clientes, proveedores, artículos y recursos

En las secciones siguientes se describe cómo asignar los grupos de registro de IVA de negocio a los objetos individuales.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Para asignar grupos de registro de IVA a cuentas contables individuales

1. Elija el icono ![Bombilla que abre la función Dígame 6.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. Abre la ficha **Cuenta** de la cuenta.  
3. En la ficha desplegable **Registro**, en el campo **Tipo IVA**, elija **Venta** o **Compra**.  
4. Elija los grupos de registro de IVA que se usarán para la cuenta de venta o de compra.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Para asignar grupos de registro de IVA a clientes y proveedores

1. Elija el icono ![Bombilla que abre la función Dígame 7.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cliente** o **Proveedor** y luego elija el enlace relacionado.  
2. En la ficha **Cliente** o **Proveedor**, amplíe la ficha desplegable **Facturación**.  
3. Elija el grupo de registro de IVA de negocio.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Para asignar grupos de registro de IVA de producto a productos y recursos individuales

1. Elija el icono ![Bombilla que abre la función Dígame 8.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Producto** o **Recurso** y luego elija el enlace relacionado.  
2. Realice una de las siguientes acciones:  

    * En la ficha **Producto**, expanda la ficha desplegable **Precio y registro** y haga clic en **Mostrar más** para mostrar el campo **Grupo registro IVA producto**.  
    * En la ficha **Recurso**, amplíe la ficha desplegable **Facturación**.  
3. Elija el grupo de registro de IVA de producto.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Configurar cláusulas para explicar la exención del IVA o los tipos de IVA no estándar

Configura una cláusula de IVA para describir información acerca del tipo de IVA que se está aplicando. La legislación puede requerir la información. Una vez que haya configurado una cláusula de IVA y la haya asociado a una configuración de registro de IVA, la cláusula de IVA se muestra en los documentos de venta impresos que usan ese grupo de configuración de registro de IVA.

Si es necesario, también puede especificar cómo traducir las cláusulas de IVA a otros idiomas. A continuación, cuando cree e imprima un documento de venta que contenga un identificador de IVA, el documento traducido incluirá la cláusula de IVA. El código de idioma especificado en la ficha de cliente determina el idioma.

Cuando se usan tipos de IVA no estándar en diferentes tipos de documentos, como facturas o abonos, a las empresas generalmente se les exige que incluyan un texto de exención (cláusula de IVA) que indique por qué se ha calculado un tipo de IVA reducido o cero. Puede definir diferentes cláusulas de IVA que se incluirán en los documentos comerciales por tipo de documento, como factura o abono. Haces esto en la página **Cláusulas de IVA por tipo de documento**.

Puede modificar o eliminar una cláusula de IVA, y las modificaciones se reflejarán en un informe generado. Sin embargo, [!INCLUDE[prod_short](includes/prod_short.md)] no mantiene un historial de cambios. En el informe, la descripciones de cláusula de IVA se imprimen y se muestran para todas las líneas del informe junto al importe de IVA y el importe base de IVA. Si una cláusula de IVA no se ha definido para ninguna línea en el documento de venta, se omite toda la sección cuando se imprima el informe.

### <a name="to-set-up-vat-clauses"></a>Para configurar las cláusulas de IVA

1. Elija el icono ![Bombilla que abre la función Dígame 9.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cláusulas de IVA** y luego elija el enlace relacionado.  
2. En la página **Cláusulas de IVA**, cree una nueva línea.  
3. En el campo **Código**, especifique un identificador para la cláusula. Utilice este código para asignar la cláusula a grupos de registro de IVA.  
4. En el campo **Descripción**, escriba el texto de exención de IVA que desea mostrar en los documentos que pueden incluir el IVA. En el campo **Descripción 2**, escriba texto adicional, en caso necesario. El texto aparecerá en nuevas líneas de documento.
5. Elija la acción **Descripción por tipo de documento**.
6. En la página **Cláusulas de IVA por tipo de documento**, complete los campos para configurar qué texto de exención de IVA se mostrará para cada tipo de documento.  
7. Opcional: para asignar la cláusula de IVA a una configuración de registro de IVA inmediatamente, elija **Configuración** y, a continuación, la cláusula. Si desea esperar, puede asignar la cláusula después en la página **Config. grupos registro IVA**.  
8. Opcional: para especificar cómo traducir la cláusula de IVA, elija la acción **Traducciones**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Para asignar una cláusula de IVA a una configuración de registro de IVA

1. Elija el icono ![Bombilla que abre la función Dígame 10.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego elija el vínculo relacionado.  
2. En la columna **Cláusula de IVA**, seleccione la cláusula que se usará por cada configuración de registro de IVA al que se aplique.  

### <a name="to-specify-translations-for-vat-clauses"></a>Para especificar las traducciones de las cláusulas de IVA

1. Elija el icono ![Bombilla que abre la función Dígame 11.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cláusulas de IVA** y luego elija el vínculo relacionado.  
2. Elija la acción **Traducciones**.  
3. En el campo **Código idioma**, seleccione el idioma al que realizará la traducción.  
4. En los campos **Descripción** y **Descripción 2**, especifique las traducciones de las descripciones. Este texto se muestra en los documentos de informes de IVA traducidos.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Crear una configuración de registro de IVA para usar el IVA de importación

Puede usar la característica de *IVA de importación* cuando necesite registrar un documento cuyo importe total sea el IVA. Se utiliza si se recibe de las autoridades fiscales una factura por el IVA de los productos importados.  

Para configurar los códigos del IVA de importación, realice los pasos siguientes:  

1. Elija el icono ![Bombilla que abre la función Dígame 12.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de registro IVA de producto** y luego elija el vínculo relacionado.  
2. En la página Grupos de registro de IVA de producto, configure un nuevo grupo de registro de IVA de producto para el IVA de importación.  
3. Elija el icono ![Bombilla que abre la función Dígame 13.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego elija el vínculo relacionado.  
4. En la página Configuración de registro de IVA, cree una nueva línea o use una combinación de grupos de registro de IVA de negocio ya existente y el nuevo grupo de registro de IVA de producto.  
5. En el campo **Tipo cálculo IVA**, elija **Total**.  
6. En el campo **Cta. IVA acreditable**, escriba la cuenta que se utilizará para registrar el IVA de importación. Las demás cuentas son opcionales.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Usar el IVA de reversión para las transacciones entre países o regiones de la UE

Algunas empresas deben usar el IVA de reversión al realizar transacciones comerciales con otras empresas. Por ejemplo, esta norma se aplica a compras de países o regiones de la UE y a ventas a países o regiones de la UE.  

> [!NOTE]  
> Esta norma se aplica al realizar transacciones comerciales con empresas cuyo registro del IVA está en otro país o región de la UE. Si realiza transacciones comerciales directamente con consumidores de otros países o regiones de la UE, debe ponerse en contacto con las autoridades fiscales de su país o región para obtener información sobre la normativa de IVA vigente.  

> [!TIP]  
> Puede comprobar que una empresa está sujeta a IVA en otro país de la UE utilizando el servicio de validación de CIF/NIF de la UE. El servicio está disponible gratis en [!INCLUDE[prod_short](includes/prod_short.md)]. Para más información, consulte [Verificar CIF/NIF](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Ventas a países o regiones de la UE

El IVA no se calcula para las ventas a empresas sujetas al IVA de otros países o regiones de la UE. Debe declarar el valor de estas ventas por separado en la declaración del IVA.  

Para calcular correctamente el IVA en las ventas a países o regiones de la UE, debe:  

* Configurar una línea para las ventas con la misma información de las compras. Si ya ha creado líneas en la página Config. grupos registro IVA para las compras a países o regiones de la UE, puede usarlas para las ventas.  
* Asigne grupos de registro de IVA de negocio en el campo **Grupo registro IVA neg.** de la ficha desplegable **Facturación** de la ficha cliente de cada cliente de la UE. También debe introducir el CIF/NIF del cliente en el campo **CIF/NIF** en la Ficha desplegable **Comercio exterior**.  

Cuando registre una venta a un cliente de otro país o región de la UE, se calculará el importe del IVA y se creará un movimiento del IVA con la información sobre el IVA de reversión y la base del IVA (importe utilizado para calcular el importe del IVA). No se registran movimientos en las cuentas del IVA de contabilidad.

## <a name="vat-rounding-for-documents"></a>Redondeo del IVA en los documentos

Los importes de los documentos que todavía no se han registrado se redondean y se muestran para que ajusten al redondeo final de los importes que realmente se registren. El IVA se calcula para un documento completo, lo que significa que el IVA se calcula según la suma de todas las líneas con el mismo identificador de IVA en el documento.  

## <a name="set-up-vat-reporting"></a>Configurar informes de IVA

Debe configurar la información sobre cómo las autoridades fiscales de su país o región requieren que presente informes de IVA. Los siguientes pasos ilustran la información más utilizada habitualmente. Sin embargo, su país o región puede requerir pasos adicionales. Para obtener más información, consulte el artículo correspondiente en la sección *Funcionalidad local* del panel de la izquierda.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Consulte también

[Configurar tipos de declaración de IVA y nombres de declaración de IVA](finance-how-setup-vat-statement.md)  
[Configurar el impuesto sobre el valor añadido no realizado](finance-setup-unrealized-vat.md)  
[Crear informes de IVA para la autoridad fiscal](finance-how-report-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Trabajar con la herramienta de cambio de tipo de IVA](finance-how-use-vat-rate-change-tool.md)  
[Comprobar CIF/NIF](finance-how-validate-vat-registration-number.md)  
[Funcionalidad local en Business Central](about-localization.md)  
[Declaración de IVA en la versión alemana](LocalFunctionality/Germany/vat-reporting.md)  
[IVA Belga](LocalFunctionality/Belgium/belgian-vat.md)  
[IVA italiano](LocalFunctionality/Italy/italian-vat.md)  
[Configurar declaraciones electrónicas de IVA e ICP en la versión holandesa](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[Informes de IVA en la versión en español](LocalFunctionality/Spain/vat-reports.md)  
[Configurar la contabilización de impuestos sobre bienes y servicios en la versión australiana](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[IVA en la versión checa](LocalFunctionality/Czech/finance-vat.md)  
[Declaración de IVA en la versión noruega](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Informes del impuesto sobre bienes y servicios e impuesto armonizado en Canadá](LocalFunctionality/Canada/sales-tax-goods-services.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
