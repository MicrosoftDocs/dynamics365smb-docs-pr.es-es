---
title: Configurar la consolidación de empresas
description: Descubra cómo puede configurar cómo se informan los datos de diferentes empresas de Business Central en una empresa de consolidación.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 453cebcddb1fdfd2f3127fd08548deccc8fe1876
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512209"
---
# <a name="set-up-company-consolidation"></a>Configuración de la consolidación de empresas

Para poder consolidar los movimientos de contabilidad de dos o más empresas separadas (subsidiarias) en una empresa consolidada, debe preparar los planes de cuentas y la empresa de consolidación.  

En función de la complejidad de sus negocios, hay dos formas de configurar la consolidación:

* Si no necesita configuraciones avanzadas, como incluir una empresa de la que posea sólo una parte, puede utilizar la guía de configuración asistida **Consolidación de la empresa** para crear rápidamente una consolidación. La guía le asiste con los pasos básicos.
* Si necesita alguna configuraciones más avanzada, puede configurar las empresas consolidadas y las unidades de negocio manualmente.
  * En cada empresa, especifique qué cuentas de contabilidad se deben incluir en la consolidación y especifique el método de traducción de consolidación para cada cuenta.
  * En la empresa consolidada, configure una tarjeta de empresa para cada empresa que se desee incluir en la consolidación. La tarjeta de empresa incluye información como las fechas del ejercicio de la empresa y el porcentaje de cada cuenta que debe incluirse en la consolidación.

## <a name="simple-consolidation-setup"></a>Configuración de consolidación sencilla

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Si su consolidación es directa, por ejemplo porque es propietario de la totalidad de las empresas a consolidar, la guía de configuración asistida **Consolidación de la empresa** le ayudará con los pasos siguientes:

* Indique si crear una nueva empresa consolidada, o si consolidar los datos en una empresa que ya haya creado para la consolidación. La empresa no debe contener transacciones.
* Previsualizar los resultados. [!INCLUDE[prod_short](includes/prod_short.md)] comprueba que los datos y las transacciones maestros se pueden transferir correctamente a la empresa consolidada.

Para usar la guía de configuración asistida, realice los pasos siguientes:

1. En el centro de rol **Contador** , seleccione la acción **Configuración asistida** .
2. Seleccione **Configurar informe de consolidación** y después complete cada paso en la guía de configuración asistida.

## <a name="advanced-consolidation-setup"></a>Configuración de consolidación avanzada

Si necesita más configuraciones avanzadas para su consolidación, puede configurar la consolidación manualmente. Por ejemplo, si tiene empresas de las que es propietario sólo parcialmente, o tiene las empresas que no desea incluir en la consolidación.  

### <a name="set-up-the-consolidated-company"></a>Configurar la empresa consolidada

Primero, debe configurar la empresa consolidada. Configure la empresa consolidada de la misma forma que se configuran las demás empresas. Para obtener más información, vea [Preparación para hacer negocios](ui-get-ready-business.md).  

La siguiente lista ilustra los aspectos clave de la empresa consolidada.

