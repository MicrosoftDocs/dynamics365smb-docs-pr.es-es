---
title: Crear empresas de contacto | Documentos de Microsoft
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: es-es
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Crear empresas de contacto
Su empresa asiste con frecuencia a reuniones con empresas de las que en muchas ocasiones surgen futuras relaciones de negocio. Cuando se crea un nuevo contacto, se debe registrar esta información de modo que pueda establecerse una comunicación continua.

Al asignar la mayor información posible sobre una empresa específica se garantiza una comunicación eficaz. Por ejemplo, si asigna el grupo de industria correspondiente, se asegura que las empresas se incluyan en todas las comunicaciones relevantes.

También puede definir la relación de negocio que mantiene con un contacto. Por ejemplo, un contacto podría ser un cliente potencial, un banco o un contratista.

## <a name="creatinge-contact-companies"></a>Crear empresas de contacto
Puede crear un contacto por cada nueva empresa con la que se relacione, como puede ser un cliente, un proveedor, un posible cliente, un banco, un despacho de abogados, una consultora, etc.

Existen dos formas de crear un contacto: desde cero o a partir de un cliente, proveedor o cuenta bancaria existente.

Antes de crear un contacto, es posible que desee comprobar la configuración de la página **Configuración marketing**. Para obtener más información, consulte [Configurar la gestión de relaciones](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Para crear un contacto de compañía desde cero
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **N.º de campo** introduzca un número para el contacto.

    Por otra parte, si configuró un número de serie para los contactos de la página **Configuración marketing**, puede pulsar Entrar para hacer que el sistema especifique el siguiente número de contacto disponible.  
4. Establezca **Tipo** en **Empresa**.
5. Rellene los demás campos según sea necesario.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Para crear un contacto desde un cliente, proveedor o banco
Si ya configuró un cierto número de clientes, proveedores o bancos, podrá crear contactos según los datos existentes. Al crear un contacto de esta manera, la información de contacto se sincroniza con la información del cliente, proveedor o de la cuenta bancaria.

> [!NOTE]  
>   Para poder crear empresas de contacto, es necesario especificar un código de relación de negocio para los clientes, proveedores y las cuentas bancarias en la página **Configuración de marketing**. Si va a crear contactos a partir de cuentas bancarias, también debe especificar números de serie para las cuentas bancarias en la página **Configuración de contabilidad**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), especifique una de las siguientes opciones, según la ubicación desde la cual desee crear contactos y, a continuación, elija el vínculo relacionado.
   * **Crear Contactos desde Clientes**
   * **Crear contactos desde proveedores**
   * **Crear contactos desde bancos**
2. En la página del proceso que se abre, establezca filtros en la sección **Cliente**, **Proveedor** o **Banco** si desea crear contactos solo desde determinados clientes, proveedores o bancos.
3. Para crear contactos, seleccione **Aceptar**.

    Los siguientes números de contacto de la serie se asignan a los nuevos contactos. El programa asigna la relación comercial para proveedores especificada en la página **Configuración marketing** a los contactos recién creados.

