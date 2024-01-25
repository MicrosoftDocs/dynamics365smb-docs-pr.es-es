---
title: Exportación de archivo de auditoría
description: 'Este artículo explica cómo configurar diferentes formatos de exportación y luego usarlos, según los requisitos del auditor o de la autoridad.'
author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# <a name="audit-file-export"></a>Exportación de archivo de auditoría

La exportación de información contable del sistema es una solicitud común de algunas autoridades locales o auditores. Las exportaciones de formatos y la información requerida pueden diferir. Los asientos para la exportación suelen ser asientos del libro mayor (G/L) o asientos del impuesto al valor agregado (IVA). Sin embargo, a veces se requiere otra información.

**Exportación de archivos de auditoría** es una extensión preinstalada que le permite exportar diferentes entradas, según los requisitos del auditor o de la autoridad. Independientemente del tipo de formato o las entradas, puede usar la funcionalidad de la extensión para controlar el proceso de exportación de datos. La funcionalidad no tiene un formato de archivo preinstalado para la exportación. Por lo tanto, debe instalar una aplicación que tenga un formato específico (por ejemplo, SIE, SAF-T o FAC) o desarrollar una propia.

> [!NOTE]
> Actualmente, puede seleccionar el formato SIE (Suecia), FEC (Francia) o SAF-T como una aplicación adicional. Los socios también pueden desarrollar un formato personalizado. El número de formatos disponibles aumentará con el tiempo.

## <a name="set-up-audit-file-export"></a>Configurar la exportación de archivos de auditoría

1. Seleccione el botón de búsqueda ![Botón de lupa que abre la función Tell Me.](media/ui-search/search_small.png "Dígame qué desea hacer"), ingrese **Configuración de exportación de archivo de auditoría** y luego seleccione el enlace relacionado.
2. En la página **Configuración de exportación de archivo de auditoría**, siga estos pasos:

    1. En la ficha desplegable **General**, en el campo **Código de formato de exportación de archivo de auditoría** , especifique el código para el archivo de auditoría predeterminado formato de exportación. Solo están disponibles los formatos que se habilitaron cuando se instaló un formato de archivo específico desde la administración de funciones y los que se agregaron como un formato personalizado.
    2. En la ficha desplegable **Calidad de datos**, seleccione la casilla de verificación **Comprobar información de la empresa** para recibir notificaciones sobre los campos de información de la empresa que no No se ha configurado correctamente.
    3. Seleccione la casilla **Comprobar cliente** para recibir notificaciones sobre los campos que no se han configurado correctamente para clientes concretos.
    4. Seleccione la casilla **Comprobar proveedor** para recibir notificaciones sobre los campos que no se han configurado correctamente para proveedores concretos.
    5. Seleccione la casilla **Comprobar cuenta bancaria** para recibir notificaciones sobre los campos que no se han configurado correctamente para cuentas bancarias concretas.
    6. Seleccione la casilla de verificación **Comprobar código postal** para recibir notificaciones sobre un código postal que no se ha configurado correctamente.
    7. Seleccione la casilla de verificación **Comprobar dirección** para recibir una notificación cuando una dirección no se haya configurado correctamente.
    8. En el campo **Código postal predeterminado**, ingrese el código postal a usar si no se especifica ningún código postal en la tarjeta del cliente o proveedor.

3. Seleccione el botón de búsqueda ![Botón de lupa que abre la función Tell Me.](media/ui-search/search_small.png "Dígame qué desea hacer"), ingrese **Configuración de formato de exportación de archivo de auditoría** y luego seleccione el enlace relacionado.
4. En la página **Configuración de formato de exportación de archivo de auditoría**, siga estos pasos:

    1. Seleccione el formato de exportación del archivo de auditoría que desea configurar. Solo están disponibles los formatos que se habilitaron cuando se instaló un formato de archivo específico desde la administración de funciones y los que se agregaron como un formato personalizado.
    2. En el campo **Nombre del archivo de auditoría**, especifique el nombre de archivo predeterminado o la plantilla de nombre de archivo para el archivo de auditoría que desea exportar.
    3. Seleccione la casilla de verificación **Archivar en Zip** para comprimir automáticamente los archivos exportados.

## <a name="provide-the-gl-account-mapping-for-audit-file-export"></a>Proporcione la asignación de cuentas de mayor para la exportación de archivos de auditoría

La mayoría de los formatos requeridos por las autoridades para las cuentas de mayor requieren un plan de cuentas estándar específico. Por lo tanto, después de configurar sus cuentas de mayor, su archivo exportado se basará en las asignaciones. Puede utilizar más asignaciones en su sistema.

Siga estos pasos para proporcinoar la asignación de cuentas de mayor para la exportación de archivos de auditoría.

