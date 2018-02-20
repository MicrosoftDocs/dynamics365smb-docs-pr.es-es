---
title: Crear un cliente o un proveedor a partir de un contacto | Documentos de Microsoft
description: "Puede registrar un contacto existente como cuenta de cliente, proveedor o banco usando datos existentes y especificando una relación de negocio."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0c4cf74ef7b0b2e48a8608a0859a71b919e46397
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="create-a-customer-vendor-or-bank-account-from-a-contact"></a>Crear un contacto, proveedor o una cuenta bancaria a partir de un contacto
Puede que desee registrar algunos de sus contactos existentes como clientes, proveedores o bancos. Crear un cliente, un proveedor o una cuenta bancaria a partir de un contacto le permite usar datos existentes. Al crear un cliente, proveedor o cuenta bancaria de esta forma, se sincroniza con el contacto. La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.

Para poder registrar los contactos de esta forma, es necesario especificar un código de relación de negocio para los clientes, proveedores y las cuentas bancarias en la ventana **Configuración de marketing**. Si va a registrar contactos como cuentas bancarias, también debe especificar números de serie para las cuentas bancarias en la ventana **Configuración de contabilidad**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Para crear un contacto como cliente, proveedor o banco
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Contactos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el contacto que desea crear como cliente, proveedor o banco.
3. Elija la acción **Crear como** y, a continuación, elija **Cliente**, **Proveedor** o **Banco**.
4. Confirme el mensaje que aparece después.

La información de contacto se transfiere desde la ficha **Contacto** a la ficha **Cuenta bancaria**, en la ficha **Cliente** o en la ficha **Proveedor**. Tal vez desee agregar información específica a cada una de las fichas, como detalles de facturación y de pago.

## <a name="see-also"></a>Consulte también
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Configurar la gestión de relaciones](marketing-setup-marketing.md)  
[Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Vincular contactos con clientes, proveedores o cuentas bancarias existentes](marketing-how-link-contact.md)  
[Asignar relaciones de negocio a un contacto](marketing-business-relations.md#AssignBusRelContact)  
[Trabajar con Finance and Operations, Business edition](ui-work-product.md)

