---
title: "Acerca de la configuración del impuesto sobre el valor añadido | Documentos de Microsoft"
description: "Asegúrese de que calcula, registra y crea informes correctamente del IVA de las ventas y las compras."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bf06b41a87e24af9e7657dd0585d7d13e3cad1b2
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---

# <a name="setting-up-included365finlongincludesd365finlongmdmd-to-calculate-and-post-value-added-tax"></a>Configuración de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] para calcular y registrar el impuesto sobre el valor añadido
Los consumidores y las empresas pagan el impuesto sobre el valor añadido (IVA) cuando compran mercancías o servicios. El importe de IVA a pagar puede variar, dependiendo de varios factores. En [!INCLUDE[d365fin](includes/d365fin_md.md)], puede configurar el IVA para especificar las tasas que se usarán para calcular los importes de impuesto a partir de lo siguiente: 

* A quién vende  
* A quién compra  
* Qué vende  
* Qué compra  
  
Puede configurar los cálculos de IVA de forma manual, pero puede ser difícil y largo. Para que sea fácil, hemos proporcionado a una guía de configuración asistida denominada **Configuración de IVA** que le ayudará con los pasos. Es recomendable que use la guía de configuración asistida para configurar el IVA.

**Nota**: Puede usar la guía únicamente si ha creado una mi empresa, y no haya registrado transacciones que incluyen IVA. De lo contrario, sería muy sencillo usar tasas de IVA distintas por error, y crear informes relacionados con IVA inexactos.  
  
Si desea configurar cálculos del IVA, o solo desea obtener información acerca de cada paso, este tema contiene descripciones de cada paso. Estos incluyen cómo:  
  
* Configurar grupos de registro de IVA de negocio para definir las tasas de IVA para los mercados en los que opera. Los asignará a clientes y proveedores.  
* Configurar grupos de registro de IVA de producto para definir las tasas de IVA para los productos o servicios que compra o vende.  
  
   **Nota**: Los conceptos de los grupos de registro de IVA de negocio y de producto son parecidos a los grupos de registro generales. Para obtener más información, consulte [Configuraciones de grupos de registro](finance-posting-groups.md).
* Combinar grupos de registro de IVA de negocio y de producto para crear configuraciones de IVA que calculen los importes de IVA de ventas y compras.  
* Asignar grupos de registro de IVA de producto a las cuentas de contabilidad que usa para ventas, compras, productos y recursos.  

   **Nota**: Para configurar el IVA para los recursos, debe permitir la experiencia del usuario **Conjunto de aplicaciones** en la empresa. Para obtener más información, consulte [Personalizar la experiencia de Dynamics 365 for Financials](ui-experiences.md).
