---
title: 'Tutorial: Configuración y facturación de prepagos de ventas | Documentos de Microsoft'
description: Los prepagos son pagos que se facturan y registran en un pedido de prepago de ventas o compras antes de la facturación final. Es posible que solicite un depósito antes de fabricar productos del pedido, o que solicite un pago antes de enviar productos al cliente. La funcionalidad de prepagos en Business Central se utiliza para facturar y cobrar depósitos de los clientes o remitir depósitos a los proveedores. De este modo, puede asegurar que todos los pagos estén registrados contra una factura.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: c24fe7eea180b008401f58a401f0e74de2981086
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786676"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Tutorial: Configuración y facturación de prepagos de ventas

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

Los prepagos son pagos que se facturan y registran en un pedido de prepago de ventas o compras antes de la facturación final. Es posible que solicite un depósito antes de fabricar productos del pedido, o que solicite un pago antes de enviar productos al cliente. La funcionalidad de prepagos en [!INCLUDE[d365fin](includes/d365fin_md.md)] se utiliza para facturar y cobrar depósitos de los clientes o remitir depósitos a los proveedores. De este modo, puede asegurar que todos los pagos estén registrados contra una factura.  

 Los requisitos de los prepagos se pueden definir para un cliente o proveedor, para todos los productos o para algunos. Una vez realizada la configuración necesaria, puede generar facturas de prepago a partir de pedidos de compra y venta para el importe calculado del prepago. Puede cambiar los importes predeterminados en la factura según sea necesario. Por ejemplo, puede enviar facturas de prepago adicionales si es necesario añadir nuevos productos al pedido.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial  
 En este tutorial aparecen los siguientes ejemplos:  

-   Configuración de prepagos  
-   Creación de un pedido que requiera un prepago  
-   Creación de una factura de prepago  
-   Corrección de los requisitos de prepago en un pedido  
-   Aplicación de prepagos a un pedido  
-   Facturación del importe final en un pedido con prepago  

### <a name="roles"></a>Roles  
 En este tutorial se incluyen tareas para las siguientes funciones:  

-   Administradora de contabilidad (Felisa)  
-   Procesadora de pedidos (Susana)  
-   Administrador Cobros (Andrés)  

## <a name="story"></a>Historia  
 Felisa es administradora de contabilidad. Ella decisiones sobre qué clientes deben abonar un depósito antes de que se fabriquen o envíen los productos. Felisa configura [!INCLUDE[d365fin](includes/d365fin_md.md)] para calcular automáticamente los prepagos.  

 Susana es procesadora de pedidos de ventas. Cuando un cliente llama para realizar un pedido, ella lo introduce en el sistema mientras el cliente está en el teléfono. Así, puede verificar los precios y las condiciones de pago con el cliente en el momento, y puede realizar ajustes en el pedido mientras negocia con el cliente.  

 Andrés trabaja en el departamento de Cobros, donde registra facturas y pagos.  

 En este ejemplo, Felisa configura los requisitos de prepago para el cliente Sellafrio, basándose en su historial crediticio, e imparte instrucciones a Susana sobre el modo de gestionar sus pedidos.  

 Cuando el cliente llama, Susana negocia con el cliente hasta alcanzar un acuerdo. Ella puede elegir calcular el prepago de varias maneras diferentes.  

 Una vez que Susana envíe la factura prepago, el cliente solicita un producto adicional. Susana actualiza el pedido y crea una segunda factura prepago.  

 Andrés registra el pago del cliente y lo aplica a las facturas; a continuación, envía la factura final.  

## <a name="setting-up-prepayments"></a>Configuración de prepagos  
 Felisa configura el sistema para gestionar los prepagos de los clientes.  

-   Felisa decide utilizar la misma serie numérica para los prepagos que las usadas para la facturación de venta.  
-   Felisa configura la aplicación para que compruebe si se requieren prepagos antes de la facturación final de los pedidos.  
-   Felisa configura valores predeterminados para un porcentaje de prepago requerido para ciertos productos y clientes.  

