---
title: Crear depósitos bancarios
description: Puede realizar depósitos para mantener un registro de transacciones que contenga información que se pueda aplicar a facturas y notas de crédito pendientes.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="create-bank-deposits"></a><a name="create-bank-deposits"></a><a name="create-bank-deposits"></a><a name="create-bank-deposits"></a>Crear depósitos bancarios
> [!NOTE]
> La capacidad de crear depósitos bancarios es nueva en el lanzamiento de versiones 1 de Business Central de 2022 para muchas versiones de país o región. Si utilizaba Business Central en los Estados Unidos, Canadá o México antes de ese lanzamiento, es posible que esté usando las capacidades anteriores. Puede continuar, pero las nuevas capacidades reemplazarán a las anteriores en una versión futura. Para empezar a usar las nuevas características descritas en este artículo, su administrador puede ir a la página **Administración de características** y active **Actualización de características: conciliación y depósitos bancarios estandarizados**.  

Use la página **Depósitos bancarios** para registrar depósitos como un solo documento que registra uno o varios movimientos en una cuenta bancaria. Por lo general, los depósitos bancarios se utilizan para registrar depósitos en efectivo. La página Depósitos bancarios está disponible en el menú **Tesorería** en el área de trabajo del administrador de negocio y otras áreas de trabajo que se ocupan de la tesorería.

Los importes de los depósitos bancarios pueden proceder de varias fuentes:

* Ventas, mediante una cuenta de contabilidad para los ingresos.
* Pagos del cliente.
* Reembolsos en efectivo de los proveedores o pagos en efectivo a estos. 

Las líneas de depósito bancario contienen información sobre depósitos individuales, como cheques de clientes. El total de los importes de las líneas debe sumar el importe total del depósito.

Después de completar la información y las líneas del depósito, debe registrarlo. El registro actualizará los libros de contabilidad correspondientes. Estos libros de contabilidad incluyen el libro mayor y la contabilidad de bancos, clientes y proveedores. Los depósitos registrados se almacenan para referencia futura en la página **Depósitos bancarios registrados**.

El informe **Deposito bancario** muestra los depósitos de clientes y proveedores con el importe del depósito original, el importe del depósito que permanece abierto y el importe aplicado. El informe también muestra el importe total del depósito registrado para conciliar.

## <a name="before-you-start"></a><a name="before-you-start"></a><a name="before-you-start"></a><a name="before-you-start"></a>Antes de comenzar
Hay algunas cosas para configurar antes de poder utilizar depósitos bancarios. Debe tener lista una serie numérica y una plantilla de diario general. También debe especificar si desea registrar los importes de los depósitos bancarios como una suma total. Es decir, como un total de todos los importes en las líneas de depósito. De lo contrario, cada línea se registra como un movimiento individual. El registro de un depósito como un único movimiento de banco puede facilitar la conciliación bancaria.

### <a name="number-series-and-lump-sum-deposits"></a><a name="number-series-and-lump-sum-deposits"></a><a name="number-series-and-lump-sum-deposits"></a><a name="number-series-and-lump-sum-deposits"></a>Serie numérica y depósitos de suma total
Debe configurar una serie numérica para depósitos bancarios y luego especificar la serie en el campo **Núms. depósitos bancarios** en la página **Configuración de ventas y cobros**. Para obtener más información, consulte [Crear serie numérica](ui-create-number-series.md). 

Además, en la página **Configuración de ventas y cobros**, si desea registrar depósitos como sumas totales en lugar de líneas individuales, active el botón de alternancia **Registrar depósitos bancarios como suma total**. El registro de un depósito como suma total, que crea un movimiento de banco por el importe total del depósito, puede facilitar la conciliación bancaria.

### <a name="general-journal-templates-for-bank-deposits"></a><a name="general-journal-templates-for-bank-deposits"></a><a name="general-journal-templates-for-bank-deposits"></a><a name="general-journal-templates-for-bank-deposits"></a>Libros de diario general para depósitos bancarios
También debe crear una plantilla de diario general para depósitos. Utiliza diarios generales para registrar movimientos de cuentas bancarias, de clientes, de proveedores, de activos fijos y de contabilidad. Las plantillas del diario diseñan el diario general para que se adapte al propósito de su trabajo. Es decir, los campos de la plantilla del diario son exactamente los que necesita. 

Los depósitos serán recibos de efectivo, así que es posible que desee reutilizar su serie numérica para diarios de recibos de efectivo. Como alternativa, si tiene que distinguir entre depósitos bancarios y movimientos del diario de recibos de efectivo, utilice una serie numérica diferente.

