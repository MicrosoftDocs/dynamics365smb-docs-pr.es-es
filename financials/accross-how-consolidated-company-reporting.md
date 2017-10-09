---
title: Consolidar los datos de varias empresas | Documentos de Microsoft
description: "Obtener una visión general de la salud financiera de sus negocios."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 07/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: aba01deb3ab2294b86003957f293224bc89ea376
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-work-with-the-consolidated-trial-balance-report"></a>Procedimiento: Trabajo con el informe del balance provisional consolidado
Si tiene más de una empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)], el informe del balance provisional del centro de rol contador puede darle un resumen de la salud financiera del total de sus empresas.  

El informe combina movimientos del libro mayor (LM) de sus empresas en una empresa nueva creada por usted para contener los datos consolidados. Esta empresa valor se denomina generalmente "empresa consolidada". La empresa consolidada es sólo un contenedor para los datos consolidados, y no tiene ningún dato vivo de sus empresas. Las empresas que incluya en la empresa que se convierten en **Unidades de negocio** en el informe.

Puede realizar consolidaciones:  

* A través de las empresas que tienen varios planes de cuentas.  
* Empresas que utilizan distintos ejercicios fiscales y diferentes divisas.  
* Tanto por el importe total como por un porcentaje de la información financiera de una empresa
* Utilizando distintos tipos de cambio de divisa en distintas libros mayores de contabilidad 

En función de la complejidad de sus negocios, hay dos formas de configurar el informe:

* Si no necesita configuraciones avanzadas, como incluir una empresa de la que posea sólo una parte, puede utilizar la guía de configuración asistida **Consolidación de la empresa** para crear rápidamente una consolidación. La guía le asiste con los pasos básicos.
* Si necesita alguna configuraciones más avanzada, puede configurar las empresas consolidadas y las unidades de negocio manualmente.

## <a name="to-do-a-simple-consolidation-setup"></a>Para hacer una configuración simple de la consolidación 
Si su consolidación es directa, por ejemplo porque es propietario de la totalidad de las empresas a consolidar, la guía de configuración asistida **Consolidación de la empresa** le ayudará con los pasos siguientes:
  
* Indique si crear una nueva empresa consolidada, o si consolidar los datos en una empresa que ya haya creado para la consolidación. La empresa no debe contener transacciones.
* Previsualizar los resultados. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba que los datos y las transacciones maestros se pueden transferir correctamente a la empresa consolidada.

Para usar la guía de configuración asistida, realice los pasos siguientes:

1. En el centro de rol **Contador** , seleccione la acción **Configuración asistida** .
2. Seleccione **Configurar informe de consolidación** y después complete cada paso en la guía de configuración asistida.

## <a name="to-do-an-advanced-consolidation-setup"></a>Para hacer una configuración avanzada de consolidación
Si necesita más configuraciones avanzadas para su consolidación, puede configurar la consolidación manualmente. Por ejemplo, si tiene empresas de las que es propietario sólo parcialmente, o tiene las empresas que no desea incluir en la consolidación. Puede configurar la empresa consolidada de la misma forma que se configuran las demás empresas. Para obtener más información, vea [Preparación para hacer negocios](ui-get-ready-business.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] Le permite configurar una lista de las empresas que se van a consolidar, comprobar los datos contables antes de proceder a la consolidación, importar archivos y generar informes de consolidación.  

1. Inicie sesión en la empresa consolidada.
2. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Unidades de negocio** y, a continuación, seleccione el vínculo relacionado.  
3. Elija **Nuevo** y, a continuación, rellene los campos requeridos.  

Si su empresa utiliza una divisa extranjera debe especificar el tipo de cambio que debe utilizarse en la consolidación. También debe introducir la información de consolidación en las cuentas de la empresa. Estos procesos se describen en las siguientes secciones.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Para preparar los libros contables para la consolidación 
Si el plan de cuentas de la unidad de negocio difiere de la empresa consolidada, debe preparar los libros contables para la consolidación. Puede especificar las cuentas para apuntar debe y haber y el método a utilizar para traducir las divisas en la empresa consolidada. Por ejemplo, esto es útil en caso de ejecutar con frecuencia el informe.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la ficha de la cuenta, y rellene los campos de la ficha desplegable **Consolidación**.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Para especificar los tipos de cambio para las consolidaciones
Si una unidad de negocio utiliza una divisa diferente de la empresa consolidada, debe especificar los métodos del tipo de cambio para cada cuenta antes de que se consolide. Para cada cuenta, el contenido del campo **Método de traducción Consol.** determina el tipo de cambio. En cada ficha de unidad de negocio, debe especificar en el campo **Tabla de tipo de cambio de divisa** si la consolidación usará tipos de cambio de la unidad de negocio o de la empresa consolidada. Si utiliza tipos de cambio de la empresa consolidada, puede cambiar los tipos de cambios para una empresa. Para las unidades de negocio, el campo **Tabla de tipo de cambio de divisas** de la ficha de la unidad de negocio contiene **Local**, puede cambiar el tipo de cambio para la ficha de la unidad de negocio. Los tipos de cambio se copian desde la tabla **Tipo cambio divisa**, pero puede cambiarlos antes de la consolidación. 

En la tabla siguiente se describen los métodos del tipo de cambio que puede utilizar para las cuentas.

