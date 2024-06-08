---
title: Conciliar cuentas bancarias
description: Aprenda a conciliar transacciones en Business Central con transacciones en extractos de su banco.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 10/24/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---
# <a name="reconcile-bank-accounts"></a>Conciliar cuentas bancarias

La conciliación bancaria ayuda a garantizar que lo que hay en sus libros coincida con los estados de cuenta que recibe de su banco. La conciliación de cuentas bancarias compara y hace coincidir las entradas en las cuentas bancarias que ha configurado en [!INCLUDE[prod_short](includes/prod_short.md)] con transacciones bancarias en su banco. Luego, la conciliación puede contabilizar los saldos en sus cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)] para ponerlos a disposición de los directores de finanzas. La conciliación bancaria también es una forma práctica de descubrir y resolver pagos faltantes y errores de contabilidad.

Este artículo describe cómo realizar la conciliación bancaria en la la página **Conciliación banco**.

Sin embargo, también puede conciliar bancos en la página **Diario de conciliación de pagos** al procesar los pagos. Los movimientos de cuenta bancaria abiertos relacionados con los movimientos de los clientes aplicados se cerrarán al elegir la acción **Registrar pagos y conciliar banco**. Eso concilia automáticamente la cuenta bancaria para los pagos que registró mediante el diario. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Las versiones de EE. UU. ofrecden la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no permite importar archivos de extracto bancario. Para usar esta página en lugar de la página **Conciliación banco**, elimine la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección [Conciliar cuentas bancarias](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) en Funcionalidad local para Estados Unidos.

Las líneas de la página **Conciliación banco** se dividen en dos paneles. El panel de **Líneas de extracto bancario** muestra tanto las transacciones bancarias como los movimientos con pagos pendientes. El panel **Movimientos bancarios** muestra los movimientos del banco interno.

## <a name="about-bank-reconciliation"></a>Acerca de la conciliación bancaria

La conciliación de transacciones en extractos desde movimientos de banco en [!INCLUDE[prod_short](includes/prod_short.md)] se denomina *correspondencia*. Hay tres formas de hacer coincidir las transacciones con las entradas bancarias:

* Automáticamente, mediante la acción **Conciliar automáticamente**.

* Automáticamente, mediante la acción **Conciliar con Copilot**.

  Esta acción está disponible como parte de la función de asistencia (vista previa) de conciliación bancaria, que es una función impulsada por IA. [Obtenga más información acerca de la asistencia de conciliación de cuentas bancarias](bank-reconciliation-with-copilot.md).
* Manualmente, seleccionando líneas en ambos paneles para vincular cada línea del extracto bancario a uno o más movimientos de banco relacionados y, a continuación, utilizar la acción **Conciliar manualmente**.

La casilla de verificación **Liquidado** se selecciona en las líneas en las que los movimientos coinciden. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md). Si introduce una fecha de finalización del estado de cuenta en la conciliación bancaria después de hacer coincidir sus líneas con las entradas, [!INCLUDE [prod_short](includes/prod_short.md)] deshará las coincidencias para las líneas y las entradas posteriores a esa fecha.

> [!NOTE]
> Después de introducir una fecha en el campo **Fecha extracto**, la página **Conciliación banco** filtra las entradas del libro mayor bancario para mostrar solo las entradas hasta esa fecha. Solo puede registrar conciliaciones bancarias con entradas del libro mayor bancario en o antes de la fecha de finalización del estado de cuenta. El filtro garantiza que su libro mayor bancario esté equilibrado con su extracto bancario en la fecha de finalización del extracto, siendo la diferencia los pagos pendientes y los cheques.

Cuando el valor en el campo **Saldo total** en el panel **Líneas de extracto bancario** es igual al valor total del campo **Saldo a conciliar**, además del campo **Saldo últ. extracto**, en el panel **Movs. bancos**, puede seleccionar la acción **Registrar**. Los movimientos del libro mayor de banco no coincidentes permanecerán en la página, lo que indica las discrepancias que debe resolver para conciliar el banco.

