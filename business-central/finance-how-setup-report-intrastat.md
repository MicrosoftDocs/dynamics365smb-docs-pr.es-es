---
title: Configurar informes de Intrastat
description: Este artículo explica cómo configurar las funciones de informes de Intrastat para informar sobre el comercio con empresas de otros países de la UE.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Configurar informes de Intrastat

Todas las empresas de la Unión Europea (UE) deben emitir informes sobre sus transacciones comerciales con otros países o regiones de la UE. Las empresas deben notificar el movimiento de mercancías al organismo de estadística de su país o región todos los meses, y el informe se debe remitir a las autoridades fiscales. Intrastat es el sistema que se usa para recopilar estadísticas comerciales sobre bienes dentro de estos países/regiones. Usa el informe intrastat para completar informes periódicos de Intrastat mediante la recopilación, el registro y la generación de informes del comercio de bienes de acuerdo con la legislación local.

Los informes de Intrastat se basan en las normas básicas de la UE que se aplican a todos los países. Sin embargo, hay diferencias dentro de los países individuales. Cada país tiene sus reglas sobre qué y cómo informar.

> [!NOTE]
> La información de Intrastat no se aplica al movimiento de servicios entre países. En cambio, la información se aplica solo a bienes como artículos y activos fijos. Si su gobierno requiere registrar el movimiento de servicios entre países, use la característica **Declaración de servicio**.
>
> Esta característica está disponible a partir de noviembre de 2022 como una aplicación que puede descargar desde [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Para usar la característica, primero debe instalarla en la página **Gestión de extensiones**.

> [!IMPORTANT]
> Este artículo cubre la nueva experiencia de Intrastat disponible en la versión 21 de [!INCLUDE[prod_short](includes/prod_short.md)]. Consulte a su administrador para saber qué versión está utilizando su empresa y si debe habilitar la nueva funcionalidad.
>
> Lea el artículo de configuración y uso de Intrastat de la versión anterior en [Configurar e informar Intrastat](finance-how-setup-report-intrastat-v20.md).

## Habilitar la nueva experiencia de Intrastat

En el segundo lanzamiento de versiones de 2022, [!INCLUDE[prod_short](includes/prod_short.md)] incluye una experiencia de Intrastat rediseñada que ofrece funciones ampliadas. Si la nueva funcionalidad de Intrastat no está habilitada en su entorno, un administrador puede habilitarla en la página **Gestión de características**.

> [!IMPORTANT]
> No puede usar experiencias antiguas y nuevas en paralelo. Antes de activar la extensión en un entorno de producción, le recomendamos que primero la habilite y pruebe con una copia de los datos de producción en un entorno de pruebas aislado. Después de activar una nueva experiencia de usuario en el entorno de producción, no podrá volver a la antigua funcionalidad de Intrastat.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de características** y luego seleccione el vínculo relacionado.
2. En la página **Administración de características**, seleccione la línea para **Actualización de características: reemplazar la funcionalidad de Intrastat existente por la nueva extensión de Intrastat**. Para obtener más información sobre la administración de características, consulte [Habilitar las próximas funciones de antemano](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. En la columna **Habilitar para**, seleccione **Todos los usuarios**.
4. Lea la explicación de cómo se actualizará el sistema y seleccione **Sí** si está de acuerdo.
5. Seleccione **Siguiente**. Obtendrá la configuración básica para Intrastat. Para obtener más información sobre la configuración de Intrastat, consulte la sección [Configuración Intrastat](#intrastat-configuration) más adelante en este artículo.
6. Después de terminar la configuración, seleccione **Finalizar** para comenzar a utilizar la nueva experiencia de Intrastat.

    > [!NOTE]
    > Dependiendo de la ubicación de su empresa, será suficiente para habilitar la característica anterior. Para los países que tienen características específicas para los informes Intrastat, debería habilitar la aplicación Intrastat específica del país además de la extensión principal.

## onfiguración de Intrastat

Antes de que pueda usar los informes de Intrastat, hay varias configuraciones que se deben establecer.

### Configuración de informes de Intrastat

Use la página **Configuración de informes de Intrastat** para habilitar y configurar el comportamiento predeterminado de los informes de Intrastat. Puede especificar si necesita elaborar informes de Intrastat a partir de envíos (despachos), recibos (llegadas), o ambos, según los umbrales establecidos por sus regulaciones locales. También se pueden establecer naturalezas de transacción predeterminadas para documentos normales y de devolución, que se utilizan para los informes de transacción.

Siga estos pasos para configurar los informes de Intrastat.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de Intrastat** y luego seleccione el vínculo relacionado.
2. En la ficha desplegable **General**, seleccione o introduzca la información del campo según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La siguiente tabla describe algunos de los campos clave.

   | Campo | Descripción |
   | --- | --- |
   | **Informar recepciones** | Especifica que debe incluir las llegadas de artículos recibidos en los informes de intrastat. |
   | **Informar envíos** | Especifica que debe incluir los envíos de artículos distribuidos en los informes de intrastat. |
   | **Envíos basados en**  | Especifica en base a qué código de país se obtienen las líneas de informe Intrastat.  |
   | **N.º de IVA basado en** | Especifica en base a qué código de cliente/proveedor se obtiene el número de impuesto sobre el valor agregado (IVA) para el informe Intrastat.  |
   | **CIF de empresa en archivo** | Especifica cómo se exporta el número de registro de IVA de la empresa al archivo Intrastat.  |
   | **CIF/NIF proveedor en archivo** | Especifica cómo se exporta el número de registro de IVA del proveedor al archivo Intrastat.  |
   | **CIF/NIF de cliente en archivo** | Especifica cómo se exporta el número de registro de IVA de un cliente al archivo Intrastat.  |
   | **Obtener IVA de socio** | Especifica desde qué tipo de línea de informe de Intrastat se actualiza el CIF/NIF del partner. Según sus requisitos locales, puede elegir solo líneas de recepción, solo líneas de envío o ambos tipos de líneas. |

3. En la ficha desplegable **Transacciones predeterminadas**, seleccione o introduzca la información del campo según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La siguiente tabla describe algunos de los campos clave.

   | Campo | Descripción |
   | --- | --- |
   | **Tipo trans. predeterminado** | Especifica el tipo de transacción predeterminado para envíos de venta normales, envíos de servicios y recibos de compra. |
   | **Tipo trans. predeterminado - devoluciones** | Especifica el tipo de transacción predeterminado de devoluciones de ventas, devoluciones de servicios y devoluciones de compras. |
   | **N.º de IVA de persona privada predeterminada** | Especifica el número de IVA de la persona privada predeterminado si la persona privada deba tener un número de IVA dedicado en el informe de Intrastat. |
   | **N.º IVA comercial predeterminado de terceros** | Especifica el número de IVA comercial de terceros predeterminado si no tiene su número de IVA. |
   | **IVA predeterminado para estado desconocido** | Especifica el número de IVA predeterminado para un estado desconocido. |
   | **Código país/región predet.** | Especifica el código de país de recepción predeterminado. |

4. En la ficha desplegable **Informes**, seleccione o introduzca la información del campo según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] La siguiente tabla describe algunos de los campos clave.

   | Campo | Descripción |
   | --- | --- |
   | **Código def. intercambio datos** | Especifica el código definición de intercambio de datos para generar el archivo de Intrastat. Este campo solo está disponible si el campo **Dividir archivos de recibos/envíos** se establece en **No**. |
   | **Dividir archivos recepción/envíos** | Especifica si se comunicarán las recepciones y los envíos en dos archivos independientes. |
   | **Archivo zip (-s)** | Especifica si se agregarán los archivos de informes al archivo zip. |
   | **Código def. interc. datos - Recepción** | Especifica el código de definición de intercambio de datos para generar el archivo de Intrastat para mercancías recibidas. Este campo solo está disponible si el campo **Dividir archivos de recibos/envíos** se establece en **Sí**. |
   | **Código def. interc. datos - Envío** | Especifica el código de definición de intercambio de datos para generar el archivo de Intrastat para mercancías enviadas. Este campo solo está disponible si el campo **Dividir archivos de recibos/envíos** se establece en **Sí**. |

5. En la ficha desplegable **Numeración**, introduzca un valor en el campo **Números de Intrastat**.

### Configurar un archivo de informe

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de intercambio de datos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione **Nuevo** y, a continuación, en la ficha desplegable **General**, introduzca información sobre la definición de intercambio de datos, el tipo de archivo de datos, el separador de columna, las codeunits relacionadas, XMLport y otros campos.
3. En la ficha desplegable **Definiciones de línea**, introduzca un valor en el campo **Tipo de línea** para describir el formato de las líneas en el archivo de datos y donde necesita definir el número de columnas para esta línea.
4. En la ficha desplegable **Definiciones de columna**, complete la línea para cada columna planificada. Puede definir nombres de columnas, tipos de datos (como texto, fecha o decimal), la longitud de la línea de ancho fijo que contiene la columna si el archivo es de tipo *Texto fijo* y algunos otros parámetros.
5. En la ficha desplegable **Definiciones de línea**, seleccione **Asignación de campos**.
6. En la página **Asignación de campos**, cree una nueva entrada. 
7. En la ficha desplegable **General**, seleccione el valor **Id. de tabla** (para **Línea de informe Intrastat**, elija **4812**), e introduzca la siguiente información de campo:

   1. En el campo **Índice clave**, especifique el índice clave para ordernar los registros de origen antes de la exportación.
   2. En el campo **Codeunit de asignación**, seleccione un valor.

8. En la ficha desplegable **Mapeo de campos**, agregue las columnas que configuró previamente en la ficha desplegable **Definiciones de columna** y luego agregue la siguiente información de campo:

   1. Especifique el valor **Id. de campo** para cada una de las columnas.
   2. Especifique el valor **Regla de transformación** para cada columna según sea necesario. El valor especifica la regla que transforma el texto importado en un valor admitido para que se pueda asignar a un campo especificado en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando elige un valor en este campo, el valor exacto se introduce en el campo **Regla de transformación** en la tabla **Búfer asignación campo intercambio datos** . (Por el contratio, cuando se introduce un valor exacto en el campo **Regla de transformación** en la tabla **Búfer asignación campo intercambio datos**, se elige un valor en este campo).

9. Si necesita agrupar entradas en función de algunas columnas, en la ficha desplegable **Agrupación de campos**, seleccione los campos que desea usar para agrupar.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] viene con la definición de intercambio de datos preconfigurada para Intrastat para todos los países localizados. Para obtener más información acerca de cómo crear una nueva definición de intercambio de datos, consulte [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).

### Establecer campos obligatorios con la lista de verificación del informe Intrastat

En algunos países, las autoridades requieren que los informes de Intrastat incluyan, por ejemplo, el método de envío para compras o algunos otros valores cuando las ventas superan un cierto umbral.

Para establecer campos o valores obligatorios en la página **Informe Intrastat**, siga estos pasos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de Intrastat** y luego seleccione el vínculo relacionado.
2. Seleccione **Lista de comprobación de informe Intrastat**.
3. Siga estos pasos para agregar las líneas necesarias para comprobar:
   1. Establezca el campo **Nº de campo** en un campo que se debe comprobar para un valor no vacío.
   2. Introduzca un valor en el campo **Expresión de filtro** si es necesario, según las siguientes reglas:

        1. Cuando abra **Página de filtro**, seleccione el filtro que necesita usar para comprobar.
        2. Seleccione un valor relacionado con el filtro seleccionado.
        3. Si debe llenar más filtros para el campo elegido, repita los dos pasos anteriores para agregar otro filtro.
        4. Cuando termine de introducir los filtros para el campo elegido, seleccione **Aceptar**.

   3. Seleccione la casilla **Expresión de filtro inversa** para especificar que la comprobación de campos se ejecuta solo en las líneas que no coinciden con la expresión de filtro. Si la línea no está filtrada, este campo se ignora.

> [!NOTE]
> Cuando abre la **Página de filtro** desde la línea **Expresión de filtro**, puede usar todas las expresiones de filtro estándar relacionadas con el campo específico que desea filtrar.
>
> Tenga cuidado al configurar las reglas de validación, ya que pueden diferir entre países.

## Usar codeunits personalizadas en informes Intrastat

Si desea cambiar el funcionamiento de Intrastat y la configuración predeterminada no es suficiente, puede personalizar el sistema ampliando las funciones estándar. Si necesita cambiar aún más el comportamiento de Intrastat, puede desarrollar sus propias codeunits. Cuando crea codeunits, debe realizar cambios adicionales para usarlas. Para configurar el sistema para usar sus propios objetos, siga estos pasos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de IVA** y luego elija el vínculo relacionado.
2. En lapágina **Configuración de informes de IVA**, agregue una nueva línea.
3. En el campo **Tipo de informe de IVA**, seleccione **Informe de Intrastat**.
4. En el campo **Versión del informe de IVA**, especifique la versión del informe.
5. Agregue sus codeunits para las siguientes opciones:
   1. En el campo **Id. de codeunit de líneas sugeridas**, especifique la nueva codeunit para las líneas sugeridas en las líneas del informe intrastat.
   2. En el campo **Id. de codeunit de contenido**, especifique la nueva codeunit para exportar datos como un archivo mediante una definición de intercambio de datos.
   3. En el campo **Validar id. de codeunit**, especifique las nuevas codeunits para validar los resultados en las líneas del informe intrastat.

> [!IMPORTANT]
> Esta línea debe estar vacía si utiliza las codeunits estándar. Solo debe crear una línea y configurarla si ha desarrollado codeunits personalizadas.

## Otras configuraciones de Intrastat

Las fichas de cliente y proveedor incluyen el campo **Tipo socio Intrastat**, que tiene los mismos valores de opción que el campo **Tipo socio**: 

- "" (en blanco)
- *Compañía*
- *Persona*
    
El campo **Tipo socio Intrastat** ha reemplazado al campo **Tipo socio** en los informes de Intrastat. El campo **Tipo de socio** se utiliza en el Área Única de Pagos en Euros (SEPA) para definir el Esquema de Débito Directo SEPA (Core o B2B). El campo **Tipo de socio Intrastat** se utiliza solo para informes de Intrastat. Por lo tanto, puede especificar valores diferentes para los dos campos, si es necesario.

Si el campo **Tipo socio Intrastat** se deja en blanco, el valor del **Tipo socio** se utiliza para los informes de Intrastat.

Además de **Configuración del informe Intrastat**, **Definiciones de intercambio de datos** y **Lista de verificación del informe Intrastat**, también debe configurar los siguientes ajustes.

| Página | Descripción |
| ---- | ----------- |
| **Países y regiones** | En la página **Países/regiones**, agregue **Código de país/región de la UE** e información del **Código Intrastat** para especificar un código en el país/región con el que está operando. Esta información se usará en los informes de Intrastat. |
| **Códigos arancelarios** | En muchos paises, las autoridades aduaneras y fiscales han establecido códigos de ocho dígitos para los distintos productos. Para habilitar los movimientos de productos que contengan la información necesaria cuando el sistema los importe en la línea del diario de Intrastat, debe introducir el código de elemeno en la página **Códigos arancelarios**. Averigüe los códigos correspondientes a los productos que oferta su empresa e introdúzcalos en la página **Códigos arancelarios**. |
| **Modos transporte** | Hay siete códigos de un dígido para los métodos de transporte Intrastat: **1** para mar, **2** para ferrocarril, **3** para carretera, **4** para aire, **5** para correo, **7** para instalaciones fijas y **9** para autopropulsión (por ejemplo, transportar un coche conduciéndolo). [!INCLUDE[prod_short](includes/prod_short.md)] no requiere estos códigos específicos. Sin embargo, recomendamos que las descripciones proporcionen un significado similar. |
| **Naturalezas transacciones** | Los países y regiones tienen diferentes códigos para los tipos de transacciones de Intrastat, como la compra y venta ordinaria, el intercambio de mercancías devueltas y el intercambio de mercancías no devueltas. Configure todos los códigos que se aplican a su país o región. Luego estos códigos se usan en la ficha despegable **Comercio exterior** en los documentos de venta y compra, y cuando procese las devoluciones. |
| **Especificación transacciones** | Configure códigos para complementar las descripciones del tipo de transacción. |
  
> [!NOTE]
> A partir de enero de 2022, Intrastat requiere códigos de naturaleza de transacción diferente para envíos a particulares o empresas sin registro de IVA y empresas registradas con IVA. Para cumplir con este requisito, le recomendamos que revise o agregue nuevos códigos de naturaleza de transacción en la página **Tipos de transacciones**, de acuerdo con los requisitos de su país. También debe comprobar y actualizar el campo **Tipo socio Intrastat** a *Persona* para clientes particulares o empresas no registradas a efectos del IVA en la página **Cliente**. Si no está seguro del Itipo de socio Intrastat o del tipo de transacción que se usará, le recomendamos que consulte a un experto de su país o región.

|   Campo   |   Descripción   |
| --------- | --------------- |
| **Peso neto** | El peso es una de las configuraciones básicas relacionadas con los informes de Intrastat, ya que el peso total es obligatorio para informar. Para estar listo para este requisito, introduce un valor en el campo **Peso neto** en la tarjeta de artículo o activo fijo. |
| **Cód. país/región de origen** | Use los códigos alfa ISO de dos letras en la tarjeta del elemento o activo fijo para el país donde se obtuvo o produjo el bien. Si la mercancía fue producida en más de un país, el país de origen es el último país donde fue significativamente procesada. |
| **Número de identificación a efectos del IVA del operador asociado en el Estado miembro de importación** | Es el número de identificación a efectos del IVA del operador asociado en el Estado miembro de importación. El VAT-ID también se utiliza en el intercambio de datos de exportación dentro de la UE entre los Estados miembros, y permite a los Estados miembros asignar los datos recibidos a la empresa importadora en su propio país. Las unidades declarantes deben comunicar el NIF-IVA de la empresa que declaró la adquisición de bienes dentro de la Unión en el Estado miembro de importación. |

Opcionalmente, también puede configurar:

* **Códigos de mercancía**: las autoridades aduaneras y fiscales han establecido códigos numéricos que clasificar productos y servicios. Puede especificar estos códigos para los productos.
* **Áreas**: información complementaria sobre los países y regiones.
* **Puertos y aeropuertos**: especifique las ubicaciones de otros países donde envía o recibe productos. Un aeropuerto de Heathrow es un ejemplo de valor de este campo. Introduzca los puertos y aeropuertos en los documentos de ventas y compras en la ficha desplegable **Internacional**. Esta información se copia también de los movimientos de productos al crear el diario de Intrastat.
* **Unidad de medida suplementaria**: la cantidad de mercancías para el informe de Intrastat puede ser peso neto (en kilogramos) o una unidad suplementaria. Si se requieren unidades adicionales, debe configurarlas para artículos y activos fijos.

#### Configurar métodos de transporte

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Métodos de transporte** y luego seleccione el vínculo relacionado.
2. Rellene la información de los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Configurar códigos de naturaleza de transacción

1. seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tipos de transacción** y luego seleccione el vínculo relacionado.
2. Rellene la información de los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Otras configuraciones relacionadas

Antes de utilizar la característica de informes de Intrastat, debe definir campos en las fichas de artículos, activos fijos, clientes y proveedores.

#### Fichas de producto

Siga estos pasos para configurar toda la información necesaria relacionada con Intrastat en fichas de artículos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego seleccione el vínculo relacionado.
2. Seleccione el elemento que quiere configurar.
3. En la ficha despelgable **Costos y publicación**, en los campos **Número de arancel**, **Unidad de medida suplementaria** y **Código de país/región de origen**, introduzca un valor.

    > [!NOTE]
    > Para usar una unidad de medida para suplmentar la unidad de medida base, configure la unidad de medida suplementaria en la página **Unidades medida producto**.

4. En la ficha desplegable **Inventario**, introduzca el valor decimal en el campo **Peso neto**.

> [!NOTE]
> Cuando agrega el número de tarifa a una unidad de medida definida para el artículo, [!INCLUDE [prod_short](includes/prod_short.md)] rellena automáticamente el campo **Unidad de medida suplementaria** en función de la configuración del número de tarifa. Puede cambiar el valor del campo **Unidad de medida suplementaria** según sea necesario.

#### Configurar activos fijos para Intrastat

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego seleccione el vínculo relacionado.
2. Seleccione el activo fijo que desee configurar.
3. En la ficha desplegable **Intrastat**, en los campos **Cód. arancelario**, **Peso neto** y **Unidad de medida suplementaria**, introduzca un valor.

> [!NOTE]
> Puede utilizar diferentes unidades de medida como su unidad de medida suplementaria. Pero, con independencia del **Código de unidad de medida** que elija, su **Cantidad** en los informes de Intrastat siempre será 1.

#### Configurar proveedores para Intrastat

Antes de que pueda incluir un proveedor en los informes de Intrastat, introduzca su información en la página **Ficha proveedor**. Por ejemplo, especifique un valor para **Código de país/región** y otro para **CIF/NIF**.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego seleccione el vínculo relacionado.
2. Seleccione el proveedor que quiere configurar.
3. En la ficha desplegable **Intrastat**, en los campos **Tipo de trans. predeterminada**, **Tipo de trans. predeterminada - Devoluciones** y **Método de transporte predeterminado**, establezca un valor predeterminado para cada uno.
4. En la ficha desplegable **Pagos**, elija la opción en el campo **Tipo socio Intrastat** para especificar si el proveedor es una persona o una empresa en los informes de Intrastat.

#### Configurar clientes para Intrastat

Antes de que pueda incluir un cliente en los informes de Intrastat, introduzca su información en la página **Ficha cliente**. Por ejemplo, debe especificar un valor para **Código de país/región** y otro para **CIF/NIF**.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego seleccione el vínculo relacionado.
2. Seleccione el cliente que quiere configurar.
3. En la ficha desplegable **Intrastat**, en los campos **Tipo de trans. predeterminada**, **Tipo de trans. predeterminada - Devoluciones** y **Método de transporte predeterminado**, establezca un valor predeterminado para cada uno.
4. En la ficha desplegable **Pagos**, elija la opción en el campo **Tipo socio Intrastat** para especificar si el proveedor es una persona o una empresa en los informes de Intrastat.

#### Excluir artículos y activos fijos de los informes de Intrastat

Si hay un motivo para excluir un artículo o activo fijo específico de los informes de Intrastat, cambie la opción en su tarjeta.

##### Excluir un artículo de un informe Intrastat

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego seleccione el vínculo relacionado.
2. Seleccione el elemento que desea configurar y, a continuación, en la página **Coste y publicación**, seleccione la casilla **Excluir del informe Intrastat**.

##### Excluir activos fijos de los informes de Intrastat

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego seleccione el vínculo relacionado.
2. Seleccione el activo fijo que desee configurar.
3. En la ficha desplegable **Intrastat**, seleccione la casilla **Excluir del informe de Intrastat**.

#### Configurar códigos arancelarios

1. Seleccione el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Códigos arancelarios** y, a continuación, elija el vínculo relacionado.  
2. En la página **Códigos arancelarios**, introduzca información en los campos tal como se describe en la tabla siguiente.

    | Campo | Descripción |  
    |-------|-------------|
    | **Nº** | Especifica el código arancelario. |
    | **Descripción** | Especifica una descripción para el código arancelario relacionado. |
    | **Unidades suplementarias** | Especifica si las autoridades aduaneras y fiscales requieren información sobre la cantidad y la unidad de medida de este producto. |
    | **Factor de conversión** | Especifica el factor de conversión para el código arancelario. |
    | **Unidad de medida** | Especifica la unidad de medida del código arancelario. |

> [!NOTE]
> Si agrega una unidad de medida adicional, [!INCLUDE [prod_short](includes/prod_short.md)] le pregunta si desea actualizar los elementos relacionados. Si elige actualizar los elementos relacionados, se actualiza el valor de **Unidad de medida** en la página **Unidades de medida del elemento** para todos los elementos que tienen el mismo código arancelario.
> 
> Cuando agrega un código arancelario que tiene un valor definido de **Unidad de medida** al elemento, [!INCLUDE [prod_short](includes/prod_short.md)] agrega automáticamente una nueva unidad de medida al valor del elemento **Unidades de medida del elemento**. El valor **Cant. por unidad de medida** se basa en el campo **Precisión de redondeo de cantidad**.

## Introducir configuraciones de Intrastat específicas de países

Los requisitos de Intrastat son similares en todos los estados miembros de la UE, aunque hay excepciones importantes. En teoría, las reglas deberían aplicarse de manera uniforme en todos los estados miembros. Sin embargo, existen diferencias en las implementaciones porque algunos estados miembros brindan pautas sobre cómo aplicar los principios generales del reglamento en situaciones específicas (por ejemplo, muestras comerciales, devolución de bienes, etc.). Estas pautas pueden producir resultados diferentes para diversas situaciones. Por lo tanto, la información que los países deben introducir puede diferir, al igual que el formato de archivo que deben usar para informar.

### Austria

Los informes de Intrastat en Austria requieren dos archivos diferentes para recibos y envíos. Para comprobar que su configuración es correcta, siga estos pasos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de Intrastat** y luego seleccione el vínculo relacionado.  
2. En la ficha desplegable **Informes**, compruebe si se ha seleccionado **Dividir archivos recepción/envíos**. Si es así, encontrará dos valores de **Código def. intercambio datos** configurados. 
3. Compruebe que el campo **Archivo zip (-s)** está seleccionado para garantizar que los archivos de informe se agregarán al archivo comprimido.

El proceso de trabajo con informes Intrastat es el mismo que el de la característica global.

<!-- ### Belgium-->

### República Checa

La nueva experiencia del informe Intrastat para la República Checa estará disponible en el primer lanzamiento de versiones de 2023. Mientras tanto, siga utilizando la característica **Diario de Instrastat**.

### Finlandia

En Finlandia, hay algunos pasos adicionales para configurar Intrastat. Los informes de Intrastat en Finlandia requieren dos archivos diferentes para recibos y envíos. También verá que hay dos valores de **Código def. intercambio datos** separados configurados.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de Intrastat** y luego seleccione el vínculo relacionado.  
2. En la página **Configuración de informe Intrastat**, en la ficha desplegable **Configuración del archivo**, introduzca información en los campos como se describe en la siguiente tabla.

    |                 Campo              |            Descripción                |  
    |------------------------------------|---------------------------------------|
    | **Código personalizado** | Especifica un código personalizado para la información de configuración del archivo Intrastat. |
    | **Número de serie de la compañía** | Especifica un número de serie de la compañía para la información de configuración del archivo Intrastat. |

3. En la ficha desplegable **Informes**, compruebe si se ha seleccionado **Dividir archivos recepción/envíos**.

El proceso de trabajo con informes Intrastat es el mismo que el de la característica global.

<!-- ### Germany-->

### Italia

Una nueva experiencia de informes Intrastat para Italia estará disponible a partir de febrero de 2023. Mientras tanto, siga utilizando la característica **Diario de Instrastat**.

<!-- ### France-->

### Suecia

Los informes de Intrastat en Suecia requieren dos archivos diferentes para recibos y envíos. Para comprobar que su configuración es correcta, siga estos pasos.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de informes de Intrastat** y luego seleccione el vínculo relacionado.  
2. En la ficha desplegable **Informes**, compruebe que se ha seleccionado **Dividir archivos recepción/envíos**. Si es así, encontrará dos valores de **Código def. intercambio datos** configurados.

El proceso de trabajo con informes Intrastat es el mismo que el de la característica global.

<!-- ### United Kingdom-->

## Consulte la formación relacionada en [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Consulte también .

[Informes de Intrastat en Business Central](finance-how-report-intrastat.md)  
[Gestión financiera](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
