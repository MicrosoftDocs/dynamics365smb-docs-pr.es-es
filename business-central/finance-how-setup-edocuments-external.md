---
title: Configurar el conector de documentos electrónicos con puntos finales externos
description: Este artículo explica cómo configurar la funcionalidad de documentos electrónicos cuando está conectada a puntos finales externos.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, access-point, endpoint'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 12/13/2023
ms.author: altotovi
---

# <a name="set-the-e-documents-connector-with-external-endpoints"></a>Configurar el conector de documentos electrónicos con puntos finales externos

Este artículo explica cómo configurar la funcionalidad de documentos electrónicos cuando está conectada a puntos finales externos.

Antes de utilizar la funcionalidad que se describe en este artículo, instale la aplicación **E-Documents Connector con puntos finales externos** en la parte superior de la aplicación **E- Aplicación Document Core**. Esta aplicación se puede utilizar para la integración predeterminada con puntos de acceso externos (de terceros) para automatizar el flujo de documentos electrónicos. Debido a que esta aplicación representa solo algunos de los conectores seleccionados, no está limitado a las integraciones existentes en ella. La mayoría de los conectores estarán disponibles en AppSource en el futuro.

## <a name="set-up-the-connection"></a>Configurar la conexión

Para comenzar la configuración, siga los pasos en [Aplicación principal de documentos electrónicos](finance-how-setup-edocuments.md). Después de completar esos pasos, regrese a este artículo y complete los siguientes pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios de documentos electrónicos** y luego seleccione el enlace relacionado.
2. En el campo **Integración de servicios**, seleccione uno de los códigos de integración que se ofrecen para la configuración del servicio de terminal.
3. Seleccione **Configurar integración de servicio**.
4. En la página **Configuración de conexión externa de documento electrónico**, seleccione **Solicitar código de autorización**. Se le redirigirá a la página web de autorización de servicios externos y se le solicitarán sus datos de inicio de sesión.
5. Copie el código de autorización en el campo **Ingresar código de autorización**.
6. Seleccione **Actualizar token de acceso** para asegurarse de que puede actualizar el token.

    > [!NOTE]
    > Esta conexión requiere comunicación con proveedores de servicios externos que podrían estar sujetos a pagos adicionales y requerir contratos con ellos. Para obtener todas las credenciales necesarias, contacte con los proveedores de servicios.

7. En la página **Configuración de conexión externa de documento electrónico**, complete los siguientes campos:

    | Nombre del campo | Descripción |
    |---|---|
    | URL FileAPI | Especifique la dirección URL de la API del archivo. |
    | URL partes archivo | Especifique la dirección URL de partes de archivo. |
    | URL de DocumentAPI | Especifique la dirección URL de la API del documento. |
    | Id. de empresa | Especifique el id. de empresa. |
    | Modo de envío | Especifique el modo de envío. Puede seleccionar **Producción**, **Prueba** o **Certificación**. |

    > [!NOTE]
    > Solicite a su proveedor de servicios todos los detalles anteriores para establecer una conexión con su punto de acceso.

## <a name="set-up-company-information"></a>Configurar la información de la empresa

Antes de comenzar a utilizar documentos electrónicos, actualice su página **Información de la empresa** realizando los siguientes pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información empresa** y luego seleccione el enlace relacionado.
2. Además de rellenar los campos habituales, también debe rellenar los campos siguientes:

    | Nombre del campo | Descripción |
    |---|---|
    | Código SWIFT | Especifique el código SWIFT (código de identificación bancaria internacional) del banco donde tiene la cuenta principal. |
    | Cód. sucursal banco | Especifique el número de cuatro dígitos de la sucursal del banco. |
    | CIF/NIF  | Especifique el número de registro del IVA de la empresa. |

3. Cierre la página.

## <a name="set-up-customers-to-receive-e-documents"></a>Configurar clientes para recibir documentos electrónicos

Para permitir que los clientes reciban sus documentos electrónicos, complete los siguientes pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego seleccione el vínculo relacionado.
2. Abra la tarjeta **Cliente**.
3. Además de rellenar los campos habituales, en el campo **GLN**, indique el cliente en relación con el envío de documentos electrónicos.
4. Marque el campo **Usar GLN en documentos electrónicos** para indicar si el Número de ubicación global (GLN) se utiliza como número de identificación de parte en documentos electrónicos.
5. Cierre la página.

## <a name="other-setup"></a>Otra configuración

Antes de comenzar a trabajar con documentos electrónicos, configure los **flujos de trabajo** y **perfiles de envío de documentos** para usar sus flujos de trabajo. Una vez establecida la conexión del servicio, puede comenzar a utilizar su solución de documentos electrónicos.

## <a name="available-service-providers"></a>Proveedores de servicios disponibles

Microsoft quiere alentar a los proveedores de puntos de acceso a agregar sus conectores además de nuestra estructura **Núcleo de documentos electrónicos**.

Actualmente, Pagero es el único proveedor de puntos de acceso cubierto por este sistema. Microsoft no tiene ninguna obligación contractual con Pagero. Por lo tanto, debe realizar un contrato con ellos para obtener todas las credenciales necesarias.

Actualizaremos esta lista a medida que obtengamos nuevos proveedores de puntos de acceso de intercambio de documentos electrónicos.

## <a name="see-also"></a>Consulte también

[Cómo configurar documentos electrónicos en Business Central](finance-how-setup-edocuments.md)  
[Cómo usar documentos electrónicos en Business Central](finance-how-use-edocuments.md)  
[Cómo ampliar documentos electrónicos en Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Gestión financiera](finance.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Registrar compras con facturas de compra y pedidos](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
