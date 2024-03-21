---
title: Configurar la consolidación de empresas
description: Descubra cómo puede configurar cómo se informan los datos de diferentes empresas de Business Central en una empresa de consolidación.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="set-up-company-consolidation"></a>Configuración de la consolidación de empresas

Para poder consolidar los movimientos de contabilidad de dos o más empresas (subsidiarias) en una empresa consolidada, debe preparar los planes de cuentas y la empresa de consolidación.  

En función de la complejidad de sus negocios, hay dos formas de configurar la consolidación:

* Si no necesita configuraciones avanzadas, como incluir una empresa de la que posea sólo una parte, puede utilizar la guía de configuración asistida **Consolidación de la empresa** para crear rápidamente una consolidación. La guía le asiste con los pasos básicos.
* Si necesita alguna configuraciones más avanzada, puede configurar las empresas consolidadas y las unidades de negocio manualmente.
  * En cada empresa, especifique qué cuentas de contabilidad se deben incluir en la consolidación y especifique el método de traducción de consolidación para cada cuenta.
  * En la empresa consolidada, configure una ficha de empresa para cada empresa que se desee incluir en la consolidación. La tarjeta de empresa incluye información como las fechas del ejercicio de la empresa y el porcentaje de cada cuenta que debe incluirse en la consolidación.

## <a name="simple-consolidation-setup"></a>Configuración de consolidación sencilla

Si su consolidación es directa, por ejemplo porque es propietario de la totalidad de las empresas a consolidar, la guía **Consolidación de la empresa** le ayudará con los pasos siguientes:

* Cree una nueva empresa consolidada o consolide una empresa que ya haya creado. La empresa no debe contener transacciones.
* Previsualizar los resultados. [!INCLUDE[prod_short](includes/prod_short.md)] comprueba que los datos y las transacciones maestros se pueden transferir correctamente a la empresa consolidada.

Para usar la guía de configuración asistida, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración asistida** y luego elija el enlace relacionado.
2. Seleccione **Procesar consolidaciones** y después complete cada paso en la guía de configuración asistida de consolidación de empresa.

## <a name="advanced-consolidation-setup"></a>Configuración de consolidación avanzada

Si necesita más configuraciones avanzadas para su consolidación, puede configurar la consolidación manualmente. Por ejemplo, si tiene empresas de las que es propietario sólo parcialmente, o tiene las empresas que no desea incluir.  

### <a name="set-up-the-consolidated-company"></a>Configure la empresa consolidada

Primero, debe configurar la empresa consolidada. Configure la empresa consolidada de la misma forma que se configuran las demás empresas. Para obtener más información sobre cómo crear una empresa, vaya a [Preparándose para hacer negocios](ui-get-ready-business.md).  

La siguiente lista ilustra los aspectos clave de la empresa consolidada.

