---
title: Introducción a la fabricación de Contoso Coffee
description: Descripción general de escenarios sobre cómo los datos de demostración de Contoso Coffee pueden ayudarle a aprender a usar las capacidades de fabricación en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4765
author: brentholtorf
ms.author: bholtorf
---

# Introducción a la fabricación de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para Business Central agregan datos de demostración que puede usar para aprender a usar las capacidades de fabricación en Business Central.  

La aplicación proporciona cuatro productos optimizados para diferentes escenarios:

- **SP-SCM1009 Airpot**  

  Este producto es una lista de materiales (L.M.) con un producto semiterminado, **Ruta**. Úselo para demostrar el flujo de producción estándar. Está configurado con rutas alternativas que puede usar para demostrar varios escenarios que implican a subcontratistas. El método de coste es *Estándar*.  

- **SP-SCM1011 Airpot Duo**  

  Este producto requiere seguimiento de artículos y tiene un componente que también requiere seguimiento de artículos. El método de coste es *Específico*.  

- **SP-SCM1004 Autodrip**  

  Este producto es una L.M. con un producto semiterminado, **Ruta**. Le recomendamos que demuestre los diversos métodos de baja tanto para componentes como para operaciones. El método de coste es *Estándar*.

- **SP-SCM1006 AutoDripLite**

  Este producto tiene tres variantes y tres listas de materiales (L.M.) que se pueden asignar a unidades de almacenamiento. El producto utiliza el concepto de L.M. ficticia. El método de coste es *Estándar*.

Las actividades de fabricación para todos los escenarios utilizan la ubicación *PRINCIPAL*.  

> [!IMPORTANT]
> Antes de ejecutar cualquiera de los escenarios para Contoso Coffee, registre las líneas del diario de productos con saldos iniciales. Para ver más requisitos, consulte la sección [Configurar datos de Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## Configuración de datos de demostración de Contoso Coffee para fabricación

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

|Campo  |Descripción  |
|---------|---------|
|**Almacén de fabricación** |Especifica el almacén que desea usar para las operaciones de producción. El valor predeterminado es *PRINCIPAL*, pero puede cambiarlo para adaptarlo a sus necesidades.|


Una vez que esté listo, elija la acción **Crear datos de demostración** acción. Se tarda unos minutos en agregar los datos a la base de datos subyacente, pero luego ya está listo para ejecutar los distintos escenarios.  

## Escenarios

Los datos de fabricación de Contoso Coffee admiten actualmente los siguientes escenarios de fabricación para pruebas y entrenamiento:

1. [Crear una nueva L.M. de producción y una versión de L.M.](create-new-production-bom-version.md)  
2. [Crear una nueva ruta](create-new-routing.md)  
3. [Crear una nueva orden de producción planificada en firme y cambiarla](create-firm-planned-production-order-change.md)  
4. [Combinar la baja automática y la manual](combine-automatic-manual-flushing.md)  
5. [Utilizar la planificación de pedidos para crear y reservar suministros](order-planning-create-reserve-supply.md)  
6. [Configurar y procesar una operación de subcontratación](set-up-process-subcontracting-operation.md)  
7. [Configurar nueva capacidad](set-up-new-capacity.md)  
8. [Previsión de la demanda de variantes de producto con diferentes L.M. asignadas](variants.md)  

Lea los pasos para cada escenario en el artículo correspondiente.  

> [!IMPORTANT]
> Estos tutoriales requieren que la experiencia del usuario esté establecida en *Premium* en la página **Información empresa**.

## Consulte también .

[Fabricación](../../production-manage-manufacturing.md)  
[Informes y análisis de producción en Business Central](../../production-reports.md)  
