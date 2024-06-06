---
title: Introducción a Contoso Coffee
description: Descripción general de escenarios sobre cómo los datos de demostración de Contoso Coffee pueden ayudarle a aprender a usar las capacidades de almacenamiento en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# Introducción al almacenamiento de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para Business Central agregan datos de demostración que puede usar para aprender a usar las capacidades de almacenamiento en Business Central. Puede configurar las características del almacén de varias maneras, consulte [Descripción general de las diferentes opciones de configuración](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

La aplicación proporciona tres almacenes optimizados para diferentes escenarios:

- **PLATA**  

  Este almacén está configurado para usar ubicaciones. Se puede configurar fácilmente para admitir funciones básicas o avanzadas. 

- **AMARILLO**  

  Este almacén utiliza la configuración de almacén avanzada, pero no utiliza ubicaciones. Se puede reconfigurar para admitir configuraciones básicas.

- **BLANCO**  

  Esta ubicación utiliza la configuración de almacén avanzado con ubicaciones y almacenamientos dirigidos, lo que permite reglas más avanzadas sobre cómo se mueven los productos en el almacén.

## Configurar datos de Contoso Coffee para almacenamiento

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Una vez instaladas las aplicaciones relevantes, vaya a la página de la [Herramienta de demostración de Contoso](https://businesscentral.dynamics.com/?page=5194) en [!INCLUDE [prod_short](../../includes/prod_short.md)], seleccione la línea *Módulo de almacén* y use la acción **Configurar** para preparar los módulos. En las siguientes tablas se describen las configuraciones:  

|Campo  |Descripción  |
|---------|---------|
|**Ubicación almacén**  |El almacén a utilizar para escenarios de almacén básico.|
|**Avanzada de almacén**  |El almacén a utilizar para escenarios de logística sencilla.|
|**Almacenamiento y recogida dirigidos por almacén**  |El almacén a utilizar para escenarios de logística avanzada.|
|**Ubicación en tránsito**  |La ubicación que se usará para el almacén de tránsito en escenarios de transferencia.|
|**Nº cliente**  |El cliente a utilizar para los escenarios básicos y sencillos en las operaciones de venta.|
|**N.º proveedor**  |El proveedor que se utilizará para todos los escenarios en las operaciones de compra.|
|**N.º de producto 1**  |El producto principal que se usará para todos los escenarios.|
|**N.º de producto 2**  |El producto adicional que se usará para todos los escenarios.|
|**N.º de producto 3**  |El producto con seguimiento.|

Una vez que esté listo, elija la acción **Crear datos de demostración** acción. Se tarda unos minutos en agregar los datos a la base de datos subyacente, pero luego ya está listo para ejecutar los distintos escenarios.  

> [!IMPORTANT]
> Si está ejecutando los escenarios, es posible que desee verificar que su usuario se haya agregado para los almacenes seleccionados. Para obtener más información, vea [Configurar los empleados de almacén](../../warehouse-how-to-set-up-warehouse-employees.md).

## Escenarios

Los datos de demostración de almacenamiento de Contoso Coffee admiten actualmente los siguientes escenarios de pruebas y entrenamiento:

1.  [Tutorial de flujo entrante y saliente en las configuraciones de almacén básico](warehouse-basic-flow-putaway-pick.md)
2.  [Tutorial sobre el flujo entrante y saliente en configuraciones del almacenamiento mixto](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Tutorial del flujo de entrada y salida en Configuración avanzada de almacén con ubicación y selección dirigidas](warehouse-directed-flow.md)

Lea los pasos para cada escenario en el artículo correspondiente.  

## Consulte también .

[Configuración de inventario](../../inventory-setup-inventory.md) 
[Cómo configurar almacenes](../../inventory-how-setup-locations.md) 
[Almacenamiento](../../warehouse-manage-warehouse.md) 
[Detalles de diseño](../../design-details-warehouse-overview.md) 
