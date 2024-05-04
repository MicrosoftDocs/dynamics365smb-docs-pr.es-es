---
title: Cómo registrar entradas de sostenibilidad
description: Aprenda a registrar las emisiones de GEI (gases de efecto invernadero).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="how-to-record-sustainability-entries"></a>Cómo registrar entradas de sostenibilidad

En este momento, la única forma de registrar las emisiones de GEI en los **Movimientos de sostenibilidad** es utilizar los **Diarios de sostenibilidad**.   

## <a name="sustainability-journal"></a>Diario de sostenibilidad

Los **diarios de sostenibilidad** están diseñados para realizar un seguimiento y registrar actividades relacionadas con la sostenibilidad utilizando la misma experiencia de usuario que otras revistas en Business Central. Dentro de la revista, los usuarios tienen la opción de introducir las emisiones manualmente si poseen la información necesaria. Alternativamente, si carecen de estos datos, pueden utilizar fórmulas incorporadas para calcular con precisión las emisiones basándose en parámetros específicos conocidos correspondientes a varios tipos de fuentes y cuentas. 

La información que introduzca en un diario es temporal y se puede modificar mientras se encuentre en el diario. Al registrar el diario, la información se transfiere a movimientos a **Movimientos de sostenibilidad** en **Cuentas de sostenibilidad** individuales, donde no se puede modificar. Sin embargo, puede publicar entradas revertidas o corregidas.  

### <a name="use-journal-templates-and-batches"></a>Usar plantillas y secciones del diario

Hay dos **Plantillas de diario de sostenibilidad** de ​​manera predeterminada, la estándar y la periódica. Para cada plantilla de diario, puede configurar su propio diario personal como una sección de diario. Para hacerlo, debe elegir la acción **Lotes** en la página **Plantillas de diario de sostenibilidad** y crear el nuevo **Lote del diario de sostenibilidad** en la nueva página. Por ejemplo, puede definir su propio lote de diario para cada ámbito de emisión, utilizando la opción **Ámbito de emisión** donde puede elegir entre tres ámbitos existentes. También puede agregar o cambiar el **Código fuente** y el **Código de auditoría** para cada uno de los lotes. 

>[!TIP]
>Puede tener un lote de diario para cada tipo de emisión, si tiene muchas líneas, ya que puede reducir la posibilidad de cometer errores, pero también puede usar el lote común para todos los tipos de emisiones.   

### <a name="validating-sustainability-journals"></a>Validar diarios de sostenibilidad

Puede activar una verificación de antecedentes en la página **Configuración de sostenibilidad** que ayudará a evitar retrasos al publicar. La comprobación le notificará cuando haya un error mientras trabaja en el **Diario de sostenibilidad** y esto le impedirá registrar el diario.  

Cuando habilita la validación, el Cuadro informativo **Comprobación de diario** mostrará los problemas en la línea actual y en todo el lote. La validación ocurre cuando carga una sección de diario y cuando elige otra línea de diario. La ventana **Total de problemas** del Cuadro informativo muestra el número total de problemas que [!INCLUDE [prod_short](includes/prod_short.md)] ha encontrado y puede elegirla para abrirla y ver una descripción general de los problemas. 

### <a name="work-with-sustainability-journals"></a>Trabajar con diarios de sostenibilidad

Para comenzar a trabajar con los **Diarios de sostenibilidad**, siga los pasos:   

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de sostenibilidad** y, a continuación, seleccione el vínculo relacionado. 
2. En la página **Diario de sostenibilidad**, puede introducir tantas líneas como planee publicar con el mismo lote.  
3. Como **Tipo de documento**, puede mantener la opción vacía o elegir usar **Factura** o **Nota de abono**.  
4. En el campo **Nº de cuenta**, puede elegir solo **Cuentas de sostenibilidad** con el campo **Publicación directa**, **Contabilización** como el **Tipo de contabilidad** y cuenta no bloqueada. Además, las Cuentas deben haberse configurado con categoría y subcategoría.  

