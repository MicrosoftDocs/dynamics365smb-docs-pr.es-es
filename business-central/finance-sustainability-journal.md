---
title: Registrar entradas de sostenibilidad
description: Aprenda a registrar las emisiones de GEI (gases de efecto invernadero).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Registrar entradas de sostenibilidad

Actualmente, la única forma de registrar las emisiones de gases de efecto invernadero (GEI) en el libro de sostenibilidad es utilizar diarios de sostenibilidad.

## Diarios de sostenibilidad

Los diarios de sostenibilidad están diseñados para realizar un seguimiento y registrar actividades relacionadas con la sostenibilidad utilizando la misma experiencia de usuario que otras revistas en Business Central. Los usuarios que tengan la información necesaria pueden introducir manualmente las emisiones en un diario. Alternativamente, si carecen de esta información, pueden utilizar fórmulas incorporadas para calcular con precisión las emisiones basándose en parámetros específicos conocidos correspondientes a varios tipos de fuentes y cuentas.

La información que introduzca en un diario es temporal y se puede modificar mientras se encuentre en ese diario. Al contabilizar el diario, la información se transfiere a las entradas del libro mayor de sostenibilidad en las cuentas individuales de sostenibilidad, donde no puede modificarse. Sin embargo, puede publicar entradas revertidas o corregidas.

### Usar plantillas y secciones del diario

De manera predeterminada, existen dos plantillas de diario de sostenibilidad: la plantilla estándar y la plantilla periódica.

Para cada plantilla de diario, puede configurar su propio diario personal como una sección de diario. Para hacerlo, seleccione **Lotes** en la página **Plantillas de diario de sostenibilidad** y cree el nuevo **Lote del diario de sostenibilidad** en la nueva página. Por ejemplo, puede definir su propio lote de diario para cada ámbito de emisión, utilizando la opción **Ámbito de emisión** y luego seleccionando entre los tres ámbitos existentes. Para cada lote puede agregar o cambiar los valores de **Código fuente** y **Código de auditoría**.

> [!TIP]
> Si tiene muchas líneas, puede ayudar a reducir el riesgo de errores al tener un lote de diario para cada tipo de emisión. Alternativamente, puede utilizar el lote común para todos los tipos de emisiones.

### Validar diarios de sostenibilidad

En la página **Configuración de sostenibilidad**, puede activar la comprobación en segundo plano para evitar retrasos al publicar. Si se produce algún error mientras trabaja en el diario de sostenibilidad, la validación se lo notifica y le impide contabilizar el diario.

Cuando habilita la validación, el Cuadro informativo **Comprobación de diario** muestra los problemas en la línea actual y en todo el lote. La validación ocurre cuando carga una sección de diario y cuando selecciona otra línea de diario. El mosaico **Total de problemas** en el cuadro informativo muestra el número total de problemas que [!INCLUDE [prod_short](includes/prod_short.md)] encontró. Puede seleccionar el mosaico para abrir una descripción general de los problemas.

### Trabajar con diarios de sostenibilidad

Para comenzar a trabajar con los diarios de sostenibilidad, siga estos pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de sostenibilidad** y, a continuación, seleccione el vínculo relacionado.
2. En la página **Diario de sostenibilidad**, puede introducir tantas líneas como planee publicar en el mismo lote.
3. Puede dejar el campo **Tipo de documento** en blanco o puede seleccionar **Factura** o **Nota de abono**.
4. En el campo **Nº cuenta** puede seleccionar solo cuentas de sostenibilidad no bloqueadas en las que el campo **Registro directo** se ha seleccionado y el campo **Tipo de contabilidad** se ha establecido en **Registrar**. Las cuentas también deben configurarse con una categoría y una subcategoría.

    > [!NOTE]
    > Si utiliza un lote donde está configurado el ámbito de la emisión, el valor **Ámbito de la emisión** en la cuenta de sostenibilidad debe ser igual al valor de **Ámbito de emisión** en el lote usado.

5. Puede registrar manualmente los importes o utilizar fórmulas.

    - Si dispone de información precisa sobre la emisión y desea contabilizarla (es decir, si dispone de la información de la factura recibida), seleccione el campo **Entrada manual** para indicar que introducirá manualmente los importes. En este caso, no puede introducir sus datos directamente en **Combustible/Electricidad**, **Distancia**, **Importe personalizado**, **Multiplicador de instalación** y **Factor de tiempo** porque se convierten en no editables. Sin embargo, los campos **Emisiones de CO2**, **Emisiones de CH4** y **Emisiones de N2O** serán editables y podrá introducir los datos directamente en ellos.
    - Si no tiene un conocimiento preciso de la emisión y debe calcularla, no seleccione el campo **Entrada manual**. En este caso, los campos **Emisiones de CO2**, **Emisiones de CH4** y **Emisiones de N2O** dejan de ser editables. Sin embargo, puede introducir los detalles de su cálculo según la fórmula que esté utilizando. Obtenga más información sobre las fórmulas que están y definidas en la **categoría de cuentas de sostenibilidad** en [Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md#account-categories).

6. Para registrar el diario, seleccione la acción **Registrar**. Al publicar en un diario de sostenibilidad, las entradas se generan en el movimiento de sostenibilidad.

Si su fórmula se base en la opción **Calcular desde contabilidad general** en la categoría de cuenta de sostenibilidad, debe utilizar la acción **Recopilar importe de movs. contables** antes de publicar el diario para calcular las emisiones basándose en este origen de datos. Además, si realizó cambios en los factores de emisión después de que se rellenaran las líneas del diario, deberá seleccionar la acción **Recalcular** para obtener la cantidad adecuada en el diario.

### Diarios periódicos

Un diario periódico es un diario de sostenibilidad con campos específicos para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno. Los ejemplos incluyen transacciones de sostenibilidad como electricidad, calefacción u otras transacciones similares. Puede utilizar diarios periódicos para contabilizar importes fijos y variables.

Cuando utilice un diario recurrente, las entradas que vaya a registrar periódicamente deberán crearse una sola vez. La información como las cuentas, las dimensiones y los valores de las dimensiones permanecen en el diario tras la contabilización. Cada vez que publique, podrá realizar los cambios que sean necesarios.

El campo **Periodicidad** es importante. Determina la forma en que se tratará el importe en la línea de diario una vez realizado el registro. Por ejemplo, si utiliza el mismo importe cada vez que contabiliza la línea, puede seleccionar **F Fijo** para dejar que el importe se conserve tras el registro. Si utiliza las mismas cuentas y el mismo texto en la línea, pero el importe varía cada vez que contabiliza, puede seleccionar la opción **V Variable** para borrar el importe después de la contabilización.

El campo **Frecuencia repetición** también es importante y debe configurarse. Es un campo de fórmula de fecha que determina la frecuencia con la que se contabiliza el asiento en la línea del diario. Obtenga más información en [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

El campo **Fecha de caducidad** determina la fecha en que se registrará la línea por última vez. La línea no se registrará después de esa fecha. La ventaja de usar el campo **Fecha de caducidad** es que la línea no se borra del diario inmediatamente. Puede introducir una fecha posterior para poder utilizar la línea en el futuro. Si el campo se deja en blanco, la línea se registrará cada vez que se elimine del diario.

## Consulte también

[Finanzas](finance.md)  
[Información general de la administración de la sostenibilidad](finance-manage-sustainability.md)  
[Configuración de sostenibilidad](finance-sustainability-setup.md)  
[Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
