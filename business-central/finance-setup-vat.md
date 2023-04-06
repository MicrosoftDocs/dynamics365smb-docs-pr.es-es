---
title: Configurar el impuesto sobre el valor añadido
description: 'Asegúrese de que calcula, registra y crea informes correctamente del IVA de las ventas y las compras. Es recomendable que use la guía de configuración asistida para configurar el IVA.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 01/31/2023
ms.author: bholtorf
---

# Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido

Los consumidores y las empresas pagan el impuesto sobre el valor añadido (IVA) cuando compran mercancías o servicios. El importe de IVA a pagar puede variar, dependiendo de varios factores. En [!INCLUDE[prod_short](includes/prod_short.md)], puede configurar el IVA para especificar las tasas que usó para calcular los importes de impuesto a partir de los siguientes parámetros:

* A quién vende  
* A quién compra  
* Qué vende  
* Qué compra  

Puede configurar los cálculos de IVA de forma manual, pero puede ser difícil y largo. La razón es que es muy sencillo usar tasas de IVA distintas por error, y crear informes relacionados con IVA inexactos. Para facilitar la configuración del IVA, le recomendamos que utilice la guía asistida **Configuración de IVA** provista en el producto. 

Sin embargo, si desea configurar los cálculos del IVA, o solo desea obtener información acerca de cada paso, este artículo contiene descripciones de cada paso.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## Configurar el IVA mediante la guía de configuración asistida (recomendado)

> [!NOTE]
> Puede usar la guía **Configuración de IVA** únicamente si ha creado una *Mi empresa* y no ha registrado transacciones que incluyen IVA todavía.

Para iniciar la guía de configuración asistida, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") y escriba **Configuración asistida**. 
2. Escoja **Configurar IVA** y complete los pasos.
3. Cuando haya completado la configuración asistida, visite la página **Configuración de registro de IVA** para verificar si necesita completar campos adicionales de acuerdo con los requisitos locales de su versión de [!INCLUDE [prod_short](includes/prod_short.md)]. Obtenga más información en [Funcionalidad local en Business Central](about-localization.md).  

### Comprobar la configuración de registro de IVA

Para ayudarle a empezar rápido, [!INCLUDE [prod_short](includes/prod_short.md)] le notifica si le faltan cuentas de contabilidad general (CG) en grupos contables o configuraciones de registro, como en la página **Configuración de registro de IVA**. Puede activar o desactivar este tipo de notificación utilizando la notificación *Cuentas contables que faltan en grupo de registro o configuración* en la página **Mis notificaciones**. Solo tiene que ir a la página **Mi configuración** y luego elegir *Cambiar cuándo recibo notificaciones.* .  

Si elige esta notificación, [!INCLUDE [prod_short](includes/prod_short.md)] crea automáticamente esas configuraciones de registro en función de los grupos de registro en el documento o diario en el que esté trabajando actualmente.  

En este punto, puede completar las cuentas de contabilidad general que falten. Sin embargo, más adelante, cuando redefina aún más la configuración, es posible que se dé cuenta de que esta configuración era errónea. Y [!INCLUDE [prod_short](includes/prod_short.md)] no permite la eliminación de una configuración de registro de IVA y la configuración de registro general cuando se han creado entradas basadas en dichas configuraciones. Por lo tanto, a partir del primer lanzamiento de versiones de 2022, puede usar el campo **Bloqueado** en la página **Configuración de registro de IVA** para evitar que los usuarios utilicen por error una configuración que ya no es pertinente para los nuevos registros.

## Configurar una fecha de IVA predeterminada para documentos y diarios

La declaración de IVA en [!INCLUDE [prod_short](includes/prod_short.md)] se basa en la **Fecha de IVA** para incluir entradas de IVA en informes de IVA de un período de IVA. La fecha de IVA se puede cambiar en todos los documentos y diarios, pero debe especificar un valor predeterminado para la fecha de IVA.

> [!NOTE]
> Después de publicar el documento o diario, la **Fecha de IVA** aparecerá en **Movimientos de IVA** y **Movimientos de contabilidad**, así como en el documento contabilizado si existe.