* Usar IVA de reversión para las transacciones entre países o regiones de la UE  
* Descripción de redondeo del IVA en los documentos  
* Configurar cláusulas para explicar el uso de tasas de IVA no estándar
* Comprobar CIF/NIF

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Usar la guía de configuración asistida Configuración de IVA para configurar el IVA (recomendado)
Es recomendable que use la guía de configuración asistida Configuración de IVA para configurar el IVA en [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

Para iniciar la guía de configuración asistida, realice los pasos siguientes:
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") y especifique **Configuración asistida**.  
2. Elija **Configuración de IVA**.

## <a name="set-up-vat-business-posting-groups"></a>Configuración de grupos de registro de IVA de negocio
El grupo de registro de IVA de negocio debería representar los mercados en los que trabaje con clientes y proveedores, y definir cómo calcular y registrar el IVA en cada mercado. Ejemplos de grupos de registro de IVA de negocio son **Nacional** y **Unión Europea (EU)**.  

Use códigos fáciles de recordar y que describan el grupo de registro de negocio, como **UE**, **No UE** o **Nacional**. El código debe ser único. Puede configurar tantos códigos como desee, pero no puede aparecer el mismo código más de una vez en una tabla.
  
Para configurar un grupo de registro de IVA de negocio, realice los pasos siguientes:

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Grupo de registro de IVA de negocio** y elija el vínculo relacionado.  
2. Rellene los campos según sea necesario.

Para configurar grupos de registro de IVA de negocio predeterminados deberá vincularlos a grupos contables de negocio. [!INCLUDE[d365fin](includes/d365fin_md.md)]asigna automáticamente el grupo de registro de IVA de negocio cuando asigne el grupo de registro de negocio relevante a un cliente, proveedor o cuenta contable. 

## <a name="set-up-vat-product-posting-groups"></a>Configurar grupos de registro de IVA de producto
Los grupos de registro de IVA de producto representan los productos y los recursos que compra o vende, y determinan cómo se calcula y se registra el IVA en función del tipo de producto o que se adquiera o se venda.
Conviene utilizar códigos que sean fáciles de recordar y que describan el tipo, como **SIN IVA** o **Cero**, **IVA10** o **Reducido** para el IVA del 10 % e **IVA25** o **Estándar** para el 25 %.

Para configurar un grupo de registro de IVA de negocio, realice los pasos siguientes:

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Grupos de registro de IVA de producto** y elija el vínculo relacionado.  
2. Rellene los campos según sea necesario.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Combinar grupos de registro de IVA en configuraciones de registro de IVA
[!INCLUDE[d365fin](includes/d365fin_md.md)] calcula los importes de IVA de ventas y compras en función de las configuraciones de registro de IVA, que son combinaciones de grupos de registro de IVA de negocio y de producto. En cada combinación puede especificar el porcentaje de IVA, el tipo de cálculo del IVA y las cuentas de contabilidad para el registro del IVA de ventas, compras y los cargos invertidos. También puede especificar si el IVA se vuelve a calcular cuando se aplica o se recibe un descuento.  

Configure tambas combinaciones como necesite. Si desea agrupar las combinaciones de configuración de registro de IVA con atributos parecidos, puede definir un **identificador de IVA** para cada grupo y asignarlo a los miembros del grupo.

Para combinar las configuraciones de registro de IVA, realice los pasos siguientes:

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Configuración de registro de IVA** y elija el vínculo relacionado.
2. Rellene los campos según sea necesario.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Asignar los grupos de registro de IVA de forma predeterminada a varias entidades
Si desea aplicar los mismos grupos de registro de IVA a varias entidades, puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] para que lo haga de forma predeterminada. Existen un par de formas de hacer esto:

* Puede asignar los grupos de registro de IVA de negocio a los grupos de registro de negocio generales, o plantillas de cliente o proveedor 
* Puede asignar los grupos de registro de IVA de negocio a grupos de registro de producto generales  

El grupo de registro de IVA de negocio o de producto se asigna cuando elige un grupo de registro de IVA de negocio o de producto para un cliente, un proveedor, un producto o un recurso.

## <a name="assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Asignar grupos de registro de IVA a cuentas, clientes, proveedores, productos y recursos individuales
En las secciones siguientes se describe cómo asignar los grupos de registro de IVA de negocio a los objetos individuales.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Para asignar grupos de registro de IVA a cuentas contables individuales 
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Plan de cuentas** y elija el vínculo relacionado.  
2. Abre la ficha **Cuenta** de la cuenta.
3. En la ficha desplegable **Registro**, en el campo **Tipo IVA**, elija **Venta** o **Compra**.  
5. Elija los grupos de registro de IVA que se usarán para la cuenta de venta o de compra.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Para asignar grupos de registro de IVA a clientes y proveedores  
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Cliente** o **Proveedor** y elija el vínculo relacionado.  
2. En la ficha **Cliente** o **Proveedor**, amplíe la ficha desplegable **Facturación**.  
3. Elija el grupo de registro de IVA de negocio.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Para asignar grupos de registro de IVA de producto a productos y recursos individuales  
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Producto** o **Recurso** y elija el vínculo relacionado.  
2. Realice una de las siguientes acciones:
* En la ficha **Producto**, expanda la ficha desplegable **Precio y registro** y haga clic en **Mostrar más** para mostrar.  
* En la ficha **Recurso**, amplíe la ficha desplegable **Facturación**.  
3. Elija el grupo de registro de IVA de producto.

## <a name="set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Configurar cláusulas para explicar el uso de tasas de IVA no estándar
Configura una cláusula de IVA para describir información acerca del tipo de IVA que se está aplicando. La legislación puede requerir la información. Una vez que haya configurado una cláusula de IVA y la haya asociado a una configuración de registro de IVA, la cláusula de IVA se muestra en los documentos de venta impresos que usan ese grupo de configuración de registro de IVA. 