Cualquier línea que no pueda coincidir, indicada por un valor en el campo **Diferencia**, permanecerá en la página **Conciliación banco** después de registrar. Representan algún tipo de discrepancia que debe resolver antes de completar la conciliación de banco. La siguiente tabla describe algunas situaciones comerciales típicas que pueden causar diferencias.

| Diferencia | Motivo | Resolución |
|------------|--------|------------|
| Una transacción en la cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)] no figura en el extracto de cuenta. | La transacción bancaria no se creó aunque se realizó un registro en [!INCLUDE[prod_short](includes/prod_short.md)]. | Cree la transacción faltante (o solicite a un deudor que la realice). Luego, vuelva a importar el archivo del extracto bancario o ingrese la transacción manualmente. |
| Una transacción en el extracto de cuenta no existe como documento o línea de diario en [!INCLUDE[prod_short](includes/prod_short.md)]. | Se realizó una transacción bancaria sin un registro correspondiente en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, un registro de línea de diario para un gasto. | Crea y registra el movimiento que falta. Para conocer una forma rápida de iniciar esto, consulte [Para crear movimientos faltantes para que coincidan con las transacciones bancarias con](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Una transacción en el banco interno corresponde a una transacción bancaria, pero cierta información es demasiado diferente para dar una coincidencia. | La información, como el importe o el nombre del cliente, se ingresó de manera diferente en la transacción bancaria o el registro interno. | Revise la información y luego haga coincidir manualmente las dos. De manera opcional, corrija la falta de coincidencia. |

Debe resolver las diferencias, por ejemplo, creando los movimientos que faltan y corrigiendo información que no coincide, o haciendo transacciones de dinero que faltan, hasta que se complete y se registre la conciliación de banco.

Puede rellenar el panel **Líneas de extracto bancario** en la página **Conciliación banco** de la siguiente manera:

* Automáticamente, utilizando la función **Importar extracto de cuenta** para rellenar el panel **Líneas de los extractos de cuenta** con transacciones bancarias basándose en un archivo importado que proporciona el banco.
* Manualmente, usando la función **Proponer líneas** para rellenar el panel de **Líneas del extracto de cuenta** basándose en las facturas en [!INCLUDE[prod_short](includes/prod_short.md)] que tienen pagos pendientes.

## <a name="add-bank-statement-lines-by-importing-a-bank-statement"></a>Agregar líneas de extractos de bancos importando un extracto bancario

El panel de las **Líneas del extracto de cuenta** completará con las transacciones bancarias de acuerdo con un archivo o secuencia importados proporcionados por el banco.

Para importar extractos bancarios como fuentes bancarias, debe configurar el servicio Envestnet Yodlee Bank Feed. La configuración incluye vincular las cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)] a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> También puede importar archivos de extractos de cuenta en formato delimitado por coma o punto y coma (.CSV). Use la configuración asistida **Configurar un formato de archivo de extracto de cuenta** para definir formatos de importación de extractos de cuenta y adjuntar el formato a una cuenta bancaria. A continuación, puede usar estos formatos cuando importe extractos de cuenta en la página **Conciliación de cuentas bancarias**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conciliación de cuentas bancarias** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Cód. cuenta banco**, seleccione la cuenta de banco que desee. Los movimientos de cuentas bancarias que existan en la cuenta aparecen en el panel **Movs. bancos**.
4. En el campo **Fecha extracto**, escriba la fecha del extracto del banco.
5. En el campo **Saldo final extracto** escriba el saldo del extracto del banco.
6. Si tiene un archivo de extracto bancario seleccione la acción **Importar extracto bancario**.
7. Busque el archivo y haga clic en el botón **Abrir** para importar las transacciones bancarias en el panel de las **Líneas del extracto de cuenta** en la página **Conciliación banco**.