Para configurar un valor predeterminado para una fecha de IVA, siga estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad** y luego elija el enlace relacionado.  
2. En la ficha desplegable **General** del campo **Fecha de IVA predeterminada**, elija **Fecha registro** o **Fecha del documento**.
3. Cierra la página.  

> [!NOTE]
> De forma predeterminada, la **Fecha de IVA predeterminada** es la **Fecha registro**.

### Habilitación o deshabilitación de la función Fecha de IVA

Algunos países requieren que las empresas usen una fecha de IVA específica, pero otros países no. Algunos países también requieren que las empresas cambien la fecha del IVA en situaciones específicas después de haber publicado documentos, pero otros países no permiten cambios en las fechas del IVA. Para permitir diferentes contextos, puede elegir si desea utilizar esta funcionalidad y, de ser así, en qué medida.

Para configurar el nivel de uso de la fecha de IVA, siga estos pasos:

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad** y luego elija el enlace relacionado.  
2. En la ficha desplegable **General**, en el campo **Uso de fecha de IVA**, especifique el grado en que desea utilizar el Función de fecha de IVA. Puede elegir una de las opciones siguientes:

| Escriba | Descripción |
|--------------------|-----------------------------------------|
| **Utilice la funcionalidad completa de fecha de IVA** | Todo lo relacionado con **Fecha de IVA** funciona de manera predeterminada, brindándole la máxima funcionalidad **Fecha de IVA**. Puede configurar la fecha, cambiarla en los documentos, generar informes en función de ella y modificar la fecha después de la publicación, siempre que el período no esté cerrado o protegido con fechas permitidas para la publicación. |
| **Usar pero no permitir modificaciones** | Todo lo relacionado con **Fecha de IVA** funciona de forma predeterminada con una excepción. No puedes modificar la **Fecha de IVA** en **Entradas de IVA**. |
| **No usar la funcionalidad de fecha de IVA** | [!INCLUDE [prod_short](includes/prod_short.md)] se esconderá y hará que los campos **Fecha de IVA** no estén disponibles en documentos, diarios y entradas. La **Fecha de IVA predeterminada** se configurará como la **Fecha de publicación**. |

3. Cierra la página.

> [!IMPORTANT]
> Incluso si elige la opción **No usar la función de fecha de IVA**, [!INCLUDE [prod_short](includes/prod_short.md)] utilizará la **Fecha de IVA** en el fondo. Dado que la **Fecha de IVA predeterminada** se configura como la **Fecha de publicación**, y no puede cambiarla en este caso, obtendrá la misma experiencia que sin esta característica. Los campos **Fecha de IVA** se eliminarán de todas las páginas, pero este campo seguirá existiendo en las tablas y los informes funcionarán en función de él.

### Limitación de períodos para publicar y modificar la fecha del IVA

Puede evitar que las personas publiquen o cambien entradas de IVA en intervalos de fechas específicos. Puede establecer la restricción usando dos configuraciones:

* Sobre la base de un **Período de devolución del IVA** cerrado
* Sobre la base de los campos **Permitir publicar desde** y **Permitir publicar hasta**.

#### Para limitar la publicación según el período de devolución del IVA

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.  
2. En la ficha desplegable **General** en el campo **Período de control de IVA**, especifique el grado de control del Período de devolución del IVA. La siguiente tabla describe las opciones.

| Escriba | Descripción |
|--------------------|-----------------------------------------|
| **Bloquear registro en cerrado y advertir para periodo liberado** | Impida que las personas publiquen un documento o diario, o cambien entradas de IVA, que tengan una fecha de IVA dentro de un **Período de devolución del IVA**. [!INCLUDE [prod_short](includes/prod_short.md)] también mostrará una advertencia si su **Período de devolución del IVA** está abierto, pero el estado de **Devolución de IVA**  es **Liberado** o **Enviado**. |
| **Bloquear registro dentro del periodo cerrado** | Impida que las personas publiquen un documento o diario, o cambien entradas de IVA, que tengan una fecha de IVA dentro de un **Período de devolución del IVA** cerrado. |
| **Advertir al registrar en un periodo cerrado** | Muestre una advertencia, pero no bloquee la publicación, si desea registrar un documento o diario que tenga una fecha de IVA dentro de un **Período de devolución del IVA** cerrado. |
| **Deshabilitada** | No realice ninguna acción en base a un **Período de devolución del IVA** cerrado. |

