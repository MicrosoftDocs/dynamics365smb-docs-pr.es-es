---
title: Validar un CIF/NIF
description: Deje que Business Central utilice el servicio VIES para validar los números de registro de IVA automáticamente.
author: kielkenny
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 80e955e96a64c5a0bd91d0a72297b32d67ff4ab6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750565"
---
# <a name="validate-vat-registration-numbers"></a>Validar un CIF/NIF

Es importante que los números CIF/NIF que tiene para clientes, proveedores y contactos sean válidos. Por ejemplo, las empresas cambian a veces el estado de la deuda tributaria, y en algunos países o regiones las autoridades fiscales podrían solicitar informes, como, por ejemplo, el informe de lista de ventas de CE, que enumera los CIF/NIF que utiliza cuando realiza operaciones comerciales.

La Comisión Europea proporciona el servicio de validación de número de IVA VIES en su sitio web, que es público y gratuito. [!INCLUDE[prod_short](includes/prod_short.md)] puede ahorrarle un paso y permitirle utilizar el servicio VIES para validar y realizar el seguimiento de los números IVA de clientes, proveedores y contactos desde las fichas de cliente, proveedor y contacto. El servicio en [!INCLUDE[prod_short](includes/prod_short.md)] se denomina **Servicio Validar CIF/NIF de la UE**. El servicio está disponible en la página **Conexiones de servicio** y puede comenzar a usarlo de inmediato. La conexión al servicio es gratuita y no es necesario registrarse.

## <a name="to-verify-vat-registration-numbers"></a>Comprobar CIF/NIF

Para habilitar el **servicio Validar CIF/NIF de la UE** abra el movimiento en la página **Conexión de servicio**. El campo **Extremo de servicio** ya debe estar rellenado. Si no, puede usar la acción **Establecer extremo predeterminado**. Luego configure el campo **Habilitado** y está listo para empezar.

> [!NOTE]
> Para activar el CIF/NIF de la UE Servicio de validación, debe contar con permisos de administrador.

Cuando utilice nuestro conexión al servicio, guardamos un historial de números de IVA y de comprobaciones de cada cliente, proveedor o contacto en **Registro de CIF/NIF**, por lo que le será muy fácil seguirlos. El registro es específico de cada cliente. Por ejemplo, el registro es útil para demostrar que ha comprobado que el número de IVA actual es correcto. Cuando comprueba un número de IVA, la columna **Identificador de solicitud** del registro refleja que ha realizado una acción.

Puede ver el registro del registro de IVA en las fichas de cliente, proveedor o contacto, en la ficha desplegable **Facturación**, seleccionando el botón de búsqueda en el campo **CIF/NIF**.  

Nuestro servicio también puede ahorrarle tiempo al crear un cliente o un proveedor. Si conoce el número de IVA del cliente, puede introducirlo en el campo **CIF/NIF** en las fichas de cliente o proveedor, y rellenaremos automáticamente el nombre del cliente. Algunos países o regiones también proporcionan direcciones de empresa en formato estructurado. En esos países o regiones, también completaremos la dirección.  

Hay un par de cosas a recordar sobre el servicio de validación de IVA VIES:

* El servicio utiliza el protocolo HTTP, lo que significa que los datos transferidos a través del servicio no están cifrados.  
* Puede experimentar tiempo de inactividad de este servicio del que Microsoft no es responsable. El servicio forma parte de una amplia red de la UE de registros de IVA nacionales.

> [!IMPORTANT]
> Es su responsabilidad comprobar que los datos sean válidos. En ocasiones, los datos con errores son devueltos por el servicio de Validación de número de IVA VIES. Si la validación falla, valide los números de registro de IVA en el [sitio web](https://ec.europa.eu/taxation_customs/vies/), imprima el resultado o guárdelo en una ubicación compartida y luego agregue el enlace al registro de su cliente, proveedor o contacto. Para obtener información, consulte [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md).

## <a name="see-also"></a>Consulte también

[Configurar el impuesto sobre el valor añadido](finance-setup-vat.md)  
[Configuración del impuesto sobre el valor añadido no realizado](finance-setup-unrealized-vat.md)  
[Crear informes de IVA para la autoridad fiscal](finance-how-report-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Funcionalidad local en Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]