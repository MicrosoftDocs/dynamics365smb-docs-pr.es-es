---
title: Tutorial de contratos de servicio para productos de servicio
description: Este artículo lo guía a través de varios escenarios que involucran contratos y artículos de servicio.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/08/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="walkthrough-of-service-contracts-for-service-items"></a>Tutorial de contratos de servicio para productos de servicio

Este tutorial demuestra varios procesos principales:

- Creación de artículos de servicio a través de ventas
- Creación y facturación de un contrato de servicio
- Creación de un pedido de servicios para un contrato de servicio
- Asignar un recurso según la capacidad y la zona
- Completar la entrada de tiempo para la Orden de Servicio
- Registrar y facturar el pedido de contrato de servicio

## <a name="creation-of-service-items"></a>Creación de productos de servicio

### <a name="scenario"></a>Escenario

Susan, la procesadora de pedidos, registra un pedido de venta que vende un artículo configurado para generar un artículo de servicio.  

### <a name="steps"></a>Pasos

1. Verifique que el **Artículo** tenga **Grupo de artículos de servicio** seleccionado.
   
    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
    2. Seleccione el elemento *S-100* y ábralo.
    3. Verifique el valor en el campo **Grupo de elementos de servicio**.
       
2. Publique la **Orden de venta** para crear el artículo de servicio para el cliente.  

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
    2. Seleccione el pedido para el cliente 10000. El n.º de pedido externo es: *SVC-1*.
    3. Elija la acción **Registrar** para enviar el artículo al cliente.

### <a name="results"></a>Resultados

- Se crea un producto de servicio para el cliente 10 000

## <a name="invoicing-a-service-contract"></a>Facturar un contrato de servicio

### <a name="scenario-1"></a>Escenario

Charles, el gerente de servicio, crea un contrato de servicio para facturar las visitas de mantenimiento periódicas.

3. Cree el **Contrato de servicio** para el nuevo artículo de servicio
    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Contratos de servicio** y luego elija el enlace relacionado.
    2. Seleccione la acción **Nuevo**.  
    3. En el cuadro de diálogo de confirmación, elija **Sí** para crear un contrato usando una plantilla. 
    4. Seleccione *Contrato sin prepago - Mensual*.
    5. En la ficha desplegable Servicio, en **Tipo de orden de servicio**, introduzca **MANTENIMIENTO**.
    6. En las líneas, escriba la siguiente información:

    |Nº prod. servicio|Valor línea|  
    |----------------|----------|  
    |SV000001|6000|

    7. Para firmar el contrato, elija la acción **Firmar contrato**.
    8. Elija **Sí** para confirmar la creación de una factura de servicio. Recibe un mensaje de confirmación con el número de factura de servicio.

3. Registre la factura de servicio
   1. Elija el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Factura servicio** y luego elija el enlace relacionado.
   2. Localice la factura de servicio y elija la acción **Registrar**.

### <a name="results-1"></a>Resultados

- Se crea un contrato de servicio firmado, con asientos en el libro mayor
- Se crea una factura de servicio registrada

## <a name="create-a-service-order-for-a-service-contract-and-assign-resources"></a>Creación de un pedido de servicio para un contrato de servicio y asignar recursos

### <a name="scenario-2"></a>Escenario

Charles, el gerente de servicio, crea las órdenes de servicio para las órdenes de mantenimiento regulares según el contrato de servicio y luego revisará el panel de distribución para asignarlas.

### <a name="steps-1"></a>Pasos

1. Ejecutar las Órdenes de Servicio que cumplen con las obligaciones de los Contratos de Servicio activos.
   1. Elija el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear pedidos serv. contrato** y, a continuación, elija el enlace relacionado.
   2. Ingrese las fechas de inicio y finalización del mes en los campos Fecha de inicio y Fecha de finalización en la ficha desplegable Opciones
   3. Elija **Aceptar** para confirmar la creación de una orden de servicio. Recibe un mensaje de confirmación con el número de órdenes de servicio creadas.

2. Revisar los Pedidos en espera de asignación a través del Panel de distribución
   1. Elija el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Panel despacho** y luego elija el enlace relacionado.
   2. El Panel de distribución muestra todas las Órdenes de Servicio abiertas, junto con el **N.º de Asignaciones** para mostrar si las Órdenes de Servicio se han asignado a un Recurso.
   3. Elija la acción **Mostrar documentos** para abrir una Orden de servicio.  Ve que el cuadro informativo Líneas de elementos de servicio muestra qué recursos están capacitados para trabajar con este elemento.

3. Asignar un recurso a la orden de servicio
   1. Desde la orden de servicio, elija la acción de línea **Asignaciones de recurso**
   2. Escriba la siguiente información para la Asignación de recurso

    |Nº prod. servicio|N.º recurso|Fecha asignación|Horas asignadas|
    |----------------|------------|---------------|---------------|  
    |SV000001|RESOURCE1|h|1|

    3. La asignación se cambia a un estado activo.
    4. Al actualizar el tablero de distribución se muestra el **N.º de asignaciones** cambiando de 0 a 1 para la orden de servicio.

### <a name="results-2"></a>Resultados

- Se crean órdenes de servicio para los contratos de servicio
- Las órdenes de servicio se asignan a un recurso para completar el trabajo

## <a name="complete-the-time-entry-for-the-service-order-and-post-the-service-order"></a>Complete la entrada de tiempo para la orden de servicio y publique la orden de servicio

### <a name="scenario-3"></a>Escenario

El técnico de servicio registra su tiempo directamente en la Orden de servicio y luego marcará la orden como finalizada.

> [!NOTE]
> El ingreso de horas para órdenes de servicio se puede ingresar a través de hojas de horas. Para obtener más información, consulte [enlace a la parte de horas si esta nota tiene sentido].

### <a name="steps-2"></a>Pasos

1. Localice la Orden de Servicio e ingrese el tiempo en la Línea de Servicio
   1. Elija el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.
   2. Localice la orden de servicio para ingresar el tiempo.
   3. Elija la acción de línea **Línea de servicio**.
   4. Escriba la siguiente información

    |Tipo|N.º|Cantidad|Cant. a consumir|
    |----|---|--------|--------|   
    |Recurso|RESOURCE1|2|2|

2. En el pedido de servicio, registre el consumo
   1. Elija la acción **Registrar** para completar la Orden de Servicio, seleccione la acción **Envío y consumo** y luego elija el botón **Aceptar**.

### <a name="results-3"></a>Resultados

- Los asientos del libro mayor de servicios se crean asociados con el artículo de servicio, el contrato de servicio y el recurso

## <a name="see-also"></a>Consulte también

[Introducción a datos de demostración de Contoso Coffee](../../contoso-coffee/contoso-coffee-intro.md)  
[Acerca de las órdenes de producción](../../production-about-production-orders.md)