#### Para limitar la publicación en función de Permitir desde/hasta el período

Puede configurar la limitación en la empresa o en niveles de usuario específicos.

Para limitar todas las publicaciones para toda la empresa:

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.  
2. En la ficha desplegable **General** en el campo **Permitir publicar desde**, especifique la fecha de IVA a partir de la cual permite la publicación. No se permite publicar un documento o diario con una fecha de IVA anterior a esta fecha.  
3. En la ficha desplegable **General** en el campo **Permitir publicar hasta**, especifique la fecha de IVA hasta la cual permite la publicación. No se permite publicar un documento o diario con una fecha de IVA posterior a esta fecha.

Para limitar las publicaciones para el usuario específico:

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de usuario** y luego elija el enlace relacionado.  
2. En el campo **ID de usuario**, especifique el usuario al que desea permitir publicar en un período específico.  
3. En el campo **Permitir la publicación desde**, Especifique la fecha de IVA a partir de la cual permite la publicación. No se permite publicar un documento o diario con una fecha de IVA anterior a esta fecha.
4. En el campo **Permitir la publicación hasta**, especifique la fecha de IVA hasta la cual permite la publicación. No se permite publicar un documento o diario con una fecha de IVA posterior a esta fecha.

## Configurar números CIF/NIF para su país o región

Para ayudar a garantizar que las personas introduzcan números CIF/NIF válidos, puede definir formatos que se usan en los países o regiones con los que mantiene relaciones comerciales. [!INCLUDE[prod_short](includes/prod_short.md)] mostrará un mensaje de error si alguien comete un error o utiliza un formato que sea incorrecto para el país o región.

Para configurar números CIF/NIF, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Países/Regiones**.
2. Elija el país o región y después elija la acción **Formatos CIF/NIF**.
3. En el campo **Formatos**, puede definir el formato introduciendo uno o varios de los siguientes caracteres:  

* **#** Requiere un número de un solo dígito.  
* **@** Requiere una letra. Este formato no distingue entre mayúsculas y minúsculas.  
* **?** Permite cualquier carácter.  

    > [!TIP]
    > Puede usar otros caracteres siempre que estén presentes en el formato de país o región. Por lo tanto, si necesita incluir un punto o un guión entre conjuntos de números, puede definir el formato como ##.####.### o @@-###-###.  

## Configuración de grupos de registro de IVA de negocio

El grupo de registro de IVA de negocio debería representar los mercados en los que trabaje con clientes y proveedores, y definir cómo calcular y registrar el IVA en cada mercado. Ejemplos de grupos de registro de IVA de negocio son **Nacional** y **Unión Europea (EU)**.  

Use códigos fáciles de recordar y que describan el grupo de registro de negocio, como **UE**, **No UE** o **Nacional**. Cada código debe ser único, lo que significa que puede configurar tantos códigos como desee, pero no puede aparecer el mismo código más de una vez en una tabla.

Para configurar un grupo de registro de IVA de negocio, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de registro de IVA de negocio** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

Puede configurar grupos de registro de IVA de negocio predeterminados deberá vincularlos a grupos contables de negocio. [!INCLUDE[prod_short](includes/prod_short.md)]asigna automáticamente el grupo de registro de IVA de negocio cuando asigne el grupo de registro de negocio relevante a un cliente, proveedor o cuenta contable.

## Configurar grupos de registro de IVA de producto

Los grupos de registro de IVA de producto representan los productos y los recursos que compra o vende, y determinan cómo se calcula y se registra el IVA en función del tipo de producto o recurso.

Conviene utilizar códigos que sean fáciles de recordar y que describan el tipo, como **SIN IVA** o **Cero**, **IVA10** o **Reducido** para el IVA del 10 por ciento e **IVA25** o **Estándar** para el 25 por ciento.

Para configurar un grupo de registro de IVA de negocio, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de registro IVA de producto** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario.

