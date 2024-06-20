---
title: Plan de cuentas de sostenibilidad y contabilidad
description: 'Aprenda a administrar el plan de cuentas de sostenibilidad (CoSA), las categorías y subcategorías, y los detalles sobre las entradas de libro mayor de sostenibilidad.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Plan de cuentas y libro mayor de sostenibilidad

## Plan de cuentas de sostenibilidad

El plan de cuentas de sostenibilidad (CoSA) constituye la lista estructurada fundamental que se utiliza para registrar todos los datos sobre emisiones. Funciona como un marco que categoriza y organiza las cuentas de sostenibilidad en función de sus atributos, como el ámbito u otras agrupaciones. Por lo general, a cada cuenta se le asigna un código o número único para facilitar la referencia y el seguimiento. Tiene la misma estructura que un plan de cuentas tradicional, pero está personalizado específicamente para supervisar datos y métricas relacionados con la sostenibilidad en una organización.

Los usuarios pueden agregar categorías de cuentas de sostenibilidad y subcategorías de cuentas de sostenibilidad para definir cómo se comporta el sistema. De esta manera, pueden seleccionar emisiones dedicadas para rastrear, factores de emisión, fórmulas y configuraciones similares.

> [!NOTE]
> Según las normas sobre gases de efecto invernadero (GEI), existen tres ámbitos de emisión:
>
> - **Emisiones de ámbito 1**: incluyen las emisiones que provienen de la combustión de equipos estacionarios y móviles, de por emisiones fugitivas involuntarias.
> - **Emisiones de ámbito 2**: incluyen emisiones indirectas de la generación de energía que se compra a proveedores de servicios.
> - **Emisiones de ámbito 3**: incluyen un amplio espectro de emisiones, desde bienes y servicios adquiridos y bienes de capital, actividades relacionadas con combustibles y energía, transporte ascendente y descendente, residuos generados, viajes de negocios y desplazamientos de empleados, etc.

Desde CoSA, puede hacer cosas como:

- Ver informes que muestran movimientos de sostenibilidad y saldos.
- Abra la Ficha de cuenta de sostenibilidad para agregar o cambiar la configuración.
- Ver la categoría y subcategoría de la cuenta. 
- Ver saldos separados para cada emisión de una sola cuenta.
- Agregar una o varias dimensiones a cada una de las cuentas y establecer filtros de dimensiones.

Puede agregar, cambiar o eliminar cuentas de sostenibilidad. Sin embargo, para evitar discrepancias, no puede eliminar una cuenta de sostenibilidad si hay uno o más asientos contables asociados con ella.

### Agregar o cambiar cuentas

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas de sostenibilidad** y luego seleccione el vínculo relacionado.
2. En la página **Plan de cuentas de sostenibilidad**, puede abrir cada cuenta de sostenibilidad y, a continuación, agregar o cambiar la configuración. Pase el cursor sobre un campo para leer una breve descripción.

Para cuentas del tipo **Total** , deberá establecer el campo **Sumatorio**.

Para las cuentas del tipo **Total fin**, la función Aplicar sangría establece automáticamente el campo **Sumatorio**. Después de configurar todas las cuentas, seleccione la acción **Aplicar sangría a plan de cuentas de sostenibilidad** para ejecutar la función Aplicar sangría y establecer el campo **Sumatorio**.

> [!IMPORTANT]
> La función Aplicar sangría sobrescribe el valor de todos los campos de las cuentas **Total fin** . Por lo tanto, si ha introducido definiciones en el campo **Sumatorio** para las cuentas de **Total fin** antes de ejecutar la función Aplicar sangría, deberá volver a introducirlas.

### Eliminar cuentas

Puede eliminar una cuenta de sostenibilidad. Sin embargo, primero debe asegurarse de que no haya ningún movimiento asociado con él. Business Central le impide eliminar una cuenta de sostenibilidad si hay uno o más asientos contables asociados con ella.

## Categorías de cuenta

