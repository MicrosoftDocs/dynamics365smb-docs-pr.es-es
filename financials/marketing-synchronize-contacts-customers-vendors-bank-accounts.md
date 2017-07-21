---
title: Sincronizar contactos con clientes y proveedores | Documentos de Microsoft
description: "Puede acoplar o sincronizar la información de contacto de los contactos que también son clientes, proveedores o cuentas bancarias, de modo que actualice únicamente la información en un solo lugar."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: dbb29d9d53618eec69817455d4304da2a6bfe466
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Sincronizar contactos con clientes, proveedores y cuentas bancarias
Si algunos contactos también son clientes, proveedores o bancos, podrá sincronizar la información de contacto con el cliente, proveedor o la cuenta bancaria relacionados. La sincronización unifica la información que es común entre los contactos y los clientes, los proveedores o la cuenta bancaria.  

Antes de sincronizar los contactos con los clientes, proveedores o bancos, debe especificar un código de relación de negocio para clientes, proveedores y bancos en la ventana **Configuración de marketing**. Para obtener más información, consulte [Configurar la gestión de relaciones](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Formas distintas de sincronizar contactos con clientes, proveedores y cuentas bancarias
Puede sincronizar sus contactos con clientes, proveedores o bancos mediante tres métodos:

* relacionar los contactos relacionados con clientes existentes, proveedores o bancos de la ficha de contacto. Para obtener más información, consulte [Procedimiento: Vincular contactos con clientes, proveedores y cuentas bancarias](marketing-how-link-contact.md).
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

