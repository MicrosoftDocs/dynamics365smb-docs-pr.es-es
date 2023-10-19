---
title: Sincronización e integración de datos | Documentos de Microsoft
description: 'La sincronización copia los datos entre las tablas de Microsoft Dataverse y los registros de Business Central, y mantiene actualizados los datos de ambos sistemas.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
---

# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Sincronización de datos en Business Central con Microsoft Dataverse

Cuando integra [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puede decidir si desea sincronizar los datos de campos seleccionados de [!INCLUDE[prod_short](includes/prod_short.md)] (como clientes, contactos y personal de ventas) con las filas equivalentes en [!INCLUDE[prod_short](includes/cds_long_md.md)] (como cuentas, contactos y usuarios). Dependiendo del tipo de fila, puede sincronizar datos de [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)], o viceversa. Para obtener más información, vea [Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronización utiliza los siguientes elementos:

* Lista de asignaciones de tablas de integración
* Asignaciones de campo de integración
* Reglas de sincronización
* Registros emparejados

Cuando la sincronización está configurada, puede emparejar filas de [!INCLUDE[prod_short](includes/prod_short.md)] con registros de [!INCLUDE[prod_short](includes/cds_long_md.md)] para sincronizar sus datos. Puede iniciar una sincronización manualmente o según una programación. La tabla siguiente proporciona un resumen de las formas en que puede sincronizar.  

|  Escriba  |  Método  |  Vea  |  
|--------|----------|-------|  
|Sincronización manual|Sincronizar en una base de fila a fila.<br /><br /> Puede sincronizar registros individuales en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, un cliente, con una fila de [!INCLUDE[prod_short](includes/cds_long_md.md)] correspondiente, por ejemplo, una cuenta. Normalmente, los usuarios trabajarán de esta manera con los datos de [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)].|[Emparejar y sincronizar registros manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Sincronizar sobre según la asignación de tablas.<br /><br /> Puede sincronizar todos los registros de una tabla de [!INCLUDE[prod_short](includes/prod_short.md)] con una tabla de [!INCLUDE[prod_short](includes/cds_long_md.md)].|[Sincronizar las asignaciones de tablas individuales](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Sincronizar todos los registros modificados para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los registros que se han modificado en las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] desde la última sincronización.|[Sincronización de todos los registros modificados](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Sincronización completa de todos los datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los datos de las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y tablas de [!INCLUDE[prod_short](includes/cds_long_md.md)] asignadas y crear nuevos registros en la solución de destino para los registros o filas desemparejados en la solución de origen.<br /><br /> La sincronización completa sincroniza todos los datos y omite el emparejamiento. Normalmente, se realiza una sincronización completa cuando se configura la integración y solo una de las soluciones contiene datos. Una sincronización completa también puede ser útil en un entorno de demostración.|[Ejecutar una sincronización completa](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Sincronización programada|Sincronizar todos los cambios en datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)] en intervalos programados configurando proyectos en la cola de proyectos.|[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> La sincronización entre [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)] se basa en la ejecución programada de las entradas de la cola de trabajos y no garantiza la coherencia de los datos en tiempo real entre dos servicios. Para obtener coherencia de datos en tiempo real, debe explorar [Mesas virtuales de Business Central](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) o API de Business Central.   

## <a name="standard-table-mapping-for-synchronization"></a>Asignación de tablas estándar para la sincronización

Las tablas en [!INCLUDE[prod_short](includes/cds_long_md.md)], como las cuentas, se integran con tipos equivalentes de tablas en [!INCLUDE[prod_short](includes/prod_short.md)], como los clientes. Para trabajar con datos de [!INCLUDE[prod_short](includes/cds_long_md.md)] se establecen vínculos, llamados emparejamientos, entre tablas en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)].

La siguiente tabla enumera la asignación estándar entre tablas en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Puede restablecer los cambios de configuración realizados en la tabla de integración y las asignaciones de campo a su configuración predeterminada, seleccionando las asignaciones y luego eligiendo **Usar la configuración de sincronización predeterminada**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Dirección de la sincronización | Filtro predeterminado |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Vendedor/Comprador | Usuario | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de contacto de [!INCLUDE[prod_short](includes/cds_long_md.md)]: **Estado** es **No**, **Usuario con licencia** es **Sí**, Modo de integración de usuario es **No** |
| Cliente | Cuenta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de cuenta de [!INCLUDE[prod_short](includes/cds_long_md.md)]: el **Tipo de relación** es **Cliente** y el **Estado** es **Activo**. Filtro de [!INCLUDE[prod_short](includes/prod_short.md)]: **Bloqueado** está vacío (Cliente no está bloqueado). |
| Proveedor | Cuenta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de cuenta de [!INCLUDE[prod_short](includes/cds_long_md.md)]: el **Tipo de relación** es **Proveedor** y el **Estado** es **Activo**. Filtro de [!INCLUDE[prod_short](includes/prod_short.md)]: **Bloqueado** está vacío (Proveedor no está bloqueado). |
| Contacto | Contacto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de contacto de [!INCLUDE[prod_short](includes/prod_short.md)]: el **tipo** es **Persona** y el contacto se asigna una empresa. Filtro de contacto de [!INCLUDE[prod_short](includes/cds_long_md.md)]: el contacto se asigna a una empresa y el tipo de cliente principal es **Cliente**. |
| Divisa | Divisa de la transacción | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> Las acciones de **Dataverse** no estarán disponibles en páginas, por ejemplo, la página Ficha de cliente, para registros que no respetan el filtro de tabla en la asignación de la tabla de integración.

### <a name="tip-for-admins-viewing-table-mappings"></a>Consejo para administradores: visualización de asignaciones de tabla