También deberá crear un trabajo por lotes para la plantilla. Para crear un trabajo por lotes, en la página **Libros diario general**, elija la acción **Lotes**. Para obtener más información, consulte [Usar plantillas y secciones de diario](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="dimensions-on-bank-deposit-lines"></a><a name="dimensions-on-bank-deposit-lines"></a><a name="dimensions-on-bank-deposit-lines"></a><a name="dimensions-on-bank-deposit-lines"></a>Dimensiones en líneas de depósito bancario
Las líneas del depósito bancario usarán automáticamente las dimensiones predeterminadas que especificó en los campos **Cód. departamento** y **Cód. grupo clientes**. Cuando elige **Cliente** o **Proveedor** en el campo **Tipo mov.**, las dimensiones que se especifican para el cliente o proveedor sustituirán a las predeterminadas. Puede cambiar las dimensiones en las líneas, según sea necesario.

> [!TIP]
> Las dimensiones en las líneas se establecen de acuerdo con las prioridades de dimensión predeterminadas. Las dimensiones de la línea tenían prioridad sobre las dimensiones de la cabecera. Para evitar conflictos, puede crear reglas que prioricen cuándo utilizar una dimensión según el origen. Si desea cambiar la forma en que se priorizan las dimensiones, puede cambiar su ranking en la página **Prioridades de dimensión predeterminadas**. Para obtener más información, consulte [Para configurar prioridades de dimensiones predeterminadas](finance-dimensions.md#to-set-up-default-dimension-priorities).

## <a name="create-a-bank-deposit"></a><a name="create-a-bank-deposit"></a><a name="create-a-bank-deposit"></a><a name="create-a-bank-deposit"></a>Crear un depósito bancario
1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Depósitos bancarios** y luego elija el vínculo relacionado.
2. Elija **Nuevo** para abrir la página **Deposito bancario**. 
3. Seleccione la plantilla de diario general que creó para los depósitos bancarios.  

    > [!NOTE]
    > Si la plantilla de diario general tiene más de un lote, se le pedirá que elija uno.

4. En el campo **N.º cuenta bancaria**, escoja la cuenta bancaria en la que hacer el depósito.

    > [!TIP]
    > Puede volver a comprobar que está depositando en la cuenta correcta mediante las acciones **Ficha banco** y **Movs. bancos** para buscar los movimientos de la cuenta bancaria seleccionada. Por ejemplo, para ver si se hicieron depósitos similares en la cuenta.

5. En el campo **Total importe depósito**, introduzca el importe total del depósito. Este total debe ser la suma de los importes en todas las líneas.
6. Rellene los campos restantes según sea necesario. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    La fecha en el campo **Fecha registro** y las dimensiones en los campos **Cód. departamento** y **Cód. grupo clientes** se asignarán a las líneas que cree para el depósito bancario. Puede cambiarlos si lo necesita. 

7. Dependiendo de si desea registrar el depósito bancario como una suma total o cada línea individualmente en el movimiento del banco, active o desactive el botón de alternancia **Registrar como suma total**. La configuración predeterminada proviene del mismo botón de alternancia de la página **Configuración de ventas y cobros**.

    > [!NOTE]
    > El campo **Cód. divisa** muestra la divisa que se especifica para la cuenta bancaria que eligió. No puede elegir una divisa diferente.

8. En la ficha desplegable **Líneas**, cree una nueva línea para cada pago en efectivo que desee depositar.
9. En el campo **Tipo mov.**, especifique dónde se originó el pago. Para los depósitos bancarios, el tipo suele ser **Cliente** o **Proveedor**. 

    > [!NOTE]
    > También puede registrar un pago en efectivo a un proveedor. Para ello, elija **Proveedor** y luego introduzca el importe del pago como un número negativo en el campo **Importe haber** en la línea. 

10. En el campo **N.º documento**, introduzca el número de documento de la factura del proveedor desde la que se originó el importe del haber. Puede usar un número de documento para cada línea o el mismo número para todas las líneas.

    > [!TIP]
    > Por lo general, no es necesario completar el campo **Tipo documento** para entradas financieras. Por ejemplo, si va a depositar efectivo de la venta de un día, deje el campo en blanco. Si va a depositar efectivo de un pago de cliente, elija **Pago**.

11. Si va a depositar un pago en efectivo para una factura de cliente específica, elija la acción **Liquidar movs.** y, a continuación, introduzca el número de factura en el campo **Liq. por id**. 
12. Si está listo para registrar el depósito bancario, elija la acción **Registrar**.

    > [!TIP]
    > Antes de registrar el depósito, puede usar la acción **Informe de prueba** para revisar sus datos. El informe mostrará si hay algún problema, como datos que faltan, que impida el registro.  

## <a name="finding-posted-bank-deposits"></a><a name="finding-posted-bank-deposits"></a><a name="finding-posted-bank-deposits"></a><a name="finding-posted-bank-deposits"></a>Encontrar depósitos bancarios registrados
La página **Depósitos bancarios registrados** indica los depósitos anteriores de su empresa. En la lista puede revisar los comentarios y dimensiones que se especificaron para los depósitos. Puede abrir el depósito bancario para ver más detalles, y desde ahí puede investigar más. Por ejemplo, puede elegir la acción Buscar movimiento para ver los movimientos de banco registrados. Desde el movimiento de banco, puede encontrar su movimiento de contabilidad registrado correspondiente.

Si desea buscar todos los movimientos de contabilidad para las líneas de depósito registradas, vaya a la página **Registro movs. contabilidad** y use la acción **Contabilidad**. Allí encontrará todos los movimientos de contabilidad, incluidos los movimientos de clientes y proveedores.

## <a name="reversing-a-posted-bank-deposit"></a><a name="reversing-a-posted-bank-deposit"></a><a name="reversing-a-posted-bank-deposit"></a><a name="reversing-a-posted-bank-deposit"></a>Reversión de un depósito bancario registrado
Para revertir un depósito registrado, vaya a la página **Registro movs. contabilidad**, busque el registro para el depósito y luego elija la acción **Revertir mov.**.

> [!NOTE]
> Solo puede revertir un registro que contenga un único tipo de movimiento. Es decir, el registro debe contener solo movimientos de clientes o de proveedores, pero no ambos. Si un registro contiene ambos, debe revertir manualmente el depósito.      

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Configurar las finanzas](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