1. Configurar el plan de cuentas.

    Obtenga más información sobre cómo configurar el plan de cuentas, consulte [Configurar o cambiar los planes de cuentas](finance-setup-chart-accounts.md).  

    Los planes de cuentas pueden ser idénticos en una empresa y en la empresa consolidada, o bien la empresa consolidada puede tener un plan de cuentas diferente. Si el plan de cuentas de una unidad de negocio es diferente al de la empresa consolidada, debe asignar las cuentas a las cuentas de la unidad de negocio. Para obtener más información, consulte la sección [Preparar cuentas de contabilidad para la consolidación](#glacc).

2. Agregar unidades de negocio.

    Para consolidar los datos de varias empresas, debe configurar las subsidiarias como unidades de negocio y especificar qué parte de sus saldos desea incluir. Para obtener más información sobre las unidades de negocio, vaya a la sección [Agregar unidades de negocio](#busunit).

3. Especifique los tipos de cambio, si es necesario.

    Especifique tipos de cambio si va a consolidar datos para unidades de negocio que utilizan diferentes monedas. Los tres tipos de cambio que puede usar son **Tipo de cambio medio (manual)**, **Tipo de cambio al cierre** y **Último cambio al cierre**. Para obtener más información sobre los tipos de cambio, vaya a la sección [Especificar tipos de cambio para consolidaciones](#exchrates).

4. Puede consolidar información sobre dimensiones y cuentas de contabilidad.

    Para obtener más información, consulte la sección [Incluir o excluir dimensiones](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Agregar empresas

En la empresa consolidada, configure cada empresa que de la que quiera consolidar sus datos como una unidad de negocio. Antes de ejecutar una consolidación y generar su informe de consolidación, es una buena idea verificar los datos financieros en cada unidad de negocio.

Una gran parte de la configuración de la unidad de negocios es especificar cómo la unidad compartirá sus datos financieros con la empresa consolidada. Hay opciones manuales y automatizadas:

* Para utilizar un proceso manual, para [!INCLUDE [prod_short](includes/prod_short.md)] en línea y local, puede exportar un archivo .xml que contenga los asientos del libro mayor de la unidad. Luego importe el archivo en la empresa consolidada.
* Para automatizar el intercambio de datos, para [!INCLUDE [prod_short](includes/prod_short.md)] en línea puedes usar una API que [!INCLUDE [prod_short](includes/prod_short.md)] proporciona para compartir datos entre entornos. Si sus empresas están en el mismo entorno, puede utilizar la opción **Base de datos**.

> [!NOTE]
> La opción API también le permite compartir asientos del libro mayor de otros entornos [!INCLUDE [prod_short](includes/prod_short.md)]. Para utilizar la opción API, el usuario que configura la consolidación debe tener permiso para acceder a las entradas del L/M. Por ejemplo, los conjuntos de permisos D365 Basic y D365 Read brindan acceso.

1. Inicie sesión en la empresa consolidada.
2. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de negocio** y luego elija el enlace relacionado.  
3. Elija **Nuevo** y, a continuación, rellene los campos necesarios de las fichas desplegables **General** y **Cuentas de L/M**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Cuando rellene los campos **Fecha inicial** y **Fecha final**, asegúrese de cumplir con las reglas GAAP relacionadas con los periodos fiscales de la unidad de negocio y la empresa principal.
4. En la ficha desplegable **Importar de datos** en el campo **Importación de datos predeterminada**, especifique cómo compartirá los asientos del libro mayor con la empresa consolidada:

   * Para compartir datos entre empresas en el mismo entorno, elija **Base de datos**.
   * Para compartir datos entre empresas en diferentes entornos, elija **API** y luego complete el campo **Punto final de API**.
        
        Para obtener la URL del punto de conexión, en la página [!INCLUDE [prod_short](includes/prod_short.md)] de la empresa de la unidad de negocio, abra la página **Tarjeta de unidad de negocio** y elija la acción **Configuración**. 
   * Para exportar un archivo .xml y compartirlo manualmente, elija **Formato de archivo**.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Preparar los libros de contabilidad para la consolidación

En el plan de cuentas de una empresa que se va a consolidar se deben especificar cuentas para consolidación. Por cada cuenta de contabilidad de cada empresa, debe especificar la cuenta de la empresa consolidada a la que transferir el saldo tras la consolidación. Esta asignación le permite consolidar empresas que tienen diferentes planes de cuentas.

Si el plan de cuentas de la unidad de negocio difiere de la empresa consolidada, debe preparar los libros contables para la consolidación. Puede especificar las cuentas para apuntar debe y haber y el método a utilizar para traducir las divisas en la empresa consolidada.

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
|Tipo de cambio compuesto | Los importes del periodo actual se traducen con el tipo de cambio medio y se agregan al saldo anteriormente registrado en la empresa consolidada. Normalmente utiliza este método para cuentas de ganancias retenidas. Esas cuentas incluyen cantidades de diferentes períodos, por lo que contienen cantidades convertidas con diferentes tipos de cambio.|
|Tasa de participación | Esta opción es similar a **Compuesto**. Las diferencias se registran para separar cuentas de libro mayor.|

Para especificar los tipos de cambio para las unidades de negocio, realice los pasos siguientes:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de negocio** y luego elija el enlace relacionado.  
2. En la página **Lista de unidades de negocio**, seleccione la unidad de negocio y, después, seleccione la acción **Tipo de cambio medio (manual)**.  
3. En la página **Modificar tipo de cambio**, el contenido del campo **Tipo de cambio relacionado** se ha copiado de la tabla **Tipo de cambio de divisa**, pero se puede modificar. Cierre la página.  
4. Seleccione la acción **Tipo de cambio al cierre**.  
5. En el campo **Cantidad del tipo de cambio relacionado**, introduzca el tipo de cambio.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Incluir o excluir dimensiones

Puede consolidar información sobre dimensiones y cuentas de contabilidad.

* En las dimensiones, especifique el campo **Código de consolidación** o déjelo en blanco.
  * Para excluir una dimensión en la consolidación, deje el campo **Código de consolidación** en la dimensión, y no elija dimensiones en los campos **Copiar dimensiones** de cualquier función o informe de consolidación.
  * Para incluir información de dimensión en la consolidación, deje el campo **Código de consolidación** en blanco. Sin embargo, la consolidación sólo funcionará si los valores de dimensión de la empresa son iguales que los de la empresa consolidada.
  * Para consolidar el código de valor de dimensión de la empresa con un código de valor de dimensión distinto en la empresa consolidada, rellene el campo **Código de consolidación** en las dimensiones.  
* Agregue las dimensiones a las cuentas de contabilidad.

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Excluir una empresa de la consolidación

Si no desea incluir una unidad de negocio en la consolidación, puede excluirla. Para hacerlo, vaya a la ficha de unidad de negocio y borre la casilla de verificación **Consolidar**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Incluir una empresa poseída parcialmente en la consolidación

Si posee únicamente parte de una empresa, puede incluir un porcentaje de cada transacción que refleja el porcentaje que le pertenece. Por ejemplo, si le pertenece el 70 % de la empresa, la consolidación incluirá 70 $ de una factura de 100 $. Para especificar el porcentaje de la empresa que le pertenece, vaya a la ficha de la unidad de negocio e introduzca el porcentaje en el campo **Consolidación %**.  

## <a name="see-also"></a>Consulte también

[Consolidar los datos financieros de varias empresas](finance-consolidated-company-reporting.md)  
[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exportar los datos de negocio a Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
