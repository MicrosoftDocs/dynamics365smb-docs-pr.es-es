---
title: Trabajar con contratos u ofertas de servicio | Documentos de Microsoft
description: 'Puede crear un contrato de servicio de forma manual o desde una oferta de contrato de servicio. Puede crear un contrato basado en una oferta de contrato de servicio:'
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ab8ded6ef2b93c2ab038472609093ef7e5ad3d88
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-service-contracts-and-service-contract-quotes"></a>Trabajar con contratos de servicio y ofertas de contrato de servicio
Puede crear un contrato de servicio de forma manual o desde una oferta de contrato de servicio. Puede utilizar una oferta de contrato de servicio como precursora de un contrato de servicio, en ésta su empresa realiza una oferta al cliente para obtener así su aprobación para poder convertirla en un contrato de servicio. Los procedimientos para crear un contrato de servicio o una oferta de contrato de servicio son similares.  
  
## <a name="to-create-a-service-contract-or-service-contract-quote"></a>Para crear un contrato u oferta de contrato de servicio  
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Contratos servicio**, **Ofertas contrato servicio** y elija el vínculo relacionado.  
2. Crear un contrato u oferta de contrato de servicio nuevos:  
3. Rellene el campo **No.**. . Se abrirá un cuadro de diálogo en el que se le preguntará si desea rellenar los datos comunes del contrato a partir de una plantilla de contrato. Si desea crear este tipo de contrato u oferta de contrato de servicio, seleccione **Sí**. Se abrirá la ventana **Lista plantilla contrato serv.**  
4. Seleccione la plantilla adecuada y, a continuación, elija **Aceptar** para utilizarla al crear el contrato u oferta de contrato de servicio.  
5. En el campo **Nº cliente**, elija el cliente.  
6. Si no desea que se distribuya automáticamente la diferencia de importe anual, elija la casilla **Permite importes sin saldar**. Los valores de los campos **Importe anual** e **Importe anual calculado** no se igualan automáticamente. Si desea que el programa distribuya automáticamente la diferencia de importe anual que pueda generarse con el cambio de contrato de servicio, no seleccione la casilla **Permite importes sin saldar**.  
7. Agregue líneas de contrato al contrato o a la oferta de contrato de servicio.  
8. Rellene el resto de campos según sea necesario.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a>Para convertir una oferta de contrato de servicio en un contrato de servicio  
Una vez que el cliente ha aceptado la oferta de contrato de servicio, puede convertirla en un contrato de servicio. Al mismo tiempo, puede crear una factura de servicio para el periodo inicial del contrato si la fecha inicial del mismo es anterior al inicio del siguiente periodo de factura. 

Una vez que finalice los pasos siguientes, se crea un contrato de servicio con el estado **Firmado**. Si se crea una factura de servicio para el periodo inicial del contrato, se calcula el importe facturado de la siguiente forma, en función de si se trata de un contrato detallado o no:  
  
Para los contratos detallados, el importe facturado se calcula de la siguiente forma:  
  
* Importe facturado = suma del importe facturado de cada línea de contrato.  
* Importe facturado para cada línea de contrato = (valor de la oferta ÷ 12) × número de meses del periodo inicial) + (valor de la oferta ÷ número de días del año) × número de días restantes del periodo inicial).  
* Si la línea de contrato vence antes de que finalice el periodo inicial, la fecha de finalización se convierte en la fecha final del periodo inicial de la línea.  
  
Para contratos no detallados, el importe facturado se calcula de la siguiente forma:  
  
* Importe facturado = (importe anual ÷ número de días del año) × número de días del periodo inicial.  
* Si el contrato vence antes de que finalice el periodo inicial, la fecha de finalización se convierte en la fecha final del periodo inicial.    
  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ofertas de contrato de servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la oferta de contrato de servicio que desea convertir en contrato de servicio.  
