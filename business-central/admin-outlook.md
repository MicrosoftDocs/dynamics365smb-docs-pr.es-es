---
title: Obtener el complemento Business Central para Outlook
description: Obtenga información sobre cómo instalar el complemento Business Central para Outlook para su organización o para su propio uso.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Microsoft 365, Outlook
ms.search.form: 1831, 1832, 9020, 9022, 9027, 9030, 9004, 9005, 9018, 9006, 9007, 9010
ms.date: 08/13/2021
ms.author: jswymer
ms.openlocfilehash: 007d23bcb1d257402e33689ebe3ac57db10b84c2
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323207"
---
# <a name="get-the-business-central-add-in-for-outlook"></a>Obtener el complemento Business Central para Outlook

Con [!INCLUDE[prod_short](includes/prod_short.md)] puede administrar interacciones comerciales con sus clientes y proveedores directamente en Microsoft Outlook. Con el complemento de [!INCLUDE[prod_short](includes/prod_short.md)] Outlook, puede ver datos financieros relacionados con clientes y proveedores. También puede crear y enviar documentos financieros, como presupuestos y facturas.  

Hay dos formas de instalar el complemento Business Central para Outlook, según su función en la organización:

- Como administrador de Microsoft 365, utilice *Implementación centralizada* para instalar el complemento automáticamente para toda la organización, grupos o usuarios específicos.

- Como cualquier usuario, instale el complemento para su propio uso, si su administrador aún no lo ha implementado por usted.

## <a name="about-the-business-central-add-in-for-outlook"></a>Acerca del complemento Business Central para Outlook

El complemento Business Central para Outlook consta de dos complementos más pequeños:

- Información del contacto

    Este complemento proporciona a los usuarios información del cliente o proveedor de [!INCLUDE[prod_short](includes/prod_short.md)] en los correos electrónicos de Outlook y las citas del calendario. También le permite crear y enviar documentos comerciales de [!INCLUDE[prod_short](includes/prod_short.md)], como ofertas de ventas y facturas a un contacto. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Vista de documento

    Cuando un correo electrónico hace referencia a un número de documento comercial en el cuerpo del correo electrónico, este complemento proporciona un enlace directo en línea desde el cuerpo del correo electrónico al documento comercial real en [!INCLUDE[prod_short](includes/prod_short.md)].

Para obtener más información sobre lo que hace con los complementos, consulte [Uso de Business Central como su bandeja de entrada comercial en Outlook](work-outlook-addin.md).

Cada complemento se proporciona como archivo XML, llamado *manifiesto*, que debe instalarse en Outlook de cualquier persona que desee esta funcionalidad. Estos archivos describen cómo activar los complementos y conectarse a Business Central cuando se usan en Outlook. El trabajo con estos archivos normalmente lo realiza un administrador. Como usuario normal, en la mayoría de los casos, no tendrá que manejar estos archivos directamente. Su administrador configurará el complemento para que se instale automáticamente o usted utilizará la configuración asistida incorporada para manejar la instalación.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin"></a>Implementar el complemento mediante Implementación centralizada como administrador

Implementación centralizada es una característica del Centro de administración de Microsoft 365 que se usa para instalar complementos automáticamente en las aplicaciones de Office de los usuarios, como Outlook. Es la forma recomendada para que los administradores implementen complementos de Office para usuarios y grupos dentro de su organización.

> [!NOTE]
> Para Business Central local, consulte [Configuración del complemento para la integración de Outlook con Business Central local](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) en el contenido de administración (solo en inglés).

### <a name="prerequisites"></a>Requisitos previos

- Una suscripción a Microsoft 365  
- A los usuarios se les asigna una licencia de Microsoft 365  
- Su cuenta de Microsoft 365 tiene el rol *Administrador global* o *Administrador de Exchange*

### <a name="deploy-the-add-in"></a>Implementar el complemento

1. En Business Central, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración asistida** y luego elija el enlace relacionado.
2. Elija **Implementación centralizada complementos Outlook** para iniciar la guía de configuración asistida.
3. Revise la primera página y elija **Siguiente** para abrir la página para descargar los complementos.
4. En la columna **Implementar**, seleccione la casilla de los complementos que desea implementar, y luego elija **Descargar y continuar**.

    Un archivo con el nombre *OutlookAddins.zip* se descarga en su dispositivo.

5. En este punto, ha terminado con el trabajo que necesita hacer en Business Central, por lo que puede elegir **Hecho**.

   >[!TIP]
   > Antes de que elija **Siguiente**, seleccione el vínculo **Ir a Microsoft 365 (se abre en una nueva ventana)** para abrir e iniciar sesión en el Centro de administración de Microsoft 365 en una nueva ventana del navegador. De todos modos, tendrá que ir al Centro de administración de Microsoft 365 en un paso posterior.

