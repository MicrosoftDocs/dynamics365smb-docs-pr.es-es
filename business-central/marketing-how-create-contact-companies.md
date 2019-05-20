---
title: Crear empresas de contacto | Documentos de Microsoft
description: Describe cómo crear un contacto para cada nueva empresa o empresa potencial con la que interactúe o tenga una relación.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 67945b8825ae94ff3a09a4072309c401abb41c6b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238468"
---
# <a name="create-contacts"></a>Crear contactos
Puede crear un contacto por cada nueva empresa con la que se relacione, como puede ser un cliente, un proveedor, un posible cliente, un banco, un despacho de abogados, una consultora, etc.

Existen dos formas de crear un contacto: desde cero o a partir de un cliente, proveedor o cuenta bancaria existente.

## <a name="create-a-company-contact-from-scratch"></a>Crear un contacto de compañía desde cero
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **N.º de campo** introduzca un número para el contacto.

    Por otra parte, si configuró un número de serie para los contactos de la página **Configuración marketing**, puede pulsar Entrar para hacer que el sistema especifique el siguiente número de contacto disponible.  
4. Establezca **Tipo** en **Empresa**.
5. Rellene los demás campos según sea necesario.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Para crear un contacto desde un cliente, proveedor o banco
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

## <a name="see-also"></a>Consulte también
[Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Asignar relaciones de negocio a un contacto](marketing-business-relations.md#AssignBusRelContact)  
[Para asignar grupos de industria a un contacto](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Asignar grupos de correo a un contacto](marketing-mailing-groups.md#AssignMailGroupContact)  
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Trabajar con Business Central](ui-work-product.md)
