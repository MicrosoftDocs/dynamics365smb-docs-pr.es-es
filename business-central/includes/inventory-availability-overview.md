---
author: brentholtorf
ms.topic: include
ms.date: 04/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Aumente la eficiencia de su almacén con información precisa y en tiempo real sobre los factores que pueden afectar las cantidades disponibles. Por ejemplo: 

* Niveles de inventario
* Almacenes
* Fases del procesamiento
* Artículos en cuarentena
* Reservas

Puede acceder a información sobre la disponibilidad de artículos desde los siguientes documentos fuente:

* Pedidos de venta
* Órdenes de producción
* Pedidos de ensamblados
* Proyectos

La información también respeta otros factores que afectan la disponibilidad. Por ejemplo, contenedores exclusivos, contenedores bloqueados y artículos que no están disponibles para su recolección. Por ejemplo, los artículos pueden estar reservados o pendientes de almacenamiento o operaciones de envío. La página **Resumen de selección** le permite revisar los elementos que [!INCLUDE [prod_short](prod_short.md)] no ha incluido en la selección de documentos y tomar las acciones necesarias.

> [!NOTE]
> Esta capacidad requiere que active la opción **Almacenamiento y recogida dirigidos** para las ubicaciones que utiliza en su proceso de selección.

### <a name="set-up-previews"></a>Configurar versiones preliminares

Para obtener detalles sobre lo que se selecciona y lo que no, active la opción **Mostrar resumen (almacenamiento y selección dirigidos)** en las páginas de solicitud **Almacén - Origen - Crear Documento** o **Almacén - Envío - Crear Selección**.

### <a name="determine-the-quantity-you-can-pick"></a>Determina la cantidad que puede elegir

En líneas en la página **Crear resumen de selección de almacén**, el campo **Cant. para gestionar (base)** muestra cuáles y cuántos elementos [!INCLUDE [prod_short](prod_short.md)] intentó elegir. El cuadro informativo **Resumen** proporciona más detalles.

Para investigaciones simples, **Cant. seleccionable** podría darle suficiente información. El campo muestra cuántos artículos hay disponibles. Si la cantidad que se puede recoger es menor de lo esperado, explore el contenido del contenedor.

La **Cant. seleccionable** es la cantidad máxima que [!INCLUDE [prod_short](prod_short.md)] puede considerar para recolección. Esta cantidad consta de artículos en contenedores recolectables. La cantidad excluye cantidades que están en ubicaciones bloqueadas o dedicadas, o artículos que se están seleccionando en documentos de selección de almacén. Si el artículo que desea seleccionar requiere seguimiento de artículos, los números de lote o de serie almacenados en contenedores de recolección se excluyen de la cantidad de recolección.

Si la cantidad a recoger difiere de la cantidad en los contenedores a recoger, puede haber un problema. Explore el contenido de la ubicación para encontrar ubicaciones o cantidades bloqueadas en documentos activos.

El campo **Cantidad en almacén** muestra la cantidad total que encontrará en su almacén si realiza un recuento físico. Puede profundizar en los asientos del libro mayor del almacén desde este campo. Si el campo muestra una cantidad menor que la cantidad en **Cantidad en contenedores seleccionables**, hay una desalineación entre las cantidades del almacén y del inventario. En ese caso, utilice la acción **Calcular ajuste de almacén** en la página **Diario de artículos** y luego cree la selección de almacén de nuevo.

La siguiente imagen ilustra la cantidad máxima considerada para recolección.

:::image type="content" source="../media/pickable-qty.png" alt-text="Cantidad máxima considerada para recolección.":::

**Leyenda**

|Letra  |Descripción  |
|---------|---------|
|P     |Contenedores con contenido de tipo Pick         |
|D     |Contenedores con contenido de tipo Pick marcados como ubicaciones dedicadas        |
|A     |Ubicaciones con contenido de tipo Pick en los documentos activos (como otro pick)       |
|H     |Contenedores con contenido de tipo Pick con artículos con seguimiento bloqueado         |
|P     |Contenedores con contenido de tipo Pick con movimiento saliente bloqueado         |
|C     |Otros contenedores         |

### <a name="reservations"></a>Reservas

Si hay reservas para el artículo que se está seleccionando, el cálculo continúa. La idea es que la demanda reservada tiene mayor prioridad que la no reservada, lo que significa que seleccionar la demanda no reservada no debería impedir seleccionar la demanda reservada más adelante.

Para verificar que su cantidad puede cubrir una demanda, compare el valor de **Cant. seleccionable** en el cuadro informativo **Resumen** con el valor en el campo **Cant. a gestionar (Base)** en las líneas.

Puede encontrar reservas en el campo **Cant. total reservada en el Almacén**. Las cantidades reservadas que ya están seleccionadas y listas para su envío, uso o consumo no afectan la disponibilidad. El campo **Cant. reservada. en contenedores de recogida/envío** muestra esta cantidad.

El campo **Cant. disponible excluyendo contenedor de envío** muestra la cantidad que está disponible, excluyendo las cantidades para las cuales se cumple lo siguiente:

* Ya están recogidas para los envíos.
* Están en lotes de artículos bloqueados o números de serie.
* Están en contenedores bloqueados.
* Están en huecos dedicados.

Es posible que estas cantidades estén disponibles, pero es posible que aún no pueda seleccionarlas. Todavía podrían estar en las áreas de recepción, almacenamiento o control de calidad. Puede moverlos al área de selección procesando una hoja de trabajo de almacenamiento o movimiento.

La diferencia entre **Cant. disponible excluyendo el contenedor de envío** y la cantidad reservada en el almacén, es la cantidad disponible para recolección sin afectar el stock reservado.

La siguiente imagen ilustra la asignación de cantidad disponible para cantidad reservada.

:::image type="content" source="../media/Warehouse_Reservation_Pick.png" alt-text="Cantidad máxima considerada para picking cuando se trata de reserva.":::

**Leyenda**

|Letra  |Descripción  |
|---------|---------|
|P     |Cantidad para picking         |
|TR    |Cant. reservada total en almacén.         |
|RS    |Las cantidades reservadas que ya están seleccionadas y listas para su envío, uso o consumo       |
|A     |Cant. dispon. sin ubicación envío         |
|P     |Cantidad en contenedores exclusivos o bloqueados, lotes de artículos bloqueados o números de serie         |

Si bien hay suficiente cantidad disponible en el almacén para satisfacer la selección por completo, esto provocará que la cantidad total reservada se asigne a las cantidades en contenedores dedicados o bloqueados, lo que impide la selección para esta demanda. Debido a que la demanda reservada tiene mayor prioridad, [!INCLUDE [prod_short](prod_short.md)] reduce la cantidad a seleccionar para evitar impactos negativos, como la imposibilidad de seleccionar, en la demanda reservada.

### <a name="other-details"></a>Otros detalles

Si los artículos requieren seguimiento de artículos, también puede encontrar la cantidad en lotes bloqueados o números de serie, lo que provoca las siguientes reducciones:

* La cantidad recogible
* Cantidad disponible sin ubicación de envío
* Cantidad reservada en el almacén 

Si selecciona el mismo artículo para múltiples documentos o líneas de origen, lo que también ocurre cuando selecciona números de serie, también se muestra información sobre selecciones para otras líneas porque reduce la cantidad seleccionable.
