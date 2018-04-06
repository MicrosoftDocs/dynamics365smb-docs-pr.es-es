---
title: Procesar oportunidades de ventas en ciclos de ventas | Documentos de Microsoft
description: "Puede ver, cerrar o eliminar oportunidades de ventas, y también puede crear ofertas y pedidos de venta para oportunidades, y mover una oportunidad por las etapas de un ciclo de ventas."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 61c40317e2c45d2978118a7a6459c6a1b04ddd8f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="process-sales-opportunities"></a>Procesar oportunidades de ventas
Después de crear una oportunidad, existen numerosas funciones para gestionarla y avanzar hasta completarla.

## <a name="to-view-opportunities"></a>Para ver oportunidades
Las oportunidades de venta existentes están disponibles en la ventana **Lista oportunidades**. Existen varias formas de acceder a esta ventana para procesar las oportunidades de ventas:

| Para ver las oportunidades | Entonces |
| --- | --- |
| Todos los vendedores y contactos |Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Lista oportunidad** y, a continuación, seleccione el vínculo relacionado. |
| Un vendedor específico |Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Vendedores** y, a continuación, seleccione el vínculo relacionado. Seleccione el vendedor, seleccione la acción **Oportunidades** y, a continuación, seleccione la acción **Lista**. |
| Un contacto específico |Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contactos** y, a continuación, seleccione el vínculo relacionado. Seleccione el contacto de la lista y, a continuación, seleccione la acción **Oportunidades**. |

Todas estas tareas abren la ventana **Lista oportunidades**.

## <a name="to-close-opportunities"></a>Para cerrar oportunidades
Puede cerrar oportunidades cuando terminen las negociaciones. Al cerrar una oportunidad, puede especificar tanto si las ha ganado como si las ha perdido y también las razones de su cierre. Para especificar una razón, debe configurar los cód. oportunidades cerradas.

1. En la ventana **Lista oportunidad**, seleccione la oportunidad y, a continuación, seleccione la acción **Cerrar**. Se abre la ventana **Cerrar oportunidad**.
2. Rellene los campos relevantes y, a continuación, haga clic en el botón **Aceptar**.

   Los campos **Cód. cierre oportunidad** y **Fecha cerrada** son obligatorios y deben rellenarse antes de hacer clic en **Aceptar**.

   En el campo **Cód. cierre oportunidad**, puede seleccionar entre uno de los códigos cierre oportunidad existentes o agregar uno nuevo. Para agregar un nuevo código, seleccione **Seleccionar de la lista completa** de la lista desplegable y, a continuación, seleccione **Nuevo**. En la nueva línea en blanco, rellene los campos **Código**, **Tipo** y **Descripción** y, a continuación, haga clic en **Aceptar**.

## <a name="to-create-quotes-for-opportunities"></a>Para crear ofertas para oportunidades
Puede crear ofertas de venta para los contactos que no están registrados como clientes.

1. En la ventana **Lista oportunidad**, seleccione la oportunidad y, a continuación, seleccione la acción **Asignar oferta ventas**. Se abre la ventana **Oferta de ventas**.
2. Rellene los campos pertinentes.

## <a name="to-create-sales-orders-for-opportunities"></a>Para crear pedidos de venta para oportunidades
Puede hacer pedidos ventas desde las ofertas ventas creadas para las oportunidades. Antes de poder crear pedidos de ventas para sus contactos, debe crear el contacto como cliente. Para obtener más información, consulte [Crear un cliente, proveedor o cuenta bancaria a partir de un contacto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. En la ventana **Lista oportunidad**, busque la oportunidad para la que creó la oferta de venta.
2. Seleccione la acción **Asignar oferta ventas**. Aparece la ventana **Oferta ventas** para mostrar la oferta de ventas asignada a la oportunidad.
3. Rellene los campos adicionales y, a continuación, seleccione la acción **Convertir en pedido**.

Al manejar oportunidades de ventas puede ser necesario crear una oferta para el contacto con el que se relaciona la oportunidad.

## <a name="to-delete-opportunities"></a>Para eliminar oportunidades
Puede borrar oportunidades, por ejemplo, después de terminar un acuerdo. Sin embargo, solo puede borrar las oportunidades cerradas. Hay dos formas de borrar oportunidades cerradas. Puede eliminar oportunidades cerradas individuales de la ventana **Lista oportunidad** o puede ejecutar el proceso **Eliminar oport. cerradas** para eliminar múltiples oportunidades basándose en los criterios especificados.

Para eliminar oportunidades cerradas de la ventana **Lista oportunidad**, seleccione la oportunidad y, a continuación, seleccione la acción **Eliminar**.

Para borrar oportunidades cerradas usando el proceso **Eliminar oport. cerradas** siga estos pasos:

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar oportunidades** y, a continuación, seleccione el vínculo relacionado.
2. En la sección **Oportunidad** configure los filtros que especifican las oportunidades que se tienen que eliminar.
3. Elija el botón **Aceptar**.

Después de borrar una oportunidad, se elimina de la ventana **Lista oportunidad**.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Para mover una oportunidad a varias etapas del ciclo de ventas
Si una oportunidad sigue un ciclo de ventas, podrá moverlo hacia adelante o hacia atrás en las diferentes etapas, por ejemplo ir a una etapa anterior o previa, e incluso saltarla.

1. En la ventana **Lista oportunidades**, seleccione la acción **Actualizar**. Aparecerá el asistente **Actualizar oportunidad**,
2. Use el campo **Tipo acción** para mover la oportunidad a través de las etapas del ciclo de ventas:
   * **Siguiente** mueve la oportunidad una etapa adelante.
   * **Omitir** mueve la oportunidad hacia adelante una o varias etapas del ciclo de ventas, que usted especifica en el campo **Presentación**. Puede omitir solo las etapas que se han configurado como permitidas.
   * **Anterior** mueve la oportunidad una etapa hacia atrás.
   * **Saltar** mueve la oportunidad hacia atrás una o varias etapas del ciclo de ventas, que usted especifica en el campo **Presentación**.
   * **Actualizar** le permite cambiar la información (por ejemplo modificar la evaluación de las posibilidades de éxito y valores estimados) sin moverse a otra etapa.
3. Rellene los otros campos requeridos y, a continuación, haga clic en el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Creación y administración de contactos](marketing-contacts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