Puede ver la asignación entre las tablas en [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)] en la página **Lista de asignaciones de tablas de integración**, donde también puede aplicar filtros. La asignación entre los campos de las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y las columnas de las tablas de [!INCLUDE[prod_short](includes/cds_long_md.md)] se define en la página **Lista de asignaciones de campos de integración**, donde se puede añadir lógica de asignación adicional. Por ejemplo, esto puede ser útil si necesita solucionar problemas de sincronización.

## <a name="use-virtual-tables-to-get-more-data"></a>Utilice tablas virtuales para obtener más datos

Cuando configura su integración, puede usar tablas virtuales para que haya más datos disponibles en [!INCLUDE[prod_short](includes/cds_long_md.md)], sin la ayuda de un desarrollador.

Una tabla virtual es una tabla personalizada de que tiene columnas y filas que contienen datos de un origen de datos externo, como [!INCLUDE [prod_short](includes/prod_short.md)]. Las columnas y filas de una tabla virtual parecen una tabla normal; sin embargo, los datos no se almacenan en una tabla física en la base de datos [!INCLUDE[prod_short](includes/cds_long_md.md)]. En cambio, los datos se recuperan en tiempo de ejecución.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] contiene objetos que también se denominan tablas virtuales. Esos objetos de tabla no están relacionados con las tablas virtuales que usa con [!INCLUDE[prod_short](includes/cds_long_md.md)].

Para obtener más información sobre las tablas virtuales, consulte los siguientes artículos:

* [Crear y editar tablas virtuales que contienen datos desde un origen de datos externo](/power-apps/maker/data-platform/create-edit-virtual-entities) (documentación de Power Apps)
* [Tabla virtual de Business Central para Microsoft Dataverse, referencia administrativa](/business-central/dev-itpro/powerplatform/powerplat-admin-reference) (documentación de [!INCLUDE [prod_short](includes/prod_short.md)])

Para utilizar tablas virtuales, debe instalar la aplicación **Business Central Virtual Entity** desde [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

Después de instalar la aplicación, puede habilitar tablas virtuales desde una de las siguientes páginas en [!INCLUDE [prod_short](includes/prod_short.md)]:

* Cuando ejecuta la guía de configuración asistida de **Configurar conexión de Dataverse**, puede usar la página **Tablas virtuales de Dataverse disponibles** para seleccionar varias tablas virtuales. Luego, las tablas están disponibles en [!INCLUDE[prod_short](includes/cds_long_md.md)] y en el PowerApps Maker Portal. 
* Desde las páginas **Configuración de conexión de Dataverse**, **Tablas virtuales** y **Tablas virtuales disponibles**.  
* Desde Power App Maker Portal.

## <a name="synchronize-data-from-multiple-companies-or-environments"></a>Sincronice datos de múltiples empresas o entornos

Puede sincronizar datos de varias empresas o entornos de [!INCLUDE [prod_short](includes/prod_short.md)] con un entorno de [!INCLUDE[prod_short](includes/cds_long_md.md)]. En escenarios de sincronización de varias empresas, hay varias cosas a considerar.

### <a name="set-company-ids"></a>Establecer ID de empresa

Cuando sincroniza registros, configuramos un ID de empresa en la entidad [!INCLUDE[prod_short](includes/cds_long_md.md)] para aclarar la empresa [!INCLUDE [prod_short](includes/prod_short.md)] de dónde provienen los registros. Las asignaciones de tablas de integración tienen campos de filtro de tablas de integración que tienen en cuenta el ID de la empresa. Para incluir una asignación de tablas en una configuración de varias empresas, en la página **Asignación de tablas de integración**, elija la casilla de verificación **Sincronización multiempresa habilitada**. La configuración optimiza la forma en que los campos de filtro de la tabla de integración filtran los ID de empresa en una configuración de varias empresas.

Para asignaciones de tablas de integración que sincronizan documentos, como pedidos, cotizaciones y oportunidades, si elige la opción **Sincronización multiempresa habilitada**, la integración solo considera entidades que tienen el ID de empresa del actual [!INCLUDE [prod_short](includes/prod_short.md)] compañía. Para sincronizar documentos, por ejemplo, entre Business Central y Sales, los usuarios de Sales deben especificar el ID de la empresa en los documentos. De lo contrario, los documentos no se sincronizarán.  

Para todas las demás asignaciones de tablas de integración, elegir la casilla de verificación **Sincronización multiempresa habilitada** elimina el filtro por ID de empresa. La sincronización considerará entidades relacionadas, independientemente de su ID de empresa.

### <a name="specify-the-synchronization-direction"></a>Especifica la dirección de sincronización

Si habilita el soporte para varias empresas en una asignación de tabla de integración, le recomendamos que establezca la dirección de la asignación en **FromIntegration**. Si establece la dirección en **ToIntegration** o **Bidirectional**, es una buena idea utilizar **Filtro de tabla** y **Filtro de tabla de integración** para controlar qué entidades se sincronizan con qué empresa. También es una buena idea utilizar el acoplamiento basado en coincidencias para evitar la creación de registros duplicados. Para obtener más información sobre emparejamiento basado en coincidencias, vaya a [Personalizar el emparejamiento basado en coincidencias](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### <a name="use-unique-numbers"></a>Utilice números únicos

Si su serie numérica no garantiza que los valores de clave principal sean únicos para cada empresa, le recomendamos que utilice prefijos. Para comenzar a usar prefijos, cree una regla de transformación en la asignación de campos de integración. Para obtener más información sobre las reglas de transformación, vaya a [Gestionar diferencias en los valores de campo](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## <a name="see-also"></a>Consulte también

[Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
