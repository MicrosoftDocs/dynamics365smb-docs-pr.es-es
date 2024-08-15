---
title: Trabajar con informes de Intrastat
description: Obtener información sobre cómo informar sobre el comercio con empresas de otros países o regiones de la UE con el sistema Intrastat.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 07/12/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="work-with-intrastat-reporting"></a>Trabajar con informes de Intrastat

Todas las empresas de la Unión Europea (UE) deben emitir informes sobre sus transacciones comerciales con otros países o regiones de la UE. Debe notificar el movimiento de mercancías al organismo de estadística de su país o región todos los meses, y el informe se debe remitir a las autoridades fiscales. Intrastat es el sistema para recopilar estadísticas comerciales de bienes dentro de estos países/regiones. Usa el **Informe intrastat** para completar informes periódicos de Intrastat (generalmente mensuales), recopilar, registrar e informar el comercio de bienes de acuerdo con la legislación del gobierno local.

Los informes de Intrastat se basan en las normas básicas de la UE que se aplican a todos los países y regiones; sin embargo, en la práctica, existen algunas diferencias dentro de los países o regiones individuales. Cada país o región tiene sus reglas sobre qué y cómo informar exactamente.

> [!IMPORTANT]  
> Este artículo describe la nueva experiencia Intrastat disponible en [!INCLUDE[prod_short](includes/prod_short.md)] a partir del segundo lanzamiento de versiones de 2022, que incluye funciones ampliadas y [debe estar activado para las empresas existentes](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Póngase en contacto con su administrador para activar y configurar la nueva capacidad.
>
> Lea el artículo de configuración y uso de Intrastat de la versión anterior en [Configurar e informar Intrastat](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]  
> La información de Intrastat no se aplica al movimiento de servicios entre países o regiones, sino solo de bienes (artículos y activos fijos). Si el gobierno local requiere registrar el movimiento de servicios entre países y regiones, puede hacerlo utilizando la característica **Declaración de servicio**.
>
> Actualmente esperamos que esta función esté disponible a partir de noviembre de 2022 como una aplicación en [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). En ese momento, para usarlo, primero debe instalarlo en la página **Gestión de extensiones**.

## <a name="fill-in-the-intrastat-report"></a>Rellenar el informe de Intrastat

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), Icono, ingrese a **Lista de informes Intrastat** y seleccione el vincular relacionado.
2. Seleccione la acción **Nuevo** para crear un nuevo **Informe Intrastat**.
3. Si necesita introducir alguna información interna sobre el **Informe Intrastat**, complete esta información en el campo **Descripción**.
4. En el campo **Período de la estadística**, especifique el mes para el que informar datos. Ingrese el período como un número de cuatro dígitos sin espacios ni símbolos. Dependiendo de su país o región, ingrese primero el mes y luego el año, o viceversa. Por ejemplo, escriba *2206* o *0622* para junio de 2022.
5. Elija la acción **Proponer líneas**. Los campos **Fecha inicial** y **Fecha final** aparecerán con las fechas especificadas como periodo estadístico en el encabezado del informe Intrastat.
6. En el campo **% Coste territorio nacional**, puede introducir un porcentaje que cubra el transporte y el seguro. Si escribe un porcentaje, el contenido del campo **Valor estadístico** del diario es proporcionalmente superior. Pero si desea utilizar esta función, debe cambiar el campo **Importe incluido Cargos por artículo** a **Sí**.
7. Eventualmente puede establecer configuraciones adicionales en la ficha rápida **Adicional**:
   1. **Omitir Recálculo para Cantidades Cero** para especificar que las líneas sin importes no se volverán a calcular durante el trabajo por lotes.
   2. **Omitir importes cero** para especificar que los movimientos de producto sin importes no se incluirán en el proceso.
   3. **Omitir movimientos no facturados** para especificar si los movimientos de producto que se envían o reciben, pero que aún no se han facturado, deben excluirse del proceso.
8. Elija **Aceptar** para iniciar el trabajo por lotes.

El proceso recupera todos los movimientos de producto en el periodo estadístico y los inserta como líneas en el **Informe Intrastat**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Modificar el informe de Intrastat

Si es necesario, puede modificar las líneas, pero siempre que cambie un valor en la línea del informe Intrastat, el campo **Corrección** se marcará automáticamente como **Sí**. Eventualmente, puede agregar una nueva línea manualmente si hay una razón para eso. Para agregar una nueva línea manualmente:

