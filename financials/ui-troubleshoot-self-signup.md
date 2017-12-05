---
title: Maneras de solucionar problemas con el registro al autoservicio | Documentos de Microsoft
description: "Obtenga información sobre los motivos más habituales por los que es posible que no pueda realizar el registro a Dynamics 365 Business edition y formas de solucionarlos."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c97d406d0213c7b2ade23a2d209adf54bf9dfcae
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="troubleshooting-self-service-sign-up"></a>Solución de problemas en el registro de autoservicio
Registrarse en [!INCLUDE[d365fin](includes/d365fin_md.md)] es muy fácil y se puede realizar muy rápidamente. Puede crear una cuenta gratuita incluso si es una organización existente. Este recurso aborda los problemas que pueda tener durante el registro.

## <a name="what-email-address-can-i-use-with-dynamics-365"></a>¿Qué dirección de correo electrónico puedo usar en Dynamics 365?
Para iniciar sesión, [!INCLUDE[d365fin](includes/d365fin_md.md)] requiere una dirección de correo electrónico del trabajo o la escuela. [!INCLUDE[d365fin](includes/d365fin_md.md)] no admite direcciones de correo electrónico proporcionadas por servicios de correo electrónico del consumidor ni por proveedores de la telecomunicación. Esto incluye outlook.com, hotmail.com, gmail.com y otros.

Si intenta iniciar sesión con una dirección de correo personal, recibirá un mensaje indicando que use una dirección del trabajo o la escuela.

## <a name="troubleshooting"></a>Solución de problemas
En muchas ocasiones, el registro para [!INCLUDE[d365fin](includes/d365fin_md.md)] se puede conseguir siguiendo el proceso de registro. Sin embargo, existen varias razones por las que puede no completar su registro de autoservicio. La tabla siguiente resume algunas de las razones más comunes por las que no le es posible completar el registro y las formas con las que puede solucionar estos problemas.

| Síntoma/Mensaje de error | Causa y solución alternativa |
| --- | --- |
| Para las direcciones de correo electrónico de Office 365 que no se han registrado en Estados Unidos, recibirá un mensaje como el siguiente durante el registro:<br /><br />**No funciona, aún no es soportado en su país o región.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] actualmente solo admite las cuentas de correo electrónico de Office 365 registradas en los EE. UU. |
| No se admiten las cuentas de correo electrónico personales, como nancy@gmail.com. Recibe un mensaje como el siguiente durante el registro:<br /><br />**Introdujo una dirección de correo electrónico personal: Introduzca su dirección de correo electrónico del trabajo para que se puedan guardar con seguridad los datos de su empresa.**<br> O <br> **Parece una dirección de correo electrónico personal. Introduzca su dirección de trabajo para que podamos conectarle con otros usuarios de la empresa. No se preocupe, no compartiremos su dirección con nadie.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] no admite direcciones de correo electrónico proporcionadas por servicios de correo electrónico del consumidor ni por proveedores de telecomunicaciones. Para completar el registro, intente de nuevo usar una dirección de correo electrónico asignada por su trabajo o escuela. Si todavía no puede registrarse y quiere completar un proceso de configuración más avanzado, puede registrarse en una nueva suscripción de prueba de Office 365 y usar esa dirección de correo electrónico para registrarse. |
| Las direcciones de correo electrónico de .gov o de .mil recibirán un mensaje como el siguiente durante el registro:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] no disponible: [!INCLUDE[d365fin](includes/d365fin_md.md)] no está disponible para usuarios con direcciones de correo electrónico .gov o .mil en este momento. Utilice otra dirección de correo electrónico de trabajo o vuelva más tarde.** <br>O <br>**No se puede finalizar el registro. Parece que [!INCLUDE[d365fin](includes/d365fin_md.md)] no se encuentra disponible actualmente para su trabajo o escuela.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] no admite las direcciones de correo de .gov o .mil en este momento. |
| El registro de autoservicio no está habilitado. Recibe un mensaje como el siguiente durante el registro:<br /><br />**No se puede finalizar el registro. Su departamento de TI ha desactivado el registro para [!INCLUDE[d365fin](includes/d365fin_md.md)]. Póngase en contacto con ello para completar el registro.** <br>O <br> **Parece una dirección de correo electrónico personal. Introduzca su dirección de trabajo para que podamos conectarle con otros usuarios de la empresa. No se preocupe, no compartiremos su dirección con nadie.** |El administrador de TI de su organización ha desactivado el registro de autoservicio para [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para completar el registro, póngase en contacto con su administrador de TI y pídale que siga las instrucciones en la página siguiente para permitir a los usuarios existentes que se registren en [!INCLUDE[d365fin](includes/d365fin_md.md)] y para permitir que los nuevos usuarios se unan a su suscriptor existente. También puede experimentar este problema si se registró en Office 365 a través de un socio. |
| La dirección de correo electrónico no es una Id. de Office 365. Recibe un mensaje como el siguiente durante el registro:<br /><br />**No es posible encontrarle en contoso.com. ¿Usa un identificador diferente en el trabajo o en la escuela? Intente iniciar sesión y, si no es posible, póngase en contacto con su departamento de TI.** |Su organización usa identificadores para iniciar sesión en Office 365 y otros servicios de Microsoft que son diferentes a su dirección de correo electrónico. Por ejemplo, su dirección de correo electrónico podría ser Nancy.Smith@contoso.com pero su Id. nancys@contoso.com. Para completar la suscripción, utilice el Id. que la empresa le ha asignado al iniciar sesión en los servicios de Office 365 u otros servicios de Microsoft. Si no sabe qué es, contacte con su administrador IT. Si todavía no puede registrarse y completar un proceso de configuración más avanzado, puede registrarse en una nueva suscripción de prueba de Office 365 y usar esa dirección de correo electrónico para registrarse. |

## <a name="see-also"></a>Consulte también
[[!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

