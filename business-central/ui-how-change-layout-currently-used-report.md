---
title: Cambiar el aspecto de un informe seleccionando otro diseño
description: Puede utilizar diseños distintos para un informe y cambiar de un diseño a otro para cambiar el aspecto de un informe.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
---
# <a name="legacy-set-the-layout-used-by-a-report"></a><a name="legacy-set-the-layout-used-by-a-report"></a><a name="legacy-set-the-layout-used-by-a-report"></a>(Versión heredada) Establecer el diseño utilizado por un informe

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Un informe se puede configurar con varios diseños de informe, entre los que puede cambiar según sea necesario.

Según los diseños disponibles para un informe, puede optar por usar un diseño de informe de RDLC integrado, un diseño de informe de Word integrado o un diseño personalizado. Para obtener más información acerca de los diseños de informe de RDLC y de Word, diseños personalizados e integrados y otros temas, consulte [Gestionar diseños de informe](ui-manage-report-layouts.md).

Cuando se definen diseños de informes personalizados, puede seleccionarlos de las tarjetas de clientes y proveedores para especificar que los diseños seleccionados se utilizarán para los documentos que cree para el cliente o el proveedor en cuestión. Para obtener más información, vea [Definir diseños de documentos para clientes y proveedores](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Los informes de documento (no listas) que utilizan un diseño de informe de Word suelen ser más rápidos que los que utilizan un diseño de informe RDLC. Por lo tanto, si tiene la opción de elegir entre un diseño de informe Word o RDLC para un informe de documento, utilice el diseño de informe Word para obtener el mejor rendimiento.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a><a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a><a name="to-change-which-report-layout-to-use-for-a-report-or-document"></a>Para cambiar qué diseño de informe se usará para un informe o documento

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selección de diseño de informes** y luego elija el enlace relacionado.
  
   La página **Selección de diseño de informes** muestra todos los informes disponibles en la empresa especificada en el campo **Empresa** en la parte superior de la página. El campo **Descripción de diseño** <!-- **Selected Layout** -->especifica el diseño que se está usando en el informe actualmente.
2. Establezca el campo **Empresa** en la parte superior en la empresa que incluye el informe.

   Este campo le permite establecer diferentes diseños para el mismo informe en diferentes empresas.

3. Para cambiar el diseño que se usa en un informe, en la fila del informe, establezca el campo **Diseño seleccionado** en una de las opciones siguientes:
   * **RDLC (integrado)**, usa el diseño de informe de RDLC integrado en el informe.
   * **Word (integrado)**, usa el diseño de informe de Word integrado en el informe.
   * **Personalizado**, usa un diseño personalizado en el informe.  

> [!NOTE]
> Si elige un diseño de informe de tipo **RDLC (integrado)** o **Word (integrado)** y recibe un mensaje de error en el que se indica que el informe no tiene un diseño del tipo especificado, debe elegir otra opción de diseño o crear un diseño de informe personalizado del tipo que desea usar. Vea el procedimiento siguiente.

Si ha seleccionado un diseño de informe de RDLC o de Word, no se requiere ninguna otra acción y el diseño se utilizará la próxima vez que se ejecute el informe.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a><a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a><a name="to-change-the-custom-layout-to-use-for-a-report-layout"></a>Para cambiar el diseño de informe personalizado para usar un diseño de informe

También es posible que desee cambiar el diseño personalizado utilizado actualmente. Para obtener más información, vea [Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

Todos los diseños de informe personalizados que existen para los diseños de informe en una empresa se enumeran en la página **Diseños de informe personalizados**. En la página **Selección de diseño de informes** puede ver qué diseños personalizados estarán disponibles para cada informe en el cuadro informativo **Diseños personalizados**.

1. En la página **Selección de diseño de informes**, en la línea del diseño de informe que desea cambiar, elija el botón de búsqueda en el campo **Descripción de diseño personalizado**.
2. En la página **Diseños de informe personalizados**, seleccione la fila del diseño personalizado que desee usar y, después, seleccione el botón **Aceptar**.

El nombre del diseño personalizado seleccionado ahora se muestra en el campo **Descripción de diseño personalizado** y se usará la próxima vez que se obtenga una vista previa, imprima o envíe el informe o documento.

Ahora puede ir a sus fichas de cliente y proveedor para especificar cuál de los diseños se usará para diferentes documentos que cree para el cliente o proveedor en cuestión, como confirmaciones de pedido o recordatorios de pagos. Para obtener más información, vea [Definir diseños de documentos para clientes y proveedores](ui-define-customer-vendor-document-layouts.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/change-documents-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
