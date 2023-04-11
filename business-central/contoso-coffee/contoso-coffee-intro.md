---
title: Introducción a datos de demostración de Contoso Coffee
description: Descripción general de escenarios sobre cómo los datos de demostración de Contoso Coffee pueden ayudarle a aprender a usar las capacidades de Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Introducción a datos de demostración de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para Business Central agregan datos de demostración que puede usar para aprender a usar las capacidades de Business Central.  


## Configurar datos de Contoso Coffee

Para usar los datos de demostración de Contoso Coffee, debe instalar dos aplicaciones en la empresa correspondiente en [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Conjunto de datos de demostración de Contoso Coffee**  

    Esta aplicación ofrece datos de demostración para la aplicación base.  
- **Conjunto de datos de demostración de Contoso Coffee (ID de país)**  

    Esta aplicación agrega contenido específico del país sobre la aplicación base.

Agregue las aplicaciones a una empresa vacía en una suscripción pagada o como parte de una prueba. Por ejemplo, cree una nueva empresa sin datos de muestra de la guía de configuración asistida **Crear nueva empresa** que puede abrir desde la lista **Empresas**. A continuación, agregue las aplicaciones del [mercado](../ui-extensions-install-uninstall.md#install) en caso de que no se indiquen en la página **Administración de extensiones**.  

A continuación, debe completar:
 - La [Configuración de fabricación](manufacturing/contoso-coffee-manufacturing-intro.md) para preparar el uso de los [Escenarios de fabricación](#manufacturing-scenarios)
 - La [Configuración de almacenamiento](warehousing/contoso-coffee-warehousing-intro.md) para preparar el uso de los [Escenarios de almacenamiento](#warehousing-scenarios)

## Escenarios de Fabricación

Los datos de demostración de Contoso Coffee admiten actualmente los siguientes escenarios de fabricación para pruebas y entrenamiento:

1. [Crear una nueva L.M. de producción y una versión de L.M.](manufacturing/create-new-production-bom-version.md)  
2. [Crear una nueva ruta](manufacturing/create-new-routing.md)  
3. [Crear una nueva orden de producción planificada en firme y cambiarla](manufacturing/create-firm-planned-production-order-change.md)  
4. [Combinar la baja automática y la manual](manufacturing/combine-automatic-manual-flushing.md)  
5. [Utilice la planificación de pedidos para crear y reservar suministros](manufacturing/order-planning-create-reserve-supply.md)  
6. [Configurar y procesar una operación de subcontratación](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Configurar nueva capacidad](manufacturing/set-up-new-capacity.md)  
8. [Previsión de la demanda de variantes de producto con diferentes L.M. asignadas](manufacturing/variants.md)  

Lea los pasos para cada escenario en el artículo correspondiente.  

> [!IMPORTANT]
> Los tutoriales de fabricación requieren que la experiencia del usuario esté establecida en *Premium* en la página **Información empresa**.

## Escenarios de almacenamiento

Los datos de demostración de Contoso Coffee admiten actualmente los siguientes escenarios de almacenamiento para pruebas y entrenamiento:

1.  Configure ubicaciones predeterminadas, reciba y almacene con inventario, seleccione y envíe con selección de inventario en orden por pedido con [Tutorial del flujo de entrada y salida en Configuraciones básicas de almacén](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Reciba y almacene varios pedidos entrantes a la vez con recibo de almacén, envíe varios pedidos a la vez con envío de almacén, seleccione con selecciones de almacén con [Guía del flujo de entrada y salida en configuraciones de almacén mixtas](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Configure contenedores fijos para la unidad de medida del producto, tránsito directo del usuario para reducir los movimientos físicos de las mercancías, optimice la ubicación de las mercancías con el reabastecimiento de contenedores, divida las unidades de medida grandes en unidades más pequeñas, distribuya la selección entre los empleados del almacén con la hoja de trabajo de selección con [Guía del flujo de entrada y salida en Configuración avanzada de almacén con ubicación y recolección dirigidas](warehousing/warehouse-directed-flow.md)

Lea los pasos para cada escenario en el artículo correspondiente.
   
## Consulte también .

[Fabricación](../production-manage-manufacturing.md)  
[Gestión de almacén](../warehouse-manage-warehouse.md)  