1. Seleccione el botón de búsqueda ![Botón de lupa que abre la función Tell Me.](media/ui-search/search_small.png "Dígame qué desea hacer"), ingrese **Asignación de contabilidad general** y luego seleccione el enlace relacionado.
2. En la página **Asignación de L/M** , seleccione **Nuevo** para crear una asignación.
3. En el campo **Código**, especifica el código de asignación que representa el periodo de informe.
4. En el campo **Tipo de cuenta estándar**, seleccione el tipo de cuentas de mayor estándar.
5. En el campo **Formato de exportación del archivo de auditoría**, especifique el formato de exportación del archivo de auditoría al que están vinculadas las cuentas de mayor estándar.
6. En el campo **Tipo de período**, el sistema especifica un período contable o un tipo de período personalizado que tiene una fecha y hora de inicio flexibles, según su selección. Si selecciona un período contable específico, el campo se establecerá en **Período contable**. De lo contrario, se establecerá en **Rango de datos**.
7. En el campo **Período contable**, especifique la fecha de inicio del período contable que se utilizará como período de informe, si desea que sean iguales.
8. Si configura el campo **Período contable**, los campos **Fecha de inicio** y **Fecha de finalización** se configuran automáticamente, en función del período que haya especificado. De lo contrario, puede establecer manualmente las fechas de inicio y finalización de sus informes.
9. Si ya agregó un plan de cuentas estándar, siga estos pasos:

    1. En el campo **N.º categoría cuenta estándar**, especifica la categoría del código de cuenta o agrupación estándar que se usa para la asignación.
    2. En el campo **N.º de cuenta estándar**, especifica la categoría del código de cuenta o agrupación estándar que se usa para la asignación.

10. Selecciona la casilla **Incluir saldo entrante** para considerar el saldo entrante de la cuenta de mayor del tipo **Balance de cuenta** para el mapeo en lugar del cambio neto del período de informe.
11. Para iniciar la asignación, siga estos pasos:

    1. Para generar líneas en la página **Asignación de cuentas de mayor**, en función de un catálogo de cuentas existente, seleccione **Inicializar fuente para mapeo**. Para copiar la asignación de cuenta de mayor de algún otro código de asignación, seleccione **Copiar desde otra asignación**. Cuando haya terminado de crear líneas, todas las cuentas de mayor que hayan registrado asientos se marcarán en verde.
    2. Para marcar solo las cuentas de mayor que tienen entradas, seleccione **Actualizar disponibilidad de entrada de L/M**. Si **Incluir saldo entrante** está activado, todas las entradas del L/M contabilizadas se tienen en cuenta para el cálculo. De lo contrario, solo se consideran las entradas del L/M del período de informe.

## <a name="export-the-audit-file"></a>Exportar el archivo auditoría

1. Seleccione el botón de búsqueda ![Botón de lupa que abre la función Tell Me.](media/ui-search/search_small.png "Dígame qué desea hacer"), ingrese **Documentos de exportación de archivo de auditoría** y luego seleccione el enlace relacionado.
2. Sobre la página **Documentos de exportación de archivos de auditoría**, seleccione **Nuevo**.
3. Sobre la pestaña desplegable **General**, siga estos pasos:

    1. En el campo **Formato de exportación de archivos de auditoría**, seleccione el formato que se utiliza para exportar el archivo de auditoría.
    2. En **Código de asignación de cuenta de mayor**, seleccione el código de asignación de cuenta de mayor para el período de informe.
    3. Selecciona la casilla **Dividir por mes** si se deben generar múltiples archivos de auditoría por mes.
    4. Selecciona la casilla **Dividir por fecha** si se deben generar múltiples archivos de auditoría por día.
    5. En el campo **Comentario de encabezado**, ingrese el comentario para incluir en el encabezado del archivo de auditoría.
    6. En el campo **Contacto**, especifica el contacto que se exporta al encabezado del archivo de auditoría
    7. Selecciona la casilla **Crear varios archivos zip** para generar múltiples archivos zip.

        > [!IMPORTANT]
        > Seleccione esta casilla de verificación solo si instaló previamente algunas de las aplicaciones de formato o creó una personalizada. La instalación de uno o más de los formatos específicos probablemente agregará campos y funciones a la funcionalidad de **Exportación de archivos de auditoría**, en función de los requisitos de formato.

4. Sobre la pestaña desplegable **Procesamiento**, siga estos pasos:

    1. Selecciona casilla **Procesamiento en paralelo** si desea que la generación de archivos de auditoría sea procesada por trabajos paralelos en segundo plano. Desactive la casilla de verificación para exportar datos en su sesión actual.
    2. Si seleccionó la casilla de verificación **Procesamiento paralelo**, en el campo **Número máximo de trabajos**, especifique el número máximo de trabajos en segundo plano que se pueden ejecutar al mismo tiempo.
    3. En el campo **Fecha/hora de inicio más temprano**, especifique la fecha y hora más tempranas en que se debe ejecutar el trabajo en segundo plano. Si ejecuta el proceso seleccionando **Iniciar**, puede realizar un seguimiento del estado en las fichas desplegables **Procesando** y **Líneas**.

5. Cuando haya terminado, seleccione **Descargar como archivo** para descargar el archivo de auditoría de la línea seleccionada.

> [!IMPORTANT]
> Si tiene varias entradas para exportar, no le recomendamos que las exporte en la sesión actual, debido a posibles problemas de rendimiento. En su lugar, le recomendamos que utilice el procesamiento paralelo durante los días o las horas no laborables.

## <a name="see-also"></a>Consulte también .
[Gestión financiera](finance.md)  
[Descripción de contabilidad y plan de cuentas](finance-general-ledger.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Trabajar con Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
