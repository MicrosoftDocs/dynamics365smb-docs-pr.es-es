---
title: Crear contactos comerciales
description: Describe las tareas necesarias para crear contactos y definir sus relaciones comerciales en la Ficha de contacto.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.date: 08/30/2022
ms.author: edupont
---
# Crear contactos

Cuando desarrolle una relación comercial con alguien de otra empresa, agréguelo como contacto en [!INCLUDE[prod_short](includes/prod_short.md)]. Luego, agregue cualquier información sobre ellos o su empresa que pueda ser útil para futuras comunicaciones. Puede crear los siguientes tipos de contactos en la página **Ficha contacto**:

* **Persona**: utilícelo cuando ha tenido contacto directo con alguien y tiene sus datos de contacto.
* **Empresa**: utilícelo para un contacto no es una persona individual sino una entidad, como un contratista o un banco.

La información relevante para cada tipo de contacto es diferente, por lo que los campos y acciones disponibles son diferentes. Por ejemplo, solo se pueden asignar responsabilidades de trabajo a una persona y un grupo industrial a una empresa.

También puede modificar el valor del campo **Tipo** más tarde. Alternativamente, use los campos de la ficha desplegable **Herencia** en la página **Configuración de marketing** para especificar los datos que se compartirán entre una persona y su empresa. Obtenga más información en [Configurar contactos](marketing-setup-contacts.md).

Cuando un contacto se convierte en cliente, por ejemplo, la persona de contacto o la empresa de contacto pasa a ser el nombre del cliente. El registro del contacto se mantiene y puede vincular el contacto y el cliente para que sus datos se sincronicen en el futuro.

> [!NOTE]
> Si activa la [actualización de características para plantillas de conversión](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees), también puede crear proveedores o empleados a partir de contactos comerciales.
>
> Sin embargo, si ya está utilizando la funcionalidad incorporada para crear clientes o artículos automáticamente, esta actualización de características no admite campos personalizados y los clientes o artículos recién creados no incluirán dichos datos.

## Para crear un contacto manualmente

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **N.º**, introduzca un número para el contacto.

   Por otra parte, si configuró un número de serie para los contactos de la página **Configuración de marketing**, puede seleccionar <kbd>Entrar</kbd> para hacer que el sistema inserte el siguiente número de contacto disponible.
4. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Para crear un contacto desde un cliente, proveedor o banco

