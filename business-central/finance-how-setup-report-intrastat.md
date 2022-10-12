---
title: Configuración de informes de Intrastat
description: Obtener información sobre cómo configurar las funciones de informes de Intrastat y cómo informar sobre el comercio con empresas de otros países de la UE.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077
ms.date: 09/02/2022
ms.author: altotovi
ms.openlocfilehash: b6adddb338af36f07abe4c6cb67c8113657ccb7c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605494"
---
# <a name="set-up-intrastat-reporting"></a>Configuración de informes de Intrastat

Todas las empresas de la Unión Europea (UE) deben emitir informes sobre sus transacciones comerciales con otros países o regiones de la UE. Las empresas deben notificar el movimiento de mercancías al organismo de estadística de su país o región todos los meses, y el informe se debe remitir a las autoridades fiscales. Intrastat es el sistema para recopilar estadísticas comerciales de bienes dentro de estos países/regiones. Usa el **Informe intrastat** para completar informes periódicos de Intrastat (generalmente mensuales), recopilar, registrar e informar el comercio de bienes de acuerdo con la legislación local.

Los informes de Intrastat se basan en las normas básicas de la UE que se aplican a todos los países; sin embargo, en la práctica, existen algunas diferencias dentro de los países individuales. Cada país tiene sus reglas sobre qué y cómo informar exactamente.

> [!NOTE]
> La información de Intrastat no se aplica al movimiento de servicios entre países, sino solo de bienes (artículos y activos fijos). Si el gobierno local requiere registrar el movimiento de servicios entre países, puede hacerlo utilizando la característica **Declaración de servicio**.
>
> Se espera que esta función esté disponible a partir de noviembre de 2022 como una aplicación en [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646), por lo que, si desea usarla, primero deberá instalarla en la página **Gestión de extensiones**.

