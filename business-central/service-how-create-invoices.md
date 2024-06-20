---
title: Crear facturas o abonos de servicios
description: Aprenda a crear facturas para y notas de abono para sus servicios.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-service-invoices-or-credit-memos"></a>Crear facturas o notas de abono de servicios

La facilidad de facturar sus pedidos de servicio es una función esencial de [!INCLUDE[prod_short](includes/prod_short.md)]. Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] de modo que un técnico de servicio de campo pueda crear una factura para un servicio que no esté vinculado con un contrato o pedido. Como alternativa, configure [!INCLUDE[prod_short](includes/prod_short.md)] para facturar contratos de servicio periódicamente. El periodo de factura de cada contrato define la frecuencia con que se factura.

## <a name="to-invoice-several-service-contracts"></a>Para facturar varios contratos de servicio

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear facturas de contrato de servicio** y, a continuación, elija el enlace relacionado.  
2. Establezca los filtros que desea aplicar.  
3. En el campo **Fecha registro**, escriba la fecha que se utilizará como fecha de registro de las facturas de servicio.  
4. En el campo **Factura hasta fecha**, introduzca la fecha hasta la que desea facturar contratos. El proceso incluirá contratos con fechas siguientes de factura hasta esta fecha.  
5. En el campo **Acción**, elija **Crear facturas**.  
6. Elija **Aceptar** para crear las facturas de servicio.  
  
También puede facturar un contrato de servicio directamente desde la página **Contrato servicio**, si la siguiente fecha de factura del contrato es anterior a la fecha de trabajo.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Facturar un contrato de servicio desde la página de contrato de servicio

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Contratos de servicio** y luego elija el enlace relacionado.  
2. Elija el contrato de servicio que desea facturar y abra la ficha de contrato.  
3. Elija la acción **Crear factura servicio**. 
4. Elija **Sí** para crear las facturas de servicio.  
  
  > [!NOTE]  
  > No puede crear facturas de servicio para el contrato de servicio cuando el valor del campo **Cambiar estado** es **Abierto**.  

## <a name="to-post-an-invoice-from-a-service-order"></a>Para registrar una factura de un pedido de servicio

En el siguiente procedimiento se describe cómo definir la parte del servicio por la que cobrará al cliente.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Elija el pedido de servicio que desea facturar y abra la ficha de pedido.  
3. Elija la acción **Líneas de servicio**.  
4. Busque los movimientos requeridos y especifique las cantidades por las que va a cobrar al cliente en el campo **Cdad. a facturar**.  
  
   > [!NOTE]  
   > Puede emitir una factura al cliente por el servicio registrado de forma total o en partes. Si decide emitir la factura por el total, el valor del campo **Cdad. a facturar** deberá ser igual que el valor del campo **Cantidad**. Puede registrar una factura completa junto con un envío completo y puede registrar una factura completa para un envío completo ya registrado que no se haya facturado ni consumido.  
   >  
   > Cuando se registra una factura parcial, hay dos formas de especificar la cantidad para facturar. Si va a registrar el servicio con la opción **Enviar y facturar**, el valor del campo **Cdad. a facturar** deberá ser igual que el valor del campo **Cantidad a enviar**. Si desea facturar un envío ya registrado, la cantidad para facturar no debe ser superior al valor especificado en el campo **Cantidad enviada**.  
  
5. Seleccione **Registrar** y, a continuación, en **Facturar** o **Enviar y facturar**. Obtenga más información, vaya a [Registrar en Service Management](service-service-posting.md).  
  
 La línea de servicio seleccionada se registrará. Puede registrar varias líneas de servicio a la vez. Para ello, selecciónelas y elija **Registrar**. Para hacerlo, asegúrese de rellenar toda la información necesaria en las líneas.  
  
 Cuando se registra el pedido con la opción **Facturar**, se crea una factura de servicio registrada junto con los movimientos correspondientes y actualiza los campos pertinentes en las líneas de servicio del pedido. Asimismo, se actualizan los documentos de envío registrados previamente con las cantidades facturadas. Si selecciona la opción de registro **Enviar y facturar**, se crea un envío registrado.

## <a name="to-create-a-service-invoice-manually"></a>Para crear una factura de servicio manualmente

