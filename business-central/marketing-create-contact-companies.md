---
title: Crear contactos de negocio | Microsoft Docs
description: Describe las tareas para crear contactos y definir sus relaciones de negocio.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d5885ac3310e545c0a2550ca49d67f1f9ab6ca35
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922724"
---
# <a name="create-contacts"></a>Crear contactos
Cuando desarrolle una relación de negocio con alguien de otra empresa, puede crearla como un contacto e introducir alguna información sobre él o su empresa, que puede ser útil para futuras comunicaciones. En la página **Tarjeta de contacto**, puede crear los siguientes tipos de contactos:

* **Persona**: Normalmente, esto sucede cuando ha tenido contacto directo con alguien y tiene sus datos de contacto.
* **Empresa**: si el contacto no es una persona individual sino una entidad, como un contratista o un banco. 

La información relevante para cada tipo de contacto es diferente, por lo que los campos y acciones disponibles son diferentes. Por ejemplo, solo se pueden asignar responsabilidades de trabajo a una persona y un grupo industrial a una empresa. 

Puede modificar el valor del campo **Tipo** más adelante, o puede usar los campos de la Pestaña desplegable **Herencia** en la página **Configuración de marketing** para especificar los datos que se comparten entre una persona y su empresa. Para obtener más información, consulte [Configurar contactos](marketing-setup-contacts.md).

Cuando un contacto se convierte en cliente, por ejemplo, la persona de contacto o la empresa de contacto pasa a ser el nombre del cliente. El registro del contacto se mantiene y puede vincular el contacto y el cliente para que sus datos se sincronicen en el futuro.

## <a name="to-create-a-contact-manually"></a>Para crear un contacto manualmente
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **N.º**, introduzca un número para el contacto.

    Por otra parte, si configuró un número de serie para los contactos de la página **Configuración de marketing**, puede pulsar **Entrar** para hacer que el sistema inserte el siguiente número de contacto disponible.  
5. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Para crear un contacto desde un cliente, proveedor o banco
Si tiene clientes, proveedores y cuentas bancarias para los que desea crear tarjetas de contacto, puede usar los trabajos por lotes **Crear Contactos desde** para crear contactos tomando como base los datos existentes. Al crear un contacto de esta manera, la información de contacto se sincroniza más tarde con la información del cliente, proveedor o de la cuenta bancaria relacionada. Para obtener más información, consulte [Procedimiento: Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Antes de que pueda crear contactos basados en datos existentes, debe especificar un código de relación de negocio para clientes, proveedores o cuentas bancarias en la pestaña desplegable **Interacciones** en la página **Configuración de marketing**. Para obtener más información, consulte [Configurar contactos](marketing-setup-contacts.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), especifique una de las siguientes opciones, dependiendo desde dónde desee crear contactos y, a continuación, elija el vínculo relacionado.
   * **Crear contactos desde clientes**
   * **Crear contactos desde proveedores**
   * **Crear contactos desde bancos**
2. En la página de solicitud que se abre, establezca filtros en la sección **Cliente**, **Proveedor** o **Banco** si desea crear contactos solo desde determinados clientes, proveedores o bancos.
3. Para crear contactos, seleccione **Aceptar**.

Los siguientes números de contacto de la serie se asignan a los nuevos contactos. Las relaciones comerciales que se especifican en la página **Configuración marketing** a los contactos recién creados.

> [!TIP]  
> También puede hacerlo al revés, es decir, creando un cliente, proveedor o cuenta bancaria desde un contacto. Para obtener más información, consulte [Para crear un contacto como cliente, proveedor o banco](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Para crear un un cliente, proveedor, empleado o banco a partir de un contacto
Si tiene un cliente, proveedor, empleado o banco para la empresa para la que desea crear un contacto, puede usar la función **Crear como**. Al crear un contacto de esta manera, la información de contacto se sincroniza más tarde con la información del cliente, proveedor, empleado o banco. Para obtener más información, consulte [Procedimiento: Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Para poder crear clientes, proveedores, empleados o bancos a partir de contactos, debe especificar un código de relación de negocio en la página **Configuración de marketing** de la Ficha desplegable **Interacciones**. Para obtener más información, consulte [Configurar contactos](marketing-setup-contacts.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione el contacto que desea crear como cliente, proveedor, empleado o banco.
3. Elija la acción **Crear como** y, a continuación, elija **Cliente**, **Proveedor**, **Banco** o **Empleado**.
4. Elija el botón **Aceptar**.

La información de contacto se transfiere de la ficha de contacto a una nueva tarjeta de cliente, proveedor, empleado o banco. Tal vez desee agregar información específica a cada una de las fichas, como detalles de facturación y de pago. Para obtener más información, consulte, por ejemplo, [Registrar clientes nuevos](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Para vincular un contacto con un cliente, proveedor, empleado o cuenta bancaria existente
Si tiene un contacto y un cliente, proveedor, empleado o banco para la misma empresa, puede vincular las dos entidades para sincronizar datos.

1. Abra el contacto que quiere vincular.
2. Elija la acción **Vincular con existente** y, a continuación, el **Cliente**, **Proveedor**, **Banco** o **Empleado**.
3. En la página que se abre, seleccione el cliente, el proveedor, el empleado o el banco al que quiere vincular el contacto.
4. En el campo **Campos principales actuales**, especifique los campos a los que el sistema da prioridad en caso de información conflictiva de los campos comunes al contacto y cliente, proveedor, empleado o banco. Por ejemplo, si el código de vendedor es diferente del contacto y el cliente, puede optar por mantener el de la tarjeta de contacto seleccionando **Contacto**.
5. Elija el botón **Aceptar**.

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Sincronizar contactos con clientes, proveedores, empleados y bancos
Si algunos contactos también son clientes, proveedores, empleados o bancos, podrá sincronizarlos con datos del contacto y obtener las siguientes ventajas:

* Solo es necesario actualizar la información en una de ellas. Por ejemplo, si modifica el número de teléfono del contacto, dicho número se actualizará automáticamente para el cliente, el proveedor, el empleado o el banco.
* Si especificó un número de serie para los contactos, al crear una tarjeta de cliente, proveedor, empleado o banco, se creará automáticamente un contacto.
* Puede crear ofertas de venta y pedidos, y pedir ofertas y pedidos, desde el contacto.
* Puede registrar sus interacciones, como impresión de pedidos, pedidos abiertos, creación de pedidos de servicio, envío de correos electrónicos, etc.
* Si elimina un contacto relacionado con un cliente, proveedor, empleado o banco, solo se borra el contacto. El cliente, el proveedor, el empleado o el banco permanecen.
* Si elimina un cliente, proveedor, empleado o cuenta bancaria que está relacionado con un contacto, el contacto permanecerá.

> [!NOTE]  
> Algunos detalles, como los datos de facturación y registro, no están disponibles para los contactos. Cuando crea contactos como clientes, proveedores, empleados o bancos, es posible que desee agregarlos manualmente.

Hay tres maneras de habilitar la sincronización de datos entre contactos y clientes, proveedores, empleados o bancos:

* Cuando crea contactos a partir de clientes, proveedores, empleados o bancos. Consulte [Para crear un contacto a partir de un cliente, proveedor o cuenta bancaria](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Cuando crea clientes, proveedores, empleados o bancos a partir de contactos. Consulte [Para crear un un cliente, proveedor o banco a partir de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Cuando se vinculan los contactos con clientes existentes, proveedores, empleados o bancos desde la tarjeta de contacto. Consulte [Para vincular un contacto con un cliente, proveedor o cuenta bancaria existente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Para ver con qué cliente, proveedor, empleado o banco está relacionado un contacto
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la línea de un contacto, elija la acción **Información relacionada** y, a continuación, la acción **Cliente/Proveedor/Empleado/Banco**.

## <a name="see-also"></a>Consulte también
[Gestionar contactos](marketing-contacts.md)  
[Configurar contactos](marketing-setup-contacts.md)  
[Trabajar con Business Central](ui-work-product.md)
