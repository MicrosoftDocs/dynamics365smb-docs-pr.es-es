---
title: Modelos de propiedad de datos para la sincronización.
description: 'Las empresas son construcciones legales y comerciales, y se utilizan para proteger y visualizar datos comerciales.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'CDS, Dataverse, integration, sync'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="data-ownership-models-for-synchronization"></a>Modelos de propiedad de datos para la sincronización.

[!INCLUDE[prod_short](includes/cds_long_md.md)] requiere que especifique un propietario para los datos que almacena. Para más información, consulte [Tipos de tablas](/powerapps/maker/data-platform/types-of-entities) en la documentación de Power Apps. Cuando configura la integración entre [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)], debe elegir la propiedad **Usuario o equipo** para los registros que están sincronizados. Las acciones que se pueden realizar en estos registros se pueden controlar a nivel de usuario. <!--We recommend the Team ownership model because it makes it easier to manage ownership for multiple people.NO LONGER TRUE IN DATAVERSE-->

## <a name="team-ownership"></a>Propiedad de equipo
En [!INCLUDE[prod_short](includes/prod_short.md)], una empresa es una tabla legal y comercial que ofrece formas de proteger y visualizar datos comerciales. Los usuarios siempre trabajan en el contexto de una empresa. Lo más cerca que [!INCLUDE[prod_short](includes/cds_long_md.md)] llega a este concepto es la tabla de unidad de negocio, que no tiene implicaciones legales o comerciales.

Debido a que las unidades de negocio carecen de implicaciones legales y comerciales, no puede forzar una asignación uno a uno (1:1) para sincronizar los datos entre una empresa y una unidad de negocio, ya sea unidireccional o bidireccional. Para hacer posible la sincronización, cuando habilita la sincronización para una empresa en [!INCLUDE[prod_short](includes/prod_short.md)], lo siguiente sucede en [!INCLUDE[prod_short](includes/cds_long_md.md)]:

* Creamos una tabla de empresa que es equivalente a la tabla de empresa en [!INCLUDE[prod_short](includes/prod_short.md)]. El nombre de la empresa tiene el sufijo "BC Id. de empresa". Por ejemplo, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creamos una unidad de negocio predeterminada que tiene el mismo nombre que la empresa. Por ejemplo, Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Creamos un equipo de propietarios aparte con el mismo nombre que la empresa y lo asociamos con la unidad de negocios. El nombre del equipo tiene el prefijo "BCI -". Por ejemplo, BCI - Cronus International Ltd. (93555b1a-af3e-ea11-bb35-000d3a492db1).
* Los registros que se crean y sincronizan con [!INCLUDE[prod_short](includes/cds_long_md.md)] se asignan al equipo "Propietario de BCI" que está vinculado a la unidad de negocios.

> [!NOTE]
> Si cambia el nombre de una empresa en [!INCLUDE[prod_short](includes/prod_short.md)], no se actualizan los nombres de la empresa, el negocio y el equipo que creamos automáticamente en [!INCLUDE[prod_short](includes/cds_long_md.md)]. Debido a que solo se usa el id. de la empresa para la integración, esto no afecta a la sincronización. Si desea que los nombres coincidan, debe actualizar la empresa, la unidad de negocio y el equipo en [!INCLUDE[prod_short](includes/cds_long_md.md)].

La siguiente imagen muestra un ejemplo de esta configuración de datos en [!INCLUDE[prod_short](includes/cds_long_md.md)].

![La unidad de negocio raíz está en la parte superior, los equipos están en el centro y luego las empresas están en la parte inferior.](media/cds_bu_team_company.png)

En esta configuración, los registros relacionados con la empresa Cronus US serán propiedad de un equipo vinculado a la unidad de negocio Cronus US [!INCLUDE[prod_short](includes/cds_long_md.md)]. Los usuarios que pueden acceder a esa unidad de negocio a través de un rol de seguridad que se establece en la visibilidad de nivel de unidad de negocio [!INCLUDE[prod_short](includes/cds_long_md.md)] ahora pueden ver esos registros. En el siguiente ejemplo, se muestra cómo usar equipos para proporcionar acceso a esos registros.

