---
title: Configuración y facturación de prepagos de ventas
description: Los prepagos son pagos que se facturan y registran en un pedido de prepago de ventas o compras antes de la facturación final.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/03/2021
ms.author: bholtorf
---
# Tutorial: Configuración y facturación de prepagos de ventas

Este tutorial lo lleva a través del proceso de configuración y uso de prepagos en [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Por ejemplo, puede enviar más facturas prepago adicionales si es necesario añadir más productos al pedido.  

## Acerca de este tutorial  

En este tutorial aparecen los siguientes ejemplos:  

- Configuración de prepagos  
- Creación de un pedido que requiera un prepago  
- Creación de una factura de prepago  
- Corrección de los requisitos de prepago en un pedido  
- Aplicación de prepagos a un pedido  
- Facturación del importe final en un pedido con prepago  

### Roles

En este tutorial se incluyen tareas para las siguientes funciones:  

- Administradora de contabilidad (Felisa)  
- Procesadora de pedidos (Susana)  
- Administrador Cobros (Andrés)  

## Historia

 Phyllis es administradora de contabilidad y toma decisiones sobre qué clientes deben abonar un depósito antes de que se fabriquen o envíen los productos. Felisa configura [!INCLUDE[prod_short](includes/prod_short.md)] para calcular automáticamente los prepagos.  

 Susana es procesadora de pedidos de ventas. Cuando un cliente llama para realizar un pedido, Susan lo introduce en el sistema mientras el cliente está al teléfono. Así, Susan puede verificar los precios y las condiciones de pago con el cliente en el momento, y realiza cambios en el pedido mientras negocia con el cliente.  

 Arnie trabaja en el departamento de Clientes y registra facturas y pagos.  

 En este ejemplo, Felisa configura los requisitos de prepago para el cliente Sellafrio, basándose en su historial crediticio. Phyllis le da instrucciones a Susan sobre cómo manejar sus pedidos.  

 Cuando llama el cliente, Susan negocia con el cliente hasta alcanzar un acuerdo, y luego elige calcular el prepago de diversas formas distintas.  

 Una vez que Susana envíe la factura prepago, el cliente solicita un producto adicional. Susana actualiza el pedido y crea una segunda factura prepago.  

 Andrés registra el pago del cliente y lo aplica a las facturas; a continuación, envía la factura final.  

## Configurar prepagos

Felisa configura el sistema para gestionar los prepagos de los clientes.  

- Felisa decide utilizar la misma serie numérica para los prepagos que las usadas para la facturación de venta.  
- Felisa configura la aplicación para que compruebe si se requieren prepagos antes de la facturación final de los pedidos.  
- Felisa configura valores predeterminados para un porcentaje de prepago requerido para ciertos productos y clientes.  

En los siguientes procedimientos, se describe cómo realizar las tareas de Felisa:  

### Para configurar series numéricas para prepagos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.  
2. En la página **Conf. ventas y cobros**, amplíe la ficha desplegable **Numeración**.  
3. Verifique que la serie numérica de las facturas de prepago registradas en el campo **Nº fact. prepago registrada** sea la misma que para las facturas de venta registradas (**Nº serie fact. registrada**) y que la serie numérica para abonos de prepago registrados (**Nº abono prepago registrado**) sea la misma que para los abonos registrados (**Nº serie abono registrado**).  

### Para bloquear envíos por prepagos sin abonar

1. En la página **Conf. ventas y cobros**, en la ficha desplegable **General**, seleccione la casilla **Comprobar prepago al registrar**.

Hora no se puede enviar ni facturar un pedido que tenga una cantidad de prepago sin abonar.  

Felisa exige que al cliente 20000 se le facture un prepago del 30% en todos los pedidos, de manera predeterminada. Por lo tanto, Phyllis escribirá un porcentaje de prepago predeterminado en la ficha del cliente.  

Felisa requiere que a todos los clientes se les facture un depósito del 20 % para el producto 1896-S. El cliente 20000 tiene un mal historial de pagos, por lo que Phyllis requiere un prepago del 40 % para el cliente 20000, para el producto 1896-S. En el procedimiento siguiente se ilustra el modo de configurar los porcentajes de prepago predeterminados.  

### Para asignar porcentajes de prepago predeterminados a clientes y productos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2. Abra la ventana de la ficha del cliente 20000 (Trey Research).
3. En la ficha desplegable **Pagos**, campo **% prepago**, introduzca **30**.  
4. Elegir la acción **Relacionado**, seleccione el elemento de menú **Ventas** y, a continuación, elija el elemento de menú **Porcentajes prepago**.  
5. Rellene dos líneas en la página **Porcentajes prepago ventas** como sigue:  

    |**Tipo venta**|**Código ventas**|**Nº producto**|**% prepago**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Cliente**|**20000**|**1896-S**|**40**|
    |**Cliente**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > Dependiendo de su país o región, también debe especificar un código de grupo de impuesto en la ficha desplegable **Costes y registro** para el producto 1896-S. Cuando utiliza la empresa de demostración, este campo ya está configurado.

6. Cierre todas las páginas.  

### Para especificar una cuenta para los prepagos de ventas en la configuración del registro general

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración grupos contables** y luego elija el enlace relacionado.  
2. Seleccione la línea donde el campo de **General neg. grupo contable** se establece en **NAC**, y el campo **General producción. grupo contable** se establece en **MERCADERÍA**.  
3. En el campo **Cuenta prepago venta**, especifique la cuenta relevante. Su selección se guarda automáticamente.  

> [!TIP]
> Si no puede ver el campo de la página **Configuración grupos contables**, utilice la barra de desplazamiento horizontal situada en la parte inferior de la página para desplazarse hacia la derecha.  

## Crear un pedido que requiera un prepago

 En el siguiente ejemplo, Susana, la procesadora de pedidos, crea un pedido cuando habla con un cliente. Los artículos que el cliente está ordenando requieren un prepago. Además, el cliente ha realizado algunos pagos atrasados en el pasado. Se ha indicado a Susana para requerir un importe fijo de **800** como prepago en el pedido.  

El cliente solicita que le permitan pagar el 35 %, lo que Susana acepta, y cambia el pedido.  

Susana crea la factura de prepago y la envía al cliente.  

### Para crear un pedido de venta con prepago

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el camppo **Nombre del cliente**, elija **Trey Research**.  
4. Cierre la advertencia de saldo pendiente que se muestra.  
5. Rellene dos líneas de venta con la siguiente información.  

    |**Tipo**|**Nº**|**Cantidad**|  
    |--------------|-------------|------------------|  
    |**Producto**|**1896-S**|**1**|  
    |**Producto**|**1900-S**|**1**|

    Los campos de prepago de la línea de ventas están ocultos de manera predeterminada. Para mostrar los campos debe personalizar la página. Para más información, vea [Para comenzar a personalizar una página a través del banner de personalización](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6. Compruebe que el campo **% prepago** de la línea con el producto **1900-S** contiene **30**. El valor predeterminado se ha tomado de la cabecera de venta, que se ha rellenado de la ficha cliente.  

    El campo **% prepago** de la línea con el producto **1896-S** contiene **40**. 40 es el porcentaje que especificó en la página **Porcentajes prepago ventas** para el producto **1896-S** y el cliente **20000**.  

    Para obtener más información, consulte [Configurar prepagos](finance-set-up-prepayments.md).  
7. En la acción **Pedido**, elija **Estadísticas**.  
8. En la ficha desplegable **Prepago**, el campo de **Cantidad prepago excl. IVA** contiene **458.16**. Si ahora crea una factura prepago para el pedido, 458,16 será el importe que figura en la factura.  

    En este ejemplo, se ha indicado a Susana que sugiera un prepago total de **800** para el pedido.  

    > [!IMPORTANT]  
    >  Dependiendo de su país o región, el paso siguiente puede que no se aplique.  
9. Cambie el importe que aparece en el campo **Importe prepago excl. Imp.** a **800** y cierre la página.  
10. Consulte el campo **% prepago** de la líneas de ventas, y verá que se ha calculado de nuevo el valor hasta **67,02438** y **67,02282**.  

     El nuevo cálculo incluye todas las líneas con un porcentaje de prepago superior a 0.  

     Ahora, el cliente pregunta si el porcentaje de prepago se puede ajustar en 35%. El supervisor de Susana aprueba el cambio.
11. En la página **Pedido venta**, en la ficha desplegable **Prepago**, en el campo **% de prepago**, especifique **35**.  
12. En la advertencia que aparece, seleccione el botón de **Sí**. Un índice del 35% será aplicado como el porcentaje de pago para todo el pedido.  
13. Verifique que se han actualizado las líneas correctamente.  

## Crear una factura de prepago

Después de escribir los valores de prepago correctos en el pedido, Susana crea la factura de prepago y la envía al cliente.  

### Para crear una factura de prepago

1. En la página **Pedido de ventas**, elija **Acciones**, en el grupo **Registro**, elija **Prepago** y, a continuación, seleccione **Registrar e imprimir factura prepago**.
2. Para registrar la factura, elija el botón **Sí**.  

> [!NOTE]  
> Susan ahora enviaría la factura al cliente.  

## Crear una factura de prepago adicional

Al día siguiente, el cliente llama a Susana y realiza cambios en el pedido. El cliente desea dos unidades del producto 1896-S. Susana vuelve a abrir y actualiza el pedido y, a continuación, crea una segunda factura de prepago del pedido y la envía al cliente.  

### Para crear una factura de prepago adicional

1. En la página **Pedido venta**, seleccione la acción **Liberar** y, después, **Reabrir**.  
2. En la línea del producto **1896-S**, en el campo **Cantidad**, escriba **2**.  

    En la acción **Pedido**, elija **Estadísticas**. El campo de **Cantidad prepago excl. IVA** contiene ahora **768.04** y el campo **Importe prepago facturado excl. IVA** contiene **417.76**. Estos valores muestran que hay un importe de prepago extra que aún no se ha facturado.  
3. Para registrar una factura para el importe de prepago extra, elija **Acciones**, **Registro**, **Prepago** y seleccione **Registrar e imprimir factura prepago**.
4. Para registrar la factura, elija el botón **Sí**.  

## Aplicar los prepagos

El cliente paga el importe del prepago. Arnie, del departamento de contabilidad, registra el pago y lo aplica a las facturas de prepago.  

### Para aplicar un pago a las facturas de prepago

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de recibos de efectivo**, y luego elija el enlace relacionado.  
2. Rellene una línea de diario con la siguiente información.  

    |Nombre del campo|Introduzca|  
    |----------------|-----------|  
    |**Tipo documento**|**Pago**|  
    |**Tipo mov.**|**Cliente**|  
    |**Nº cuenta**|**20000**|  
3. Elija la acción **Proceso**, y luego **Liquidar movs.**.  
4. En la página **Movs. pendientes cliente**, seleccione la primera factura prepago y, a continuación, elija la acción **Procesar** y, después, seleccione la acción **Marcar id. de liquidación**.  
5. Repita el paso anterior para el segundo prepago.  
6. Elija el botón **Aceptar**.  

    Los campos **Importe** se habrán rellenado ahora con la suma de las dos facturas de prepago.  

7. Para publicar el diario, elija la acción **Registrar e imprimir**, luego seleccione **Publicar**.
8. Elija el botón **Sí**.

## Facturar el importe restante

Se ha notificado a Andrés que los productos del pedido se han enviado y que el pedido está listo para su facturación. Andrés crea la factura para el pedido.  

### Para facturar el importe restante

1. Abra el pedido de venta.
2. Elija la acción **Registrar**, después **Registrar**.
3. Seleccione **Enviar y facturar** y, a continuación, elija el botón **Aceptar**.
4. Si desea obtener una vista previa de la factura, elija el botón **Sí**.

    > [!NOTE]  
    > Normalmente, el departamento de envíos ya habrá registrado el envío.  

    Andrés puede ver el historial para verificar que la factura de venta fue creada tal como se previó.

5. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas venta** y luego elija el enlace relacionado.  

## Actualizar el estado de los pedidos y facturas prepago automáticamente

Puede acelerar el procesamiento de pedidos y facturas configurando entradas de cola de trabajos que actualizan automáticamente el estado de esos documentos. Cuando se paga una factura de prepago, las entradas de la cola de trabajos pueden cambiar automáticamente el estado del documento de **Pago anticipado pendiente** a **Liberado**. Cuando configure las entradas de la cola de trabajos, las unidades de código que necesitará usar son **383 actualizado Pendiente Prepago Ventas** y **383 actualizado Pendiente Prepago Compra**. Le recomendamos que programe las entradas para que se ejecuten con frecuencia, por ejemplo, cada minuto. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md).

## Pasos siguientes

En este tutorial se han tratado los pasos siguientes para configurar [!INCLUDE[prod_short](includes/prod_short.md)] para gestionar prepagos. 

- Condigurar porcentajes de prepago predeterminados en clientes y productos.
- Utilizar diferentes métodos para calcular los prepagos de un pedido.  
- Calcular el monto del prepago como un porcentaje del total del pedido.
- Asignar un importe total de prepago al pedido.  

También ha registrado una factura de prepago, creado una segunda factura de prepago cuando se modificó el pedido y registrado la factura final por el importe restante.  

Las capacidades de prepago facilitan la configuración y aplicación de reglas de prepago para clientes y artículos. También le permiten registrar cada pago contra una factura.  

## Consultar la [formación de Microsoft](/training/modules/prepayment-invoices-dynamics-365-business-central/) relacionada

## Consulte también .

[Facturación de prepagos](finance-invoice-prepayments.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