En los siguientes procedimientos, se describe cómo realizar las tareas de Felisa:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Para configurar series numéricas para prepagos  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.  
2.  En la página **Conf. ventas y cobros**, amplíe la ficha desplegable **Numeración**.  
3.  Verifique que la serie numérica de las facturas de prepago registradas en el campo **Nº fact. prepago registrada** sea la misma que para las facturas de venta registradas (**Nº serie fact. registrada**) y que la serie numérica para abonos de prepago registrados (**Nº abono prepago registrado**) sea la misma que para los abonos registrados (**Nº serie abono registrado**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Para bloquear envíos por prepagos sin abonar  
1.  En la página **Conf. ventas y cobros**, en la ficha desplegable **General**, seleccione la casilla **Comprobar prepago al registrar**.

    Hora no se puede enviar ni facturar un pedido que tenga una cantidad de prepago sin abonar.  

Felisa exige que al cliente 20000 se le facture un prepago del 30% en todos los pedidos, de manera predeterminada. Por lo tanto, escribirá un porcentaje de prepago predeterminado en la ficha cliente.  

Felisa requiere que a todos los clientes se les facture un depósito del 20% para el producto 1100. El cliente 20000 tiene un mal historial de prepagos, por lo que requiere un prepago del 40% para el cliente 20000 para el producto 1100. En el procedimiento siguiente se ilustra el modo de configurar los porcentajes de prepago predeterminados.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Para asignar porcentajes de prepago predeterminados a clientes y productos  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.  
2.  Abra la ventana de la ficha del cliente 20000 (Sellafrio).
3.  En el campo **% prepago**, escriba **30**.  
4.  Elija el botón **Aceptar** para cerrar la ficha de cliente.  
5.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
6.  Abrir la ficha para el cliente 1100.
7.  Seleccione la acción **Porcentajes prepago**.  
8.  Rellene dos líneas en la página **Porcentajes prepago ventas** como sigue:  

    |**Tipo venta**|**Código ventas**|**Nº producto**|**% prepago**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Cliente**|**20000**|**1100**|**40**|  
    |**Todos clientes**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Dependiendo de su país o región, también debe especificar un código de grupo de impuesto en la ficha desplegable **Facturación** para los productos 1000 y 1100.  

9. Cierre todas las páginas.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Para especificar una cuenta para los prepagos de ventas en la configuración del registro general  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración grupos contables** y luego elija el enlace relacionado.  
2.  Seleccione la línea donde el campo de **General neg. grupo contable** se establece en **EXPORTAR**, y el campo **General producción. grupo contable** se establece en **MERCADERÍA** y, a continuación, seleccione **Editar**.  
3.  En la página **Ficha grupos contabilización**, en el campo **Cuenta prepago ventas**, especifique la cuenta correspondiente.  
4.  Elija el botón **Aceptar**.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Creación de un pedido que requiera un prepago  
 En el siguiente ejemplo, Susana, la procesadora de pedidos, crea un pedido cuando habla con un cliente. Los productos que solicita del cliente requieren un prepago, y el cliente ha realizado en el pasado algunos pagos con retraso. Por tanto, se ha indicado a Susana para requerir un importe fijo de 2.000 como prepago en el pedido.  

El cliente solicita poder pagar el 35%, con lo que Susana está de acuerdo. Por tanto, ella cambia el pedido.  

Susana crea la factura de prepago y la envía al cliente.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Para crear un pedido de venta con prepago  
1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  En el campo **Venta a-N.º cliente**, seleccione **20000**.  
5.  Acepte el la advertencia de saldo pendiente que se muestra.  
6.  Rellene dos líneas de venta con la siguiente información.  

    |**Escriba**|**Nº**|**Cantidad**|  
    |--------------|-------------|------------------|  
    |**Producto**|**1000**|**1**|  
    |**Producto**|**1100**|**1**|

    Los campos de prepago de la línea de ventas están ocultos de manera predeterminada, por lo que deberá mostrarlos.  

7. Compruebe que el campo **% prepago** de la línea con el producto **1000** contiene **30**. El valor predeterminado se ha tomado de la cabecera de venta, que se ha rellenado de la ficha cliente.  

    El campo **% prepago** de la línea con el producto **1100** contiene **40**. Es el porcentaje que especificó en la página **Porcentajes prepago ventas** para el producto **1100** y el cliente **20000**.  

    Para obtener más información, consulte [Configurar prepagos](finance-set-up-prepayments.md).  
8. Seleccione la acción **Estadísticas**.  
9. En la ficha desplegable **Prepago**, el campo de **Importe línea prepago excl. IVA** contiene **1.560**. Si ahora crea una factura prepago para el pedido, ésta será el importe que figura en la factura.  

    En este ejemplo, se ha indicado a Susana que sugiera un prepago total de 2000 para el pedido.  

    > [!IMPORTANT]  
    >  Dependiendo de su país o región, el paso siguiente puede que no se aplique.  
10. Cambie el importe que aparece en el campo **Importe línea prepago excl. IVA** a **2000** y cierre la página.  
11. Consulte el campo **% prepago** de la líneas de ventas, y verá que se ha calculado de nuevo el valor hasta **40,81625**.  

    El nuevo cálculo incluye todas las líneas con un porcentaje de prepago superior a 0.  

    Ahora, el cliente pregunta si el porcentaje de prepago se puede ajustar en 35%. El supervisor de Susana aprueba el cambio.  

12. En la página **Pedido venta**, campo **% prepago**, introduzca **35**.  
13. En la advertencia que aparece, seleccione el botón de **Sí**. Un índice del 35% será aplicado como el porcentaje de pago para todo el pedido.  
14. Verifique que se han actualizado las líneas en consecuencia.  

## <a name="creating-a-prepayment-invoice"></a>Creación de una factura de prepago  
Después de escribir los valores de prepago correctos en el pedido, Susana crea la factura de prepago y la envía al cliente.  

#### <a name="to-create-a-prepayment-invoice"></a>Para crear una factura de prepago  

1.  En la página **Pedido de ventas**, elija la acción **Registrar factura prepago**.  

> [!NOTE]  
>  Susana debería seleccionar **Registrar e imprimir factura prepago** y enviar por correo la factura al cliente.  

## <a name="creating-an-additional-prepayment-invoice"></a>Creación de una factura de prepago adicional  
Al día siguiente, el cliente llama a Susana y realiza cambios en el pedido. El cliente desea dos unidades del producto 1100. Susana vuelve a abrir y actualiza el pedido y, a continuación, crea una segunda factura de prepago en el pedido y la envía al cliente.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Para crear una factura de prepago adicional  

1.  En la página **Pedido venta**, seleccione la acción **Volver a abrir**.  
2.  En la línea del producto **1100**, en el campo **Cantidad**, escriba **2**.  

    Desplácese para ver los campos de prepago. El campo de **Prepago Excl de la línea importe. IVA** contiene ahora **630** y el campo **Importe prepago facturado excl. IVA** contiene **315**. Este campo muestra que hay un importe de prepago adicional que aún no se ha facturado.  
3.  Para registrar una factura para el importe de prepago adicional, elija la acción **Registrar factura prepago**.  

## <a name="applying-the-prepayments"></a>Aplicación de los prepagos  
El cliente paga el importe de prepago y Andrés, que trabaja en el departamento contable, registra el pago y lo aplica a las facturas de prepago.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Para aplicar un pago a las facturas de prepago  

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de recibos de efectivo** y luego elija el enlace relacionado.  
2.  Rellene una línea de diario con la siguiente información.  

    |Nombre del campo|Introduzca|  
    |----------------|-----------|  
    |**Tipo documento**|**Pago**|  
    |**Tipo mov.**|**Cliente**|  
    |**Nº cuenta**|**20000**|  
3. Seleccione la acción **Liquidar movs.**.  
4.  En la página **Movs. pendientes cliente**, seleccione la primera factura prepago y, a continuación, elija **Marcar id. de liquidación**.  
5.  Repita el paso anterior para el segundo prepago.  
6.  Elija el botón **Aceptar**.  

    El campo de importe se habrá rellenado ahora con la suma de las dos facturas de prepago.  

7.  Registre el diario.  

## <a name="invoicing-the-remaining-amount"></a>Facturación del importe restante  
Se ha notificado a Andrés que los productos del pedido se han enviado y que el pedido está listo para su facturación. Andrés crea la factura para el pedido.  

#### <a name="to-invoice-the-remaining-amount"></a>Para facturar el importe restante  
1. Abra el pedido de venta.  
2. Seleccione **Entregar y facturar** y, a continuación, **Aceptar**.  

> [!NOTE]  
>  Normalmente, el departamento de envíos ya habrá registrado el envío.  

Andrés puede ver el historial para verificar que la factura de venta fue creada tal como se previó.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Histórico facturas venta** y luego elija el enlace relacionado.  

## <a name="next-steps"></a>Pasos siguientes  
En este tutorial, ha visto los pasos necesarios para configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] para gestionar prepagos. Ha configurado los porcentajes de prepago predeterminados en clientes y productos, y también ha utilizado distintos métodos para calcular los prepagos de un pedido. Ha tratado de asignar un importe de prepago total al pedido y ha calculado el importe de prepago como un porcentaje del pedido completo.  

También ha registrado una factura de prepago, creado una segunda factura de prepago cuando se modificó el pedido y registrado la factura final por el importe restante.  

La función de prepagos en [!INCLUDE[d365fin](includes/d365fin_md.md)] facilita la configuración y la imposición de reglas de prepago para clientes y productos; además, permite registrar cada pago contra una factura.  

## <a name="see-also"></a>Consulte también  
[Facturación de prepagos](finance-invoice-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)
