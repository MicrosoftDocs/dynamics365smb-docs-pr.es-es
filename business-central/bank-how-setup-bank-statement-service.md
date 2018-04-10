---
title: Configurar las fuentes de banco de Envestnet Yodlee | Documentos de Microsoft
description: "Puede convertir la información sobre pagos a cualquier formato de datos que requiera el banco y habilitar la exportación o importación de los archivos de banco."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: f3507de1dbf463066b81b8504b832d12731f9138
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Configuración del servicio de fuentes de banco de Envestnet Yodlee
Puede importar extractos electrónicos de su banco para rellenar rápidamente la ventana **Diario de conciliación de pagos** para que pueda liquidar pagos y conciliar la cuenta bancaria. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

El servicio de fuentes de banco de Envestnet Yodlee está instalado como una extensión de [!INCLUDE[d365fin](includes/d365fin_md.md)] y está listo para ser activado. Para obtener más información, consulte [Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante extensiones](ui-extensions.md).

> [!NOTE]
> El servicio de fuentes de banco de Envestnet Yodlee sólo se admite en EE.UU., Canadá, y Reino Unido.

Después de habilitar el servicio de fuentes de banco, debe vincular una cuenta bancaria a la cuenta bancaria de la que proviene la fuente. Vincula las cuentas a cuentas en línea en los siguientes ejemplos:

* No existe una cuenta en [!INCLUDE[d365fin](includes/d365fin_md.md)] para su cuenta bancaria en línea. Por tanto, cree la cuenta vinculando de la cuenta bancaria en línea.
* Existe una cuenta en [!INCLUDE[d365fin](includes/d365fin_md.md)] que desea vincular a una cuenta bancaria en línea.
* Una cuenta vinculada debe ser desvinculada porque desea dejar de usar el servicio de fuente de banco de la cuenta.
* Las cuentas en línea se han modificado y desea actualizar la información en las cuentas en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Cuando se ha habilitado el servicio de fuente de banco, puede definir una cuenta bancaria que importe automáticamente nuevos extractos de cuenta en la ventana **Diario de conciliación de pagos** cada dos horas. Las transacciones para los pagos que ya se hayan registrado como liquidados o conciliados en la ventana **Diario de conciliación de pagos** no se importarán. Para obtener más información, vea la sección “Para habilitar la importación automática de los extractos bancarios”.

> [!NOTE]  
> Si usa la configuración asistida de la Configuración de la empresa, algunos de los pasos en los procedimientos siguientes se producen automáticamente cuando accede a la configuración de la cuenta bancaria de la empresa. Para obtener más información, vea [Introducción](product-get-started.md).

## <a name="to-enable-the-bank-feed-service"></a>Para activar el servicio de fuente de banco
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Abra la cuenta bancaria que usará para el servicio de fuente de banco.
3. En la ventana **Cuenta bancaria**, en el campo **Formato de importación de extractos bancarios**, seleccione YODLEEBANKFEED.  

El servicio de fuente de banco se activará cuando vincule una cuenta a la cuenta bancaria en línea relacionada. Vea el procedimiento siguiente.  

## <a name="to-create-a-new-linked-bank-account"></a>Para crear una nueva cuenta bancaria vinculada
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la cuenta bancaria correspondiente y, a continuación, seleccione **Crear una nueva cuenta bancaria vinculada**. La ventana **Vinculación de cuenta bancaria** se abre después de unos segundos.

    > [!NOTE]  
    > Esta ventana muestra la página web del servicio de fuentes de banco de Envestnet Yodlee. La terminología y las funciones de la ventana pueden no coincidir con las instrucciones que ofrece este tema.  