Los usuarios deben agregar una categoría de cuentas de sostenibilidad a cada cuenta de sostenibilidad para definir cómo se comporta el sistema. Pueden seleccionar ámbitos de emisiones, emisiones dedicadas para rastrear, fórmulas y configuraciones similares.

Para revisar categorías de cuentas de sostenibilidad, siga los pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Categorías de cuentas de sostenibilidad** y luego seleccione el vínculo relacionado.
2. En la página **Categorías de cuentas de sostenibilidad**, puede editar la lista existente o crear una nueva categoría. Para crear una nueva categoría, seleccione la acción **Nuevo**.
3. Establezca los campos **Código** y **Descripción**.
4. En el campo **Ámbito de la emisión**, seleccione una de las opciones de ámbito.
5. Seleccione las emisiones de gases que desea rastrear. Actualmente, están disponibles las siguientes opciones: **CO2**, **CH4** y **N2O**. Puede seleccionar cualquier combinación que desee rastrear, pero debe seleccionar como mínimo una emisión.
6. En el campo **Fundación de cálculo**, puede seleccionar la base de cálculo (fórmula) que se utilizará para los cálculos de emisiones si no conoce la cantidad exacta de emisiones. Puede seleccionar una de las siguientes opciones: **Combustible/Electricidad**, **Distancia**, **Instalación** o **Personalizada**.

    > [!NOTE]
    > Si el conjunto de fórmulas disponibles en el campo **Base de cálculo** no es suficiente, puede ampliar el campo y agregar más cálculos al sistema para utilizarlos en los diarios de sostenibilidad.

7. Si seleccionó **Personalizada** en el campo **Base de cálculo**, puede configurar una descripción personalizada en el campo **Valor personalizado**.

Si configura el campo **Base de cálculo**, la siguiente tabla explica cómo el sistema calcula las emisiones según la opción que ha seleccionado. (En esta tabla, *FE* representa el valor **Factor de emisión** que puede configurar en la página **Subcategoría de cuenta de sostenibilidad**.)

| Tipo de emisiones | Base de cálculo | Fórmula | Comentario |
|---------------|------------------------|---------|---------|
| **Ámbito 1** | | | |
| Combustión estacionaria | Combustible/Electricidad | *Emisión* = *Combustible* &times; *FE* | *Combustible* = Cantidad de combustible que se gasta en calderas, calentadores, oxidadores térmicos, etc. |
| Combustión móvil | Combustible/Electricidad | *Emisión* = *Combustible* &times; *FE* | *Combustible* = Cantidad de combustible que se gasta para vehículos de carretera o no de carretera, ferrocarril, etc. |
| | | *Emisión* = *Distancia* &times; *FE* | *Distancia* = Kilometraje de vehículos de carretera o no, ferrocarril, etc. |
| Emisiones fugitivas | Instalación | *Emisión* = *Multiplicador de instalación* &times; *Cantidad personalizada* &divide; 100 &times; *Factor de tiempo* | *Cantidad personalizada* = Pérdidas de montaje, índice anual de fugas, etc. |
| **Ámbito 2** | | | |
| Proveedores de servicios públicos | Combustible/Electricidad | *Emisión* = *Electricidad* &times; *FE* | *Combustible/Electricidad* = Cantidad de electricidad, cantidad de vapor, unidad de calefacción, etc. |
| | Personalizada | *Emisión* = *Cantidad personalizada* &times; *FE* | *Cantidad personalizada* = Unidad térmica, tonelada-hora, etc. |
| **Ámbito 3** | | | |
| Bienes y servicios adquiridos y bienes de capital | Personalizada | *Emisión* = *Cantidad personalizada* &times; *FE* | *Cantidad personalizada* = Coste (libro mayor), etc. |
| Transporte y distribución ascendentes | Distancia | *Emisión* = *Distancia* &times; *FE* | |
| | Distancia | *Emisión* = *Distancia* &times; *Multiplicador* &times; *FE* | *Multiplicador* = Toneladas de carga |
| Transporte y distribución descendentes | Distancia | *Emisión* = *Distancia* &times; *FE* | |
| | Distancia | *Emisión* = *Distancia* &times; *Multiplicador* &times; *FE* | *Multiplicador* = Toneladas de carga |
| Residuos generados en operaciones y tratamiento de fin de vida de productos vendidos | Personalizada | *Emisión* = *Cantidad personalizada* &times; *FE* | *Cantidad personalizada* = Residuos |
| Viajes de negocios y desplazamientos de empleados | Distancia | *Emisión* = *Distancia* &times; *FE* | *Distancia* = Kilometraje del coche de empresa utilizado, coche de alquiler, tren, vuelo, etc. |
| | Personalizada | *Emisión* = *Cantidad personalizada* &times; *FE* | *Cantidad personalizada* = Estancias en hotel |
| | Combustible/Electricidad | *Emisión* = *Combustible* &times; *FE* | *Combustible* = Cantidad de combustible gastado en el coche de empresa, de alquiler, etc. |

