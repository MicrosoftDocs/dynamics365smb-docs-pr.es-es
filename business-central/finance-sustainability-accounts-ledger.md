---
title: Plan de cuentas y libro mayor de sostenibilidad
description: 'Aprenda a administrar el plan de cuentas, categorías y subcategorías de sostenibilidad y detalles sobre movimientos de sostenibilidad.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="chart-of-sustainability-accounts-and-ledger"></a>Plan de cuentas y libro mayor de sostenibilidad

## <a name="chart-of-sustainability-accounts"></a>Plan de cuentas de sostenibilidad

El **Plan de cuentas de sostenibilidad** (CoSA) forma la lista estructurada fundamental que se utiliza para registrar todos los datos de emisiones. Funciona como un marco que categoriza y organiza las cuentas de sostenibilidad en función de sus atributos, como el ámbito u otras agrupaciones. Por lo general, a cada cuenta se le asigna un código o número único para una fácil referencia y seguimiento, siguiendo la misma estructura que un **Plan de cuentas** tradicional, pero personalizado específicamente para supervisar datos relacionados con la sostenibilidad y métricas dentro de una organización. 
 
Los usuarios pueden agregar **Categorías de cuenta** y **Subcategorías** para definir cómo se comporta el sistema, seleccionando emisiones dedicadas para el seguimiento y factores de emisión., fórmulas y configuraciones similares.  

>[!NOTE]
>Para familiarizarse con los ámbitos, con base en los estándares de GEI (Gases de efecto invernadero), existen tres ámbitos de emisiones:  
>- **Emisiones de ámbito 1**: incluyen las emisiones que provienen de la combustión de equipos estacionarios y móviles, de por emisiones fugitivas involuntarias. 
>- **Emisiones de ámbito 2**: incluyen emisiones indirectas de la generación de energía que se compra a proveedores de servicios. 
>- **Emisiones de ámbito 3**: incluyen un amplio espectro de emisiones, desde bienes y servicios adquiridos y bienes de capital, actividades relacionadas con combustibles y energía, transporte ascendente y descendente, residuos generados, viajes de negocios y desplazamientos de empleados, etc. 

Desde el **Plan de cuentas de sostenibilidad** (CoSA), puede hacer cosas como:  

-   Ver informes que muestran movimientos de sostenibilidad y saldos. 
-   Abra la **Ficha de cuenta de sostenibilidad** para agregar o cambiar la configuración.  
-   Vea la categoría y subcategoría de esa cuenta.   
-   Ver saldos separados para cada una de las emisiones de una sola cuenta. 
-   Agregue una o varias **Dimensiones** a cada una de las cuentas y establezca el filtro de dimensiones. 
    
Puede agregar, cambiar o eliminar **Cuentas de sostenibilidad**. Sin embargo, para evitar discrepancias, no puede eliminar una **Cuenta de sostenibilidad** si hay uno o más asientos contables asociados con esta cuenta.  

### <a name="add-or-change-accounts"></a>Agregar o cambiar cuentas

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas de sostenibilidad** y luego seleccione el vínculo relacionado. 
2. En la página **Plan de cuentas de sostenibilidad** (CoSA), puede abrir cada **Cuenta de sostenibilidad** y, a continuación, agregue o cambie la configuración. Pase el cursor sobre un campo para leer una breve descripción. 

Para cuentas del tipo **Total** , deberá completar el campo **Sumatorio**. Para las cuentas **Fin Total**, éste lo rellena automáticamente la función Aplicar sangría. Una vez que haya configurado todas las cuentas, elija la acción **Aplicar sangría a plan de cuentas de sostenibilidad** para aplicarla.  

>[!IMPORTANT]
>Si ha escrito definiciones en los campos **Sumatorio** referentes a las cuentas **Fin-Total** antes de ejecutar la función Indentar, deberá volver a escribirlas, ya que esta función sobrescribe los valores de todos los campos **Fin-Total**.  

### <a name="delete-accounts"></a>Eliminar cuentas