Normalmente, después de que registre un pedido de servicio con la opción **Facturar** o **Enviar y facturar**, se registrará automáticamente una factura de servicio. Aún así, puede que necesite emitir una factura que no esté vinculada a un contrato o pedido de servicio. Este procedimiento explica cómo emitir una factura al mismo tiempo que el cliente recibe el servicio.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Factura servicio** y luego elija el enlace relacionado.  
2. Cree una factura de servicio nueva.  
3. Rellene el campo **No.**. .  
  
    > [!NOTE]  
    >  Si ha configurado números de serie para facturas de servicio en la página **Config. gestión servicio**, puede seleccionar **Entrar** para seleccionar el siguiente número de factura de servicio disponible.  
  
4. En el campo **Nº cliente**, introduzca el número de un cliente. Seleccione el cliente pertinente de la lista.  
  
    Los campos del cliente se rellenan con información de la tarjeta **Cliente**.  
  
5. Especifique una fecha en el campo **Fecha registro**. Esta fecha aparecerá en los movimientos registrados. Este campo muestra su fecha de trabajo actual, pero puede cambiar la fecha.  
6. En el campo **Fecha emisión documento** introduzca la fecha que aparecerá en la factura impresa y se utilizará para calcular la fecha de vencimiento.  
7. Rellene las líneas de servicio de la factura. Rellene los campos **Tipo**, **Nº** y **Cantidad** para registrar los productos, los recursos y los costes que se han empleado en el servicio.

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders"></a>Para crear una factura que combine líneas de albarán registradas de uno o más pedidos de servicio

Tal vez necesite crear una factura de servicio por un servicio que ya se ha enviado, ya sea de uno o de varios pedidos, pero que aún no se ha facturado ni consumido. Puede rellenar las líneas de factura de forma automática con las líneas de envío registrado seleccionadas para un cliente concreto.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Factura servicio** y luego elija el enlace relacionado.  
2. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Cree líneas de factura para servicios enviados pero no facturados. Opcionalmente, puede utilizar la acción **Obtener líneas envío** para agregar líneas de envío a la factura.  
4. Registre la factura de servicio.  
  
 Se crean la factura de servicio registrada y los movimientos correspondientes. Los documentos de envío registrados previamente se actualizan con las cantidades facturadas y las cantidades en las líneas de servicio de los pedidos de origen.  

## <a name="to-create-a-service-credit-memo"></a>Para crear un abono de servicio

Normalmente se utiliza un documento de nota de crédito de servicio cuando un cliente devuelve un artículo. Sin embargo, también puede utilizarlos para reembolsar a un cliente o para corregir una factura que fue un error.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Abonos servicio** y, a continuación, elija el vínculo relacionado.  
2. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Los campos **Fecha de registro** y **Fecha de emisión de documento** muestran la fecha del trabajo. Aunque podría cambiarlo si lo necesita.    
4. En las líneas de abono, escriba información acerca de los productos devueltos o eliminados, o bien especifique la compensación que se va a proporcionar al cliente.  

## <a name="correct-errors-in-service-invoices"></a>Corregir errores en facturas de servicios

Puede eliminar facturas de servicios que tengan asientos del libro mayor de servicios asociados. Esto significa que puede corregir errores o realizar cambios en las facturas de servicios sin quedarse atascado ni perder datos. Por ejemplo, si olvida asignar un grupo contable de productos a una cuenta del L/M, puede agregarlo más tarde y volver a crear la factura del servicio.

Use la acción :::image type="content" source="media/copilot-delete-trash-can.png" alt-text="Icono Eliminar acción"::: para eliminar una factura de servicio. 

Cuando elimina una factura de servicio, sucede lo siguiente:

* Publicar un movimiento de contabilidad de servicios correctivos
* Restaure la fecha y el período de facturación en el contrato, lo que le permitirá crear la factura nuevamente.

> [!NOTE]
> Puede revertir varias facturas, pero debe hacerlo de forma secuencial, empezando por la última factura.
>
> No puede eliminar una factura de servicio si sus detalles, como el período de facturación o la opción **Pagado por adelantado** se cambiaron en el contrato de servicio relacionado. Asegúrese de eliminar las facturas antes de cambiar la configuración del contrato de servicio.

## <a name="see-also"></a>Consulte también

[Registrar facturas de servicio](service-how-to-post-service-orders.md)  
[Configurar la gestión de servicios](service-setup-service.md)  
[Registro de servicio](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
