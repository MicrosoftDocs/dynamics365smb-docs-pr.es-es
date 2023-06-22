---
title: Validar un CIF/NIF
description: 'Permita que Business Central valide los números de registro de IVA para sus contactos, clientes y proveedores, de acuerdo con el servicio de validación de números de IVA VIES de la UE.'
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: andregu
---

# <a name="validate-vat-registration-numbers" />Validar un CIF/NIF

Es importante que los CIF/NIF que tiene para clientes, proveedores y contactos sean válidos, si utiliza [!INCLUDE [prod_short](includes/prod_short.md)] en un país que utilice IVA. Por ejemplo, las empresas cambian a veces el estado de la deuda tributaria, y en algunos países o regiones las autoridades fiscales podrían solicitar informes, como, por ejemplo, el informe de **lista de venta de CE**, que enumera los CIF/NIF que utiliza cuando realiza operaciones comerciales.

La Comisión Europea proporciona el servicio de validación de número de IVA VIES en su sitio web, que es público y gratuito. [!INCLUDE [prod_short](includes/prod_short.md)] puede ahorrarle un paso y permitirle utilizar el servicio VIES para validar y realizar el seguimiento de los CIF/NIF de clientes, proveedores y contactos y otra información de empresas. El servicio en [!INCLUDE [prod_short](includes/prod_short.md)] se denomina **Servicio Validar CIF/NIF de la UE**. El servicio está disponible en la página **Conexiones de servicio** y puede comenzar a usarlo de inmediato. La conexión al servicio es gratuita y no es necesario registro adicional.

## <a name="configure-the-service-to-verify-vat-registration-numbers-automatically" />Configure el servicio para verificar los CIF/NIF automáticamente

Para habilitar el **Servicio de validación de CIF/NIF de la UE**, abra el movimiento en la página **Conexión de servicio**. Si el campo **Punto final de servicio** aún no está relleno, use la acción **Establecer punto final predeterminado**. Luego configure el campo **Habilitado** y está listo para empezar.  

> [!IMPORTANT]
> Para habilitar el servicio de validación, debe contar con permisos de administrador.

Opcionalmente, configure plantillas para los tipos de datos relacionados con el IVA que desea que el servicio también compruebe. Para obtener más información, consulte la sección [Plantillas de validación](#validation-templates).

Cuando utilice nuestro conexión al servicio, guardamos un historial de números de IVA y de comprobaciones de cada cliente, proveedor o contacto en **Registro de CIF/NIF**, por lo que le será muy fácil seguirlos. El registro es específico de cada cliente. Por ejemplo, el registro es útil para demostrar que ha comprobado que el número de IVA actual es correcto. Cuando comprueba un número de IVA, la columna **Identificador de solicitud** del registro refleja que ha realizado una acción.

Puede ver el registro del registro de IVA en las fichas de cliente, proveedor o contacto, en la ficha desplegable **Facturación**, seleccionando el botón de búsqueda en el campo **CIF/NIF**.  

Hay un par de cosas a recordar sobre el servicio de validación de IVA VIES:

* El servicio utiliza el protocolo HTTP, lo que significa que los datos transferidos a través del servicio no están cifrados.  
* Puede experimentar tiempo de inactividad de este servicio del que Microsoft no es responsable. El servicio forma parte de una amplia red de la UE de registros de IVA nacionales.

> [!IMPORTANT]
> Es su responsabilidad comprobar que los datos sean válidos. En ocasiones, los datos con errores son devueltos por el servicio de Validación de número de IVA VIES. Si la validación falla, valide los números de registro de IVA en el [sitio web](https://ec.europa.eu/taxation_customs/vies/), imprima el resultado o guárdelo en una ubicación compartida y luego agregue el enlace al registro de su cliente, proveedor o contacto. Para obtener información, consulte [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md).

## <a name="validation-templates" />Plantillas de validación

Puede utilizar el servicio VIES para comprobar también otra información de la empresa, como la dirección, además del CIF/NIF. En la página **Plantillas de validación de CIF/NIF**, cree una entrada para cada país para el que desea obtener una validación adicional y luego especifique la información que desea que se valide automáticamente.  

Por ejemplo, agregue una entrada para España donde desea obtener la validación del nombre, la calle, la ciudad y el código postal, y luego otra entrada para Alemania donde solo desea la validación del código postal, por ejemplo. Luego, en la página **Configuración del servicio de validación de CIF/NIF**, especifique la plantilla predeterminada.  

> [!NOTE]
> Asegúrese siempre de que la plantilla predeterminada funcione para sus necesidades. Puede cambiar el valor predeterminado para que coincida con sus requisitos, como obtener validación para todos los campos o para ningún campo.

La próxima vez que especifique un CIF/NIF, el servicio validará el número y cualquier dato adicional, según lo determinen sus plantillas de validación. Si los valores especificados son diferentes de los valores devueltos por el servicio, verá los detalles en la página **Detalles de validación**, donde puede aceptar o restablecer los valores.  

## <a name="see-also" />Consulte también

[Configurar el impuesto sobre el valor añadido](finance-setup-vat.md)  
[Configuración del impuesto sobre el valor añadido no realizado](finance-setup-unrealized-vat.md)  
[Crear informes de IVA para la autoridad fiscal](finance-how-report-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  
[Funcionalidad local en Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
