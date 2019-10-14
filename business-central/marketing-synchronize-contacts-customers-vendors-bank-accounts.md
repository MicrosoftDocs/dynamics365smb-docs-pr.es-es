---
title: Sincronizar contactos con clientes y proveedores | Documentos de Microsoft
description: Puede acoplar o sincronizar la información de contacto de los contactos que también son clientes, proveedores o cuentas bancarias, de modo que actualice únicamente la información en un solo lugar.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 10/01/2019
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: f102b6dac47732d96aff8413697c172fbea3f687
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308649"
---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Sincronizar contactos con clientes, proveedores y cuentas bancarias
Si algunos contactos también son clientes, proveedores o bancos, podrá sincronizar la información de contacto con el cliente, proveedor o la cuenta bancaria relacionados. La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.  

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Formas distintas de sincronizar contactos con clientes, proveedores y cuentas bancarias
Puede sincronizar sus contactos con clientes, proveedores o bancos mediante tres métodos:

* relacionar los contactos relacionados con clientes existentes, proveedores o bancos de la ficha de contacto. Para obtener más información, consulte [Vincular contactos con clientes, proveedores y cuentas bancarias](marketing-how-link-contact.md).
* Crear clientes, proveedores o cuentas bancarias a partir del contacto. Para obtener más información, consulte [Crear un cliente, proveedor o cuenta bancaria a partir de un contacto](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Crear contactos a partir de clientes, proveedores o bancos: Para obtener más información, consulte [Crear un contacto de empresa a partir de un cliente, proveedor o una cuenta bancaria](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Consecuencias de la sincronización
Al sincronizar el contacto con el cliente, el proveedor o la cuenta bancaria:

* Solo es necesario actualizar la información en una de ellas. Por ejemplo, si modifica el número de teléfono del contacto, dicho número se actualizará automáticamente para reflejar la modificación en el cliente, el proveedor o la cuenta bancaria.
* Si especificó un número de serie para los contactos y crea una ficha de cliente, proveedor o banco, se creará automáticamente una ficha de contacto para el cliente, proveedor o banco.
* Puede crear ofertas de venta y pedidos, y obtenerlos desde el contacto.
* Puede hacer que se registren sus interacciones al llevar a cabo acciones como imprimir o abrir pedidos, crear pedidos de servicio, enviar correos electrónicos, etc.
* Si elimina un contacto relacionado con un cliente, proveedor o banco, solo se borra del sistema el contacto. El cliente, el proveedor o la cuenta bancaria permanece.
* Si elimina un cliente, proveedor o banco relacionado con un contacto, el contacto permanecerá.

> [!NOTE]  
>   Algunos detalles, como los datos de facturación y registro, no aparecen en la ficha de contacto. Por tanto, puede que desee agregarlos manualmente en la ficha de cliente, de proveedor o de banco al crear contactos como clientes, proveedores o bancos.

## <a name="see-also"></a>Consulte también
[Gestionar contactos](marketing-contacts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