3. En la ventana **Vinculación de banco en línea**, en el panel **Vínculo de cuenta** use la función Buscar para buscar el banco en el que tiene una o varias cuentas bancarias en línea.
4. Seleccione el nombre del banco. Se abre el panel **Iniciar sesión**.
5. Introduzca el nombre de usuario y la contraseña que usa para conectarse al banco en línea y, a continuación, seleccione el botón **Siguiente**.  
6. El servicio de fuente de banco se prepara para vincular la primera cuenta bancaria en línea en el banco especificado a una nueva cuenta en [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
    > Si ha configurado más de una cuenta en línea en el banco deberá crear las cuentas adicionales en [!INCLUDE[d365fin](includes/d365fin_md.md)] para ellas. Consulte los pasos 8 a 10.  

    Después de que se haya completado el proceso, el nombre del banco aparecerá en el panel **Mis cuentas** en la pestaña **Vinculado**. El valor entre corchetes indica la cantidad de cuentas bancarias en línea que están vinculadas.  
7. Elija el botón **Aceptar**.

    Si solo vincula una cuenta bancaria en línea, se abre la ventana **Ficha banco** y se muestra el nombre de la cuenta bancaria en línea. En este caso, la vinculación de la cuenta bancaria se ha completado. Lo único que tiene que hacer es configurar la cuenta bancaria. Para obtener más información, consulte [Configurar cuentas bancarias](bank-how-setup-bank-accounts.md).

    Si va a vincular más de una cuenta bancaria en línea, la ventana **Vinculación de banco** abre una ventana y enumera las cuentas bancarias en línea adicionales que todavía no se han vinculado en [!INCLUDE[d365fin](includes/d365fin_md.md)]. En ese caso, siga el paso siguiente.  
8. En la ventana **Vinculación de banco**, seleccione la línea para una cuenta bancaria en línea y, a continuación, seleccione la acción **Vincular a nuevo banco**.  

    La ventana **Ficha banco** se abre para crear una nueva y muestra el nombre de la cuenta bancaria en línea.

    Si ya existe una cuenta bancaria en [!INCLUDE[d365fin](includes/d365fin_md.md)] al que desea vincular la cuenta bancaria en línea adicional, siga el siguiente paso.  
9. En la ventana **Vinculación de banco**, seleccione la línea para una cuenta bancaria en línea y, a continuación, seleccione la acción **Vincular a banco existente**.
10. En la ventana **Lista de bancos**, seleccione la cuenta bancaria que desee vincular y, a continuación, haga clic en **Aceptar**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Para vincular una cuenta bancaria a una cuenta bancaria en línea.
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la línea para una cuenta bancaria que no está vinculada a una cuenta en línea y, a continuación, seleccione la acción **Vincular a banco en línea**. La ventana **Vinculación de banco en línea** se abre rellenada previamente con el nombre del banco en el panel **Vincular cuenta**.
3. Seleccione el nombre del banco. Se abre el panel **Iniciar sesión**.
4. Introduzca el nombre de usuario y la contraseña que usa para conectarse al banco en línea y, a continuación, seleccione el botón **Siguiente**.  

    El servicio de fuentes de banco se prepara para vincular su cuenta bancaria en [!INCLUDE[d365fin](includes/d365fin_md.md)] a la cuenta bancaria en línea relacionada.  

    Cuando el proceso ha finalizado correctamente, el nombre del banco aparecerá en el panel **Mis cuentas** en la pestaña **Vinculado**. Si el banco tiene más de una cuenta bancaria, solo se vincula la cuenta bancaria seleccionada en el paso 2.  
5. Elija el botón **Aceptar**.

En la ventana **Lista de bancos**, se activa la casilla **Vinculado**.

## <a name="to-unlink-a-bank-account"></a>Para desvincular una cuenta bancaria
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la línea para una cuenta bancaria vinculada que desee desvincular de su cuenta en línea relacionada y, a continuación, seleccione la acción **Desvincular un banco en línea**.

> [!NOTE]  
> Si selecciona **Sí** en el cuadro de diálogo de confirmación, el vínculo a la cuenta bancaria en línea se elimina y se eliminan los detalles de inicio de sesión. Para vincular nuevamente la cuenta bancaria a una cuenta bancaria en línea, debe volver a iniciar sesión en el banco. Para obtener más información, vea la sección “Para vincular una cuenta bancaria a una cuenta bancaria en línea“.

## <a name="to-update-bank-account-linking"></a>Para actualizar la vinculación de la cuenta bancaria
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la cuenta bancaria correspondiente y, a continuación, seleccione la acción **Actualizar vinculación de banco**.

Si surgen problemas para alguna de las cuentas bancarias vinculadas en la ventana **Lista de bancos**, se abre la ventana **Vinculación de banco** y se especifican qué cuentas bancarias tienen problemas. Los problemas se solucionan mejor desvinculando la cuenta y reconstruyendo el vínculo. Para obtener más información, vea la sección “Para vincular una cuenta bancaria a una cuenta bancaria en línea“.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Para activar la importación automática de los extractos de cuenta
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la línea para una cuenta bancaria vinculada y, a continuación, seleccione la acción **Configuración de la importación automática de extractos bancarios**.
3. En la ventana **Configuración de la importación automática de extractos bancarios**, en el campo **N.º de días incluidos**, especifique hasta qué fecha en el pasado desea obtener nuevas transacciones bancarias.

    > [!NOTE]  
    > Se recomienda establecer este valor a 7 días o más.  
4. Seleccione la casilla de verificación **Habilitado**.  

Cada hora, la ventana **Diario de conciliación de pagos** mostrará cualquier nuevo pago que se realice en la cuenta bancaria en línea.

> [!NOTE]  
> Las transacciones para los pagos que ya se hayan registrado como liquidados o conciliados en la ventana **Diario de conciliación de pagos** no se importarán.

## <a name="see-also"></a>Consulte también
[Configurar banca](bank-setup-banking.md)  
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

