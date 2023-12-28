---
title: Procesar oportunidades de ventas en ciclos de ventas
description: Este tema describe las diferentes formas en que puede procesar oportunidades de ventas en ciclos de ventas y mover una oportunidad a través de las etapas de un ciclo de ventas.
author: jswymer
ms.author: jswymer
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'relationship, prospect'
ms.date: 12/28/2023
ms.custom: bap-template
---
# <a name="process-sales-opportunities"></a>Procesar oportunidades de ventas

Después de crear una oportunidad, existen numerosas funciones para gestionarla y avanzar hasta completarla.

## <a name="view-opportunities"></a>Ver oportunidades

Las oportunidades de venta existentes están disponibles en la página **Lista oportunidades**. La siguiente tabla describe formas de acceder a la página para procesar oportunidades de ventas.

| Para ver las oportunidades | Entonces |
| --- | --- |
| Todos los vendedores y contactos |Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Lista oportunidades** y luego elija el enlace relacionado. |
| Un vendedor específico |Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Vendedores** y luego elija el enlace relacionado. Seleccione el vendedor, seleccione la acción **Oportunidades** y, a continuación, seleccione la acción **Lista**. |
| Un contacto específico |Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Contactos** y luego elija el enlace relacionado. Seleccione el contacto de la lista y, a continuación, seleccione la acción **Oportunidades**. |

Todas estas tareas abren la página **Lista oportunidades**.

## <a name="close-opportunities"></a>Para cerrar oportunidades

Puede cerrar oportunidades cuando terminen las negociaciones. Al cerrar una oportunidad, puede especificar tanto si las ha ganado como si las ha perdido y también las razones de su cierre. Para especificar una razón, debe configurar los cód. oportunidades cerradas.

1. En la página **Lista oportunidad**, seleccione la oportunidad y, a continuación, seleccione la acción **Cerrar**. Se abre la página **Cerrar oportunidad**.
2. Rellene los campos relevantes y, a continuación, haga clic en el botón **Aceptar**.

   Los campos **Cód. cierre oportunidad** y **Fecha cerrada** son obligatorios y deben rellenarse antes de hacer clic en **Aceptar**.

   En el campo **Cód. cierre oportunidad**, puede seleccionar entre uno de los códigos cierre oportunidad existentes o agregar uno nuevo. Para agregar un nuevo código, seleccione **Seleccionar de la lista completa** de la lista desplegable y, a continuación, seleccione **Nuevo**. En la nueva línea en blanco, rellene los campos **Código**, **Tipo** y **Descripción** y, a continuación, haga clic en **Aceptar**.

## <a name="create-quotes-for-opportunities"></a>Crear ofertas para oportunidades

> [!NOTE]
> Solo puede crear ofertas de venta a partir de oportunidades en las que el tipo de contacto sea Empresa.

1. En la página **Lista oportunidad**, seleccione la oportunidad y, a continuación, seleccione la acción **Asignar oferta ventas**. Se abre la página **Oferta de ventas**.
2. Rellene los campos pertinentes.

## <a name="create-sales-orders-for-opportunities"></a>Crear pedidos de venta para oportunidades

Puede hacer pedidos ventas desde las ofertas ventas creadas para las oportunidades. Antes de poder crear pedidos de ventas para sus contactos, debe crear el contacto como cliente. Para obtener más información, consulte [Crear contactos](marketing-create-contact-companies.md).

1. En la página **Lista oportunidad**, busque la oportunidad para la que creó la oferta de venta.
2. Seleccione la acción **Asignar oferta ventas**. Aparece la página **Oferta ventas** para mostrar la oferta de ventas asignada a la oportunidad.
3. Rellene los campos adicionales y, a continuación, seleccione la acción **Convertir en pedido**.

Al manejar oportunidades de ventas puede ser necesario crear una oferta para el contacto con el que se relaciona la oportunidad.

## <a name="delete-opportunities"></a>Eliminar oportunidades

Puede borrar oportunidades, por ejemplo, después de terminar un acuerdo. Sin embargo, solo puede borrar las oportunidades cerradas. Hay dos formas de borrar oportunidades cerradas. Puede eliminar oportunidades cerradas individuales de la página **Lista oportunidad** o puede ejecutar el proceso **Eliminar oportunidades** para eliminar múltiples oportunidades basándose en los criterios especificados.

Para eliminar oportunidades cerradas de la página **Lista oportunidad**, seleccione la oportunidad y, a continuación, seleccione la acción **Eliminar**.

Para borrar oportunidades cerradas usando el proceso **Eliminar oportunidades** siga estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") Elija el icono , escriba **Administración de datos** y luego elija el vínculo relacionado.
2. Elija la acción **Eliminar oportunidades** y después establezca los filtros que especifican las oportunidades que se tienen que eliminar.
3. Elija el botón **Aceptar**.

Después de eliminar una oportunidad, se elimina de la página **Lista oportunidad**.

## <a name="move-an-opportunity-through-sales-cycle-stages"></a>Mueva una oportunidad a varias etapas del ciclo de ventas

Si una oportunidad sigue un ciclo de ventas, podrá moverlo a una etapa anterior o previa, e incluso saltarla.

1. En la página **Lista oportunidades**, seleccione la acción **Actualizar**. Aparecerá el asistente **Actualizar oportunidad**,
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
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
