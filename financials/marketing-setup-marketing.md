---
title: "Configurar la información de administración de marketing y de contactos | Documentos de Microsoft"
description: "Puede configurar la administración de marketing y de contacto de Financials para optimizar las relaciones con los clientes potenciales o actuales, y mejorar las campañas y las promociones."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2f258a2bf1852b4cc1741a312c78bedfc06b5c11
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-relationship-management"></a>Configurar la gestión de relaciones
Antes de empezar a trabajar con sus contactos e intereses de marketing, hay algunas decisiones y pasos que debe tomar para configurar la manera en que el área de marketing administra ciertos aspectos de sus contactos. Por ejemplo, puede decidir si sincronizar la ficha de contacto con la ficha de cliente, proveedor o cuenta bancaria, cómo se definirán las series numéricas o qué saludo estándar se usará al escribir a sus contactos.

La gestión de contactos y el establecimiento de una estrategia para identificar, atraer y conservar a los clientes le ayudará a optimizar su negocio y a incrementar la satisfacción del cliente. Asimismo, el uso de un sistema adecuado de gestión de contactos será de gran ayuda en los procesos de creación y mantenimiento de relaciones con los clientes. La comunicación es la clave en estas relaciones. Para lograr el éxito, las empresas deben ser capaces de establecer la comunicación adecuada con sus clientes, proveedores y socios comerciales potenciales y existentes. El establecimiento de una estrategia sobre cómo utilizará la empresa la información de contactos es un paso fundamental. Esta información estará accesible para muchos grupos diferentes de su empresa, por lo que un sistema adecuado incrementará la productividad de todos los usuarios.

Puede configurar la gestión de marketing y de contactos desde la ventana **Configuración de marketing**. Para abrir la ventana **Configuración de marketing**, elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Configuración de marketing** y elija el vínculo relacionado.

## <a name="automatically-copying-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Copiar automáticamente información específica desde las empresas de contacto a las personas de contacto
Parte de la información de contacto de las empresas es la misma que la de las personas que trabajan allí, como la dirección. En la sección **Herencia** de la ventana **Configuración de marketing**, puede configurar la aplicación para que copie automáticamente campos específicos de la ficha de empresa de contacto a la ficha de persona de contacto cada vez que cree una persona de contacto de una empresa de contacto. Por ejemplo, puede seleccionar copiar el código de vendedor, los detalles de dirección (dirección, dirección 2, ciudad, código postal y provincia), los detalles de comunicación (número de fax, respuesta de télex y el número de teléfono) y más.

Al modificar uno de estos campos en la ficha Empresa de contacto, el programa modificará de forma automática el campo de la ficha Persona de contacto, a menos que ese campo se haya modificado manualmente.

Para obtener más información, consulte [Crear personas de contacto](marketing-how-create-contact-persons.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Usar valores predeterminados en contactos nuevos
Puede hacer que la aplicación asigne de forma automática ciertos códigos de idioma, territorio, vendedor y país/región como valores predeterminados para cada nuevo contacto. También se puede especificar un ciclo de ventas predeterminado que el sistema asignará de forma automática a cada nueva oportunidad creada.

La herencia de campos sobrescribe los valores predeterminados en la configuración. Por ejemplo, si el idioma predeterminado es el inglés, pero el de la empresa contacto es el alemán, el programa asignará automáticamente el alemán como idioma para las personas de contacto almacenadas de esa empresa.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Interacciones registradas automáticamente
[!INCLUDE[d365fin](includes/d365fin_md.md)] puede registrar automáticamente los documentos de compras y ventas como interacciones (por ejemplo, los pedidos, facturas, recibos, etc.), así como los correos electrónicos, las llamadas telefónicas y las hojas de portada.

Para obtener más información, vea [Registro automático de interacciones con contactos](marketing-auto-record-interactions.md)

## <a name="synchronizing-contacts-with-customers-and-more"></a>Sincronizar contactos con clientes, etc.
Para poder sincronizar la ficha del contacto con la del cliente, proveedor y banco, debe seleccionar un código de relación de negocio para clientes, proveedores y bancos. Por ejemplo, solo se puede enlazar un contacto con un cliente existente si seleccionó un código de relación de negocio para los clientes en la ventana **Configuración de marketing**.

Para obtener más información, consulte [Procedimiento: Sincronizar contactos con clientes, proveedores y cuentas bancarias](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Asignar una serie numérica a contactos y oportunidades
Puede configurar números de serie para contactos y oportunidades. Si ha configurado una serie numérica para contactos, cuando cree un contacto, pulse Entrar en el campo N.º de la ficha de contacto y el programa introduce automáticamente el siguiente número de contacto disponible.

Para obtener más información acerca de las series numéricas, consulte [Crear series numéricas](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Buscar contactos duplicados al crear contactos
Puede elegir que el sistema busque duplicados de forma automática cada vez que cree una empresa de contacto o buscarlos de forma manual después de crearlos. También puede hacer que el sistema actualice las cadenas de búsqueda de forma automática cada vez que se crea un contacto o se modifica su información. Puede elegir el porcentaje de acierto búsqueda, es decir, el porcentaje de cadenas idénticas que dos contactos deben tener para considerarlos duplicados.

## <a name="see-also"></a>Consulte también
[Gestionar contactos](marketing-contacts.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