Si es necesario, también puede especificar cómo traducir las cláusulas de IVA a otros idiomas. A continuación, cuando cree e imprima un documento de venta que contenga un identificador de IVA, el documento traducido incluirá la cláusula de IVA. El código de idioma especificado en la ficha Cliente determina el idioma.
  
### <a name="to-set-up-vat-clauses"></a>Para configurar las cláusulas de IVA
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Cláusulas de IVA** y elija el vínculo relacionado.  
2. En la página **Cláusulas de IVA**, cree una nueva línea.  
3. En el campo **Código**, especifique un identificador para la cláusula. Utilice este código para asignar la cláusula a grupos de registro de IVA.  
4. En el campo **Descripción**, escriba el texto que desea mostrar en los documentos que pueden incluir el IVA. En el campo **Descripción 2**, escriba texto adicional, en caso necesario. El texto se muestra en las líneas nuevas.  
5. Opcional: para asignar la cláusula de IVA a una configuración de registro de IVA inmediatamente, elija **Configuración** y, a continuación, la cláusula. Si desea esperar, puede asignar la cláusula después en la página Configuración de registro de IVA.  
6. Opcional: para especificar cómo traducir la cláusula de IVA, elija la acción **Traducciones**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Para asignar una cláusula de IVA a una configuración de registro de IVA
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Configuración de registro de IVA** y elija el vínculo relacionado.  
2. En la columna **Cláusula de IVA**, seleccione la cláusula que se usará por cada configuración de registro de IVA al que se aplique.  

### <a name="to-specify-translations-for-vat-clauses"></a>Para especificar las traducciones de las cláusulas de IVA
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Cláusulas de IVA** y elija el vínculo relacionado.  
2. Elija la acción **Traducciones**.  
3. En el campo **Código idioma**, seleccione el idioma que realizará la traducción.  
4. En los campos **Descripción** y **Descripción 2**, especifique las traducciones de las descripciones. Este texto se muestra en los documentos de informes de IVA traducidos.  
  
## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Crear una configuración de registro de IVA para usar el IVA de importación
Puede usar la característica de IVA de importación cuando necesite registrar un documento cuyo importe total sea el IVA. Se utiliza si se recibe de las autoridades fiscales una factura por el IVA de los productos importados.  
  
Para configurar los códigos del IVA de importación, realice los pasos siguientes:  
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Grupos de registro de IVA de producto** y elija el vínculo relacionado.  
2. En la página Grupos de registro de IVA de producto, configure un nuevo grupo de registro de IVA de producto para el IVA de importación.  
3. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Configuración de registro de IVA** y elija el vínculo relacionado.  
4. En la página Configuración de registro de IVA, cree una nueva línea o use una combinación de grupos de registro de IVA de negocio ya existente y el nuevo grupo de registro de IVA de producto.  
5. En el campo **Tipo cálculo IVA**, elija **Total**.  
6. En el campo **Cta. IVA acreditable**, escriba la cuenta que se utilizará para registrar el IVA de importación. Las demás cuentas son opcionales.  
  
## <a name="verify-vat-registration-numbers"></a>Comprobar CIF/NIF
Es importante que los números CIF/NIF que tiene para clientes, proveedores y contactos sean válidos. Por ejemplo, las empresas cambian a veces el estado de la deuda tributaria, y en algunos países las autoridades fiscales podrían solicitar informes, como, por ejemplo, el informe de lista de ventas de CE, que enumera los CIF/NIF que utiliza cuando realiza operaciones comerciales.  
  
La Comisión Europea proporciona el servicio de validación de número de IVA VIES en su sitio web, que es público y gratuito. Sin embargo, hay un paso adicional al ir al sitio web. [!INCLUDE[d365fin](includes/d365fin_md.md)] puede ahorrarle ese paso y permitirle utilizar el servicio VIES para validar y realizar el seguimiento de los números IVA de clientes, proveedores y contactos desde las fichas de cliente, proveedor y contacto. El servicio en [!INCLUDE[d365fin](includes/d365fin_md.md)] se denomina CIF/NIF de UE. N.º Servicio de validación. Está disponible en la página **Conexiones de servicio** y puede comenzar a usarlo con solo seleccionar una casilla. El servicio es gratuito y no es necesario registrarse.