1. En la página **Informe Intrastat**, elija la acción **Nueva línea** en la ficha desplegable **Líneas**.
2. Elija la opción **Recibo** o **Envío** en el campo **Tipo**.
3. En el campo **Tipo de fuente**, elija una de las fuentes: **Entrada de artículo**, **Entrada FA** o **Entrada de trabajo**.
4. Basado en el **Tipo de fuente** en el campo **N.º de artículo**, puede elegir un **Artículo** (en ambos casos, **Entrada de artículo** o **Entrada de trabajo**) o **Activos fijos**.
5. Rellene los demás campos que necesite para los informes de Intrastat.

> [!NOTE]  
> Cuando agrega manualmente una nueva línea al informe de Intrastat, el campo **Fecha** en la línea debe estar dentro del intervalo **Período de la estadística** que agregó en el encabezado.

## <a name="validate-intrastat-lines"></a>Validar las líneas de Intrastat

Después de rellenar el **Informe de Intrastat**, puede ejecutar la acción **Lista de comprobación de informe** para asegurarse de que toda la información del **informe de Intrastat** es correcta. Los campos obligatorios que ha establecido en la página Lista de verificación de informe de Intrastat a los que les faltan valores, se mostrarán en el cuadro de información de **Errores y advertencias** en la página **Informe de Intrastat**.

Ejecute el informe **Lista de verificación del informe Intrastat** para verificar las líneas de Intrastat antes de que se exporten al formato requerido. La verificación se ejecuta dentro del **Informe de Intrastat**.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Recalcular peso o unidad de medida suplementaria

Si recibió el mensaje de error *El 'Peso total' en la línea de informe de Intrastat no debe estar en blanco*, probablemente se deba a que no configuró el **Peso neto** en el origen, artículo o activo fijo utilizado. En este caso, busque la ficha del artículo o activo fijo y agregue el valor requerido. Después de eso, solo necesita volver a abrir el **Informe de Intrastat** y seguir estos pasos:

1. Elija la acción **Recalcular la unidad de medida de peso/supl.** para recalcular el **Peso total** y/o la **Cantidad suplementaria**.
2. Elija una de las siguientes opciones:

    1. **Peso** – para volver a calcular sólo el **Peso total**, con base en la información actual sobre **Peso neto** en las fichas de artículo y activo fijo.
    2. **Cantidad de unidad de medida suplementaria** – para volver a calcular sólo la **Cantidad suplementaria** sobre la línea de **Informe Intrastat**, si existe, en función de la información actual sobre la **UOM suplementaria** en las fichas de artículo y activo fijo.
    3. **Ambos** – para volver a calcular el **Peso total** y la **Cantidad suplementaria**, con base en la información actual sobre las fichas de artículo y activo fijo.
3. Elija **Aceptar** para iniciar el trabajo por lotes.

## <a name="report-intrastat-in-a-file"></a>Emitir informes de Intrastat en un archivo

Puede enviar el informe de Intrastat como un archivo según los requisitos de las diferentes autoridades locales. Antes de crear el archivo, debe ejecutar el **Informe de lista de verificación** para verificar si todas las líneas contienen toda la información necesaria y válida. Para crear un archivo:

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Lista de Intrastat** y luego elija el enlace relacionado.
2. Elija el **Informe Intrastat** que desea informar como un archivo.
3. Si todavía no lo ha hecho, rellene el **Informe Intrastat** manualmente o elija la acción **Proponer líneas**.
4. Elija la acción **Crear archivo**.
5. El archivo Intrastat se guardará en el formato requerido.

Una vez que cree el archivo, [!INCLUDE[prod_short](includes/prod_short.md)] completará automáticamente los siguientes detalles sobre los informes:

* La **Fecha de exportación** para especificar la fecha en la que se ha exportado el informe.
* La **Hora de exportación** para especificar la hora en la que se ha exportado el informe.

> [!NOTE]  
> La próxima vez que cree un archivo, los campos **Fecha de exportación** y **Hora de exportación** solo mantendrán información sobre el último archivo que creó.

## <a name="intrastat-rules"></a>Reglas Intrastat

### <a name="grouping-lines"></a>Líneas de agrupación

En las líneas **Informe intrastat**, no hay agrupación por ningún campo. Todas las entradas se copian de la fuente original, por lo que puede localizarlas rápidamente en función de la combinación de **Tipo de fuente** y **Número de entrada de fuente**.

