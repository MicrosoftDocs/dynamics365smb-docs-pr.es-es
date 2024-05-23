---
title: Configurar el IVA no deducible
description: Este artículo explica cómo configurar el IVA no deducible en Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# Configurar el IVA no deducible

El impuesto sobre el valor agregado (IVA) no deducible es el IVA que debe pagar un comprador, pero que no es deducible de la propia cuota de IVA del comprador. Las empresas generalmente pueden recuperar el IVA en la compra de bienes y servicios que están relacionados con sus actividades comerciales. Sin embargo, en algunas situaciones, una empresa incurre en un IVA que no es deducible. Estas situaciones suelen estar relacionadas con las reglamentaciones locales y pueden diferir entre países y regiones. Sin embargo, el modelo de utilización del IVA no deducible o parcialmente deducible es similar. Puede usar el IVA proporcional para calcular el IVA cuando hay IVA deducible y no deducible.

En general, el IVA no se puede deducir de algunas compras debido a los siguientes factores:

- **El tipo de bienes o servicios que se compran**: el IVA es total o parcialmente no deducible según la ley sobre bienes como automóviles, teléfonos móviles y alimentos que se compran en restaurantes.
- **IVA prorrateado parcialmente deducible**: el IVA se prorratea de acuerdo con la relación entre las operaciones de venta por las que se debe el IVA y todas las operaciones. El IVA que exceda esta relación no se puede deducir.

Debido a que puede resultar difícil saber dónde y cómo se utiliza un artículo, comuníquese con las autoridades fiscales locales de su país/región. Pueden ayudar a determinar si puede deducir un porcentaje específico del IVA, según datos históricos.

> [!IMPORTANT]
> Esta característica global está disponible en todos los países o regiones con IVA habilitado **excepto Bélgica, Italia y Noruega**. Estas ubicaciones ya tienen una característica local existente y se actualizarán en el futuro. No ejecute esta característica en estos países porque el procedimiento de actualización no existe.

## Usar IVA no deducible

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de VAT** y luego seleccione el enlace relacionado.
2. Seleccione la casilla **Habilitar IVA no deducible**.

    > [!IMPORTANT]
    > Después de habilitar el IVA no deducible, no puede desactivarlo porque la función puede incluir cambios en los datos y puede iniciar una actualización de algunas tablas de la base de datos. Microsoft recomienda enfáticamente que primero habilite y pruebe esta función en el entorno de espacio aislado antes de habilitarla en el entorno de producción.

3. Configure cómo [!INCLUDE [prod_short](includes/prod_short.md)] trata los valores de IVA no deducibles.

    1. En el campo **Usar para coste Prod.**, especifique si el IVA no deducible se debe agregar al coste del artículo cuando compra productos. De lo contrario, el IVA no deducible no influirá en el coste del producto y el importe total se registrará solo en el libro mayor.
    2. Seleccione la casilla **Usar para coste de activo fijo** para agregar el IVA no deducible al coste del activo fijo cuando compra activos fijos nuevos. De lo contrario, el IVA no deducible no influirá en el coste del activo fijo y el importe total se registrará solo en el libro mayor.
    3. Seleccione la casilla **Usar para coste proyecto** para especificar que el IVA no deducible debe agregarse al coste del proyecto cuando compra artículos para el proyecto. De lo contrario, el IVA no deducible no influirá en el coste del proyecto y el importe total se registrará solo en el libro mayor.
    4. Seleccione la casilla **Mostrar IVA no ded. en líneas** para especificar que el IVA no deducible debe mostrarse en las páginas de línea de documento para facilitar la manipulación de los importes del IVA.

## Utilizar el porcentaje de IVA no deducible

1. Seleccione el icono ![Bombilla que abre la característica Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. grupos registro IVA** y luego seleccione el vínculo relacionado.
2. En la página **Config. grupos registro IVA**, establezca los campos tal como se describe en la tabla siguiente.

    | Campo | Descripción |
    |-------|-------------|
    | Permitir IVA no deducible | Especifique si se considera el IVA no deducible para esta combinación concreta del grupo de un registro de negocio de IVA y un grupo de registro de producto de IVA. |
    | % IVA no deducible | Especifique el porcentaje del importe de transacción al que no se aplica el IVA. |
    | Cta. IVA compra no deducible | Especifique la cuenta asociada con el importe de IVA que no se deduce debido al tipo de productos o servicios comprados. |

    > [!NOTE]
    > Para tener movimientos del libro mayor (G/L) que usen la cuenta dedicada en lugar de la cuenta de compras/ventas, puede dejar el campo **Cta. IVA compra no deducible** en blanco o establecer el campo **Cuenta**.

3. Seleccione **Aceptar**.

> [!NOTE]
> No puede utilizar el IVA no realizado junto con el IVA no deducible.
>
> No use el mismo valor **Identificador de IVA** tanto para el IVA normal donde el campo **% IVA no deducible** se establece en **0** (cero) como para el IVA normal donde el campo **% IVA no deducible** se establece en un valor distinto de cero. De lo contrario, el importe total del IVA no deducible se calculará incorrectamente.

## Consulte también

[Gestión financiera](finance.md)  
[Detalles de diseño: IVA no deducible](design-details-nondeductible-vat.md)  
[Usar IVA no deducible](finance-how-use-non-deductible-vat.md)  
[Configurar los cálculos y los métodos de registro del impuesto sobre el valor añadido](finance-setup-vat.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
