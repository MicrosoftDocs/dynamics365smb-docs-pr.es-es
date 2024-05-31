---
title: Consolidar los datos de varias empresas
description: Este artículo explica cómo puede consolidar los movimientos de contabilidad de dos o más empresas independientes (filiales) en una sola empresa consolidada.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="consolidating-financial-data-from-multiple-companies"></a>Consolidar los datos financieros de varias empresas

Algunas organizaciones utilizan [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples empresas o entidades legales. Otros usan [!INCLUDE [prod_short](includes/prod_short.md)] en subsidiarias que deben reportar a organizaciones matrices. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece a los contables herramientas que les ayudan a transferir asientos del libro mayor de dos o más empresas (subsidiarias) a una empresa consolidada.  

Cada empresa implicada en una consolidación se denomina empresa. La empresa en la que combina los datos se denomina empresa consolidada.  

Puede transferir datos financieros de las filiales a la empresa consolidada, incluso si las filiales usan [!INCLUDE [prod_short](includes/prod_short.md)] en diferentes entornos. Para obtener más información sobre cómo conectarse a otros entornos, vaya a [Configurar la consolidación de empresas](finance-consolidated-company-reporting-setup.md#busunit).

Si los resultados financieros de una empresa se encuentran en una divisa diferente de los de la empresa consolidada, debe configurar tipos de cambio para la consolidación. Para obtener más información sobre los tipos de cambio para consolidaciones, vaya a [Configurar consolidación de empresa](finance-consolidated-company-reporting-setup.md#exchrates).  

Puede realizar consolidaciones:  

* A través de las empresas que tienen varios planes de cuentas.  
* Empresas que utilizan distintos ejercicios fiscales y diferentes divisas.  
* Tanto por el importe total como por un porcentaje de la información financiera de una empresa.
* Utilizando distintos tipos de cambio de divisa en distintas libros mayores de contabilidad.
* Empresas en otros programas de contabilidad y gestión empresarial.
* Empresas en entornos [!INCLUDE [prod_short](includes/prod_short.md)] distintos.

Configure la empresa consolidada de la misma forma que se configuran las demás empresas. El plan de cuentas es independiente del plan de cuentas de las unidades de negocio. El plan de cuentas de las unidades de negocio puede diferir entre sí. Para obtener más información sobre cómo configurar una consolidación, vaya a [Configurar consolidación de compañía](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> La consolidación de los datos financieros puede ser especialmente relevante para procesos entre empresas vinculadas. Para obtener más información sobre las funciones intercompañía, vaya a [Administración de transacciones intercompañía](intercompany-manage.md).

## <a name="consolidate-data"></a>Consolidar datos

Antes de consolidar, es una buena idea probar sus datos antes de transferirlos a la empresa consolidada. [!INCLUDE[prod_short](includes/prod_short.md)] busca las diferencias entre la información encontrada de las unidades de negocio y la empresa consolidada. Por ejemplo, si los números de cuenta o códigos de dimensión son diferentes. Corrija los errores antes de ejecutar el informe. Puede probar la base de datos o, si va a importar datos desde un archivo XML, el archivo.

### <a name="test-the-data-before-you-consolidate"></a>Para probar los datos antes de la consolidación

1. Abra la empresa consolidada.  
2. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de negocio** y luego elija el enlace relacionado.  
3. Pruebe el archivo y la base de datos, de la siguiente manera:  

    * Para probar un archivo, elija la acción **Probar archivo**, escriba el nombre del archivo y después seleccione **Imprimir**.  
    * Para probar la base de datos, elija **Probar base de datos**.  

### <a name="run-the-consolidation"></a>Ejecutar la consolidación

Después de haber probado los datos, puede transferirlos a la empresa consolidada. Una guía de configuración asistida le ayudará durante el proceso.

> [!NOTE]
> Cuando ejecuta la consolidación puede elegir las empresas que desea incluir. Si su empresa consolidada no tiene acceso a una o más filiales, la guía le permitirá otorgar acceso a ellas.

1. Inicie sesión en la empresa consolidada.  
2. En la página **Unidades de negocio**, seleccione la acción **Consolidar**.  
3. Rellene los campos requeridos.  

## <a name="use-the-consolidated-trial-balance-report"></a>Utilizar el informe Balance de prueba consolidado

El informe **Balance de prueba consolidado** puede darle un resumen del estado financiero general del negocio. El informe combina movimientos de contabilidad general de cada una de sus empresas en una empresa nueva creada por usted para los datos consolidados. La empresa consolidada es sólo un contenedor para los datos consolidados, y no tiene ningún dato vivo de sus empresas. Las empresas que incluya en la empresa que se convierten en **Unidades de negocio** en el informe. Si tiene cuatro unidades de empresa o menos, también puede utilizar el informe **Balance de prueba consolidado (4)**.  

El informe muestra una línea para cada cuenta y sigue la estructura del plan de cuentas. Una cuenta no aparece si todos los importes de la línea son 0. El informe muestra la siguiente información de cada cuenta:

* Número de la cuenta y nombre de la cuenta.
* Los totales de la empresa consolidada y de cada unidad de negocio. Los totales se pueden expresar bien como el saldo del periodo, bien como el saldo a la fecha.
* Las eliminaciones realizadas en la empresa consolidada. Las eliminaciones siempre se muestran para el periodo correspondiente al ejercicio de la empresa consolidada.
* El total de la empresa consolidada después de las eliminaciones se muestra bien como un cambio neto o bien como el saldo a la fecha.

## <a name="eliminate-repeated-transactions"></a>Eliminar transacciones repetidas

Una vez que haya consolidado las empresas, primero debe encontrar y eliminar las transacciones registradas más de una vez en las empresas. El procesamiento de las eliminaciones de consolidación es un procedimiento manual.  

Para eliminar transacciones repetidas:

1. Busque transacciones que tal vez deban ajustarse e introduzca líneas del diario general para eliminarlas.
2. Ejecute el informe **Eliminaciones consolidación** para que le ayude a valorar el efecto de las líneas del diario antes del registro.
3. Registrar transacciones de ajuste.

El informe **Eliminaciones de consolidación de contabilidad** muestra un balance de prueba en borrador, donde puede simular las consecuencias de eliminar asientos. El informe compara los movimientos de la empresa consolidada con las eliminaciones introducidas en el diario general.

Para poder incluir una empresa en el informe, debe configurar la unidad en la página **Unidades de negocio**. Asegúrese de activar la opción **Consolidar**.

Se crea una línea para cada cuenta, según la estructura del plan de cuentas. Una cuenta no aparece si todos los importes de la línea son 0. El informe muestra la siguiente información de cada cuenta:

* Número de cuenta.
* Nombre de cuenta.
* Si ha seleccionado uno o más códigos de unidad de negocio en el campo **Código de unidad de negocio** de la página de solicitud, el total de la empresa consolidada excluye las unidades de negocio y las eliminaciones seleccionadas. Si no ha rellenado el campo **Código de unidad de negocio**, el total de la empresa consolidada excluye las eliminaciones.
* Si ha seleccionado un código de unidad de negocio en el campo **Código de unidad de negocio** de la página de solicitud, un total amuestra los movimientos importados desde la unidad de negocio. Si no ha rellenado el campo **Código de unidad de negocio**, se muestra un total de las eliminaciones registradas en la empresa consolidada.
* El total de la empresa consolidada, con todas las empresas y las eliminaciones registradas.
* Las eliminaciones a realizar en la empresa consolidada. Es decir, las entradas del diario general que se selecciona en la página de solicitud.
* El texto de registro, copiado del diario general.
* El total de la empresa consolidada, después de las eliminaciones, si se registran.

## <a name="export-and-import-consolidated-data-between-databases"></a>Exportar e importar datos consolidados entre bases de datos

Si los datos de una unidad de negocio están en otra base de datos, puede realizar una transferencia manual basada en archivos o automatizar el proceso mediante una API. Para obtener más información sobre la API, vaya a [Utilice nuestra API para compartir datos automáticamente entre entornos](#use-our-api-to-automatically-share-data-across-environments).

Esta sección describe el proceso manual basado en archivos.

Exporta los datos a un archivo antes de incluirlos en la consolidación. Exporte cada empresa por separado utilizando el trabajo por lotes **Consolidación de Exportaciones**.  

> [!TIP]
> Utilice el mismo proceso para exportar datos consolidados que debe enviar a Dynamics 365 Finance. Por ejemplo, si la unidad de negocio es una subsidiaria y la empresa matriz utiliza Dynamics 365 Finance.

Después de ejecutar el trabajo por lotes, se procesarán todos los movimientos de todas las cuentas. Para cada combinación de dimensiones seleccionadas y fecha, se obtiene el total de los campos **Importe** de los movimientos, y se exporta. Se procesa la siguiente combinación de las dimensiones seleccionadas y la fecha con el mismo número de cuenta. Luego se procesan las combinaciones en el siguiente número de cuenta, y así sucesivamente.  

Los movimientos exportados tienen los siguientes campos: **Nº cuenta**, **Fecha registro** e **Importe**. Si también se ha exportado la información sobre dimensiones, se incluirán los códigos y los valores de dimensión.  

1. Para cada línea exportada, si el total de los campos **Importe** corresponde al debe, el número de cuenta que está configurada en el campo **Cta. consol. debe** de la unidad de negocio se exporta a la línea. Si el total corresponde al haber, el número correspondiente en el campo **Cta. consol. haber** se exporta a la línea.  
2. La fecha que se usa en cada línea exportada es la fecha final del periodo o, si la transferencia se realiza cada día, la fecha exacta del cálculo.  
3. El valor de dimensión exportado para el movimiento será el valor de dimensión de la empresa consolidada que se especifica en el campo **Código de consolidación** del valor de dimensión. Si no se ha introducido un valor de dimensión de empresa consolidada en el campo **Código de consolidación** para el valor de dimensión, se exportará a la línea el valor de dimensión en sí.  
4. Además, los archivos XML contienen los tipos de cambio de divisa del periodo consolidado. Estos tipos se incluyen en una sección aparte al principio del archivo.  

## <a name="use-our-api-to-automatically-share-data-across-environments"></a>Utilice nuestra API para compartir datos automáticamente entre entornos

[!INCLUDE [prod_short](includes/prod_short.md)] proporciona una API que le permite automatizar el proceso de compartir datos financieros de las unidades de negocio a la empresa consolidada. La API es de uso gratuito y fácil de configurar. Incluso te permite compartir datos entre entornos de [!INCLUDE [prod_short](includes/prod_short.md)]. Por ejemplo, es posible que necesite compartir entre entornos cuando las unidades de negocio no se encuentren en las mismas zonas geográficas de Azure. Para obtener más información sobre el uso de la API para automatizar el proceso de consolidación, vaya a [Configurar la consolidación de empresas](finance-consolidated-company-reporting-setup.md#busunit).

## <a name="see-also"></a>Consulte también

[Configurar la consolidación de empresa](finance-consolidated-company-reporting-setup.md)  
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportar los datos de negocio a Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