## <a name="to-fill-in-bank-reconciliation-lines-with-the-suggest-lines-action"></a>Para rellenar las líneas de conciliación bancarias con la acción Proponer líneas

El panel de las **Líneas del extracto de cuenta** se completará de acuerdo con las facturas en [!INCLUDE[prod_short](includes/prod_short.md)] que tienen pagos pendientes.  

1. En la página **Conciliación banco** seleccione la acción **Proponer líneas**.
2. En el campo **Fecha inicial** escriba la fecha de registro más antigua para la conciliación de los movimientos.
3. En el campo **Fecha final**, escriba la fecha de registro que se usó por última vez para la conciliación de los movimientos.

    > [!NOTE]
    > Normalmente, la fecha de finalización coincidirá con la fecha especificada en el campo **Fecha extracto**. Sin embargo, si desea conciliar transacciones solo para una parte de un periodo, puede introducir una fecha de finalización diferente.

4. Si no desea que los asientos del libro mayor de cuentas bancarias incluyan asientos invertidos abiertos no conciliados, seleccione la opción de alternancia **Excluir entradas invertidas**. De manera predeterminada, la lista de entradas del libro mayor de cuentas bancarias incluirá entradas invertidas hasta la fecha del estado de cuenta.
5. Elija el botón **Aceptar**.

## <a name="match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Conciliar automáticamente las líneas de extracto bancario con movimientos de la cuenta