## Combinar grupos de registro de IVA en configuraciones de registro de IVA

[!INCLUDE[prod_short](includes/prod_short.md)] calcula los importes de IVA de ventas y compras en función de las configuraciones de registro de IVA, que son combinaciones de grupos de registro de IVA de negocio y de producto. En cada combinación puede especificar el porcentaje de IVA, el tipo de cálculo del IVA y las cuentas de contabilidad para el registro del IVA de ventas, compras y los cargos invertidos. También puede especificar si el IVA se vuelve a calcular cuando se aplica o se recibe un descuento.  

Configure tambas combinaciones como necesite. Si desea agrupar las combinaciones de configuración de registro de IVA con atributos parecidos, puede definir un **identificador de IVA** para cada grupo y asignarlo a los miembros del grupo.

Para combinar las configuraciones de registro de IVA, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la característica Dígame 5.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Asignar los grupos de registro de IVA de forma predeterminada a varias entidades

Si desea aplicar los mismos grupos de registro de IVA a varias entidades, puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que lo haga de forma predeterminada. Existen un par de formas de hacer esto:

* Puede asignar los grupos de registro de IVA de negocio a los grupos de registro de negocio generales, o plantillas de cliente o proveedor
* Puede asignar los grupos de registro de IVA de negocio a grupos de registro de producto generales  

El grupo de registro de IVA de negocio o de producto se asigna cuando elige un grupo de registro de IVA de negocio o de producto para un cliente, un proveedor, un producto o un recurso.

## Asignar grupos de registro de IVA a cuentas, clientes, proveedores, artículos y recursos

En las secciones siguientes se describe cómo asignar los grupos de registro de IVA de negocio a los objetos individuales.

### Para asignar grupos de registro de IVA a cuentas contables individuales