3. Seleccione la acción **Crear contrato**.  
4. Si la fecha inicial del contrato es anterior al inicio del siguiente periodo de facturación, se le preguntará si desea crear una factura de servicio para el periodo inicial del contrato. Elija **Sí**.  
  
 La factura de servicio se registra en la cuenta de servicio del contrato, incluso si el contrato es de prepago. 

## <a name="to-create-contract-service-credit-memos"></a>Para crear abonos de servicio de contrato
Puede utilizar abonos de servicio de contrato cuando un cliente cancela un contrato de servicio de prepago o elimina un producto de servicio de un contrato de prepago. También sirven para corregir una factura de servicio incorrecta.  
  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Abonos de servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Cree un abono de servicio nuevo.  
3. Rellene el campo **No.**. .  
4. En el campo **Nº cliente**, especifique el número del cliente del contrato de servicio.  
  
     La ficha desplegable **Facturación**, muestra la información que se ha copiado de la ficha **Cliente**. Si desea registrar el abono con un cliente que no esté especificado en la ficha desplegable **General**, escriba el número del cliente en el campo **Factura a-Nº cliente** .  
  
    > [!NOTE]  
    >  Puede comparar el abono con el documento original registrado en la ventana **Facts. ventas (servicio) regis.** Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Histórico facturas servicio** y, a continuación, seleccione el vínculo relacionado.  
  
5. Rellene los campos **Fecha registro** y **Fecha documento**.  
6. En las líneas de abono, especifique información acerca de los productos devueltos o eliminados o de la deducción que se enviará. También puede utilizar el proceso **Trae movs. contrato prepag**.  
  
 Para crear automáticamente un abono cuando se eliminen líneas de contrato de un contrato de servicio, en la ventana **Contrato servicio** de la ficha desplegable **Detalles factura**, active la casilla de verificación **Abonos automáticos**.  
  
 Para crear manualmente un abono cuando se quiten líneas de contrato de un contrato de servicio, en la ventana **Contrato servicio**, en la pestaña **Acciones**, en el grupo **Funciones**, elija **Abono**.  

## <a name="updating-and-evaluating-contracts"></a>Actualización y evaluación de los contratos
A veces es necesario cambiar las condiciones de un contrato una vez creado. En la mayoría de las ocasiones, el contrato correspondiente se abre en la ventana **Contrato servicio** y se cambia según sea necesario.  
  
Puede cambiar el estado del contrato, inicialmente configurado en **Bloqueado**, agregar y eliminar líneas del contrato y cancelar un contrato. Si desea ver el desempeño de su empresa en términos de pérdidas y ganancias, puede realizar un rápido análisis empresarial usando la función de análisis de contrato.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>Para agregar una línea de contrato a una oferta de contrato o contrato de servicio  
Cuando un cliente compra un producto nuevo y desea incluirlo en el contrato u oferta de contrato de servicio existente, debe registrar el producto como un producto de servicio y, a continuación, agregarlo como una nueva línea al contrato u oferta de contrato.  
  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contratos de servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Abra el correspondiente contrato u oferta de contrato de servicio al que desea añadir una línea de contrato nueva.  
3. Elija la acción **Abrir contrato** para abrir el contrato u oferta de contrato de servicio para su modificación.  
4. En la ficha desplegable **Detalles fact.**, seleccione el campo **Permite importes sin saldar** si desea cambiar el importe anual y distribuir la diferencia del importe anual manualmente en las líneas de contrato. En caso contrario, desactive el campo **Permite importes sin saldar**. Esto distribuirá la diferencia de importe anual automáticamente en las líneas de contrato después de cambiar el importe anual.  
5. En la ficha desplegable **Líneas**, agregue un producto, producto de servicio o una descripción de texto en cada línea de contrato. Alternativamente, puede agregar líneas de oferta de contrato. Tenga en cuenta que puede crear múltiples contratos por producto de servicio para incluirlo en diferentes contratos u ofertas de contrato de servicio al mismo tiempo.  
6. Verifique y corrija los números de los campos **% Descuento línea**, **Importe dto. línea**, **Hora respuesta**, **Periodo servicio** y otros campos según sea necesario. 

