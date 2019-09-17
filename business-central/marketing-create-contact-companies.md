---
title: Crear empresas de contacto | Documentos de Microsoft
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 09/06/2019
ms.author: sgroespe
ms.openlocfilehash: 5ec6a7580cd4211b33d276f5523bfcf34b91ad59
ms.sourcegitcommit: d3035c32bb79b51179540787b98579ac0c528cc4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/06/2019
ms.locfileid: "1985843"
---
# <a name="create-contacts"></a>Crear contactos
Conoce regularmente a personas de otras empresas que pueden convertirse en relaciones de negocio, como una relación de cliente. Cuando se realiza un nuevo contacto, se debe registrar tanta información como sea posible en una ficha de contacto para que la comunicación pueda continuar.

Puede crear el contacto como tipo **Empresa**, por ejemplo, si la relación no es una persona individual sino una entidad, como un contratista o un banco. También puede crear el contacto como tipo **Persona**. La funcionalidad es más o menos la misma para ambos tipos y ambos se pueden cambiar a medida que la relación evoluciona.

Cuando una ficha de contacto se convierte en una ficha de cliente, por ejemplo, la persona de contacto o la empresa de contacto se convierte en el nombre del cliente. La ficha de contacto permanece y los datos de las dos fichas se sincronizarán en el futuro si las enlaza.

## <a name="person-or-company"></a>Persona o empresa
Puede decidir configurar un contacto como una persona o una empresa, por lo general dependiendo de si conoce el nombre de la persona de contacto en el momento de la creación. Esto se hace rellenando el campo **Tipo** en la página **Ficha contacto**. También se pueden actualizar fichas de contacto tanto para una empresa como para una o varias personas que trabajan en la empresa. Esto sucede automáticamente cuando rellena el campo **Nombre de la empresa** en una ficha de contacto del tipo **Persona**.