Puede eliminar una **Cuenta de sostenibilidad**. Sin embargo, antes de eliminarla, debe asegurarse de que haya uno o más movimientos asociados con esta cuenta, ya que Business Central le impedirá eliminar una **Cuenta de sostenibilidad** en esta situación.  

## <a name="account-categories"></a>Categorías de cuenta

Los usuarios deben agregar la **Categoría de cuenta de sostenibilidad** a cada una de las **Cuentas de sostenibilidad**, para definir cómo se comporta el sistema, seleccionando ámbitos de emisión, emisiones dedicadas para seguimiento, fórmulas y configuraciones similares.  

Para revisar **Categorías de cuentas de sostenibilidad**, siga los pasos: 

1.  Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Categorías de cuentas de sostenibilidad** y luego seleccione el vínculo relacionado. 
2.  En la página **Categorías de cuentas de sostenibilidad**, puede editar la lista existente o crear una nueva categoría. Para crear una nueva categoría, seleccione la acción **Nuevo**.  
3.  Rellene los campos **Código** y **Descripción**.   
4.  Configure el campo **Ámbito de la emisión**, eligiendo una de las opciones de ámbito.  
5.  Seleccione las emisiones de gases que desea rastrear. Actualmente, puede utilizar una de las opciones: **CO2**, **CH4** o **N2O**. Puede elegir cualquier combinación que desee rastrear, pero debe tener al menos una emisión para realizar el seguimiento.  
6.  En el campo **Base de cálculo**, puede elegir cualquiera de las fórmulas que desee utilizar, en caso de que no conozca la cantidad exacta de emisión. Aquí puede especificar la base de cálculo (fórmula) para el cálculo de las emisiones. Puede elegir una de las siguientes opciones: **Combustible/Electricidad**, **Distancia**, **Instalación** o **Personalizada**. 
7.  Si elige la fórmula **Personalizada**, puede configurar una descripción personalizada en el campo **Valor personalizado**.  

>[!NOTE]
>Si este conjunto de fórmulas ofrecidas en el campo **Base de cálculo** no es suficiente, puede ampliar este campo y agregar más cálculos al sistema para utilizarlos en los **Diarios de sostenibilidad**.  

Si usa la **Base de cálculo** (fórmulas), hay una explicación de cómo el sistema calculará según la opción que haya elegido (**FE** es el **Factor de emisión** que puede configurar en la página **Subcategoría de cuenta de sostenibilidad**): 

|  Tipo de emisiones  |  Base de cálculo  |  Fórmula         | Comentario      |
|------------|--------------|------------------------------|---------------------------------|
| **ÁMBITO 1**  |
| Combustión estacionaria | Combustible/Electricidad | Emisión = Combustible * FE | _es decir, Combustible = Cantidad de combustible gastado en calderas, calentadores, oxidadores térmicos..._ |
| Combustión móvil | Combustible/Electricidad | Emisión = Combustible * FE | _es decir, Combustible = Cantidad de combustible gastado por vehículos de carretera o no de carretera, ferrocarril..._ |
|  |  |  Emisión = Distancia * FE | _es decir, Distancia = Kilometraje de vehículos de carretera o no de carretera, ferrocarril..._ |
| Emisiones fugitivas | Instalación | Emisión = Multiplicador de instalación * Cantidad personalizada / 100 * Factor de tiempo | _es decir, Cantidad personalizada = Pérdidas de ensamblaje, Tasa de fuga anual..._ |
| **ÁMBITO 2**  |
| Proveedores de servicios públicos | Combustible/Electricidad | Emisiones = Electricidad * FE | _es decir, Combustible/Electricidad = Cantidad de electricidad, Cantidad de vapor, Unidad de calefacción..._ |
|  | Personalizada | Emisiones = Importe personalizado * FE | _es decir, Importe personalizado = Unidad térmica, Tonelada-hora..._ |
| **ÁMBITO 3**  |
| Bienes y servicios adquiridos y bienes de capital | Personalizada | Emisiones = Importe personalizado * FE | _es decir, importe personalizado = Coste (libro mayor)..._ |
| Transporte y distribución ascendentes | Distancia | Emisión = Distancia * FE |  |
|  | Distancia | Emisión = Distancia * Multiplicador * FE | _Multiplicador = Toneladas de carga_ |
| Transporte y distribución descendentes | Distancia | Emisión = Distancia * FE |  |
|  | Distancia | Emisión = Distancia * Multiplicador * FE | _Multiplicador = Toneladas de carga_ |
| Residuos generados en operaciones y tratamiento de fin de vida de productos vendidos | Personalizada | Emisiones = Importe personalizado * FE | _es decir, importe personalizado = Residuos_ |
| Viajes de negocios y desplazamientos de empleados | Distancia | Emisión = Distancia * FE | _es decir, Distancia = Kilometraje del coche de empresa usado, coche de alquiler, tren, vuelo..._ |
|  | Personalizada | Emisiones = Importe personalizado * FE | _es decir, Importe personalizado = Estancias en hoteles..._ |
|  | Combustible/Electricidad | Emisión = Combustible * FE | _es decir, Combustible = Cantidad de combustible gastado en el coche de empresa, coche de alquiler..._ |