## <a name="to-remove-contract-lines"></a>Para eliminar líneas de contrato  
Es posible que tenga que eliminar líneas de contrato del contrato de servicio según elimina los correspondientes productos de servicio del contrato de servicio. Normalmente, se elimina una línea de contrato que ha caducado o que se corresponde a un producto de servicio que se ha estropeado.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contratos de servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Abra el contrato de servicio cuyas líneas de contrato desee eliminar.  
3. Elija la acción **Abrir contrato** para abrir el contrato de servicio para su modificación.  
4. Seleccione la línea de contrato que desea eliminar. Rellene el campo **Fecha fin contrato** con la fecha en la que desea quitar la línea. Por ejemplo, podría especificar la fecha en la que se estropeó el producto de servicio.  
5. Seleccione la acción **Eliminar líns. contrato**. Se abre la ventana **Eliminar líns. del contrato**.  
6. Rellene los filtros por defecto: **Nº contrato**, **Nº prod. servicio** y **Tipo contrato**. Si es necesario, puede aplicar más filtros o cambiar los existentes.  
7. Rellene los campos de la ficha desplegable **Opciones**. En el campo **Acción**, seleccione **Borrar líneas**.  
  
> [!NOTE]  
>  Si el contrato no es detallado, debe actualizar el valor del campo **Importe anual** de la ficha desplegable **Detalles fact.** en la ventana **Contrato servicio**, que refleja la pérdida del producto de servicio del contrato.  
>   
>  Si el contrato es detallado y de prepago y se han registrado facturas, podrá crear un abono para el contrato. En la pestaña **Acciones** del grupo **Funciones**, seleccione **Crear abono**. Esto no es necesario si la casilla del campo **Abonos automáticos** de la ficha desplegable **Detalles de la factura** está seleccionada. En ese caso, un abono se crea automáticamente cuando se elimina una línea de contrato. 

## <a name="service-line-cost-and-value"></a>Coste y valor de la línea de servicio
En las líneas de un contrato de servicio, los importes de **Coste línea** y **Valor línea** se calculan según se describe en las siguientes tablas.

| Opciones coste de línea | Description|
|----------------------------------|---------------------------------------|  
|**Producto servicio** | El coste se recuperará automáticamente del campo **Coste contrato genérico** de la tabla **Producto servicio** y se copiará en el campo **Coste línea**. Para calcular el coste de línea se utiliza la siguiente fórmula:<br /><br /> Coste unit. venta × % Valor contrato ÷ 100|  
|**Producto** | El coste se recuperará automáticamente del campo **Coste unitario** de la tabla **Producto** y el valor del campo **% Valor contrato** de la tabla **Config. gestión servicio**. Para calcular el coste de línea se utiliza la siguiente fórmula:<br /><br /> Coste unitario × % Valor contrato ÷ 100|  
|**Descripción de texto** | El valor del campo **Coste línea** se establece en cero.|  

| Opciones valor de línea | Description|
|----------------------------------|---------------------------------------|  
|**Producto servicio** | El precio se recuperará automáticamente del campo **Valor contrato genérico** de la tabla **Producto servicio** y se copiará en el campo **Valor línea**.|  
|**Producto** | En función del valor del campo **Método cálc. valor contrato** de la tabla **Config. gestión servicio**, el importe se recuperará de los campos **Precio venta** o **Coste unitario** de la tabla **Producto**. Después de eso, este valor se multiplica por el contenido del campo **% Valor contrato** de la tabla **Config. gestión servicio** y se divide entre 100. Este importe se copia en el campo **Valor línea**.<br /><br /> **NOTA**: Si el campo **Método cálc. valor contrato** está establecido en **Ninguno**, no se calculará el contenido del campo **Valor línea**.|  
|**Descripción de texto** | El contenido del campo **Valor línea** se establece en cero.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a>Para agregar un descuento de contrato a las ofertas de contrato de servicios  
Puede agregar descuentos de contrato sobre servicios para ofertas y servicios de contrato. Los descuentos pueden efectuarse sobre componentes de grupos de producto de servicio concretos, sobre horas de recursos de grupos de recursos determinados y sobre costes de servicio específicos. 
  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ofertas de contrato de servicio** y seleccione el vínculo relacionado.  
