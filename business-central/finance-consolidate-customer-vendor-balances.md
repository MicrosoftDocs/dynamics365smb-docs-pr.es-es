---
title: Consolidar saldos para una empresa que es un cliente y un proveedor
description: Describe cómo consolidar saldos para un cliente que también es un proveedor.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 06/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="consolidate-balances-for-a-company-that-is-a-customer-and-a-vendor"></a>Consolidar saldos para una empresa que es un cliente y un proveedor
Una empresa con la que hace negocios puede ser tanto un cliente como un proveedor. Cuando ese sea el caso, puede evitar hacer pagos o recibos innecesarios, y tal vez ahorrar en gastos de transacción, al consolidar los saldos de clientes y proveedores de la empresa. La consolidación compara los saldos de la empresa como proveedor y como cliente, y luego liquida el importe de modo que quede el saldo del cliente o del proveedor, según el importe que sea mayor. 

Para consolidar los saldos, primero debe vincular las empresas de cliente y de proveedor a través de un contacto que tenga el tipo **Empresa**. Un cliente o proveedor solo puede tener un contacto del tipo **Empresa**. Para obtener más información, consulte [Crear contactos](marketing-create-contact-companies.md).

Después de vincular las empresas, la página **Ficha cliente** ofrece el campo **Saldo como proveedor** y la página **Ficha proveedor** incluye el campo **Saldo como cliente**.

Aunque no es un requisito, las empresas de cliente y de proveedor suelen ser la misma entidad jurídica. 

## <a name="before-you-start"></a>Antes de comenzar
Antes de consolidar saldos, especifique algunas configuraciones en la página **Configuración de marketing**. 

* En la ficha desplegable **Interacciones**, debe especificar los códigos de relaciones de negocio en los campos **Clientes** y **Proveedores**. [!INCLUDE[prod_short](includes/prod_short.md)] utiliza esta información para determinar el tipo de relación que se mostrará para los contactos. 
* Opcional: En la ficha desplegable **Duplicados**, active o desactive la búsqueda de duplicados. De forma predeterminada, la búsqueda de duplicados está activada. Para obtener más información, consulte [Gestión de duplicados](#handling-duplicates). 

## <a name="link-an-existing-customer-and-vendor-company-through-a-contact"></a>Vincular una empresa de cliente y proveedor existente a través de un contacto
En los siguientes pasos se describe cómo vincular un cliente y un proveedor a través de un contacto.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cliente** o **Proveedor** y luego elija el enlace relacionado.
2. Elija el cliente o el proveedor y, a continuación, elija la acción **Contacto**.   
3. Seleccione el contacto y, a continuación, elija la acción **Vincular con existente**.
4. Elija el tipo de entidad con la que crear una relación comercial.
5. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="create-a-vendor-from-a-customer-or-vice-versa"></a>Crear un proveedor desde un cliente, o viceversa
Puede crear un nuevo proveedor a partir de un cliente existente o un nuevo cliente a partir de un proveedor. En las páginas **Cliente** o **Proveedor**, abra la página **Contacto**. Elija la acción **Crear como** y, a continuación, las opciones **Cliente** o **Proveedor**. 

## <a name="create-a-new-customer-or-vendor-and-link-them-through-a-vendor-or-customer-contact"></a>Crear un nuevo cliente o proveedor y vincularlos a través de un contacto de proveedor o cliente
1. Cree un nuevo cliente o proveedor. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).
2. Después de configurar el cliente o proveedor, elija la acción **Crear** y, a continuación, las opciones **Cliente** o **Proveedor**. 

## <a name="to-consolidate-the-customer-and-vendor-balances-for-a-contact-company"></a>Consolidar saldos del cliente y de proveedor para una empresa de contacto
En la página **Diario de pagos**, utilice la acción **Saldos netos cliente/proveedor** para consolidar los saldos de clientes y proveedores en un único importe neto. La acción crea, pero no registra, líneas de diario de pagos que contienen los saldos netos.

> [!NOTE]
> Si los saldos de clientes o proveedores contienen importes en distintas divisas, se crea una línea para el importe en cada divisa.

## <a name="handling-duplicates"></a>Gestión de duplicados
Si activa la búsqueda de duplicados en la ficha desplegable **Duplicados** en la página **Configuración de marketing**, se mostrará una advertencia cuando cambie los valores de los campos que forman parte de la configuración de cadenas de búsqueda duplicadas. Cuando se encuentra un duplicado, puede realizar las siguientes acciones:

* Combine los contactos duplicados en un único contacto que sea el mismo tanto para el cliente como para el proveedor mediante la capacidad **Combinar con** en la página **Ficha contacto**. Por lo general, la combinación de contactos se realiza solo cuando el cliente y el proveedor son la misma entidad jurídica. Para obtener más información, consulte [Combinar registros duplicados](sales-how-merge-duplicate-records.md). 
* Elimine la relación de negocio del proveedor para el contacto de proveedor o cliente y, a continuación, utilice la acción **Vincular a existente** para vincular a un contacto diferente.    

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)  
[Registrar nuevos clientes](sales-how-register-new-customers.md)  