6. Vaya a la carpeta donde se descargó OutlookAddins.zip y extraiga los archivos **Contact Insights.xml** y **Document View.xml** del .zip a una carpeta de su elección.

    Para más información, vea [Comprima y descomprima archivos y carpetas](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Inicie sesión en Centro de administración de Microsoft 365, y luego vaya a [Aplicaciones integradas](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Elija **Cargar aplicaciones personalizadas**.
9. En la página **Cargar aplicaciones para implementar**, elija **Cargar archivo de manifiesto (.xml) desde el dispositivo** > **Elegir un archivo**.
10. Seleccione uno de los archivos adicionales que extrajo anteriormente, por ejemplo, **Contact Insights.xml**.
11. Siga las instrucciones para asignar usuarios e implementar el complemento.
12. Repita los pasos del 9 al 11 para el otro archivo de complemento si lo desea.

> [!IMPORTANT]
> Aparece una marca de verificación verde cuando el complemento se implementa en el centro de administración. Sin embargo, pueden pasar hasta 24 horas antes de que los usuarios vean el complemento la aplicación Outlook. Es posible que los usuarios también tengan que reiniciar Outlook.

Cuando termine, siempre puede cambiar la implementación en el Centro de administración de Microsoft 365, como asignar más usuarios. Para obtener más información sobre la implementación de complementos en el Centro de administración, consulte [Implementar complementos en el centro de administración](/microsoft-365/admin/manage/manage-deployment-of-add-in).

## <a name="install-the-add-in-for-your-own-use"></a><a name="install"></a>Instale el complemento para su propio uso

Si su organización lo permite, puede instalar el complemento Business Central solo para usted. Si no está seguro, consulte con su administrador.

1. En Business Central, vaya al icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , entre en **Obtener el complemento de Outlook**, y luego elija el enlace relacionado.
2. Lea la página y elija **Siguiente** cuando esté listo.
3. Si desea recibir un mensaje de correo electrónico de bienvenida de Business Central con una descripción general del uso del complemento, active **Enviar mensaje de correo de ejemplo**.
4. Elija **Finalizar** para completar la instalación.

Business Central se conectará a su servidor de correo electrónico e instalará el complemento en su Outlook. Esto no tardará mucho. Ahora está listo para comenzar a usar el complemento en Outlook.

### <a name="for-business-central-on-premises"></a><a name="onprem"></a>Para Business Central local

Si usa Business Central local, la instalación del complemento puede ser ligeramente diferente.

1. En Business Central, vaya al icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , entre en **Obtener el complemento de Outlook**, y luego elija el enlace relacionado.
2. Lea la página y elija **Siguiente** cuando esté listo.
3. Realice uno de los siguientes pasos, según la página que vea:

    - Si ve el botón **Instalar en mi Outlook**, elíjalo y listo.
    - Si ve el botón **Siguiente**, elíjalo. En la página siguiente, si desea recibir un mensaje de correo electrónico de bienvenida de Business Central con una descripción general del uso del complemento, active **Enviar mensaje de correo de ejemplo**. A continuación, elija **Terminar** y está listo.
    - Si ve el botón **Descargar complemento**, selecciónelo y vaya al paso siguiente.
4. Cuando elige **Descargar complemento**, un archivo con el nombre *OutlookAddins.zip* se descarga en su dispositivo. Deberá ver el archivo en la parte superior del navegador.

   Vaya a la carpeta donde se descargó OutlookAddins.zip y extraiga los archivos **Contact Insights.xml** y **Document View.xml** del .zip a una carpeta de su elección. Para obtener más información sobre cómo extraer archivos, consulte [Comprimir y descomprimir archivos y carpetas](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Abra Outlook y elija **Obtener complementos** en la cinta de opciones. O, si está usando Outlook en la web, seleccione el menú desplegable en cualquier mensaje de correo electrónico nuevo o existente, luego seleccione **Obtener complementos**.
6. Elija **Mis complementos** > **Agregar un complemento personalizado** > **Agregar desde un archivo**.
7. Elija uno de los archivos .xml que extrajo, como **Contact Insights.xml**, y luego elija **Abrir** > **Instalar**.
8. Repita los pasos 6 y 7 para el otro archivo .xml, si descargó uno.

Ahora está listo para comenzar a usar el complemento en Outlook.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Preparación para hacer negocios](ui-get-ready-business.md)  
[Obtener Business Central en mi dispositivo móvil](install-mobile-app.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Finanzas](finance.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Requisitos mínimos para Outlook](product-requirements.md#outlook)  
[Usar complementos en Outlook en la web](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]