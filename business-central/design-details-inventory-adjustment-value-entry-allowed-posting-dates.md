---
title: 'Mensaje de error: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas"'
description: 'Resuelva el error del mensaje "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas" al ejecutar el trabajo por lotes Ajustar coste: movimientos de producto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# Mensaje de error: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas"

Al usar el trabajo por lotes **Ajustar coste: movimientos de producto** puede encontrarse con el siguiente mensaje de error:

**La fecha de registro no está comprendida en su periodo de fechas de registro permitidas**

Este mensaje indica que no puede publicar entradas para la fecha que introdujo. Puede solucionar este problema cambiando su configuración de usuario.

## Cambiar la configuración del usuario  

|Id. de usuario  |Permite registro desde  | Permitir registro hasta  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

En este caso, puede publicar en el rango de fechas del 11 al 30 de septiembre. Sin embargo, no se le permite registrar la entrada del valor de ajuste con una fecha de publicación del 10 de septiembre.  

### Descripción general de la configuración de la fecha de registro

#### Periodos inventario

|Fecha final  |Nombre  |Cerrada  |
|---------|---------|---------|
|2020-01-31     |2020 de enero      |  Sí    |
|2020-02-28     |Febrero de 2020     |  Sí    |
|2020-03-31     |Marzo de 2020        |  Sí    |
|2020-04-30     |Abril de 2020        |  Sí    |
|2020-05-31     |Mayo de 2020        |  Sí    |
|2020-06-30     |Junio de 2020       |  Sí    |
|2020-07-31     |Julio de 2020        |   Sí   |
|2020-08-31     |Agosto de 2020     |   Sí   |
|2020-09-30     |Septiembre de 2020  |         |
|2020-10-31     |Octubre de 2020    |         |
|2020-11-30     |Noviembre de 2020   |         |
|2020-12-31     |Diciembre de 2020   |         |  

#### Configuración de contabilidad

|Campo|Valor|
|---------|---------|
|Permitir registro desde:  |  2020-09-10      |
|Permitir registro hasta:    |  2020-09-30      |
|Registrar tiempo:       |         |
|Formato dirección local:|   C.P.      |  

#### Configuración de usuarios

|Id. de usuario  |Permitir registro desde  | Permitir registro hasta  |
|---------|---------|--------|
|USERNAME |  2020-09-10      |2020-09-30      |

Al asignar un intervalo de fechas de en el que permite registrar en las páginas **Periodo de inventario** o la **configuración de contabilidad**, será posible evitar el conflicto que provoca el mensaje de error. Por ejemplo, el intervalo más amplio le permite publicar la entrada del valor de ajuste con una fecha de publicación del 10 de septiembre.
  
## Consulte también  

[Detalles de diseño: fecha de registro en el movimiento de valor de ajuste](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