## Subcategorías de cuenta

Los usuarios deben agregar una subcategoría de cuentas de sostenibilidad a cada cuenta de sostenibilidad. Esta subcategoría define los factores de emisión que se utilizan en las fórmulas, según la elección de seguimiento de emisiones en la categoría de cuenta de sostenibilidad.

Para revisar las subcategorías de cuentas de sostenibilidad, siga los pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Subcategorías de cuentas de sostenibilidad** y luego seleccione el vínculo relacionado. 
2. En la página **Subcategorías de cuentas de sostenibilidad**, puede editar la lista existente o crear una nueva categoría. Para crear una nueva categoría, seleccione la acción **Nuevo**.
3. Establezca los campos **Código** y **Descripción**.
4. Según las emisiones de gases que desea rastrear en la categoría de cuenta de sostenibilidad y con la que conecte esta subcategoría, también puede establecer uno o varios factores de emisión: 

    - **Factor de emisión de CO2**: el factor de emisión de emisiones de dióxido de carbono (CO<sub>2</sub>).
    - **Factor de emisión de CH4**: el factor de emisión para emisiones de metano (CH<sub>4</sub>).
    - **Factor de emisión de N2O**: el factor de emisión de emisiones de óxido nitroso (N<sub>2</sub>O).

5. Si la subcategoría está relacionada con energías renovables, seleccione el campo **Energía renovable**.

> [!NOTE]
> Los campos **Importar datos** e **Importar de** están destinados a una posible integración con sistemas externos que se utilizan para recopilar factores de emisión. Sin embargo, en **el primer lanzamiento de 2024**, estos campos no se pueden utilizar como característica de manera predeterminada.

## Movimientos de sostenibilidad

Los movimientos de sostenibilidad almacenan el historial de todas las transacciones de sostenibilidad publicadas y organizan todos los datos de emisiones de acuerdo con CoSA. Cuando un usuario publica el diario de sostenibilidad, todos los datos importantes se registrarán allí. Todos los informes activos se generan en función de los movimientos de sostenibilidad.

Para abrir este libro mayor para una cuenta específica, utilice la acción **Movimientos contables** en la página **Plan de cuentas de sostenibilidad**. Para abrir todos los movimientos de proveedores, seleccione el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de sostenibilidad** y luego seleccione el vínculo relacionado. Pase el cursor sobre un campo para leer una breve descripción.

> [!IMPORTANT]
> Después de contabilizar sus datos en el libro mayor de sostenibilidad, no podrá borrarlos. Si cometió un error, puede contabilizar una transacción inversa que tenga los mismos detalles pero que utilice el signo negativo para el importe.

## Consulte también

[Finanzas](finance.md)  
[Información general de la administración de la sostenibilidad](finance-manage-sustainability.md)  
[Configuración de sostenibilidad](finance-sustainability-setup.md)  
[Cómo registrar emisiones](finance-sustainability-journal.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