1. Configurar el plan de cuentas

    Para obtener más información, consulte [Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md).  

    Los planes de cuentas pueden ser idénticos en una empresa y en la empresa consolidada, o bien la empresa consolidada puede tener un plan de cuentas diferente. Si el plan de cuentas de una unidad de negocio es diferente al de la empresa consolidada, debe especificar la asignación entre cuentas de las cuentas de la unidad de negocio. Para obtener más información, consulte la sección [Preparar cuentas de contabilidad para la consolidación](#glacc).

2. Agregar unidades de negocio

    Para consolidar los datos financieros de varias empresas en una sola empresa consolidada, debe introducir la información sobre las subsidiarias como empresas a incluir y el grado hasta el que se incluirán sus cifras.

    Para obtener más información, consulte la sección [Agregar unidades de negocio](#busunit).
3. Puede especificar tipos de cambio si va a consolidar los resultados financieros de empresas si dichos resultados están en una divisa extranjera.

    Los tres tipos de cambio que se usan son **Tipo de cambio medio (manual)**, **Tipo de cambio al cierre** y **Último cambio al cierre**. Para obtener más información, consulte la sección [Especificar tipos de cambio para consolidaciones](#exchrates).
4. Puede consolidar información sobre dimensiones y cuentas de contabilidad.

    Para obtener más información, consulte la sección [Incluir o excluir dimensiones](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Agregar empresas

[!INCLUDE[prod_short](includes/prod_short.md)] le permite configurar una lista de empresas a consolidar, comprobar los datos contables antes de proceder a la consolidación, importar archivos y generar informes de consolidación.  

1. Inicie sesión en la empresa consolidada.
2. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de negocio** y luego elija el enlace relacionado.  
3. Elija **Nuevo** y, a continuación, rellene los campos requeridos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Cuando rellene los campos **Fecha inicial** y **Fecha final**, asegúrese de cumplir con las reglas GAAP relacionadas con los periodos fiscales de la unidad de negocio y la empresa principal.
4. Repita el paso 3 para cada empresa adicional

Si su empresa utiliza una divisa extranjera debe especificar el tipo de cambio que debe utilizarse en la consolidación. También debe introducir la información de consolidación en las cuentas de la empresa. Estos procesos se describen en las siguientes secciones.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Preparar los libros de contabilidad para la consolidación

El plan de cuentas de una empresa a consolidar debe especificar las cuentas para consolidación. Por cada cuenta de contabilidad de cada empresa, debe especificar la cuenta de la empresa consolidada a la que se transferirá el saldo tras la consolidación. Esta asignación permitirá que se puedan consolidar empresas con planes de cuentas diferentes.

Si el plan de cuentas de la unidad de negocio difiere de la empresa consolidada, debe preparar los libros contables para la consolidación. Puede especificar las cuentas para apuntar debe y haber y el método a utilizar para traducir las divisas en la empresa consolidada. Por ejemplo, esto es útil en caso de ejecutar con frecuencia el informe.

1. En cada unidad de negocio [!INCLUDE [prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. Abra la ficha de la cuenta, y rellene los campos de la ficha desplegable **Consolidación**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Especificar los tipos de cambio para consolidaciones

Si una unidad de negocio utiliza una divisa diferente de la empresa consolidada, debe especificar los métodos del tipo de cambio para cada cuenta antes de que se consolide. Para cada cuenta, el contenido del campo **Método de traducción Consol.** determina el tipo de cambio. En la empresa consolidada, en cada ficha de unidad de negocio, en el campo **Tabla de tipo de cambio de divisa** debe especificar si la consolidación usará tipos de cambio de la empresa o de la empresa consolidada. Si utiliza tipos de cambio de la empresa consolidada, puede cambiar los tipos de cambios para una empresa. Para las unidades de negocio, el campo **Tabla de tipo de cambio de divisas** de la ficha de la unidad de negocio contiene **Local**, puede cambiar el tipo de cambio para la ficha de la unidad de negocio. Los tipos de cambio se copian desde la tabla **Tipo cambio divisa**, pero puede cambiarlos antes de la consolidación.

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

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de negocio** y luego elija el enlace relacionado.  
2. En la página **Lista de unidades de negocio**, seleccione la unidad de negocio y, después, seleccione la acción **Tipo de cambio medio (manual)**.  
3. En la página **Modificar tipo de cambio**, el contenido del campo **Tipo de cambio relacionado** se ha copiado de la tabla **Tipo de cambio de divisa**, pero se puede modificar. Cierre la página.  
4. Seleccione la acción **Tipo de cambio al cierre**.  
5. En el campo **Cantidad del tipo de cambio relacionado**, introduzca el tipo de cambio.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Incluir o excluir dimensiones

Puede consolidar información sobre dimensiones y cuentas de contabilidad.

* En las dimensiones relevantes, especifique el campo **Código de consolidación** o déjelo en blanco
  * Para excluir una dimensión en la consolidación, deje el campo **Código de consolidación** en la dimensión, y no elija dimensiones en los campos **Copiar dimensiones** de cualquier función o informe de consolidación.
  * Para incluir información de dimensión en la consolidación, deje el campo **Código de consolidación** en blanco. Sin embargo, la consolidación sólo funcionará si los valores de dimensión de la empresa son iguales que los de la empresa consolidada.
  * Para consolidar el código de valor de dimensión de la empresa con un código de valor de dimensión distinto en la empresa consolidada, rellene el campo **Código de consolidación** en las dimensiones relevantes.  
* Agregue las dimensiones relevantes a las cuentas de contabilidad relevantes

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Excluir una empresa de la consolidación

Si no desea incluir una unidad de negocio en la consolidación, puede excluirla. Para hacerlo, vaya a la ficha de unidad de negocio y borre la casilla de verificación **Consolidar**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Incluir una empresa poseída parcialmente en la consolidación

Si posee únicamente parte de una empresa, puede incluir un porcentaje de cada transacción que le corresponde al porcentaje de la empresa que le pertenece. Por ejemplo, si le pertenece el 70% de la empresa, la consolidación incluirá $70 de una factura de $100. Para especificar el porcentaje de la empresa que le pertenece, vaya a la ficha de la unidad de negocio e introduzca el porcentaje en el campo **Consolidación%**.  

## <a name="see-also"></a>Consulte también

[Consolidar los datos financieros de varias empresas](finance-consolidated-company-reporting.md)  
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportar los datos de negocio a Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]