>[!NOTE]
>Si utiliza el lote donde está configurado el ámbito de la emisión, el **Ámbito de la emisión** en la **Cuenta de sostenibilidad** debe ser igual al **Ámbito de emisión** en el lote usado.  

5. Tiene dos opciones: registrar manualmente los importes o utilizar fórmulas.   

    1. Si tiene información precisa sobre la emisión y desea publicarla (es decir, la tiene en la factura recibida), debe seleccionar el campo **Entrada manual** para especificar que los importes se introducirán manualmente. En este caso, no puede completar sus datos en **Combustible/Electricidad**, **Distancia**, **Importe personalizado**, **Multiplicador de instalación** y **Factor de tiempo** , ya que no serán editables para esta elección. Pero los campos **Emisiones de CO2**, **Emisiones de CH4** y **Emisiones de N2O** serán editables y podrá completar los datos directamente allí. 
    2. Si no conoce sus emisiones con exactitud, deberá calcularlas y no habrá seleccionado el campo **Entrada manual**, y en este caso los campos **Emisión de CO2**, **Emisión de CH4** y **Emisión de N2O** no será editable, pero puede introducir los detalles de su cálculo según la fórmula que esté usando. Puede encontrar más información sobre las fórmulas utilizadas y definidas en la **Categoría de cuentas de sostenibilidad** aquí en el [Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Para registrar el diario, elija la acción **Registrar**. Al publicar en un **Diario de sostenibilidad**, las entradas se generan en el **Movimiento de sostenibilidad**. 

En el caso de que su fórmula se base en la opción **Calcular desde contabilidad general** en la **Categoría de cuenta de sostenibilidad**, debe utilizar la acción **Recopilar importe de movs. contables** antes de publicar el diario para calcular las emisiones basándose en este origen de datos. Además, si realizó algunos cambios en los factores de emisión después de completar las líneas del diario, debe elegir la acción **Recalcular** para obtener la cantidad adecuada en el diario.  

### <a name="recurring-journals"></a>Diarios periódicos

Un diario periódico es un **Diario de sostenibilidad** con campos específicos para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno. Por ejemplo, transacciones de sostenibilidad como electricidad, calefacción u otras transacciones similares. El uso de diarios recurrentes le permite publicar cantidades fijas y variables. En un diario periódico, crea las entradas que se van a registrar con regularidad solo una vez. Por ejemplo, las cuentas, las dimensiones, los valores de dimensiones y demás, permanecen en el diario después del registro. Si se necesitan cambios, puede hacerlos cada vez que publique. 

El campo **Periodicidad** es importante. Determina la forma en que se tratará el importe en la línea de diario una vez realizado el registro. Por ejemplo, si utiliza el mismo importe cada vez que contabiliza la línea, puede dejar que el importe se mantenga y, en este caso, deberá utilizar **F Fijo** como una opción. Si usa las mismas cuentas y texto de la línea, pero el importe varía en cada una, puede optar por borrar el importe después de cada registro y, en este caso, elegirá la opción **V Variable**. 

También es necesario configurar el campo **Frecuencia repetición**, ya que este campo de fórmula de fecha determina la frecuencia con la que se contabilizará el asiento en la línea del diario, y debe rellenarse. Obtenga más información en [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).  

El campo **Fecha de caducidad** determina la fecha en que se registrará la línea por última vez. La línea no se registrará después de esta fecha. La ventaja de usar el campo **Fecha de caducidad** es que la línea no se borrará del diario inmediatamente. Puede introducir una fecha posterior para poder utilizar la línea en el futuro. Si el campo se deja en blanco, la línea se registrará cada vez que se elimine del diario.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)    
[Información general de administración de la sostenibilidad](finance-manage-sustainability.md)   
[Configuración de sostenibilidad](finance-sustainability-setup.md)   
[Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md)   
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