* El rol de Gerente de ventas se asigna a los miembros del equipo de ventas de Cronus en EE. UU.
* Los usuarios que tienen el rol de Gerente de ventas pueden acceder a los registros de cuenta de los miembros de la misma unidad de negocio.
* El equipo de ventas de Cronus US está vinculado a la unidad de negocio de Cronus US que se mencionó anteriormente. Los miembros del equipo de ventas de Cronus US pueden ver cualquier cuenta que sea propiedad del usuario de Cronus US, que habría venido de la tabla de la empresa Cronus US en [!INCLUDE[prod_short](includes/prod_short.md)].

Sin embargo, la asignación 1:1 entre la unidad de negocio, la empresa y el equipo es solo un punto de partida, como se muestra en la siguiente imagen.

![El rol de seguridad controla la visibilidad de los datos.](media/cds_bu_team_company_2.png)

En este ejemplo, se crea una nueva unidad de negocio raíz EUR (Europa) en [!INCLUDE[prod_short](includes/cds_long_md.md)] como padre tanto de Cronus DE (Alemania) como Cronus ES (España). La unidad de negocio EUR no está relacionada con la sincronización. Sin embargo, puede dar a los miembros del equipo de ventas de EUR acceso a los datos de la cuenta tanto en Cronus DE como en Cronus ES configurando la visibilidad de los datos en **BU padre/hijo** en el rol de seguridad asociado en [!INCLUDE[prod_short](includes/cds_long_md.md)].

La sincronización determina qué equipo debe poseer los registros. Esto se controla mediante el campo **Equipo propietario predeterminado** de la fila BCI. Cuando un registro BCI se habilita para la sincronización, creamos automáticamente la unidad de negocio asociada y el equipo propietario (si aún no existe) y configuramos el campo **Equipo propietario predeterminado**. Cuando la sincronización está habilitada para una tabla, los administradores pueden cambiar el equipo propietario, pero siempre se debe asignar un equipo.

> [!NOTE]
> Los registros se vuelven de solo lectura después de agregar y guardar una empresa, así que asegúrese de elegir la empresa correcta.

## <a name="choosing-a-different-business-unit"></a>Elegir una unidad de negocio diferente
Puede cambiar la selección de la unidad de negocio si está utilizando el modelo de propiedad de Teams. Si utiliza el modelo de propiedad de Persona, la unidad de negocio predeterminada siempre está seleccionada. 

Si elige otra unidad de negocio, por ejemplo, una que haya creado anteriormente en [!INCLUDE[prod_short](includes/cds_long_md.md)], mantendrá su nombre original. Es decir, no tendrá el sufijo del id. de empresa. Crearemos un equipo que utilice la convención de nomenclatura.

Al cambiar una unidad de negocio, puede elegir solo las unidades de negocio que están un nivel por debajo de la unidad de negocio raíz.

## <a name="person-ownership"></a>Propiedad de persona
Si elige el modelo de propiedad de persona, debe especificar cada vendedor que será propietario de los nuevos registros. La unidad de negocio y el equipo se crean como se describe en la sección [Propiedad de equipo](admin-cds-company-concept.md#team-ownership).

La unidad de negocio predeterminada se utiliza cuando se elige el modelo de propiedad Persona y no puede elegir otra unidad de negocio. El equipo asociado con la unidad de negocio predeterminada será propietario de registros de tablas comunes, como la tabla de Producto, que no están relacionadas con vendedores específicos.

Cuando empareja a vendedores de [!INCLUDE[prod_short](includes/prod_short.md)] con usuarios de [!INCLUDE[prod_short](includes/cds_long_md.md)], [!INCLUDE[prod_short](includes/prod_short.md)] agregará el usuario al equipo predeterminado en [!INCLUDE[prod_short](includes/cds_long_md.md)]. Puede verificar que los usuarios se agregan mirando la columna **Miembro del equipo predeterminado** de la página **Usuarios - Common Data Service**. Si no se agrega el usuario, puede agregarlo manualmente utilizando la acción **Agregar usuarios acoplados al equipo**. Para obtener más información, consulte [Sincronizar datos de Business Central con Dataverse](admin-synchronizing-business-central-and-sales.md).

## <a name="see-also"></a>Consulte también
[Acerca de [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-common-data-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