2. Seleccione la oferta en la que desea agregar un descuento.  
3. Seleccione la acción **Descuentos servicio**. Se abrirá la ventana **Descuentos contrato/servicio**.  
4. Para crear un nuevo descuento de contrato, selecione la acción **Nuevo**.  
5. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
  
> [!Tip]  
>  Para agregar descuentos de contrato directamente a un contrato de servicio, realice los mismos pasos desde la ventana **Contrato servicio**.  

## <a name="to-change-the-owner-of-a-service-contract"></a>Para cambiar el propietario de contratos de servicio  
Es posible que necesite modificar el propietario de un contrato de servicio. Si un producto de servicio incluido en un contrato de servicio está registrado en múltiples contratos no cancelados propiedad del mismo cliente, se actualizará automáticamente el propietario de todos los contratos de servicio que incluyan este producto de servicio y de todos los productos de servicio incluidos en estos contratos.  
  
> [!NOTE]  
>  En este caso, únicamente se tienen en cuenta los contratos no cancelados. El estado de las ofertas de contrato no se tiene en cuenta.  
  
> [!IMPORTANT]  
>  Los productos de servicio y contratos pueden estar relacionados. Cambiar el propietario de un contrato de servicio puede influir en estas relaciones.  
>   
>  Por ejemplo, imagine que el producto de servicio Nº 8 está incluido en los contratos SC00003 y SC00015. El contrato SC00015 también contiene el producto de servicio Nº 15, que también está incluido en el contrato SC00080. En este caso, cambiará el propietario de los tres contratos y productos de servicio.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contratos de servicio** y, a continuación, seleccione el vínculo relacionado. Abra el contrato de servicio correspondiente cuyo propietario desee modificar.  
2. Elija la acción **Abrir contrato** para abrir el contrato para su modificación.  
3. Seleccione la acción **Cambiar cliente**. Se abrirá la ventana **Cambiar cliente en contrato**.  
4. En los campos **N.º contrato** y **Nº prod. servicio** puede ver los números de contrato y producto de servicio propiedad del cliente seleccionado. Si el cliente posee más de un contrato con más de un producto de servicio, el valor de estos campos será **Múltiple**. Para ver la lista de artículos de servicio o contratos relacionados, seleccione estos valores de campo.  
5. En el campo **Nº cliente nuevo** elija el cliente nuevo.  
6. En el campo **Código nuevo de dirección de envío**, seleccione la dirección.  
7. Elija **Aceptar** para cambiar el cliente y el código de dirección de envío al cliente de los contratos de servicio.  
8. Elija la acción **Bloquear contrato** para bloquear el contrato y asegurarse de que los cambios formarán parte de él.  

## <a name="to-update-a-service-contract-price"></a>Para actualizar un precio de contrato de servicio  
Para actualizar los precios de contratos de servicio, especifique un porcentaje de actualización de precio.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Actualizar precios contrato servicio** y, a continuación, seleccione el vínculo relacionado. 
2. Elija el contrato de servicio.  
3. En el campo **Actualizar hasta fecha**, introduzca una fecha. El trabajo por lotes actualizará los precios de los contratos cuya fecha de siguiente actualización de precios sea anterior o posterior a esta fecha.  
4. En el campo **% Actualiz. precio**, introduzca el porcentaje por el que desea actualizar los precios.  
5. En el campo **Acción**, seleccione **Actualizar precios contrato**.  