Cuando utilice nuestro servicio, guardamos un historial de números de IVA y de comprobaciones de cada cliente, proveedor o contacto en **Registro de CIF/NIF**, por lo que le será muy fácil seguirlos. El registro es específico de cada cliente. Por ejemplo, el registro es útil para demostrar que ha comprobado que el número de IVA actual es correcto. Cuando comprueba un número de IVA, la **Identificador de solicitud** del registro refleja que ha realizado una acción. 

Puede ver el registro del registro de IVA en las fichas de cliente, proveedor o contacto, en la ficha desplegable **Facturación**, seleccionando el botón de búsqueda en **CIF/NIF**. .  

Nuestro servicio también puede ahorrarle algo de tiempo al crear un cliente o un proveedor. Si conoce el número de IVA del cliente, puede introducirlo en el campo **CIF/NIF** en las fichas de cliente o proveedor, y rellenaremos automáticamente el nombre del cliente. Algunos países también proporcionan direcciones de empresa en formato estructurado. En esos países, también completaremos la dirección.  

**Notas**: Hay un par de cosas a recordar sobre el servicio de validación de IVA VIES:

* El servicio utiliza el protocolo HTTP, lo que significa que los datos transferidos a través del servicio no están cifrados.
* Puede experimentar tiempo de inactividad de este servicio del que Microsoft no es responsable. El servicio forma parte de una amplia red de la UE de registros de IVA nacionales.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Uso del IVA de reversión para las transacciones entre países o regiones de la UE
Algunas empresas deben usar el IVA de reversión al realizar transacciones comerciales con otras empresas. Por ejemplo, esta norma se aplica a compras de países o regiones de la UE y a ventas a países o regiones de la UE.

**Nota**: Esta norma se aplica al realizar transacciones comerciales con empresas cuyo registro del IVA está en otro país o región de la UE. Si realiza transacciones comerciales directamente con consumidores de otros países o regiones de la UE, debe ponerse en contacto con las autoridades fiscales de su país para obtener información sobre la normativa de IVA vigente.  

**Sugerencia**: Puede comprobar que una empresa está sujeta a IVA en otro país de la UE utilizando el servicio de validación de CIF/NIF de la UE. El servicio está disponible gratis en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea la sección _Comprobar CIF/NIF_ en este tema.

### <a name="sales-to-eu-countries-or-regions"></a>Ventas a países o regiones de la UE
El IVA no se calcula para las ventas a empresas sujetas al IVA de otros países o regiones de la UE. Debe declarar el valor de estas ventas por separado en la declaración del IVA.
Para calcular correctamente el IVA en las ventas a países o regiones de la UE, debe:  
  
* Configurar una línea para las ventas con la misma información de las compras. Si ya ha creado líneas en la ventana Config. grupos registro IVA para las compras a países o regiones de la UE, puede usarlas para las ventas.  
* Asigne grupos de registro de IVA de negocio en el campo **Grupo registro IVA neg.** de la ficha desplegable **Facturación** de la ficha cliente de cada cliente de la UE. También debe introducir el CIF/NIF del cliente en el campo **CIF/NIF** de la ficha desplegable **Internacional**.  

Cuando registre una venta a un cliente de otro país o región de la UE, se calculará el importe del IVA y se creará un movimiento del IVA con la información sobre el IVA de reversión y la base del IVA (importe utilizado para calcular el importe del IVA). No se registran movimientos en las cuentas del IVA de contabilidad.

## <a name="understanding-vat-rounding-for-documents"></a>Descripción de redondeo del IVA en los documentos
Los importes de los documentos que todavía no se han registrado se redondean y se muestran para que ajusten al redondeo final de los importes que realmente se registren. El IVA se calcula para un documento completo, lo que significa que el IVA calculado en el documento se basa en la suma de todas las líneas con el mismo identificador de IVA en el documento.

## <a name="see-also"></a>Consulte también  
[Configuración del impuesto sobre el valor añadido no realizado](finance-setup-unrealized-vat.md)