## <a name="account-subcategories"></a>Subcategorías de cuenta

Los usuarios deben agregar la **Subcategoría de cuenta de sostenibilidad** a cada una de las **Cuentas de sostenibilidad** para definir los factores de emisión que se utilizarán en las fórmulas, pero se basa en la opción de seguimiento de emisiones en la **Categoría de cuenta de sostenibilidad**.  

Para revisar las **Subcategorías de cuentas de sostenibilidad**, siga los pasos:  

1.  Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Subcategorías de cuentas de sostenibilidad** y luego seleccione el vínculo relacionado. 
2.  En la página **Subcategorías de cuentas de sostenibilidad**, puede editar la lista existente o crear una nueva categoría. Para crear una nueva categoría, seleccione la acción **Nuevo**.  
3.  Rellene los campos **Código** y **Descripción**.   
4.  Según las emisiones de gases que desea rastrear en la **Categoría de cuenta de sostenibilidad** y con la que conecte esta subcategoría, también puede rellenar uno o varios factores de emisión: 

   - **Factor de emisión de CO2**: especifica un factor de emisión para emisión de CO2.  
   - **Factor de emisión de CH4**: especifica un factor de emisión para emisión de CH4. 
   - **Factor de emisión de N2O**: especifica un factor de emisión para emisión de N2O.  

5.  Si esta subcategoría está relacionada con energías renovables, seleccione el campo **Energía renovable**.   

>[!NOTE]
>Los campos **Importar datos** e **Importar de** están pensados para una posible integración con sistemas externos que se utilicen para recopilar factores de emisión, pero en el **primer lanzamiento de versiones de 2024** no se pueden usar como una característica de manera predeterminada.  

## <a name="sustainability-ledger-entries"></a>Movimientos de sostenibilidad

**Movimiento de sostenibilidad** almacena el historial de todas las transacciones de sostenibilidad publicadas, organizando todos los datos de emisiones de acuerdo con el **Plan de cuentas de sostenibilidad**. Cuando un usuario publica el **Diario de sostenibilidad**, todos los datos importantes se registrarán allí. Todos los informes activos se generan en función de los **Movimientos de sostenibilidad**.   

El usuario puede abrir este movimiento para una cuenta específica usando la acción **Movimientos** de la página **Plan de cuentas de sostenibilidad** o, para abrir todas las entradas de contabilidad, seleccione la ![bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos de sostenibilidad** y luego seleccione el vínculo relacionado. Pase el cursor sobre un campo para leer una breve descripción.  

>[!IMPORTANT]
>Una vez que publique sus datos en el Movimiento de sostenibilidad, no podrá eliminarlos. En caso de que haya cometido un error, puede registrar la transacción inversa usando los mismos detalles, pero usando el signo negativo para el importe.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)    
[Información general de administración de la sostenibilidad](finance-manage-sustainability.md)
[Configuración de sostenibilidad](finance-sustainability-setup.md)
[Cómo registrar emisiones](finance-sustainability-journal.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