## <a name="to-post-prepaid-contract-entries"></a>Para registrar movimientos de contrato de prepago  
Si trabaja con contratos de servicio de prepago, deberá registrar movimientos de contrato de prepago con regularidad, para así transferir los pagos de prepago de las cuentas de contrato de prepago a las cuentas de contrato ordinarias.  
  
Para poder registrar movimientos de contrato de prepago, deberá especificar un número de serie en el campo **Nº serie doc. regis. prepago** de la ventana **Config. gestión servicio**.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registrar movimientos de contrato de prepago** y, a continuación, seleccione el vínculo relacionado.  
2. En en el campo **Registrar hasta la fecha** especifique una fecha. El proceso registra movimientos de servicio de prepago con fechas de registro anteriores a esta fecha.  
4. En el campo **Fecha registro**, introduzca la fecha que desea utilizar como fecha de registro en la línea del diario general.  
5. En el campo **Acción**, seleccione **Registrar transacciones de prepago**  
6. Seleccione **Aceptar** para registrar los movimientos.

## <a name="changing-the-service-contract-status"></a>Cambio del estado de contrato de servicio
Después de firmar el contrato de servicio, el valor del campo **Cambiar estado** se establece automáticamente en **Bloqueado**. Si desea modificar información del contrato de servicio o de la oferta de contrato de servicio, primero tiene que cambiar el estado del contrato u oferta de **Bloqueado** a **Abierto**. Tenga en cuenta que no puede crear facturas de servicio del contrato de servicio con el estado de cambio **Abierto**. Después de modificar el contrato u oferta de contrato, tiene que cambiar el estado a **Bloqueado** para poder crear de nuevo facturas de servicio y movimientos en el contrato de servicio que incluyan los cambios que ha realizado.  
  
> [!NOTE]  
>  El campo **Cambiar estado** no está relacionada con el campo **Estado lanzamiento** de la cabecera del pedido de servicio, que regirá la dirección del almacén de productos de servicio.  

## <a name="to-cancel-a-service-contract"></a>Para cancelar un contrato de servicio  
Es posible que tenga que cancelar un contrato de servicio cuando el contrato haya caducado o cuando usted o el cliente lo hayan cancelado.  
  
> [!NOTE]  
>  No puede volver a abrir un contrato después de cancelarlo.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contratos de servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Abra el contrato de servicio relevante que desee cancelar.  
3. Elija la acción **Abrir contrato** para abrir el contrato de servicio para su modificación.  
4. En el campo **Código área cancelación**, elija el código de razón correspondiente. Para agregar más códigos de razón, elija la acción **Avanzado**.  
  
     Si activa el campo **Usar contrato Auditoría cancelación** en la ventana **Config. gestión servicio**, deberá especificar un código de auditoría de cancelación al cancelar los contratos.  
  
5. En el campo **Estado**, elija **Cancelado**.  
6. Si hay facturas, abonos o movimientos de prepago abiertos registrados para el contrato, aparecerá un mensaje de confirmación. En el cuadro de mensaje, elija **No** para volver a contrato y registrar los documentos o **Sí** para continuar el proceso de cancelación.  

## <a name="filing-a-service-contract-or-contract-quote"></a>Archivado de un contrato de servicio u oferta de contrato  
Puede archivar contratos de servicio y ofertas de contrato en cualquier momento para registrar una copia del contrato o una oferta de contrato. [!INCLUDE[d365fin](includes/d365fin_md.md)] archiva contratos de servicio automáticamente cuando se convierten ofertas de contrato en contratos de servicio o se cancelan contratos de servicio. Puede archivar un contrato u oferta mediante la acción **Archivar contrato** en las páginas **Contratos de servicio** u **Ofertas contrato servicio**. Si desea ver los contratos de ofertas archivados busque **Contratos archivados**.

## <a name="see-also"></a>Consulte también  
[Cómo configurar contratos de servicio](service-how-setup-service-contracts.md)  
[Gestión de servicios](service-service.md)  
[Convertir contratos de servicio que incluyen importes de IVA](service-how-to-convert-service-contracts.md)  

