---
title: Crear un cliente o un proveedor a partir de un contacto | Documentos de Microsoft
description: Puede registrar un contacto existente como cuenta de cliente, proveedor o banco usando datos existentes y especificando una relación de negocio.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ccddaa5d1c1a5a31c6b82b99520b90bb28fe64dd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "937875"
---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Crear un contacto, proveedor o una cuenta bancaria a partir de un contacto
Puede que desee registrar algunos de sus contactos existentes como clientes, proveedores o bancos. Crear un cliente, un proveedor o una cuenta bancaria a partir de un contacto le permite usar datos existentes. Al crear un cliente, proveedor o cuenta bancaria de esta forma, se sincroniza con el contacto. La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.

Para poder registrar los contactos de esta forma, es necesario especificar un código de relación de negocio para los clientes, proveedores y las cuentas bancarias en la página **Configuración de marketing**. Si va a registrar contactos como cuentas bancarias, también debe especificar números de serie para las cuentas bancarias en la página **Configuración de contabilidad**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Para crear un contacto como cliente, proveedor o banco
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Contactos** y luego elija el enlace relacionado.
2. Seleccione el contacto que desea crear como cliente, proveedor o banco.
3. Elija la acción **Crear como** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.
4. Confirme el mensaje que aparece después.

La información de contacto se transfiere desde la ficha **Contacto** a la ficha **Cuenta bancaria**, en la ficha **Cliente** o en la ficha **Proveedor**. Tal vez desee agregar información específica a cada una de las fichas, como detalles de facturación y de pago.

## <a name="see-also"></a>Consulte también
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Vincular contactos con clientes, proveedores o cuentas bancarias existentes](marketing-how-link-contact.md)  
[Asignar relaciones de negocio a un contacto](marketing-business-relations.md#AssignBusRelContact)  
[Trabajar con Business Central](ui-work-product.md)