La agrupación requerida por las autoridades se proporcionará en el archivo exportado. Tiene que configurar esto en la **Definición de intercambio de datos**, que es totalmente configurable. Más información en [Configurar definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Informes de activos fijos

Los activos fijos se mostrarán en las líneas de Intrastat solo si:

* El **Tipo de publicación de activos fijos** en el campo **Entrada del libro mayor de activos fijos** es **Coste de adquisición** y si el **Tipo de documento** es **Factura** en el caso de compras, y
* El **Tipo de publicación de activos fijos** en el campo **Entrada del libro mayor de activos fijos** es **Ingresos de la venta/baja** y si el **Tipo de documento** es **Factura** en el caso de ventas.

### <a name="intrastat-report-statuses"></a>Estados de informes Intrastat

Cuando trabaja con el **Informe Intrastat** verá un campo **Estado** en el encabezado del documento. Puede encontrar los siguientes estados junto con las reglas relacionadas:

* **Abierto**: este estado se crea automáticamente cuando crea un nuevo informe Intrastat y puede realizar todas las operaciones en este estado.
* **Liberado**: [!INCLUDE[prod_short](includes/prod_short.md)] cambia automáticamente el estado a *Liberado* cuando se crea un archivo. A partir de ese momento, no podrá modificar su **Informe Intrastat**. Si necesita cambiar algo e informar nuevamente, puede usar la acción **Reabrir** para reabrir el informe Intrastat. Una vez que se vuelve a abrir el documento, puede utilizar la acción **Liberar** para liberar el documento de nuevo.
* **Notificado**: especifica si el movimiento ya se ha declarado a las autoridades fiscales. Este no es un estado regular sino un campo independiente, e incluso si reabriera el informe de Intrastat, aún mostraría que el archivo ya se creó para este informe.

### <a name="locations-in-intrastat-reporting"></a>Ubicaciones en los informes Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] siempre utiliza la información en el campo **Código de país/región** en la página **Tarjeta de ubicación** como el país para **enviar desde** o para **recibir a** mercancías. Cuando esta información no existe o no se utilizó la ubicación, el sistema utiliza la información de la página **Información empresa**.   

> [!NOTE]  
> Si la empresa opera desde más de un país o región, los informes Intrastat no funcionan para todos los países o regiones donde están configuradas las ubicaciones. Los informes se basan únicamente para el país o región principal, ya que actualmente no es posible utilizar informes para varios países o regiones.  

### <a name="triangular-trade-in-intrastat"></a>Comercio triangular en Intrastat

El comercio triangular implica el comercio entre tres países o regiones donde los bienes pasan por alto el país o región de la empresa informante. En Business Central, esto se puede facilitar a través de la funcionalidad [Envío directo](sales-how-drop-shipment.md). Para habilitar esta opción, active el campo **Incluir envío directo** en la **Configuración de informe Intrastat**.  

Cuando habilita esta opción, el sistema usa las siguientes reglas, pero solo si tiene **Drop Shipment** marcada en el **Pedido de venta**: 

| Recibiendo de | Entregando a | Resultado intrastat esperado |
|----------|------------|----------------------|
| País o región como en **Información empresa** | País o región como en **Información empresa** | Sin líneas intrastat |  
| País o región como en **Información empresa** | País o región de la UE diferente del país o región en **Información empresa** | Línea de envío intrastat | 
| País o región como en **Información empresa** | País o región no perteneciente a la UE | Sin líneas intrastat |   
| País o región de la UE diferente del país o región en **Información empresa** | País o región como en **Información empresa** | Línea de recepción intrastat | 
| País o región de la UE diferente del país o región en **Información empresa** | País o región de la UE diferente del país o región en **Información empresa** | Sin líneas intrastat |
| País o región de la UE diferente del país o región en **Información empresa** | País o región no perteneciente a la UE | Sin líneas intrastat | 
| País o región no perteneciente a la UE | País o región como en **Información empresa** | Sin líneas intrastat |  
| País o región no perteneciente a la UE | País o región de la UE diferente del país o región en **Información empresa** | Sin líneas intrastat |
| País o región no perteneciente a la UE | País o región no perteneciente a la UE | Sin líneas intrastat |   

## <a name="see-also"></a>Consulte también .

[Configurar informes de Intrastat](finance-how-setup-report-intrastat.md)  
[Gestión financiera](finance.md)  
[Envío directo](sales-how-drop-shipment.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
