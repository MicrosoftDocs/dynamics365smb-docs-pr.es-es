---
title: Cerrar periodos contables para un ejercicio
description: Este artículo describe cómo cerrar los periodos contables que componen el ejercicio fiscal para el cierre del ejercicio.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: '100,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
---
# Cerrar periodos contables

Cuando finaliza un ejercicio, debe cerrar los periodos que lo forman.

## Para cerrar periodos contables

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Periodos contables** y luego elija el enlace relacionado.
2. En la página **Periodos contables**, elija la acción **Cerrar ejercicio**.

    Si hay más de un ejercicio abierto, se selecciona automáticamente el más antiguo para cerrarse. Un mensaje identifica el ejercicio que se va a cerrar y las consecuencias del cierre.
3. Para cerrar el ejercicio, elija el botón **Sí**.

El ejercicio se ha cerrado y se seleccionan los campos **Cerrado** y **Fecha bloqueada** de todos los periodos del ejercicio. No se puede volver a abrir el ejercicio ni desactivar la casilla de verificación de los campos **Cerrado** o **Fecha inicial bloqueada**.

> [!NOTE]  
> No puede cerrar un ejercicio antes de haber creado uno nuevo. Conviene advertir que, una vez cerrado un ejercicio, no puede cambiar la fecha de inicio del ejercicio siguiente.

Aunque un ejercicio esté cerrado, todavía podrá registrar en él movimientos de contabilidad. Al hacerlo, los movimientos se marcan como registrados en un ejercicio cerrado y se seleccionará el campo **Asiento post-cierre**.

Después de cerrar un ejercicio, debe regularizar las cuentas de explotación y transferir los resultados del año a una cuenta del balance. Puede repetirlo cada vez que registre el ejercicio cerrado.

## Consulte también

[Cierre de libros](year-close-books.md)  
[Registrar el movimiento de cierre del ejercicio](year-how-post-year-end-close-entry.md)  
[Trabajar con periodos contables y años fiscales](finance-accounting-periods-and-fiscal-years.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]