> [!TIP]  
>   También puede crear un cliente, proveedor o una cuenta bancaria a partir de un contacto. Para obtener más información, consulte [Crear un cliente, proveedor o cuenta bancaria a partir de un contacto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Sincronizar contactos con clientes, proveedores y cuentas bancarias
Si algunos contactos también son clientes, proveedores o bancos, podrá sincronizar la información de contacto con el cliente, proveedor o la cuenta bancaria relacionados. La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.  

Antes de sincronizar los contactos con los clientes, proveedores o bancos, debe especificar un código de relación de negocio para clientes, proveedores y bancos en la página **Configuración de marketing**. Para obtener más información, consulte [Configurar la gestión de relaciones](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Formas distintas de sincronizar contactos con clientes, proveedores y cuentas bancarias
Puede sincronizar sus contactos con clientes, proveedores o bancos mediante tres métodos:

* relacionar los contactos relacionados con clientes existentes, proveedores o bancos de la ficha de contacto. Para obtener más información, consulte [Vincular contactos con clientes, proveedores y cuentas bancarias](marketing-how-link-contact.md).
* Crear clientes, proveedores o cuentas bancarias a partir del contacto. Para obtener más información, consulte [Crear un cliente, proveedor o cuenta bancaria a partir de un contacto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Crear contactos a partir de clientes, proveedores o bancos: Para obtener más información, consulte [Crear un contacto de empresa a partir de un cliente, proveedor o una cuenta bancaria](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Consecuencias de la sincronización
Al sincronizar el contacto con el cliente, el proveedor o la cuenta bancaria:

* Solo es necesario actualizar la información en una de ellas. Por ejemplo, si modifica el número de teléfono del contacto, dicho número se actualizará automáticamente para reflejar la modificación en el cliente, el proveedor o la cuenta bancaria.
* Si especificó un número de serie para los contactos y crea una ficha de cliente, proveedor o banco, se creará automáticamente una ficha de contacto para el cliente, proveedor o banco.
* Puede crear ofertas de venta y pedidos, y obtenerlos desde el contacto.
* Puede hacer que se registren sus interacciones al llevar a cabo acciones como imprimir o abrir pedidos, crear pedidos de servicio, enviar correos electrónicos, etc.
* Si elimina un contacto relacionado con un cliente, proveedor o banco, solo se borra del sistema el contacto. El cliente, el proveedor o la cuenta bancaria permanece.
* Si elimina un cliente, proveedor o banco relacionado con un contacto, el contacto permanecerá.

> [!NOTE]  
>   Algunos detalles, como los datos de facturación y registro, no aparecen en la ficha de contacto. Por tanto, puede que desee agregarlos manualmente en la ficha de cliente, de proveedor o de banco al crear contactos como clientes, proveedores o bancos.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Vincular contactos con clientes, proveedores y bancos
Si tiene un contacto y un cliente, proveedor o cuenta bancaria de la misma empresa, puede vincular las dos entidades. Al vincular las dos entidades, se pueden sincronizar los datos que son comunes para que sean los mismos en ambos sitios.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Para vincular un contacto con un cliente, proveedor o cuenta bancaria existente
1. Abra el contacto que quiere vincular.
2. Elija la acción **Vincular con** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.
3. Seleccione el cliente, el proveedor o la cuenta bancaria al que quiere vincular el contacto.

   En los **Campos principales actuales**, especifique los campos a los que el sistema debe dar prioridad en caso de información conflictiva de los campos comunes al contacto y cliente, vendedor o cuenta. Por ejemplo, si el código de vendedor es diferente entre el contacto y el cliente, seleccione **Contacto** para definir que la información válida es la de la ficha de contacto.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Crear un contacto, proveedor o una cuenta bancaria a partir de un contacto
   Puede que desee registrar algunos de sus contactos existentes como clientes, proveedores o bancos. Crear un cliente, un proveedor o una cuenta bancaria a partir de un contacto le permite usar datos existentes. Al crear un cliente, proveedor o cuenta bancaria de esta forma, se sincroniza con el contacto. La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.

   Para poder registrar los contactos de esta forma, es necesario especificar un código de relación de negocio para los clientes, proveedores y las cuentas bancarias en la página **Configuración de marketing**. Si va a registrar contactos como cuentas bancarias, también debe especificar números de serie para las cuentas bancarias en la página **Configuración de contabilidad**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Para crear un contacto como cliente, proveedor o banco
   1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
   2. Seleccione el contacto que desea crear como cliente, proveedor o banco.
   3. Elija la acción **Crear como** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.
   4. Confirme el mensaje que aparece después.

   La información de contacto se transfiere desde la ficha **Contacto** a la ficha **Cuenta bancaria**, en la ficha **Cliente** o en la ficha **Proveedor**. Tal vez desee agregar información específica a cada una de las fichas, como detalles de facturación y de pago.

## <a name="setting-up-business-relations-on-contact-companies"></a>Configurar relaciones de negocio en empresas de contacto
Puede usar relaciones de negocio se usan para indicar las relaciones de ese tipo con los contactos, por ejemplo, referencia, banco, consultora, proveedor de servicios, etc.

El uso relaciones de negocio en contactos es un proceso que consta de dos pasos. Primero, debe definir el código de relación de negocio. Solo debe realizar este paso una vez para cada relación de negocio. Una vez tenga un código de relación de negocio, puede comenzar a asignar el código a empresas de contacto.

> [!NOTE]  
>   Si desea sincronizar sus contactos con proveedores, clientes o bancos en otras partes de la aplicación, se recomienda configurar una relación de negocio para ellos.

### <a name="to-define-a-business-relation-code"></a>Para definir un código de relación de negocio
El código de relación de negocio define una categoría o un tipo de relación de negocio, como BANCO o ABO. Puede tener varios códigos de relación de negocio. Para definir relaciones de negocio, use la página **Relaciones de negocio**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Relaciones negocio** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

### <a name="AssignBusRelContact"></a> Para asignar relaciones de negocio a un contacto
No puede asignar relaciones de contacto a una persona de contacto, solo a empresas.

1. Abra el contacto.
2. Seleccione la acción **Empresa** y, a continuación, seleccione la acción **Relaciones de negocio**.

    Se abre la página **Relaciones de negocio de contacto**.
3. En el campo **Cód. relación negocio**, seleccione la relación de negocio que desea asignar.

Repita estos pasos para asignar todos las relaciones de negocio que desee. También puede asignar relaciones de negocio desde la lista de contactos con el mismo procedimiento.

Aparece automáticamente el número de relaciones de negocio asignadas al contacto del campo **N.º de relaciones de negocio** en la sección **Segmentación** de la página **Contacto**.

Después de asignar relaciones de negocio a sus contactos, puede utilizar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="see-also"></a>Consulte también
[Crear personas de contacto](marketing-create-contact-persons.md)   
[Trabajar con Business Central](ui-work-product.md)

