---
title: Transferencia y registro de movimientos de coste
description: 'Antes de definir asignaciones de coste, debe entender los distintos orígenes de dónde provienen los movimientos de coste.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Transferencia y registro de movimientos de coste

Antes de definir asignaciones de coste, debe entender cómo provienen los movimientos de coste de los orígenes siguientes:  

- Transferencia automática de movimientos de contabilidad.  
- Registro de coste manual de los movimientos de coste puros, gastos internos y asignaciones manuales.  
- Registros automáticas de asignación de costes reales.  
- Transferencia de los movimientos de presupuesto a real.

## Criterios para la transferencia de movimientos de contabilidad a movimientos de coste

Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de coste. Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad.  

Se transfieren los movimientos de contabilidad si:  

- Los movimientos tienen valores de dimensión correspondientes a un centro o un objeto de coste.  
- Los movimientos tienen valores de dimensión que corresponden a un centro de coste y a un objeto de coste. Para estos movimientos, el centro de coste tiene preferencia. Esto ayuda a evitar una situación en la que un tipo de coste aparece en un objeto de coste y un centro de coste y por lo tanto se cuenta dos veces en estadísticas.  
- El número de documento de los movimientos está vacío, por lo que aparecerá con un número de documento de 0000 en los movimientos de coste.  
- Los movimientos se transfieren a un tipo de coste que permite los movimientos agrupados y estos movimientos se transfieren como un movimiento combinado mensual o diariamente.  

No se transfieren los movimientos de contabilidad si:  

- Los movimientos tienen valores de dimensión que no corresponden a un centro de coste ni a un objeto de coste.  
- Los movimientos tienen un importe de cero.  
- Los movimientos tienen una cuenta de contabilidad que se ha eliminado.  
- Los movimientos tienen una cuenta de contabilidad que no es de tipo **Ingresos y gastos**.  
- Los movimientos tienen una cuenta de contabilidad que no tiene un tipo de coste asignado.  
- Los movimientos tienen una fecha de registro antes de **Fecha inicio para transferencia C/G**.  
- Los movimientos se registraron con una fecha de cierre. Éstos son normalmente movimientos que restablecen el saldo de regularización al final del año.

## Transferencia de movimientos de contabilidad a movimientos de coste

Puede transferir movimientos de contabilidad a movimientos de coste.  

Antes de ejecutar el proceso para transferir movimientos de contabilidad a movimientos de coste, debe preparar la transferencia para evitar el registro manual de corrección.  

### Para preparar la transferencia  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración contabilidad costes** y luego elija el enlace relacionado.  
2.  En la página **Configuración contabilidad costes**, verifique que el campo **Fecha inicio para transferencia C/G** esté definido el valor correcto.  
3.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan tipos coste** y luego elija el enlace relacionado.  
4.  En la página **Ficha tipo coste**, verifique que el campo **Intervalo cuenta C/G** está vinculado correctamente para cada tipo de coste para tomar movimientos de la contabilidad.  
5.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
6.  Para cada cuenta contable correspondiente, en la página **Ficha cuenta**, compruebe que el campo **Nº tipo coste**. está vinculado correctamente a un tipo de coste. Para obtener más información, consulte [Configuración de contabilidad de costes](finance-set-up-cost-accounting.md).  
7.  Verifique que todos los movimientos de contabilidad correspondientes tengan valores de dimensión que correspondan a un centro de coste y a un objeto de coste.  

### Para transferir movimientos de contabilidad a movimientos de coste

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transferir movimientos de contabilidad a costes** y luego elija el enlace relacionado.  
2.  Para iniciar la transferencia, elija el botón **Sí**. El proceso transfiere todos los movimientos de contabilidad que no se han transferido ya.  

Durante la transferencia, el proceso crea conexiones en las entradas en la tabla **Movimiento de coste** y la tabla **Registro de costes**. Esto permite realizar un seguimiento del origen de los movimientos de coste.

## Transferencia automática y movimientos combinados

En contabilidad de costes, puede transferir los movimientos de contabilidad a un tipo de coste mediante un registro combinado. Puede especificar si un tipo de coste recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de coste. La siguiente tabla describe las distintas opciones.  

|Combinar movimientos|Description|  
|---------------------|-----------------|  
|Ninguno|Cada movimiento de contabilidad se transfiere individualmente al tipo de coste correspondiente.|  
|Día|Los movimientos de contabilidad que tienen la misma fecha de registro se transfieren como un solo movimiento al tipo de coste correspondiente.|  
|Mes|Todos los movimientos de contabilidad general que tienen el mismo mes de calendario se transfieren como un solo movimiento al tipo de coste correspondiente.|  

> [!IMPORTANT]  
>  Si ha seleccionado la casilla **Transf. autom. desde C/G** en la página **Configuración contabilidad costes**, [!INCLUDE[prod_short](includes/prod_short.md)] actualiza la contabilidad de costes después de cada registro en la contabilidad. Ya no se pueden realizar movimientos combinados.

## Los resultados de la transferencia de movimientos de contabilidad a movimientos de coste

Durante la transferencia de movimientos de contabilidad a movimientos de coste, [!INCLUDE[prod_short](includes/prod_short.md)] crea conexiones en los movimientos de la tabla **Mov. contabilidad**, la tabla **Movimiento de coste** y la tabla **Registro de costes** para permitir realizar un seguimiento de las conexiones entre los movimientos de costes y los movimientos de contabilidad.  

### Movs. contabilidad

Para cada movimiento de contabilidad que se transfiere a la contabilidad de costes, [!INCLUDE[prod_short](includes/prod_short.md)] rellena el campo de coste **N.º mov.**.  

### Movs. coste

Para cada movimiento de coste, [!INCLUDE[prod_short](includes/prod_short.md)] guarda el número de movimiento del movimiento de contabilidad correspondiente en el campo **Nº mov. contabilidad** en la tabla **Movimiento de coste**.  

Para movimientos de coste combinados, [!INCLUDE[prod_short](includes/prod_short.md)] guarda el número del movimiento del último movimiento de contabilidad, que es el movimiento con el número más alto de movimiento.  

El campo **Cuenta** en la tabla **Movimiento de coste** contiene el número de la cuenta de la que provino el movimiento de coste.  

Para movimientos de coste únicos, [!INCLUDE[prod_short](includes/prod_short.md)] transfiere el texto de registro del movimiento de contabilidad al campo de texto **Descripción**. Para movimientos combinados, el campo de texto muestra que estos movimientos se transfieren como movimientos combinados. Por ejemplo, para un movimiento combinado del mes de octubre de 2013, el texto puede ser **Movimientos combinados, octubre de 2013**.  

### Registro costes

En la tabla **Registro de costes**, [!INCLUDE[prod_short](includes/prod_short.md)] crea un movimiento con la transferencia de origen de la contabilidad. El movimiento registra el primer y último número de los movimientos de contabilidad que se transfieren, además del primer y último número de movimientos de coste creados.

## Consulte también .

 [Acerca de la contabilidad de costes](finance-about-cost-accounting.md)  
 [Configuración de contabilidad de costes](finance-set-up-cost-accounting.md)  
 [Definir y asignar costes](finance-define-and-allocate-costs.md)  
 [Contabilidad para costes](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