> [!IMPORTANT]
> Este artículo cubre la nueva experiencia de Intrastat disponible en la versión 21 de [!INCLUDE[prod_short](includes/prod_short.md)]. Consulte a su administrador para saber qué versión está utilizando su empresa y para habilitar la nueva funcionalidad.
>
> Lea el artículo de configuración y uso de Intrastat de la versión anterior en [Configurar e informar Intrastat](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a>Habilitar la nueva experiencia de Intrastat

En el segundo lanzamiento de versiones de 2022, [!INCLUDE[prod_short](includes/prod_short.md)] incluye una experiencia de Intrastat rediseñada con funciones ampliadas. Si la nueva funcionalidad de Intrastat no está habilitada en su entorno, un administrador puede habilitarla manualmente en la página **Gestión de características**.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de características** y luego elija el enlace relacionado.
2. En la página **Administración de características**, seleccione la línea **Actualización de características: reemplazar la funcionalidad de Intrastat existente por la nueva extensión de Intrastat**. Obtenga más información sobre la administración de características en [Habilitar las próximas funciones de antemano](/dynamics365/business-central/dev-itpro/administration/feature-management), en el contenido de la administración.
3. En la columna **Habilitar para**, elija **Todos los usuarios**.
4. Lea la explicación de cómo se actualizará el sistema y elija **Sí** si está de acuerdo.
5. Seleccione **Siguiente** y obtendrá una configuración básica para Intrastat. Obtenga más información sobre la configuración de Intrastat en la sección [Configuración Intrastat](#intrastat-configuration).
6. Después de terminar la configuración, elija **Finalizar** para comenzar a utilizar la nueva experiencia de Intrastat.

> [!IMPORTANT]
> Tenga en cuenta que no puede usar experiencias antiguas y nuevas en paralelo. Antes de activar la extensión en un entorno de producción, se recomienda que primero habilite y pruebe esta función con una copia de los datos de producción en un entorno de pruebas aislado antes de hacerlo en un entorno de producción. Una vez que active una nueva experiencia de usuario en el entorno de producción, no podrá volver a la antigua funcionalidad de Intrastat.

> [!NOTE]
> Dependiendo de la ubicación de su empresa, habilitar la función descrita anteriormente será suficiente. Para los países con características específicas para los informes Intrastat, debe habilitar la aplicación Intrastat específica del país además de la extensión principal.

## <a name="intrastat-configuration"></a>onfiguración de Intrastat

Antes de que pueda usar los informes de Intrastat, hay varias configuraciones que se deben establecer.

### <a name="intrastat-reporting-setup"></a>Configuración de informes de Intrastat

La página **Configuración de informes de Intrastat** se utiliza para habilitar los informes de Intrastat y establecer sus valores predeterminados. Puede especificar si necesita elaborar informes de Intrastat a partir de envíos (despachos), recibos (llegadas), o ambos, según los umbrales establecidos por sus regulaciones locales. También se pueden establecer naturalezas de transacción predeterminadas para documentos normales y de devolución, que se utilizan para la naturaleza de los informes de transacción.

Para configurar los informes Intrastat:

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de Intrastat** y luego elija el enlace relacionado.
2. Abra la ficha desplegable **General** y rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La siguiente tabla describe algunos de los campos clave:

   | Campo | Descripción |
   | --- | --- |
   | **Informar recepciones** | Especifica que debe incluir las llegadas de artículos recibidos en los informes de intrastat. |
   | **Informar envíos** | Especifica que debe incluir los envíos de artículos distribuidos en los informes de intrastat. |
   | **Envíos basados en**  | Especifica en base a qué código de país se obtienen las líneas de informe Intrastat. Puede elegir una de las opciones: **País de venta**, **País de facturación** o **País de destino**. |
   | **N.º de IVA basado en** | Especifica en base a qué código de cliente/proveedor se obtiene el número de impuesto sobre el valor agregado (IVA) para el informe Intrastat. Puedes elegir una de las opciones: **IVA de venta** o **IVA facturado**. |
   | **CIF de empresa en archivo** | Especifica cómo se exporta el número de registro de IVA de la empresa al archivo Intrastat. Puede elegir una de las opciones: IVA Reg. No., agregando el código de país de la UE como prefijo y eliminando el código de país de la UE del registro de IVA. No. |
   | **CIF/NIF proveedor en archivo** | Especifica cómo se exporta el número de registro de IVA del proveedor al archivo Intrastat. Puede elegir una de las opciones: IVA Reg. No., agregando el código de país de la UE como prefijo y eliminando el código de país de la UE del registro de IVA. No. |
   | **CIF/NIF de cliente en archivo** | Especifica cómo se exporta el número de registro de IVA de un cliente al archivo Intrastat. Puede elegir una de las opciones: IVA Reg. No., agregando el código de país de la UE como prefijo y eliminando el código de país de la UE del registro de IVA. No. |
   | **Obtener IVA de socio** | Especifica desde qué tipo de línea de **Informe Intrastat** se actualiza el CIF/NIF del socio. Según sus requisitos locales, puede elegir solo para recepción, solo para envío o para ambos tipos de líneas. |
3. Abra la ficha desplegable **Transacciones predeterminadas** y rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La siguiente tabla describe algunos de los campos clave:

   | Campo | Descripción |
   | --- | --- |
   | **Tipo trans. predeterminado** | Especifica el tipo de transacción predeterminado para envíos de venta normales, envíos de servicios y recibos de compra. |
   | **Tipo trans. predeterminado - devoluciones** | Especifica el tipo de transacción predeterminado de devoluciones de ventas, devoluciones de servicios y devoluciones de compras. |
   | **N.º de IVA de persona privada predeterminada** | Especifica el número de IVA de la persona privada predeterminado en caso de que la persona privada deba tener un número de IVA dedicado en el informe de Intrastat. |
   | **N.º IVA comercial predeterminado de terceros** | Especifica el número de IVA comercial de terceros predeterminado en caso de que no tenga su número de IVA. |
   | **IVA predeterminado para estado desconocido** | Especifica el número de IVA predeterminado para un estado desconocido. |
   | **Código país/región predet.** | Especifica el código de país de recepción predeterminado. |
4. Abra la ficha desplegable **Informes** y rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La siguiente tabla describe algunos de los campos clave:

   | Campo | Descripción |
   | --- | --- |
   | **Código def. intercambio datos** | Especifica el código definición de intercambio de datos para generar el archivo de Intrastat. Funciona solo si el campo **Dividir archivos de recibos/envíos** se establece en **No**. |
   | **Dividir archivos recepción/envíos** | Especifica si se comunicarán las recepciones y los envíos en dos archivos independientes. |
   | **Archivo zip (-s)** | Especifica si se agregará el archivo de informe (-s) al archivo zip. |
   | **Código def. interc. datos - Recepción** | Especifica el código de definición de intercambio de datos para generar el archivo de Intrastat para mercancías recibidas. Funciona solo si el campo **Dividir archivos de recibos/envíos** se establece en **Sí**. |
   | **Código def. interc. datos - Envío** | Especifica el código de definición de intercambio de datos para generar el archivo de Intrastat para mercancías enviadas. Funciona solo si el campo **Dividir archivos de recibos/envíos** se establece en **Sí**. |
5. Abra la ficha rápida **Numeración** para configurar **Números de Intrastat**.

### <a name="set-up-a-reporting-file"></a>Configurar un archivo de informe

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la ficha desplegable **General**, describa la definición de intercambio de datos, el tipo de archivo de datos, el separador de columna, las codeunits relacionadas, XMLport y otros campos.
4. En la ficha desplegable **Definiciones de línea**, describa el formato de las líneas en el archivo de datos completando los campos según el campo **Tipo de línea** y donde necesita definir el número de columnas para esta línea.
5. En la ficha desplegable **Definiciones de columna**, complete la línea para cada columna planificada. Puede definir nombres de columnas, tipos de datos (*Texto*, *Fecha* o *Decimal*), la longitud de la línea de ancho fijo que contiene la columna si el archivo es de tipo Texto fijo y algunos otros parámetros.
6. Elija la acción **Asignación de campos** en la ficha desplegable **Definiciones de línea** para abrir la página **Mapeo de campos**.
7. Cree la nueva entrada y, en la ficha desplegable **General**, elija el **Id. de tabla** adecuado (para la **Línea de informe Intrastat**, elija 4812) y luego complete más campos:
   1. Especifique el índice de clave para ordenar los registros de origen antes de la exportación en el campo **Índice clave**.
   2. Seleccione la **Codeunit de mapeo** adecuada.
8. En la ficha desplegable **Mapeo de campos**, agregue columnas que configuró previamente en la ficha desplegable **Definiciones de columna**, luego agregue lo siguiente:
   1. Especifique el **Id. de campo** para cada una de las columnas.
   2. Especifique la **Regla de transformación** para cada columna que lo necesite. Especifica la regla que transforma el texto importado en un valor admitido para que se pueda asignar a un campo especificado en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando elige un valor en este campo, el valor exacto se introduce en el campo **Regla de transformación** en la tabla **Búfer asignación campo intercambio datos** y viceversa.
9. Si necesita agrupar entradas en función de algunas columnas, en la ficha desplegable **Agrupación de campos**, elija los campos que desea usar para agrupar.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] viene con la definición de intercambio de datos preconfigurada para Intrastat para todos los países localizados. Obtenga más información acerca de cómo crear una nueva definición de intercambio de datos en el artículo [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Establecer campos obligatorios con la lista de verificación del informe Intrastat

En algunos países, las autoridades requieren que los informes de Intrastat incluyan, por ejemplo, el método de envío para compras o algunos otros valores cuando las ventas superan un cierto umbral.

Para establecer campos y/o valores obligatorios en la página **Informe Intrastat**:

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informe Intrastat** y luego elija el enlace relacionado.
2. Elija la acción **Lista de comprobación de informe Intrastat**.
3. Agregue las líneas necesarias para verificar usando las siguientes instrucciones:
   1. Establezca el campo **Nº de campo** en un campo que se debe comprobar para un valor no vacío.
   2. Rellene el campo **Expresión de filtro** si es necesario, según las siguientes reglas:
      1. Cuando abra **Página de filtro**, elija el **Filtro** que necesita usar para comprobar.
      2. En el siguiente paso, elija un valor relacionado con el **Filtro** que usó.
      3. Si tiene más filtros que debe completar para este campo específico, puede agregar otro filtro siguiendo los mismos pasos.
      4. Cuando termine de ingresar los filtros para el campo elegido, elija **Aceptar**.
   3. Seleccione el campo **Expresión de filtro inversa** para especificar que la comprobación de campos se ejecuta solo en las líneas que no coinciden con la expresión de filtro. Si la línea no está filtrada, este campo se ignora.

> [!NOTE]
> Cuando abre la **Página de filtro** desde la línea **Expresión de filtro**, puede usar todas las expresiones de filtro estándar relacionadas con el campo específico que desea filtrar.
>
> Tenga cuidado con la configuración de las reglas de validación, ya que pueden diferir de un país a otro.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Usar codeunits personalizadas en informes Intrastat

Si desea cambiar el funcionamiento de Intrastat y la configuración predeterminada no es suficiente, puede personalizar el sistema ampliando las funciones estándar. Si necesita cambiar aún más el comportamiento de Intrastat, puede desarrollar sus propias codeunits. Sin embargo, cuando crea codeunits, debe realizar cambios adicionales para usarlas. Para configurar el sistema para usar sus propios objetos:

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de IVA** y luego elija el vínculo relacionado.
2. En lapágina **Configuración de informes de IVA**, agregue una nueva línea.
3. En el campo **Tipo de informe de IVA** campo, elija la opción **Informe intrastat**.
4. En el campo **Versión del informe de IVA**, especifique la versión del informe.
5. Después de eso, puede agregar sus codeunits para las siguientes opciones: a. En el campo **ID de codeunit de líneas sugeridas**, especifique la nueva codeunit para las líneas sugeridas en las líneas del informe Intrastat.
   b. En el campo **ID de codeunit de contenido**, especifique la nueva codeunit para exportar datos como un archivo mediante una definición de intercambio de datos.
   c. En el campo **Validar ID de codeunit**, especifique las nuevas codeunits para las validar los resultados en las líneas del informe Intrastat.

> [!IMPORTANT]
>
> Esta línea debe estar vacía si utiliza las codeunits estándar. Solo debe crear una línea y configurarla si ha desarrollado codeunits personalizadas.

## <a name="other-intrastat-configurations"></a>Otras configuraciones de Intrastat

> [!IMPORTANT]
> Las fichas de cliente y proveedor incluyen un campo, **Tipo socio Intrastat**, que tiene los mismos valores de opción que el campo **Tipo socio**: "" (vacío), *Compañía* y *Persona*. El campo **Tipo socio Intrastat** ha reemplazado al campo **Tipo socio** en los informes de Intrastat. El campo **Tipo de socio** se utiliza en el Área Única de Pagos en Euros (SEPA) para definir el Esquema de Débito Directo SEPA (Core o B2B). El campo **Tipo de socio Intrastat** se utiliza solo para informes de Intrastat. De esta forma, puede especificar valores diferentes para los dos campos, si es necesario.
>
> Si el campo **Tipo socio Intrastat** se deja en blanco, el valor del **Tipo socio** se utiliza para los informes de Intrastat.

Excepto por **Configuración del informe Intrastat**, **Definiciones de intercambio de datos** y **Lista de verificación del informe Intrastat**, también necesita configurar otros ajustes:

| Página | Descripción |
| ---- | ----------- |
| **Países/regiones** | Antes de comenzar a utilizar los informes de Intrastat, también debe configurar la página **Países/regiones**. En esta página, debe agregar el **Código de país/región de la UE** y el **Código Intrastat** para especificar un código para el país/región con el que está operando, ya que se utilizará en los informes de Intrastat. |
| **Códigos arancelarios** | En muchos paises, las autoridades aduaneras y fiscales han establecido códigos de 8 dígitos para los distintos productos. Para que los movimientos de productos contengan la información necesaria cuando el sistema los importe en la línea del diario de Intrastat, debe introducir el código de elemeno en la página **Códigos arancelarios**. Averigüe los códigos correspondientes a los productos que oferta su empresa e introdúzcalos en la página **Códigos arancelarios**. |
| **Modos transporte** | Existen siete códigos de un dígito para los modos de transporte de Intrastat. **1** para mar, **2** para ferrocarril, **3** para carretera, **4** para aire, **5** para correo, **7** para instalaciones fijas y **9** para autopropulsión (por ejemplo, transportar un coche conduciéndolo). [!INCLUDE[prod_short](includes/prod_short.md)] no requiere estos códigos específicos; sin embargo, recomendamos que las descripciones proporcionen un significado similar. |
| **Naturalezas transacciones** | Los países y regiones tienen diferentes códigos para los tipos de transacciones de Intrastat, como la compra y venta ordinaria, el intercambio de mercancías devueltas y el intercambio de mercancías no devueltas. Configure todos los códigos que se aplican a su país o región. Luego estos códigos se usan en la ficha despegable **Comercio exterior** en los documentos de venta y compra, y cuando procese las devoluciones. |
| **Especificación transacciones** | Configure códigos para complementar las descripciones del tipo de transacción. |
  > [!NOTE]
  > A partir de enero de 2022, Intrastat requiere códigos de naturaleza de transacción diferente para envíos a particulares o empresas sin registro de IVA y empresas registradas con IVA. Para cumplir con este requisito, le recomendamos que revise y/o agregue nuevos códigos de naturaleza de transacción en la página **Tipos de transacciones**, de acuerdo con los requisitos de su país. También debe comprobar y actualizar el campo **Tipo socio Intrastat** a *Persona* para clientes particulares o empresas no registradas a efectos del IVA en la página **Cliente**. Si no está seguro del Itipo de socio Intrastat o del tipo de transacción que se usará, le recomendamos que consulte a un experto de su país o región.

| **Campo** | **Descripción** |
| --------- | --------------- |
| **Peso neto** | El peso es una de las configuraciones básicas relacionadas con los informes de Intrastat como el **Peso total** es obligatorio para informar. Para estar listo para este requisito, también debe completar el campo **Peso neto** en la tarjeta de artículo o activo fijo. |
| **Cód. país/región de origen** | Use los códigos alfa ISO de dos letras en la tarjeta del elemento o activo fijo para el país donde se obtuvo o produjo el bien. Si la mercancía fue producida en más de un país, el país de origen es el último país donde fue significativamente procesada. |
| **Número de identificación a efectos del IVA del operador asociado en el Estado miembro de importación** | Es el número de identificación a efectos del IVA del operador asociado en el Estado miembro de importación. El VAT-ID también se utiliza en el intercambio de datos de exportación dentro de la UE entre los Estados miembros, y permite a los Estados miembros asignar los datos recibidos a la empresa importadora en su propio país. Las unidades declarantes deben comunicar el NIF-IVA de la empresa que declaró la adquisición de bienes dentro de la Unión en el Estado miembro de importación. |

Opcionalmente, también puede configurar:

* **Códigos de mercancía**: las autoridades aduaneras y fiscales han establecido códigos numéricos que clasificar productos y servicios. Especifique estos códigos para los productos.
* **Áreas**: información complementaria sobre los países y regiones.
* **Puertos y aeropuertos**: especifique las ubicaciones de otros países donde envía o recibe productos. Un aeropuerto de Heathrow es un ejemplo de valor de este campo. Introduzca los puertos y aeropuertos en los documentos de ventas y compras en la ficha desplegable **Internacional**. Esta información se copiará también de los movimientos de productos al crear el diario de Intrastat.
* **Unidad de medida suplementaria**: la cantidad de mercancías para el informe de Intrastat puede ser peso neto (en kilogramos) o una unidad suplementaria. Si se requieren unidades adicionales, debe configurarlas para artículos y activos fijos.

#### <a name="set-up-transport-methods"></a>Configurar métodos de transporte

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Métodos de transporte** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Configurar códigos de naturaleza de transacción

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tipos de transacciones** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Otras configuraciones relacionadas

Antes de utilizar la función de informes de Intrastat, debe configurar algunos campos en las fichas de artículos, activos fijos, clientes y proveedores.

#### <a name="item-cards"></a>Fichas de producto

Para configurar toda la información necesaria relacionada con Intrastat en fichas de artículos:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Seleccione el elemento que quiere configurar.
3. Amplíe la ficha despelgable **Costos y publicación** y rellene el **Número de arancel**, la **Unidad de medida suplementaria** y el **Código de país/región de origen**.
4. Amplíe la ficha desplegable **Inventario** e ingrese el valor decimal en el campo **Peso neto**.

> [!NOTE]
> Puede utilizar diferentes unidades de medida como su unidad de medida suplementaria. Si esto no es lo mismo que la **Unidad de medida base**, necesita configurar esta unidad de medida en la página **Unidades de medida de producto**.

#### <a name="fixed-asset-cards"></a>Fichas de activos

Para configurar toda la información necesaria relacionada con Intrastat en fichas de activos:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo fijo que desee configurar.
3. Amplíe la ficha desplegable **Intrastat** y rellene los campos **Número de arancel**, **Peso neto** y **Unidad de medida suplementaria**.

> [!NOTE]
> Puede utilizar diferentes unidades de medida como su unidad de medida suplementaria. Pero, con independencia del **Código de unidad de medida** que elija, su **Cantidad** en los informes de Intrastat siempre será 1.

#### <a name="vendor-cards"></a>Fichas de proveedor

Antes de utilizar un proveedor en los informes de Intrastat, debe tener un **Código de país/región** y un **Número de registro de IVA** dedicado para cada uno de ellos, además de más información sobre su página **Tarjeta de vendedor**:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.
2. Seleccione el proveedor que quiere configurar.
3. En la ficha desplegable **Intrastat**, puede establecer valores predeterminados para **Tipo de trans. predeterminada**, **Tipo de trans. predeterminada - Devoluciones** y **Método de transporte predeterminado**.
4. Amplíe la ficha desplegable **Pagos** y elija la opción en el campo **Tipo de socio de Intrastat** para especificar si el proveedor es una persona o una empresa en los informes de Intrastat.

#### <a name="customer-cards"></a>Fichas de cliente

Antes de utilizar un cliente en los informes de Intrastat, debe tener un **Código de país/región** y un **Número de registro de IVA** dedicado para cada uno de ellos, además de más información sobre su página **Tarjeta de cliente**:

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Seleccione el cliente que quiere configurar.
3. En la ficha desplegable **Intrastat**, puede establecer valores predeterminados para **Tipo de trans. predeterminada**, **Tipo de trans. predeterminada - Devoluciones** y **Método de transporte predeterminado**.
4. Amplíe la ficha desplegable **Pagos** y elija la opción en el campo **Tipo de socio de Intrastat** para especificar si el proveedor es una persona o una empresa en los informes de Intrastat.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Excluir artículos y activos fijos de los informes de Intrastat

Si hay un motivo para excluir un artículo o activo fijo específico de los informes de Intrastat, debe cambiar una opción en su tarjeta.

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Excluir un artículo de un informe Intrastat

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Seleccione el elemento que quiere configurar.
3. Amplíe la ficha desplegable **Costos y registros** y seleccione el campo **Excluir del informe de Intrastat**.

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Excluir activos fijos de los informes de Intrastat

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo fijo que desee configurar.
3. Amplíe la ficha desplegable **Intrastat** y seleccione el campo **Excluir del informe de Intrastat**.

## <a name="country-specific-intrastat-setup"></a>Configuración de Intrastat específica del país

<!-- PM's note: Currently, we will add only the 'Overview' topic; the topic 'Manage Intrastat Country Specifics' and country details will wait until 21.1 when I update with all country-based details -->

Los requisitos de Intrastat son similares en todos los estados miembros de la UE, aunque hay excepciones importantes. En teoría, las reglas deberían aplicarse de manera uniforme en todos los estados miembros. Sin embargo, existen diferencias en la implementación porque algunos estados miembros brindan pautas sobre cómo se deben aplicar los principios generales del reglamento en situaciones específicas (por ejemplo, muestras comerciales, devolución de bienes, etc.). Estas pautas pueden producir resultados diferentes para diversas situaciones en los estados miembros de la UE. Por eso, algunos países tienen información específica adicional separada de otros países, y también tienen un formato de archivo diferente para los informes.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Consulte también .

[Informes de Intrastat en Business Central](finance-how-report-intrastat.md)  
[Gestión financiera](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