La página **Conciliación banco** ofrece una funcionalidad de correspondencia automática basada en una coincidencia de texto en una línea del extracto de cuenta (panel izquierdo) con texto en uno o más movimientos de contabilidad (panel derecho). Puede sobrescribir correspondencias automáticas sugeridas y puede optar por no utilizar correspondencia automática. Para obtener más información, consulte [Conciliar las líneas de extracto de cuenta con los movimientos de banco manualmente](#match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Puede investigar la base de las coincidencias utilizando la acción **Detalles de correspondencia**. Por ejemplo, los detalles incluirán los nombres de los campos que contenían valores coincidentes.  

1. En la página **Conciliación banco** seleccione la acción **Conciliar automáticamente**. La página **Conciliar movimientos** se abre.
2. En el campo **Tolerancia de datos de transacción (días)**, especifique el intervalo de días antes y después de la fecha de registro del movimiento del banco dentro de la cual la acción buscará las fechas de transacciones coincidentes en el extracto bancario.

    Si especifica cero o deja el campo en blanco la acción **Conciliar automáticamente** buscará solo por las fechas de transacción coincidentes en la fecha de registro de movimientos de la cuenta.
3. Elija el botón **Aceptar**.

    Las líneas están codificadas por colores para que sea más fácil entender qué hacer con ellas. Las líneas del extracto bancario y los movimientos la cuenta que coinciden con la reconciliación bancaria actual cambian a una fuente verde en negrita. Los asientos del libro mayor de cuentas bancarias emparejados con otras conciliaciones bancarias se muestran en letra azul en cursiva.
4. Para eliminar un coincidencia seleccione la línea de extracto de cuenta y, a continuación, seleccione la acción **Eliminar conciliación**.

> [!TIP]
> Puede utilizar una combinación de correspondencia manual y automática. Si correspondido entradas manualmente, la correspondencia automática no sobrescribirá sus selecciones.

## <a name="match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Conciliar manualmente las líneas de extracto bancario con movimientos de la cuenta

> [!TIP]
> Al cotejar líneas y entradas manualmente, las acciones **Mostrar todo**, **Mostrar entradas invertidas**, **Ocultar entradas invertidas** y **Mostrar no coincidentes** pueden facilitar la obtención de una visión general. De forma predeterminada, las entradas del libro mayor de cuentas bancarias no incluyen entradas invertidas no coincidentes. Para incluir estas entradas en la lista y emparejarlas manualmente, elija la acción **Mostrar entradas invertidas**. Si elige ocultar las entradas invertidas después de haber realizado una o más coincidencias, las entradas coincidentes aún se muestran.

> [!NOTE]
> No puede publicar una conciliación bancaria si realiza una conciliación de varios a uno y los montos combinados contienen diferencias. Esto es cierto incluso si el saldo de las diferencias combinadas es cero.
>
> Este es un ejemplo de una coincidencia de muchos a uno que tiene diferencias. El valor de 200 para la entrada 1 del extracto bancario se compara con dos entradas del libro mayor bancario que tienen un valor total de 180. La diferencia es 20. El valor de 350 para del extracto bancario 2 se compara con otras dos entradas del libro mayor bancario que tienen un valor total de 370. La diferencia es -20, que equilibra el valor de 20 para el extracto bancario 1.  
>
> Para contabilizar una conciliación bancaria con diferencias en las líneas, contabilice las diferencias y luego cotejelas con los asientos contabilizados.

1. En la página **Conciliar banco** seleccione una línea no conciliada en el panel **Líneas de extracto bancario**.
2. En el panel **Movs. bancos** seleccione uno o más movimientos de la cuenta que pueden coincidir con la línea del extracto bancario seleccionada. Para elegir varias líneas, seleccione y mantenga presionada la tecla <kbd>CTRL</kbd> y luego elija las líneas.

   > [!TIP]
   > También puede corresponder manualmente varias líneas de extracto bancario con un registro de movimiento de cuenta bancaria. Por ejemplo, esto podría ser útil si su depósito bancario contenía varios métodos de pago, como tarjetas de crédito de diferentes emisores, y su banco los enumera como líneas separadas.
3. Seleccione la acción **Conciliar manualmente**.

    La línea del extracto de cuenta seleccionada y los movimientos de la cuenta de banco seleccionados cambian a fuente verde, y la casilla **Conciliado** en el panel derecho está seleccionado.
4. Repita los pasos 1 a 3 para todas las líneas del extracto de cuenta que no coinciden.

> [!TIP]
> Para eliminar un coincidencia seleccione la línea de extracto de cuenta y, a continuación, seleccione la acción **Eliminar conciliación**. Si ha correspondido varias líneas de extracto bancario con un registro de movimiento y necesita eliminar una o más de las líneas coincidentes, todas las correspondencias manuales se eliminan para el registro de movimiento cuando elija **Eliminar conciliación**.

## <a name="validate-your-bank-reconciliation"></a>Validar su conciliación bancaria

Para comprobar la conciliación de su cuenta bancaria antes de publicarla, utilice la acción **Informe de prueba** para tener una vista previa de la conciliación. El siguiente informe está disponible en los siguientes contextos:

* Cuando esté preparando una conciliación bancaria en la página **Conciliación de cuenta bancaria**.
* Cuando concilia pagos en la página **Diarios de conciliación de pagos**.

Las líneas que no se pueden emparejar permanecen en la página **Reconciliación de cuenta bancaria** después de la contabilización. Estas líneas contienen un valor en el campo **Diferencia**. La diferencia representa una discrepancia que debe resolver antes de completar la conciliación de banco. La siguiente tabla describe algunas situaciones comerciales típicas que pueden causar diferencias.

| Diferencia | Motivo | Resolución |
|------------|--------|------------|
| Una transacción en la cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)] no figura en el extracto de cuenta. | La transacción bancaria no se creó aunque se realizó un registro en [!INCLUDE[prod_short](includes/prod_short.md)]. | Cree la transacción faltante (o solicite a un deudor que la realice). Luego, vuelva a importar el archivo del extracto bancario o ingrese la transacción manualmente. |
| Una transacción en el extracto de cuenta no existe como documento o línea de diario en [!INCLUDE[prod_short](includes/prod_short.md)]. | Se realizó una transacción bancaria sin un registro correspondiente en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, un registro de línea de diario para un gasto. | Crea y registra el movimiento que falta. Para conocer una forma rápida de iniciar esto, consulte [Para crear movimientos faltantes para que coincidan con las transacciones bancarias con](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Una transacción en el banco interno corresponde a una transacción bancaria, pero cierta información es demasiado diferente para dar una coincidencia. | La información, como el importe o el nombre del cliente, se ingresó de manera diferente en la transacción bancaria o el registro interno. | Revise la información y luego haga coincidir manualmente las dos. De manera opcional, corrija la falta de coincidencia. |

Debe resolver las diferencias, por ejemplo, creando los movimientos que faltan y corrigiendo información que no coincide, o haciendo transacciones de dinero que faltan, hasta que se complete y se registre la conciliación de banco.

> [!NOTE]
> La página de conciliación bancaria y el informe de prueba asumen que solo está conciliando dentro del período hasta la fecha de finalización del estado de cuenta. Si hace coincidir una línea de extracto bancario con una entrada del libro mayor bancario antes de ingresar una fecha de finalización del extracto y luego ingresa una fecha de finalización posterior a la fecha de finalización de la entrada del libro mayor bancario, los datos en el informe de prueba serán incorrectos.

La siguiente tabla describe los campos del informe de prueba que pueden ayudarlo a completar la conciliación bancaria.

|Campo  |Descripción  |
|---------|---------|
|Fecha extracto| La fecha especificada en el campo **Fecha del extracto** en la página **Conciliación de cuenta bancaria**.|
|Saldo últ. extracto|El saldo especificado en el campo **Saldo del último del extracto** en la página **Conciliación de cuenta bancaria**. Esto se completa automáticamente a partir de la conciliación más reciente para la misma cuenta bancaria. El valor es cero si esta es su primera conciliación de cuenta bancaria.|
|Saldo final extracto|El saldo especificado en el campo **Saldo final del extracto** en la página **Conciliación de cuenta bancaria**. |
|Número de cuenta de mayor <*número*> Saldo a la <*fecha*> | El saldo de la cuenta de mayor en la fecha de finalización del extracto. Este es el saldo sin filtrar a esa fecha. Si su banco usa su moneda local, este saldo debe ser el mismo que el saldo de su cuenta bancaria (que se muestra en el lado derecho del encabezado del informe) cuando haya conciliado todas las líneas del estado de cuenta. Un **()** vacío en el nombre de este campo significa que su banco utiliza la moneda local.<br><br>Una discrepancia en este y los campos anteriores podría indicar que ha contabilizado directamente en la cuenta de mayor o que está utilizando la misma cuenta de mayor para varios bancos, lo cual no se recomienda. Los bancos están vinculados al libro mayor a través del grupo de contabilización de cuentas bancarias especificado para la cuenta.<br><br>El informe de prueba muestra una advertencia si tiene publicaciones directas, incluso si el saldo de la publicación es cero. Las contabilizaciones directas que no se equilibran a menudo dan lugar a diferencias acumuladas para futuras conciliaciones bancarias. Debe verificar el saldo del libro mayor y las entradas del libro mayor antes de registrar la conciliación bancaria. Para obtener más información sobre la publicación directa, vaya a [Evitar la publicación directa](#avoid-direct-posting).|
|Número de cuenta de mayor <*número*> Saldo (<*ML*>) a la <*fecha*>| El saldo de la cuenta de mayor en la fecha de finalización del extracto en la moneda local. El saldo se convierte a la moneda de la cuenta bancaria utilizando el tipo de cambio vigente en la fecha de finalización del estado de cuenta. Este es el saldo sin filtrar a esa fecha. Compare esto con el **Número de cuenta de mayor <* número *> Saldo en el campo <* fecha*>* si su banco utiliza una moneda extranjera. El valor en el campo Número de cuenta de mayor <* número *> Saldo a la <* fecha*> para la moneda local puede diferir ligeramente porque la conversión de moneda puede generar pequeñas diferencias. El saldo de su banco debe estar muy cerca de este saldo.  |
|Saldo de cuenta bancaria a <*fecha*>| El saldo de la cuenta bancaria la fecha de finalización del extracto.|
|Suma de las diferencias    | La suma de las diferencias para las líneas del extracto. Para acceder a los detalles, active la opción **Imprimir transacciones pendientes** cuando ingresa criterios para el informe. Una diferencia es una línea de extracto bancario que no coincide completamente con una o más entradas del libro mayor bancario. No puede contabilizar una conciliación de cuenta bancaria que tenga diferencias. Puede registrar una conciliación bancaria que contenga entradas de libro mayor que no coincidan con las líneas del extracto. Este valor se muestra en el campo **Transacciones bancarias pendientes** y en una sección separada si activa la opción Imprimir transacciones pendientes.      |
|Saldo extracto     | El valor especificado en el campo **Saldo final del extracto** en la página **Conciliación de cuenta bancaria**.  |
|Transacciones bancarias pendientes     | La suma de los asientos contables bancarios no conciliados y sin cheques que tienen una fecha de contabilización igual o anterior a la fecha de finalización del estado de cuenta. Esto sucede cuando registra transacciones antes de que se registren en su banco. Por ejemplo, al final de un período. Cuando crea la siguiente conciliación bancaria, puede conciliar estas entradas.        |
|Cheques pendientes     | La suma de los asientos contables bancarios no conciliados para cheques que tienen una fecha de contabilización igual o anterior a la fecha de finalización del estado de cuenta. Esto sucede cuando registra transacciones antes de que se registren en su banco. Por ejemplo, esto puede suceder con los cheques si un proveedor no cobra un cheque en el mismo período en que lo registró. Cuando crea la siguiente conciliación bancaria, puede conciliar estas entradas.        |
|Saldo bancos     | La suma de los valores del saldo final del extracto bancario, las transacciones bancarias pendientes y los cheques pendientes. Después de gestionar todas las diferencias en las entradas coincidentes, este saldo coincide con su saldo bancario. Por ejemplo, ha contabilizado todas las entradas coincidentes, así como las entradas que no pudo coincidir para este extracto bancario. Ahora puede contabilizar la conciliación.        |

> [!TIP]
> Si ejecuta el **Informe de prueba** desde la página **Diario de conciliación de pagos**, [!INCLUDE [prod_short](includes/prod_short.md)] calcula el valor en el **Estado de cuenta Saldo final** como sigue:
>
> * Saldo último estado de cuenta + suma de todas las líneas en el diario de conciliación de pagos
>
> Puede utilizar el valor para compararlo con su extracto bancario.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines"></a>Para crear movimientos no existentes para coincidir con las líneas del extracto de cuenta

En ocasiones, un extracto bancario contiene importes por los intereses y recargos cobrados. Dichas líneas del extracto de cuenta no pueden conciliarse porque no existen movimientos relacionados en [!INCLUDE[prod_short](includes/prod_short.md)]. A continuación, deberá registrar una linea de diario para cada transacción para crear un movimiento relacionado que pueda coincidir.

1. En la página **Conciliación banco** seleccione la acción **Transferir al diario general**.  
2. En la página **Transf. conciliación al diario**, especifique el diario general que se usará y haga clic en **Aceptar**.

    La página **Diario general** se abre una ventana con nuevas líneas del diario para las líneas de extracto bancario con los movimientos que faltan.
3. Complete la línea del diario con la información, como la cuenta de contrapartida. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  
4. Para revisar el resultado de la publicación antes de publicar, elija la acción **Informe de prueba** y, a continuación, elija una opción para acceder al informe. El informe **Estado de cuenta bancaria** muestra los mismos campos que en el encabezado de la página **Conciliación de cuenta bancaria**.
5. Seleccione la acción **Registrar**.

    Una vez registrado el movimiento, empareje con él la línea de extracto de cuenta.
6. Actualice o reabra la página **Conciliación banco**. El nuevo movimiento aparecerá en el panel **Movs. bancos**.
7. Concilie la línea del extracto bancario al movimiento de la cuenta manual o automáticamente.

## <a name="find-outstanding-transactions-in-previous-periods"></a>Encontrar transacciones pendientes en periodos anteriores

Puede utilizar el informe Extracto bancario para buscar transacciones pendientes en períodos anteriores. Las transacciones pendientes se abrieron antes de la fecha del estado de cuenta y no se han cerrado, o se cerraron después de publicar la conciliación bancaria.

Cuando ejecuta el informe de extracto bancario desde la página Lista de extractos bancarios, puede activar la opción **Entradas pendientes** y el informe incluirá una sección que enumera las entradas pendientes.

**Ejemplo** Tenemos las entradas A, B y C del libro mayor de cuentas bancarias en nuestra cuenta bancaria para el mes de agosto. Cuando conciliamos nuestra cuenta bancaria de agosto, encontramos una línea de extracto bancario que coincide con la entrada A, pero ninguna para B y C. Así que publicamos la conciliación con la entrada A conciliada y B y C como entradas pendientes.

En septiembre, recibimos un pago por la entrada B y decidimos conciliar nuestra cuenta bancaria. Si ejecutamos el informe del extracto bancario antes de publicar la conciliación, tendremos una transacción conciliada y otra pendiente.

Si imprimimos el informe de agosto, tendremos transacciones pendientes para nuestras entradas B y C, aunque cerramos la entrada B en septiembre.

## <a name="undo-a-bank-account-reconciliation"></a>Deshacer una conciliación de cuenta bancaria

Si descubre un error en una conciliación bancaria registrada, puede utilizar la acción **Deshacer** en la página **Lista de extractos de cuenta bancaria** para corregirlo. Cuando deshaga una conciliación bancaria publicada, las entradas se mueven a la página **Conciliación bancaria** y se marcarán como **Abierto**, lo que significa que no están conciliadas. A continuación, puede corregir la conciliación bancaria y volver a contabilizarla.

> [!NOTE]
> En la versión norteamericana, para usar la función Deshacer para conciliaciones bancarias y extractos bancarios publicados, debe activar el control de alternancia **Reconocimiento banc con auto. coinc.** en la página **Configuración del libro mayor**. La función Deshacer no está disponible para extractos bancarios publicados desde hojas de trabajo de conciliación bancaria.

### <a name="reusing-the-bank-statement-number"></a>Reutilizar el número de extracto bancario

El número de extracto bancario utilizado para la nueva conciliación bancaria se toma de la cuenta bancaria al igual que el último extracto del saldo. Puede cambiar estos valores antes de iniciar una nueva conciliación bancaria. Sin embargo, cuando crea una nueva conciliación bancaria, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si el número de extracto ya está asignado a un extracto bancario registrado. Si el número está en uso, pero desea que el nuevo extracto bancario lo use en su lugar, puede usar **Declaración de cambio No.** en la página **Cuenta bancaria Reconciliación**.

### <a name="examples"></a>Ejemplos

Los siguientes ejemplos muestran cómo corregir un error en una conciliación bancaria registrada con o sin el mismo número de extracto.

#### <a name="example-1"></a>Ejemplo 1

Hizo conciliaciones bancarias para enero, febrero y marzo. El número de extracto bancario era 100 para marzo. Más tarde, descubre que marzo solo incluyó entradas hasta el 30, lo que significa que faltan entradas para el 31. Por lo tanto, debe volver a realizar la conciliación bancaria de marzo. En este caso, abriremos la página **Cuenta bancaria Declaración**, elija el extracto de marzo y luego elija **Deshacer**. 

La nueva conciliación bancaria recibe el estado de cuenta número 101. Para reasignar el número 100, elija **Declaración de cambio No.** e introduzca **100**. 

> [!TIP]
> Recuerde establecer la fecha de finalización del estado de cuenta adecuada (en este ejemplo, es el 31 de marzo) y editar el campo **Saldo último extracto**. 

#### <a name="example-2"></a>Ejemplo 2

Hizo conciliaciones bancarias para enero, febrero, junio y julio. Descubre que febrero fue incorrecto. Supongamos que tiene la declaración número 100. Como en el Ejemplo 1, utiliza la declaración de deshacer y cambiar No. Acciones para cambiar el número de extracto como en el ejemplo # 1 anterior y ahora puede rehacer la conciliación bancaria de febrero.  

Después de contabilizar la conciliación bancaria corregida de febrero, en la tarjeta de cuenta bancaria correspondiente, el campo **Última Declaración No.** mostrará **100** y el campo **Saldo último extracto** mostrará el saldo final del estado de cuenta de febrero. 

Si la próxima conciliación bancaria que realice es para marzo, [!INCLUDE[d365fin](includes/d365fin_md.md)] asignará 101 como el número de declaración y le dará el **Saldo último extracto** correcto.

Si la próxima conciliación bancaria que realice es para agosto, considere cambiar los valores en los campos **Última Declaración No.** y **Saldo último extracto** en la tarjeta **Cuenta bancaria** antes de crear la siguiente conciliación bancaria, o utilice la acción **Declaración de cambio No**. y también cambie el valor en el campo **Saldo último extracto** en la página de conciliación bancaria.

> [!NOTE]
> El número de estado de cuenta es importante cuando realiza conciliaciones bancarias con archivos CAMT importados que contienen números de estado de cuenta o cuando realiza conciliaciones basadas en extractos bancarios impresos. Si acaba de descargar una serie de transacciones bancarias de su banco en línea, el número de extracto no suele ser importante.  
>
> El último estado de cuenta del saldo se guarda en la cuenta bancaria para minimizar los errores al realizar conciliaciones bancarias, pero también es editable, lo que le permite realizar conciliaciones bancarias en el orden que desee. Esto también significa que si deshace un extracto bancario, es posible que el nuevo saldo final no sea el último saldo del siguiente extracto bancario. No existe una función que le permita mover un saldo hacia adelante a todos los extractos bancarios posteriores, así que tenga esto en cuenta cuando use Deshacer.  

## <a name="avoid-direct-posting"></a>Evitar el registro directo

No utilice una cuenta de mayor que permita la contabilización directa en su grupo de contabilización de cuenta bancaria. La contabilización directa interrumpirá la conexión entre el asiento del libro mayor de la cuenta bancaria y el asiento del libro mayor de la cuenta del L/M. Cuando concilia su cuenta bancaria, las entradas registradas directamente en la cuenta de mayor no se incluirán y será difícil completar la conciliación.

Este error ocurre a menudo al ingresar un saldo inicial para una cuenta bancaria. Es importante que no registre el saldo de apertura directamente en el libro mayor. Los asientos en la cuenta de mayor que se registran directamente en la cuenta de mayor causarán problemas. Por ejemplo, estas entradas pueden impedirle conciliar su cuenta bancaria. Para las cuentas bancarias en moneda extranjera, las entradas pueden hacer que se acumulen diferencias después de contabilizar más conciliaciones bancarias debido a los ajustes del tipo de cambio de moneda. A menudo, contabiliza el saldo bancario inicial directamente en la cuenta bancaria y el importe termina en la cuenta del L/M. Como alternativa, lo revierte más tarde contra una cuenta de contabilidad que utilice para equilibrar el saldo inicial del libro mayor. En ambos casos, debe equilibrar cualquier registro directo en la cuenta de contabilidad antes de iniciar su primera conciliación bancaria, especialmente si la cuenta bancaria está en una divisa extranjera.


## <a name="see-also"></a>Consulte también

[Conciliar bancos](bank-manage-bank-accounts.md)  
[Conciliar cuentas bancarias usando la asistencia de conciliación bancaria (vista previa)](bank-reconciliation-with-copilot.md)
[Aplicar pagos automáticamente y conciliar cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Configurar reglas para la liquidación automática de los pagos](receivables-how-set-up-payment-application-rules.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
