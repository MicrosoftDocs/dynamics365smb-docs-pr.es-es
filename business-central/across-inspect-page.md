---
title: Inspección de páginas en Business Central
description: Utilice la función de inspección de página para ampliar los detalles sobre el diseño de la página y el origen de datos. El inspector de páginas es ideal para solucionar los problemas con sus datos.
ms.topic: conceptual
author: jswymer
ms.author: jswymer
ms.date: 09/15/2023
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="inspecting-pages-in-business-central"></a>Inspección de páginas en Business Central

La función de inspección de páginas le permite obtener detalles sobre una página, lo que le permite conocer el diseño de la página, los diferentes elementos que la componen y el origen de los datos que muestra. La inspección de páginas está especialmente diseñada para administradores, usuarios avanzados, personal de soporte y desarrolladores. Es ideal para aprender el modelo de datos detrás de una página y la resolución de problemas. Por ejemplo, si tiene un problema con una página, puede utilizar la inspección de páginas para obtener información que puede transmitir al administrador del sistema o al personal de soporte.

> [!NOTE]  
> Con el segundo lanzamiento de versiones de 2023 de [!INCLUDE [prod_short](includes/prod_short.md)], a través de la inspección de páginas, puede iniciar Visual Studio Code desde el cliente web para seguir investigando y depurando el código fuente de una extensión. Para obtener más información, consulte [Solucionar problemas en Visual Studio Code directamente desde el cliente web](/dynamics365/business-central/dev-itpro/developer/devenv-troubleshoot-vscode-webclient) en la ayuda para desarrolladores y profesionales de TI de Business Central.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## <a name="work-with-page-inspection"></a>Trabajar con la inspección de páginas

Puede empezar con la inspección de páginas des de la página **Ayuda y soporte técnico**. Elija el signo de interrogación en la esquina superior derecha, elija **Ayuda y soporte técnico** y, a continuación, **Inspeccionar páginas y datos**. O bien simplemente puede utilizar el método abreviado de teclado <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>F1</kbd>.

El panel **Inspección de la página** se abre en el lateral. Cuando el panel se abre por primera vez, muestra información que pertenece al objeto de la página principal.

Utilice el teclado o el dispositivo señalador para mover el enfoque a diferentes elementos de la página. Cuando selecciona un cuadro informativo o una parte de la página principal, el área delimitada se resalta con un borde y el panel **Inspección de la página** muestra información sobre el elemento seleccionado. Por ejemplo, la figura anterior muestra información sobre la parte de la lista en la página **Pedido de venta**. A medida que se desplaza a otras páginas de la aplicación, el panel **Inspección de la página** se actualizará automáticamente con la información de la página a medida que avanza.

Para obtener más información sobre lo que se muestra en la inspección de páginas, consulte [Inspección y resolución de problemas de páginas](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) en la ayuda para desarrolladores e informáticos de Business Central.

Si no ve los detalles que espera ver en el panel **Inspección de la página**, es probable que no tenga los permisos necesarios, como se describe en la siguiente sección.

## <a name="controlling-access-to-page-inspection-details"></a>Control del acceso a los detalles de inspección de páginas

Como administrador, puede controlar el acceso a todos los detalles que se muestran en el panel **Inspección de la página** configurando los permisos que tienen los usuarios. Para conceder a un usuario un permiso para todos los detalles, conceda a los usuarios el permiso **Ejecutar** en el objeto **Sistema** **5330**. Puede conceder este permiso utilizando un conjunto de permisos (como **Solución de problemas de D365**) o un grupo de usuarios (como **Solución de problemas de D365**). Para obtener más información sobre los permisos, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).

Los usuarios a los que no se les conceden permisos sobre el **objeto de sistema 5330** pueden acceder al panel **Inspección de páginas**, pero solo verán los campos **Página** y **Tabla**, que muestran los detalles básicos que pueden pasar a su equipo de soporte.

## <a name="see-also"></a>Consulte también .

[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