La funcionalidad es la misma para ambos tipos, excepto las opciones de información adicional que cambian según el tipo. Por ejemplo, solo se pueden asignar responsabilidades de funciones a una persona y a un grupo de industria a una empresa. Esto se indica en la interfaz de usuario atenuando los campos y acciones que no se aplican. Puede modificar el valor del campo **Tipo** más adelante, o puede usar los campos de la pestaña desplegable **Herencia** en la página de **Configuración de marketing** para controlar qué datos se comparten entre una persona y la empresa relacionada de la persona. Para obtener más información, consulte [Configurar contactos](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>Para crear un contacto manualmente
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **N.º**, introduzca un número para el contacto.

    Por otra parte, si configuró un número de serie para los contactos de la página **Configuración marketing**, puede pulsar Entrar para hacer que el sistema inserte el siguiente número de contacto disponible.  
5. Rellene los campos restantes según sea necesario. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Para crear un contacto desde un cliente, proveedor o banco
Si tiene clientes, proveedores y cuentas bancarias para los que desea crear tarjetas de contacto, puede usar los trabajos por lotes **Crear Contactos desde** para crear contactos tomando como base los datos existentes. Al crear un contacto de esta manera, la información de contacto se sincroniza más tarde con la información del cliente, proveedor o de la cuenta bancaria relacionada. Para obtener más información, consulte [Procedimiento: Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Antes de que pueda crear contactos basados en datos existentes, debe especificar un código de relación de negocio para clientes, proveedores o cuentas bancarias en la pestaña desplegable **Interacciones** en la página **Configuración de marketing**. Para obtener más información, consulte [Configurar contactos](marketing-setup-contacts.md).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), especifique una de las siguientes opciones, dependiendo desde dónde desee crear contactos y, a continuación, elija el vínculo relacionado.
   * **Crear contactos desde clientes**
   * **Crear contactos desde proveedores**
   * **Crear contactos desde bancos**
2. En la página de solicitud que se abre, establezca filtros en la sección **Cliente**, **Proveedor** o **Banco** si desea crear contactos solo desde determinados clientes, proveedores o bancos.
3. Para crear contactos, seleccione **Aceptar**.

Los siguientes números de contacto de la serie se asignan a los nuevos contactos. Las relaciones comerciales que se especifican en la página **Configuración marketing** a los contactos recién creados.

> [!TIP]  
> También puede hacerlo al revés, es decir, creando un cliente, proveedor o cuenta bancaria desde un contacto. Para obtener más información, consulte [Para crear un contacto como cliente, proveedor o banco](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Para crear un cliente, proveedor o banco a partir de un contacto
Si tiene un cliente, proveedor o cuenta bancaria para la empresa para la que desea crear un contacto, puede usar la función **Crear como**. Al crear un contacto de esta manera, la información de contacto se sincroniza más tarde con la información del cliente, proveedor o de la cuenta bancaria relacionada. Para obtener más información, consulte [Procedimiento: Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Antes de que pueda crear clientes, proveedores o cuentas bancarias a partir de contactos, debe especificar un código de relación de negocio para clientes, proveedores o cuentas bancarias en la pestaña desplegable **Interacciones** en la página **Configuración de marketing**. Para obtener más información, consulte [Configurar contactos](marketing-setup-contacts.md).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione el contacto que desea crear como cliente, proveedor o banco.
3. Elija la acción **Crear como** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.
4. Elija el botón **Aceptar**.

La información de contacto se transfiere de la ficha de contacto a una tarjeta de cliente, proveedor o de cuenta bancaria nueva. Tal vez desee agregar información específica a cada una de las fichas, como detalles de facturación y de pago. Para obtener más información, consulte, por ejemplo, [Registrar clientes nuevos](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Para vincular un contacto con un cliente, proveedor o cuenta bancaria existente
Si tiene un contacto y un cliente, proveedor o cuenta bancaria para la misma empresa, puede vincular las dos entidades para que se sincronicen los datos comunes.

1. Abra el contacto que quiere vincular.
2. Elija la acción **Vincular con** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.
3. En la página que se abre, seleccione el cliente, el proveedor o la cuenta bancaria al que quiere vincular el contacto.
4. En el campo **Campos principales actuales**, especifique los campos a los que el sistema da prioridad en caso de información conflictiva de los campos comunes al contacto y cliente, vendedor o cuenta. Por ejemplo, si el código de vendedor es diferente en la ficha de contacto y en la tarjeta de cliente, puede optar por mantener el de la ficha de contacto seleccionando **Contacto**.
5. Elija el botón **Aceptar**.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Sincronizar contactos con clientes, proveedores y cuentas bancarias
Si algunos contactos también son clientes, proveedores o bancos, podrá sincronizar la información de contacto con el cliente, proveedor o la cuenta bancaria relacionados.

Los siguientes beneficios existen cuando un contacto se sincroniza con un cliente, proveedor o cuenta bancaria.

* Solo es necesario actualizar la información en una de ellas. Por ejemplo, si modifica el número de teléfono del contacto, dicho número se actualizará automáticamente para reflejar la modificación en el cliente, el proveedor o la cuenta bancaria.
* Si especificó un número de serie para los contactos y crea una ficha de cliente, proveedor o banco, se creará automáticamente una ficha de contacto para el cliente, proveedor o banco.
* Puede crear ofertas de venta y pedidos, y obtenerlos desde el contacto.
* Puede hacer que se registren sus interacciones al llevar a cabo acciones como imprimir o abrir pedidos, crear pedidos de servicio, enviar correos electrónicos, etc.
* Si elimina un contacto relacionado con un cliente, proveedor o banco, solo se borra del sistema el contacto. El cliente, el proveedor o la cuenta bancaria permanece.
* Si elimina un cliente, proveedor o cuenta bancaria que está relacionado con un contacto, el contacto permanecerá.

> [!NOTE]  
> Algunos detalles, como los datos de facturación y registro, no aparecen en la ficha de contacto. Por tanto, puede que desee agregarlos manualmente en la ficha de cliente, de proveedor o de banco al crear contactos como clientes, proveedores o bancos.

La sincronización de datos comunes entre contactos y los clientes, proveedores o cuentas bancarias relacionados se habilita de tres maneras:

* Cuando crea contactos a partir de clientes, proveedores o bancos. Consulte [Para crear un contacto a partir de un cliente, proveedor o cuenta bancaria](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Cuando crea clientes, proveedores o cuentas bancarias a partir de contactos. Consulte [Para crear un un cliente, proveedor o banco a partir de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).
* Cuando se vinculan los contactos con clientes existentes, proveedores o bancos de la ficha de contacto. Consulte [Para vincular un contacto con un cliente, proveedor o cuenta bancaria existente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).

## <a name="to-view-which-customer-vendor-or-bank-account-a-contact-is-related-to"></a>Para ver con qué cliente, proveedor o banco está relacionado un contacto
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la línea de un contacto, seleccione la acción **Información relacionada** y, a continuación, la acción **Cliente/Proveedor/Banco**.

Se abre la ficha relacionada para la página.

## <a name="see-also"></a>Consulte también
[Gestionar contactos](marketing-contacts.md)  
[Configurar contactos](marketing-setup-contacts.md)  
[Trabajar con Business Central](ui-work-product.md)
