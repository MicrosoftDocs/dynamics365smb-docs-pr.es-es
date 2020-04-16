---
title: Asignación de empresas y unidades de negocio | Microsoft Docs
description: Las empresas son construcciones legales y comerciales, y se utilizan para proteger y visualizar datos comerciales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: CDS, Common Data Service, integration, sync
ms.date: 01/17/2020
ms.author: bholtorf
ms.openlocfilehash: ccd371711a53c598279fcc981c5581be5ee9bdaf
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196895"
---
# <a name="data-ownership-models"></a>Modelos de propiedad de datos
[!INCLUDE[d365fin](includes/cds_long_md.md)] requiere que especifique un propietario para los datos que almacena. Para más información, vea [Propiedad de la entidad](https://docs.microsoft.com/powerapps/maker/common-data-service/types-of-entities#entity-ownership) en la documentación de Power Apps. Cuando configura la integración entre [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)], debe elegir uno de los dos modelos de propiedad para los registros que están sincronizados:

* Equipo 
* Persona (usuario)

Las acciones que se pueden realizar en estos registros se pueden controlar a nivel de usuario. Para más información, vea [Entidades de usuario y equipo](https://docs.microsoft.com/powerapps/developer/common-data-service/user-team-entities). Recomendamos el modelo de propiedad Equipo porque facilita la administración de la propiedad de varias personas.

## <a name="team-ownership"></a>Propiedad de equipo
En [!INCLUDE[d365fin](includes/d365fin_md.md)], una empresa es una entidad legal y comercial que ofrece formas de proteger y visualizar datos comerciales. Los usuarios siempre trabajan en el contexto de una empresa. Lo más cerca que [!INCLUDE[d365fin](includes/cds_long_md.md)] llega a este concepto es la entidad de unidad de negocio, que no tiene implicaciones legales o comerciales.

Debido a que las unidades de negocio carecen de implicaciones legales y comerciales, no puede forzar una asignación uno a uno (1:1) para sincronizar los datos entre una empresa y una unidad de negocio, ya sea unidireccional o bidireccional. Para hacer posible la sincronización, cuando habilita la sincronización para una empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)], lo siguiente sucede en [!INCLUDE[d365fin](includes/cds_long_md.md)]:

* Creamos una entidad de empresa que es equivalente a la entidad de empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El nombre de la empresa tiene el sufijo "BC Id. de empresa". Por ejemplo, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creamos una unidad de negocio predeterminada que tiene el mismo nombre que la empresa. Por ejemplo, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creamos un equipo de propietarios aparte con el mismo nombre que la empresa y lo asociamos con la unidad de negocios. El nombre del equipo tiene el prefijo "BCI -". Por ejemplo, BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Los registros que se crean y sincronizan con [!INCLUDE[d365fin](includes/cds_long_md.md)] se asignan al equipo "Propietario de BCI" que está vinculado a la unidad de negocios.

La siguiente imagen muestra un ejemplo de esta configuración de datos en [!INCLUDE[d365fin](includes/cds_long_md.md)].

![La unidad de negocio raíz está en la parte superior, los equipos están en el centro y luego las empresas están en la parte inferior.](media/cds_bu_team_company.png)

En esta configuración, los registros relacionados con la empresa Cronus US serán propiedad de un equipo vinculado a la unidad de negocio Cronus US <ID> en [!INCLUDE[d365fin](includes/cds_long_md.md)]. Los usuarios que pueden acceder a esa unidad de negocio a través de un rol de seguridad que se establece en la visibilidad de nivel de unidad de negocio [!INCLUDE[d365fin](includes/cds_long_md.md)] ahora pueden ver esos registros. En el siguiente ejemplo, se muestra cómo usar equipos para proporcionar acceso a esos registros.

* El rol de Gerente de ventas se asigna a los miembros del equipo de ventas de Cronus en EE. UU.
* Los usuarios que tienen el rol de Gerente de ventas pueden acceder a los registros de cuenta de los miembros de la misma unidad de negocio.
* El equipo de ventas de Cronus US está vinculado a la unidad de negocio de Cronus US que se mencionó anteriormente. Los miembros del equipo de ventas de Cronus US pueden ver cualquier cuenta que sea propiedad del usuario de Cronus US <ID>, que habría venido de la entidad de la empresa Cronus US en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Sin embargo, la asignación 1:1 entre la unidad de negocio, la empresa y el equipo es solo un punto de partida, como se muestra en la siguiente imagen.

![El rol de seguridad controla la visibilidad de los datos.](media/cds_bu_team_company_2.png)

En este ejemplo, se crea una nueva unidad de negocio raíz EUR (Europa) en [!INCLUDE[d365fin](includes/cds_long_md.md)] como padre tanto de Cronus DE (Alemania) como Cronus ES (España). La unidad de negocio EUR no está relacionada con la sincronización. Sin embargo, puede dar a los miembros del equipo de ventas de EUR acceso a los datos de la cuenta tanto en Cronus DE como en Cronus ES configurando la visibilidad de los datos en **BU padre/hijo** en el rol de seguridad asociado en [!INCLUDE[d365fin](includes/cds_long_md.md)].

La sincronización determina qué equipo debe poseer los registros. Esto se controla mediante el campo **Equipo propietario predeterminado** del registro BCI - <ID>. Cuando un registro BCI - <ID> se habilita para la sincronización, creamos automáticamente la unidad de negocio asociada y el equipo propietario (si aún no existe) y configuramos el campo **Equipo propietario predeterminado**. Cuando la sincronización está habilitada para una entidad, los administradores pueden cambiar el equipo propietario, pero siempre se debe asignar un equipo.

> [!NOTE]
> Los registros se vuelven de solo lectura después de agregar y guardar una empresa, así que asegúrese de elegir la empresa correcta.

### <a name="choosing-a-different-business-unit"></a>Elegir una unidad de negocio diferente
Puede modificar la selección de unidad de negocio. Si elige otra unidad, por ejemplo, una que haya creado anteriormente en CDS, mantendrá su nombre original. Es decir, no tendrá el sufijo del id. de empresa. Crearemos un equipo que utilice la convención de nomenclatura.

## <a name="person-ownership"></a>Propiedad de persona
Si elige el modelo de propiedad de persona, debe especificar cada vendedor que será propietario de los nuevos registros. La unidad de negocio y el equipo se crean como se describe en la sección anterior.  

## <a name="see-also"></a>Consulte también
[Acerca de [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-common-data-service.md)