Si tiene clientes, proveedores y cuentas bancarias existentes para los que desea crear tarjetas de contacto, puede usar los trabajos por lotes **Crear Contactos desde**. Al crear un contacto de esta manera, la información de contacto se sincroniza más tarde con la información del cliente, proveedor o de la cuenta bancaria relacionada. Obtenga más información en [Sincronizar contactos con clientes, proveedores, empleados y bancos](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Antes de que pueda crear contactos basados en datos existentes, debe especificar un código de relación de negocio para clientes, proveedores o cuentas bancarias en la pestaña desplegable **Interacciones** en la página **Configuración de marketing**. Obtenga más información en [Configurar contactos](marketing-setup-contacts.md).

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , especifique una de las siguientes opciones que coincida con la entidad desde la cual desee crear contactos y, a continuación, elija el vínculo relacionado.
   * **Crear Contactos desde Clientes**
   * **Crear contactos desde proveedores**
   * **Crear contactos desde bancos**
2. En la página de solicitud que se abre, establezca filtros en la sección **Cliente**, **Proveedor** o **Banco** si desea crear contactos solo desde determinados clientes, proveedores o bancos.
3. Elija **Aceptar** para comenzar a crear contactos.

Los siguientes números de contacto de la serie se asignan a los nuevos contactos. El código de relación de negocio que se especifica en la página **Configuración marketing** se asigna a los contactos recién creados.

> [!TIP]  
> También puede hacerlo al revés, es decir, creando un cliente, proveedor, empleado o cuenta bancaria desde un contacto. Obtenga más información en la sección [Para crear un contacto como proveedor, empleado o banco de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## Para crear un un cliente, proveedor, empleado o banco a partir de un contacto

Si tiene un cliente, proveedor, empleado o banco para la empresa para la que desea crear un contacto, puede usar la acción **Crear como**. Al crear un contacto de esta manera, la información de contacto se sincroniza más tarde con la información del cliente, proveedor, empleado o banco. Obtenga más información en [Sincronizar contactos con clientes, proveedores y bancos](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).<!--Should this link include "Employees" as per the section title below?-->

> [!NOTE]  
> Para poder crear clientes, proveedores, empleados o bancos a partir de contactos, debe especificar un código de relación de negocio en la página **Configuración de marketing** de la Ficha desplegable **Interacciones**. Obtenga más información en [Configurar contactos](marketing-setup-contacts.md).

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione el contacto que desea crear como cliente, proveedor, empleado o banco.
3. Elija la acción **Crear como** y, a continuación, elija **Cliente**, **Proveedor**, **Banco** o **Empleado**.
4. Elija **Aceptar**.

La información de contacto se transfiere de la ficha de contacto a una nueva tarjeta de cliente, proveedor, empleado o banco. Tal vez desee agregar información específica a cada una de las fichas, como detalles de facturación y de pago. Para obtener un ejemplo, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).

## Para vincular un contacto con un cliente, proveedor, empleado o cuenta bancaria existente

Si tiene un contacto y un cliente, proveedor, empleado o banco para la misma empresa, puede vincular las dos entidades para sincronizar datos.

1. Abra el contacto que quiere vincular.
2. Elija la acción **Vincular con existente** y, a continuación, el **Cliente**, **Proveedor**, **Banco** o **Empleado**.
3. En la página que se abre, seleccione el cliente, el proveedor, el empleado o el banco al que quiere vincular el contacto.
4. En el campo **Campos principales actuales**, especifique los campos a los que el sistema da prioridad cuando hay información conflictiva de los campos comunes al contacto y cliente, proveedor, empleado o banco. Por tanto, si el código de vendedor difiere entre el contacto y el cliente, puede optar por mantener el de la tarjeta de contacto seleccionando **Contacto**.
5. Elija **Aceptar**.

## Para quitar un vínculo entre un contacto y un cliente, proveedor, empleado o cuenta bancaria existente

Si ha vinculado incorrectamente un contacto con un cliente, proveedor, empleado o cuenta bancaria, elimine el vínculo entre las entidades para que los datos ya no se sincronicen.

1. Abra el contacto que tiene el enlace incorrecto.  
2. Elegir la acción **Relaciones de negocio**.  
3. En la página que se abre, seleccione el cliente, el proveedor, el empleado o el banco del que quiere quitar el vínculo.  
4. Elija la acción **Eliminar**.  

> [!NOTE]  
> No utilice la ventana **Relaciones de negocio** para cambiar las relaciones existentes. En su lugar, elimine la relación y use la acción **Vincular con existente**. Obtenga más información en la sección [Para vincular un contacto a un cliente, proveedor, empleado o cuenta bancaria existente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Sincronizar contactos con clientes, proveedores, empleados y bancos

Si algunos contactos también son clientes, proveedores, empleados o bancos, podrá sincronizarlos con datos del contacto y obtener las siguientes ventajas:

* Solo es necesario actualizar la información en una de ellas. Por tanto, si modifica el número de teléfono del contacto, dicho número se actualizará automáticamente para el cliente, el proveedor, el empleado o el banco.
* Si especificó un número de serie para los contactos, al crear una tarjeta de cliente, proveedor, empleado o banco, se creará automáticamente un contacto.
* Puede crear ofertas de venta y pedidos, y pedir ofertas y pedidos, desde el contacto.
* Puede registrar sus interacciones, como impresión de pedidos, pedidos abiertos, creación de pedidos de servicio, envío de correos electrónicos, etc.
* Si elimina un contacto relacionado con un cliente, proveedor, empleado o banco, solo se borra el contacto. El cliente, el proveedor, el empleado o el banco permanecen.
* Del mismo modo, si elimina un cliente, proveedor, empleado o cuenta bancaria que está relacionado con un contacto, el contacto permanecerá.

> [!NOTE]  
> Algunos detalles, como los datos de facturación y registro, no están disponibles para los contactos. Cuando crea contactos como clientes, proveedores, empleados o bancos, es posible que desee agregar esa información manualmente.

Hay tres maneras de habilitar la sincronización de datos entre contactos y clientes, proveedores, empleados o bancos:

* Cuando crea contactos a partir de clientes, proveedores o bancos. Obtenga más información en la sección [Para crear un contacto desde un cliente, proveedor o banco](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Cuando crea clientes, proveedores, empleados o bancos a partir de contactos. Obtenga más información en la sección [Para crear un contacto como proveedor, empleado o banco de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Cuando se vinculan los contactos con clientes existentes, proveedores, empleados o bancos desde la tarjeta de contacto. Obtenga más información en la sección [Para vincular un contacto a un cliente, proveedor, empleado o cuenta bancaria existente](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## Para ver con qué cliente, proveedor, empleado o banco está relacionado un contacto

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la línea de un contacto, elija la acción **Información relacionada** y, a continuación, la acción **Cliente/Proveedor/Empleado/Banco**.

## Consulte también .

[Gestionar contactos](marketing-contacts.md)  
[Configurar contactos](marketing-setup-contacts.md)  
[Usar Mapas en línea para encontrar ubicaciones e indicaciones](across-online-maps.md)  
[Trabajar con Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
