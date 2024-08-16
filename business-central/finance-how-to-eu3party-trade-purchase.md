---
title: Transacciones de compra de la UE a terceros
description: Este artículo explica cómo configurar y utilizar transacciones de compra de terceros de la Unión Europea (UE).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/05/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="eu-third-party-purchase-transactions"></a>Transacciones de compra de la UE a terceros

El comercio con terceros de la Unión Europea (UE) ocurre cuando recibe una factura de compra de un cliente en un país/región de la UE y los productos se envían a un país/región de la UE diferente sin ingresar al país de residencia. El monto de la transacción puede identificarse y declararse por separado para cumplir con los requisitos del sistema de intercambio de información sobre el IVA (VIES) y de declaración del impuesto sobre el valor añadido (IVA) de algunos países/regiones de la UE. Microsoft Dynamics 365 Business Central permite que las transacciones de compra se configuren como comercio de terceros de la UE. Las transacciones de terceros de la UE publicadas pueden filtrarse en las declaraciones de IVA y excluirse del monto en la columna **Ventas a clientes** de la **Declaración de IVA-VIES Informe de autorización fiscal**.

Incluso si la función está preinstalada como una extensión, no está activada de forma predeterminada. Para activar la característica, siga estos paso.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono , vaya al espacio de trabajo **Administración de características** y luego seleccione el vínculo relacionado.
2. En la lista, encuentre y seleccione **Actualización de característica: reemplazar la funcionalidad de compra de comercio de terceros de la UE con la nueva extensión de compra de comercio de terceros de la UE**.
3. En la columna **Habilitada para**, seleccione **Todos los usuarios**.

> [!NOTE]
> Si usa la localización alemana o italiana, no podrá habilitar esta aplicación porque no es compatible con ciertas funciones de IVA en esas localizaciones.  

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>Habilitar la funcionalidad comercial de terceros de la UE para una compra

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de VAT** y luego seleccione el enlace relacionado.
2. En la página **Configuración de IVA**, marque el campo **Habilitar compra de terceros de la UE**.

## <a name="use-eu-third-party-trade-functionality"></a>Utilizar la funcionalidad comercial con terceros de la UE

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono , escriba **Facturas de compra** (o cualquier documento de compra) y, a continuación, seleccione el vínculo relacionado.
2. Seleccione una factura de compra existente o seleccione **Nueva** para crear una nueva.
3. En la ficha desplegable **Detalles de la factura**, seleccione la casilla de verificación **Comercio entre terceros de la UE**.
4. Seleccione **Aceptar**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Incluir o excluir registros comerciales de terceros de la UE en la declaración de IVA

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Declaración de IVA** y luego seleccione el enlace relacionado.
2. En la página **Declaración de IVA**, seleccione una de las siguientes opciones para mostrar los registros comerciales de terceros de la UE mediante el campo **Filtro comercial de terceros de la UE**.

    | Opción | Descripción |
    |--------|-------------|
    | Todo | Mostrar todos los registros, independientemente de si se marcó el campo **Comercio entre terceros de la UE** en los documentos. |
    | UE3 | Mostrar solo los registros en los que se marcó el campo **Comercio entre terceros de la UE** en los documentos. |
    | No UE3 | Mostrar solo los registros en los que no se marcó el campo **Comercio entre terceros de la UE** en los documentos. |


## <a name="see-also"></a>Consulte también .
[Gestión financiera](finance.md)  
[Trabajar con Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
