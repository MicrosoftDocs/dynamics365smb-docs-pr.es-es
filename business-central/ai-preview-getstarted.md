---
title: Comenzar a usar la versión de versión preliminar de Business Central para Copilot
description: Explica cómo obtener un entorno de Business Central con la nueva capacidad de IA para generar sugerencias de texto para descripciones de artículos/productos.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# <a name="get-started-with-a-business-central-preview-version-for-copilot" />Comenzar a usar la versión de versión preliminar de Business Central para Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Puede probar el texto de marketing de artículos impulsado por IA con Copilot, ya sea un cliente existente de Business Central o un cliente potencial, es decir, alguien que solo está interesado en explorar Business Central y probar la nueva capacidad. Para comenzar, deberá obtener acceso a una versión de Business Central Online que admita la nueva capacidad. Complete la sección a continuación que se aplica a usted.

## <a name="your-organization-already-uses-business-central" />Su organización ya usa Business Central

Como cliente o partner existente, necesitará un administrador con acceso al Centro de administración de Business Central para configurar un entorno de espacio aislado que ejecute la versión preliminar que incluye Copilot. Una vez que el entorno está en funcionamiento, los usuarios pueden probar la nueva característica.

Si es un administrador de entorno, complete los siguientes pasos:

1. Inicie sesión en el centro de administración de Business Central.
2. Seleccione **Entornos** > **Nuevo**.
3. En el panel **Crear entorno**, especifique un nombre para el nuevo entorno en el campo **Nombre del entorno**.
4. Establezca el **Tipo de entorno** en **Espacio aislado** o **Producción**.
5. Establezca **País** en cualquier país/región de la lista, pero tenga en cuenta que en la versión preliminar el texto de marketing generado por IA de Copilot solo está en inglés.
6. En el cuadro de diálogo **Versión**, elija una versión 22 o posterior de la lista.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Seleccione **Crear**.  

Para obtener más información sobre cómo crear entornos, vaya a [Crear un entorno](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Si tiene entornos aislados de versión preliminar que se ejecutan en **22.0.54157.54311 (Versión preliminar: edición Copilot)**, tenga en cuenta que estos entornos solo están disponibles hasta el 1 de mayo de 2023. Después de esta fecha, deberá aprovisionar un nuevo entorno o actualizar cualquiera de sus otros entornos a la versión 22.0 o posterior para continuar probando la versión preliminar del texto de marketing de artículos con tecnología de IA.

## <a name="your-organization-doesnt-use-business-central" />Su organización no usa Business Central

Si no es cliente de Business Central, regístrese para una prueba gratuita para probar las nuevas capacidades de IA. Registrarse para la versión de prueba es simple. Se le guiará a través de algunos pasos en los que deberá proporcionar cierta información, como su dirección de correo electrónico, número de teléfono y nombre. Para conseguir la versión de prueba, complete los siguientes pasos:

1. Vaya a [este sitio de prueba](https://go.microsoft.com/fwlink/?linkid=2227167) para comenzar con el proceso de registro.
2. Siga las instrucciones que aparecen en la pantalla.

   Se le pide que proporcione información como su dirección de correo electrónico, nombre y número de teléfono. La experiencia exacta puede variar, según la información que proporcione. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> Use su dirección de correo electrónico de trabajo o educativa como dirección de correo electrónico. Estableceremos su prueba en la cuenta de su organización. No puede utilizar direcciones de correo electrónico proporcionadas por servicios de correo electrónico para consumidores o proveedores de telecomunicaciones, como outlook.com, hotmail.com, gmail.com, y otros.
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. Cuando llegue al paso **Detalles de confirmación**, estará listo para comenzar la prueba.

   - Para ir directamente a Business Central, seleccione **Omitir e ir a Dynamics 365 Business Central** > **Empezar**.
   - También tiene la opción de invitar a otras personas de su organización a la prueba gratuita. Simplemente introduzca las direcciones de correo electrónico de cada persona, luego seleccione **Enviar invitaciones**. Seleccione **Comenzar** para ir a Business Central.  

   Se le redirigirá a su aplicación de prueba en [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). La versión de prueba puede tardar varios minutos en estar lista la primera vez que inicia sesión.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Una vez que haya iniciado sesión, verá la página de inicio de Business Central, denominada centro de roles, que se parece a la siguiente figura:

   [![Muestra el área de trabajo de Business Central y la lista de comprobación para Copilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Para obtener una introducción guiada a la creación de texto de marketing de artículos impulsado por IA con Copilot, en **Su lista de comprobación** cerca de la parte superior de la página, seleccione **Crear con Copilot** > **Iniciar recorrido**. Luego siga las instrucciones en pantalla.

   > [!TIP]
   > Si no ve **Su lista de comprobación**, seleccione primero el botón **Mostrar recorridos de demostración**.

## <a name="next-steps" />Pasos siguientes

Las capacidades de IA proporcionadas por Copilot deben estar habilitadas antes de que usted o cualquier otra persona pueda usar Copilot. Para habilitar las capacidades de IA, un administrador debe aceptar los términos y condiciones de la [versión preliminar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) y la [Declaración de privacidad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) en nombre de la organización.

> [!NOTE]
> Si está usando una versión de prueba, usted es el administrador. Si invitó a otras personas de su organización a la prueba durante el registro, no podrán usar Copilot hasta que acepte los términos y condiciones.

Hay dos formas de dar consentimiento como administrador:

- La forma más fácil es usar Copilot. La primera vez que utilice Copilot como administrador, se le pedirá que revise los términos y condiciones y que acepte o no. Para aprender a usar Copilot, vaya a [Agregar texto de marketing a los artículos](item-marketing-text.md).  

- La otra forma es usar la página **Estado de avisos de privacidad** en Business Central y aceptar la integración de **Azure OpenAI** para todos los usuarios. Para obtener más información, vaya a [Consentimiento de los términos y condiciones](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

## <a name="see-also" />Consulte también .

[Información general sobre el texto de marketing de productos impulsado por IA con Copilot](ai-overview.md)  
[Configurar texto de marketing de productos impulsado por IA con Copilot como administrador](enable-ai.md)  
[Cree texto de marketing para artículos usando Copilot](item-marketing-text.md)  
[Preguntas frecuentes sobre el texto de marketing de productos impulsado por IA (versión preliminar) con Copilot](ai-faq.md)  
