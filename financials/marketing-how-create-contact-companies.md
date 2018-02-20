---
title: Crear empresas de contacto | Documentos de Microsoft
description: "Describe cómo crear un contacto para cada nueva empresa o empresa potencial con la que interactúe o tenga una relación."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ed0f75f1e0ee8a282b58458e4fed3b4eef7c46fb
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="create-contact-companies"></a>Crear empresas de contacto
Puede crear un contacto por cada nueva empresa con la que se relacione, como puede ser un cliente, un proveedor, un posible cliente, un banco, un despacho de abogados, una consultora, etc.

Existen dos formas de crear un contacto: desde cero o a partir de un cliente, proveedor o cuenta bancaria existente.

Antes de crear un contacto, es posible que desee comprobar la configuración de la ventana **Configuración marketing**. Para obtener más información, consulte [Configurar la gestión de relaciones](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Crear un contacto de compañía desde cero
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contactos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **N.º de campo** introduzca un número para el contacto.

    Por otra parte, si configuró un número de serie para los contactos de la ventana **Configuración marketing**, puede pulsar Entrar para hacer que el sistema especifique el siguiente número de contacto disponible.  
4. Establezca **Tipo** en **Empresa**.
5. Rellene los demás campos según sea necesario.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Para crear un contacto desde un cliente, proveedor o banco
Si ya configuró un cierto número de clientes, proveedores o bancos, podrá crear contactos según los datos existentes. Al crear un contacto de esta manera, la información de contacto se sincroniza con la información del cliente, proveedor o de la cuenta bancaria.

> [!NOTE]  
>   Para poder crear empresas de contacto, es necesario especificar un código de relación de negocio para los clientes, proveedores y las cuentas bancarias en la ventana **Configuración de marketing**. Si va a crear contactos a partir de cuentas bancarias, también debe especificar números de serie para las cuentas bancarias en la ventana **Configuración de contabilidad**.

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique una de las siguientes opciones, según la ubicación desde la cual desee crear contactos y, a continuación, elija el vínculo relacionado.
   * **Crear Contactos desde Clientes**
   * **Crear Contactos desde Provs**
   * **Crear Contactos desde Bancos**
2. En la ventana del proceso que se abre, establezca filtros en la sección **Cliente**, **Proveedor** o **Banco** si desea crear contactos solo desde determinados clientes, proveedores o bancos.
3. Para crear contactos, seleccione **Aceptar**.

    Los siguientes números de contacto de la serie se asignan a los nuevos contactos. El programa asigna la relación comercial para proveedores especificada en la ventana **Configuración marketing** a los contactos recién creados.

> [!TIP]  
>   También puede crear un cliente, proveedor o una cuenta bancaria a partir de un contacto. Para obtener más información, consulte [Crear un cliente, proveedor o cuenta bancaria a partir de un contacto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Consulte también
[Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Asignar relaciones de negocio a un contacto](marketing-business-relations.md#AssignBusRelContact)  
[Para asignar grupos de industria a un contacto](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Asignar grupos de correo a un contacto](marketing-mailing-groups.md#AssignMailGroupContact)  
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Trabajar con Finance and Operations, Business edition](ui-work-product.md)