|Tipo cambio | Uso típico |
|---|---|
|Tipo de cambio medio (manual) | Calcule manualmente el tipo de cambio medio para el periodo que se va a consolidar. Calcule aa media aritmética o aproximada y especifique el resultado para cada unidad de negocio. Usado para cuenta de beneficios.| 
|Tipo de cambio al cierre | Usado para cuentas del balance.|
|Último cambio al cierre | El tipo de cambio que era válido en el mercado de divisas en la fecha para la que se está preparando el balance o el estado de resultados. Introduzca este tipo de cambio para cada unidad de negocio. Usado para cuentas del balance.|
|Tipo de cambio histórico | El tipo de cambio que era válido cuando ocurrió la transacción.|
|Tipo de cambio compuesto | Los importes del periodo actual se traducen con el tipo de cambio medio y se agregan al saldo anteriormente registrado en la empresa consolidada. Este método se utiliza por lo general para las cuentas de retención de beneficios porque incluyen importes de distintos periodos y son por tanto un compuesto de importes traducidos con distintos tipos de cambio.|
|Tasa de participación | Esto es similar a **Compuesto**. Las diferencias se registran para separar libros de contabilidad.|   

Para especificar los tipos de cambio para las unidades de negocio, realice los pasos siguientes:

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Unidades de negocio** y, a continuación, seleccione el vínculo relacionado.  
2. En la página **Lista de unidades de negocio**, seleccione la unidad de negocio y, después, seleccione la acción **Tipo de cambio medio (manual)**.   
3. En la página **Modificar tipo de cambio**, el contenido del campo **Tipo de cambio relacionado** se ha copiado de la tabla **Tipo de cambio de divisa**, pero se puede modificar. Cierre la página.  
4. En la pestaña **Navegar**, en el grupo **Cambio. Tasas**, elija **Tasa al cierre**.  
5. En el campo **Cantidad del tipo de cambio relacionado**, introduzca el tipo de cambio. 

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Para excluir una empresa de la consolidación
Si no desea incluir una unidad de negocio en la consolidación, puede excluirla. Para hacerlo, vaya a la ficha de unidad de negocio y borre la casilla de verificación **Consolidar**.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Para incluir una empresa poseída parcialmente en la consolidación
Si posee únicamente parte de una empresa, puede incluir un porcentaje de cada transacción que le corresponde al porcentaje de la empresa que le pertenece. Por ejemplo, si le pertenece el 70% de la empresa, la consolidación incluirá $70 de una factura de $100. Para especificar el porcentaje de la empresa que le pertenece, vaya a la ficha de la unidad de negocio e introduzca el porcentaje en el campo **Consolidación%**.  

### <a name="to-test-the-data-before-you-consolidate"></a>Para probar los datos antes de la consolidación:
Puede probar los datos antes de transferirlos a la empresa consolidada. [!INCLUDE[d365fin](includes/d365fin_md.md)] busca las diferencias entre la información encontrada de las unidades de negocio y la empresa consolidada. Por ejemplo, si los números de cuenta o códigos de dimensión son diferentes. Deberá corregir los errores antes de ejecutar el informe. Puede probar la base de datos o, si va a importar datos desde un archivo XML, puede probar el archivo.   
  
1. Abra la empresa consolidada.  
2. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Unidades de negocio** y, a continuación, seleccione el vínculo relacionado.  
3. Realice una de las siguientes acciones:  
  
    * Para probar un archivo, elija la acción **Probar archivo**, escriba el nombre del archivo y después seleccione **Imprimir**.  
    * Para probar la base de datos, elija **Probar base de datos**.  

## <a name="to-run-the-consolidation"></a>Para ejecutar la consolidación
Después de haber probado los datos, puede transferirlos a la empresa consolidada.  
  
1. Inicie sesión en la empresa consolidada.  
2. En el **Centro de rol contador**, seleccione la acción **Ejecutar consolidación**.  
3. Rellene los campos requeridos.  
4. En el campo **Donde**, elija **Nombre de la empresa** y, después, seleccione la empresa consolidada del campo **es**.  

## <a name="to-export-data-from-dynamics-nav-and-import-it-in-included365finincludesd365finmdmd"></a>Para exportar datos de Dynamics NAV e importarlos a [!INCLUDE[d365fin](includes/d365fin_md.md)]
Si los datos de una unidad de negocio se encuentran en otra base de datos, deberá exportar los datos a un archivo antes de incluirlos en la consolidación. Cada empresa debe exportarse por separado. Para ello, usa el proceso **Exportar consolidación**.  
  
Después de ejecutar el trabajo por lotes, se procesarán todos los movimientos de todas las cuentas. Para cada combinación de dimensiones seleccionadas y fecha, se obtiene el total de los campos **Importe** de los movimientos, y se exporta. Se procesa la siguiente combinación de dimensiones seleccionadas y fecha con el mismo número de cuenta, y después se procesan las combinaciones del siguiente número de cuenta, y así sucesivamente.  

Los movimientos exportados tienen los siguientes campos: **Nº cuenta**, **Fecha registro** e **Importe**. Si también se ha exportado la información sobre dimensiones, se incluirán los códigos y los valores de dimensión.  

1. Para cada línea exportada, si el total de los campos **Importe** corresponde al debe, el número de cuenta que está configurada en el campo **Cta. consol. debe** de la unidad de negocio se exporta a la línea. Si el total corresponde al haber, el número correspondiente en el campo **Cta. consol. haber** se exporta a la línea.  
2. La fecha que se usa en cada línea exportada es la fecha final del periodo o, si la transferencia se realiza cada día, la fecha exacta del cálculo.  
3. El valor de dimensión exportado para el movimiento será el valor de dimensión de la empresa consolidada del campo **Cód. consolidación** del valor de dimensión. Si no se ha introducido un valor de dimensión de empresa consolidada en el campo **Cód. consolidación** del valor de dimensión, se exportará a la línea el valor de dimensión en sí.   
4. Además, los archivos XML contienen los tipos de cambio de divisa del periodo consolidado. Estos tipos se incluyen en una sección aparte al principio del archivo.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Exportar los datos de negocio a Excel](about-export-data.md)