1. Elija el icono ![Bombilla que abre la característica Dígame 6.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. Abre la ficha **Cuenta** de la cuenta.  
3. En la ficha desplegable **Registro**, en el campo **Tipo IVA**, elija **Venta** o **Compra**.  
4. Elija los grupos de registro de IVA que se usarán para la cuenta de venta o de compra.  

### Para asignar grupos de registro de IVA a clientes y proveedores

1. Elija el icono ![Bombilla que abre la característica Dígame 7.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cliente** o **Proveedor** y luego elija el enlace relacionado.  
2. En la ficha **Cliente** o **Proveedor**, amplíe la ficha desplegable **Facturación**.  
3. Elija el grupo de registro de IVA de negocio.  

### Para asignar grupos de registro de IVA de producto a productos y recursos individuales

1. Elija el icono ![Bombilla que abre la característica Dígame 8.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Producto** o **Recurso** y luego elija el enlace relacionado.  
2. Realice una de las siguientes acciones:  

    * En la ficha **Producto**, expanda la ficha desplegable **Precio y registro** y haga clic en **Mostrar más** para mostrar el campo **Grupo registro IVA producto**.  
    * En la ficha **Recurso**, amplíe la ficha desplegable **Facturación**.  
3. Elija el grupo de registro de IVA de producto.  

## Configurar cláusulas para explicar la exención del IVA o los tipos de IVA no estándar

Configura una cláusula de IVA para describir información acerca del tipo de IVA que se está aplicando. Las leyes gubernamentales pueden requerir la información. Una vez que haya configurado una cláusula de IVA y la haya asociado a una configuración de registro de IVA, la cláusula de IVA se muestra en los documentos de venta impresos que usan ese grupo de configuración de registro de IVA.

Si es necesario, también puede especificar cómo traducir las cláusulas de IVA a otros idiomas. A continuación, cuando cree e imprima un documento de venta que contenga un identificador de IVA, el documento traducido incluirá la cláusula de IVA. El código de idioma especificado en la ficha de cliente determina el idioma.

Cuando se usan tipos de IVA no estándar en diferentes tipos de documentos, como facturas o abonos, a las empresas generalmente se les exige que incluyan un texto de exención (cláusula de IVA) que indique por qué se ha calculado un tipo de IVA reducido o cero. Puede definir diferentes cláusulas de IVA que se incluirán en los documentos comerciales por tipo de documento, como factura o abono. Hace esto en la página **Cláusulas de IVA por tipo de documento**.

Puede modificar o eliminar una cláusula de IVA, y las modificaciones se reflejarán en un informe generado. Sin embargo, [!INCLUDE[prod_short](includes/prod_short.md)] no mantiene un historial de cambios. En el informe, la descripciones de cláusula de IVA se imprimen y se muestran para todas las líneas del informe junto al importe de IVA y el importe base de IVA. Si una cláusula de IVA no se ha definido para ninguna línea en el documento de venta, se omite toda la sección cuando se imprima el informe.

### Para configurar las cláusulas de IVA

1. Elija el icono ![Bombilla que abre la característica Dígame 9.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cláusulas de IVA** y luego elija el enlace relacionado.  
2. En la página **Cláusulas de IVA**, cree una nueva línea.  
3. En el campo **Código**, especifique un identificador para la cláusula. Utilice este código para asignar la cláusula a grupos de registro de IVA.  
4. En el campo **Descripción**, escriba el texto de exención de IVA que desea mostrar en los documentos que pueden incluir el IVA. En el campo **Descripción 2**, escriba texto adicional, en caso necesario. El texto aparecerá en nuevas líneas de documento.
5. Elija la acción **Descripción por tipo de documento**.
6. En la página **Cláusulas de IVA por tipo de documento**, complete los campos para configurar qué texto de exención de IVA se mostrará para cada tipo de documento.  
7. Opcional: para asignar la cláusula de IVA a una configuración de registro de IVA inmediatamente, elija **Configuración** y, a continuación, la cláusula. Si desea esperar, puede asignar la cláusula después en la página **Config. grupos registro IVA**.  
8. Opcional: para especificar cómo traducir la cláusula de IVA, elija la acción **Traducciones**.

### Para asignar una cláusula de IVA a una configuración de registro de IVA

1. Elija el icono ![Bombilla que abre la característica Dígame 10.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego elija el vínculo relacionado.  
2. En la columna **Cláusula de IVA**, seleccione la cláusula que se usará por cada configuración de registro de IVA al que se aplique.  

### Para especificar las traducciones de las cláusulas de IVA

1. Elija el icono ![Bombilla que abre la característica Dígame 11.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cláusulas de IVA** y luego elija el vínculo relacionado.  
2. Elija la acción **Traducciones**.  
3. En el campo **Código idioma**, seleccione el idioma al que realizará la traducción.  
4. En los campos **Descripción** y **Descripción 2**, especifique las traducciones de las descripciones. Este texto se muestra en los documentos de informes de IVA traducidos.  

### Para especificar texto extendido para las cláusulas de IVA

> [!NOTE]  
> Si su país o región requiere un texto más largo para las cláusulas de IVA que el que admite la versión predeterminada, puede especificar el texto más largo para las cláusulas de IVA como *texto extendido* para que se imprima en los informes de compras y ventas.  

1. Elija el icono ![Bombilla que abre la característica Dígame 11.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cláusulas de IVA** y luego elija el vínculo relacionado.  
2. Elija la acción **Textos ampliados**.  
3. Seleccione la acción **Nuevo**.  
4. Rellene los campos **Código de idioma** y **Descripción**.  
5. Opcionalmente, seleccione el campo **Todos los códigos de idioma** o especifique el idioma pertinente en el campo **Código de idioma** si utiliza códigos de idioma.  
6. Rellene los campos **Fecha inicial** y **Fecha final** si desea limitar las fechas en las que se utiliza el texto adicional.  
7. En las líneas **Texto**, escriba el texto ampliado para sus cláusulas de IVA.  
8. Seleccione los campos correspondientes para los tipos de documento donde desee imprimir el texto adicional.  
9. Cierra la página.  

## Crear una configuración de registro de IVA para usar el IVA de importación

Puede usar la característica de *IVA de importación* cuando necesite registrar un documento cuyo importe total sea el IVA. Se utiliza si se recibe de las autoridades fiscales una factura por el IVA de los productos importados.  

Para configurar los códigos del IVA de importación, realice los pasos siguientes:  

1. Elija el icono ![Bombilla que abre la característica Dígame 12.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de registro IVA de producto** y luego elija el vínculo relacionado.  
2. En la página Grupos de registro de IVA de producto, configure un nuevo grupo de registro de IVA de producto para el IVA de importación.  
3. Elija el icono ![Bombilla que abre la característica Dígame 13.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego elija el vínculo relacionado.  
4. En la página Configuración de registro de IVA, cree una nueva línea o use una combinación de grupos de registro de IVA de negocio ya existente y el nuevo grupo de registro de IVA de producto.  
5. En el campo **Tipo cálculo IVA**, elija **Total**.  
6. En el campo **Cta. IVA acreditable**, escriba la cuenta que se utilizará para registrar el IVA de importación. Las demás cuentas son opcionales.  

## Usar el IVA de reversión para las transacciones entre países o regiones de la UE

Algunas empresas deben usar el IVA de reversión al realizar transacciones comerciales con otras empresas. Por ejemplo, esta norma se aplica a compras de países o regiones de la UE y a ventas a países o regiones de la UE.  

> [!NOTE]  
> Esta norma se aplica al realizar transacciones comerciales con empresas cuyo registro del IVA está en otro país o región de la UE. Si realiza transacciones comerciales directamente con consumidores de otros países o regiones de la UE, debe ponerse en contacto con las autoridades fiscales de su país o región para obtener información sobre la normativa de IVA vigente.  

> [!TIP]  
> Puede comprobar que una empresa está sujeta a IVA en otro país de la UE utilizando el servicio de validación de CIF/NIF de la UE. El servicio está disponible gratis en [!INCLUDE[prod_short](includes/prod_short.md)]. Para más información, consulte [Verificar CIF/NIF](finance-how-validate-vat-registration-number.md).

### Ventas a países o regiones de la UE

El IVA no se calcula para las ventas a empresas sujetas al IVA de otros países o regiones de la UE. Debe declarar el valor de estas ventas por separado en la declaración del IVA.  

Para calcular correctamente el IVA en las ventas a países o regiones de la UE, debe:  

* Configurar una línea para las ventas con la misma información de las compras. Si ya ha creado líneas en la página **Config. grupos registro IVA** para las compras a países o regiones de la UE, puede usarlas para las ventas.  
* Asigne grupos de registro de IVA de negocio en el campo **Grupo registro IVA neg.** de la ficha desplegable **Facturación** de la ficha cliente de cada cliente de la UE. También debe introducir el CIF/NIF del cliente en el campo **CIF/NIF** en la Ficha desplegable **Comercio exterior**.  

Cuando registre una venta a un cliente de otro país o región de la UE, se calculará el importe del IVA y se creará un movimiento del IVA con la información sobre el IVA de reversión y la base del IVA (importe utilizado para calcular el importe del IVA). No se registran movimientos en las cuentas del IVA de contabilidad.

Si desea utilizar la combinación del grupo de contabilización de empresas de IVA y el grupo contable de productos de IVA para informar como servicios en los informes periódicos de IVA, marque el campo **Servicio de la UE**.

> [!NOTE]  
> El campo **Servicio de la UE** solo se aplica a los informes de IVA. El campo no está relacionado con las funciones **Declaración de servicio** o **Intrastat para servicios** .

## Redondeo del IVA en los documentos

Los importes de los documentos que todavía no se han registrado se redondean y se muestran para que ajusten al redondeo final de los importes que realmente se registren. El IVA se calcula para un documento completo, lo que significa que el IVA se calcula según la suma de todas las líneas con el mismo identificador de IVA en el documento.  

## Configurar informes de IVA

Debe configurar la información sobre cómo las autoridades fiscales de su país o región requieren que presente informes de IVA. Los siguientes pasos ilustran la información más utilizada habitualmente. Sin embargo, su país o región puede requerir otros pasos. Para obtener más información, consulte el artículo correspondiente en la sección *Funcionalidad local* del panel de la izquierda.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## Consultar la [formación de Microsoft](/training/paths/process-vat-dynamics-365-business-central/) relacionada

## Consulte también .

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

[!INCLUDE[footer-include](includes/footer-banner.md)]
