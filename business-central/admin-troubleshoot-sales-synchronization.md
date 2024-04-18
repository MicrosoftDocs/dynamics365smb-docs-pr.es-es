---
title: Solución de problemas de errores de sincronización
description: 'Este artículo proporciona orientación para identificar, solucionar problemas y resolver errores de sincronización.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/04/2024
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="troubleshoot-synchronization-errors"></a>Solucionar errores de sincronización

Hay muchos factores involucrados en la integración de [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)], y a veces las cosas salen mal. Este artículo señala algunos de los errores típicos que se producen y ofrece algunos consejos para corregirlos.

A menudo se producen errores, ya sea por algo que un usuario ha hecho a los registros emparejados o por algo que no funciona en la configuración de la integración. En el caso de los errores relacionados con los registros emparejados, los usuarios pueden resolverlos por sí mismos. A menudo estos errores se deben a acciones tales como eliminar datos en una aplicación empresarial, pero no en las dos, y después realizar la sincronización. Para obtener más información, consulte [Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md).

Los errores relacionados con la configuración de la integración suelen requerir la atención de un administrador. Puede ver estos errores en la página **Errores de sincronización de integración**. 

La siguiente tabla proporciona ejemplos de problemas típicos:  

|Problema  |Resolución  |
|---------|---------|
|Los permisos y los roles asignados al usuario de integración no son correctos. | Este error proviene de [!INCLUDE[prod_short](includes/cds_long_md.md)]y suele incluir el siguiente texto **Usuario principal (Id=\<user id>, type=8) falta el privilegio \<privilegeName>**. Este error ocurre porque al usuario de integración le falta un privilegio que le permite acceder a una entidad. Normalmente, este error ocurre si está sincronizando entidades personalizadas o si tiene una aplicación instalada en [!INCLUDE[prod_short](includes/cds_long_md.md)] que requiere permiso para acceder a otras entidades [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para resolver este error, asigne el permiso al usuario de integración en [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> Puede encontrar el nombre de usuario de integración en la página **Configuración de la conexión de Dataverse** página. El mensaje de error proporciona el nombre del permiso, que puede ayudarlo a identificar la entidad para la que necesita permiso. Para agregar el privilegio faltante, inicie sesión en [!INCLUDE[prod_short](includes/cds_long_md.md)] con una cuenta de administrador y edite el rol de seguridad asignado al usuario de integración. Para obtener más información, consulte [Crear o editar un rol de seguridad para administrar acceso](/power-platform/admin/create-edit-security-role). |
|Está acoplando un registro que usa otro registro que no está acoplado. Por ejemplo, un cliente cuya moneda no está acoplada o un artículo para el que la unidad de medida no está acoplada. | Primero debe emparejar el registro dependiente, por ejemplo, una divisa o unidad de medida y luego volver a intentar el emparejamiento. |
|La conexión con Dataverse se detuvo durante la sincronización. Por ejemplo, porque se agotó el tiempo de espera de su sesión. Cuando esto sucede, aparece el siguiente error al reanudar la sesión: _La conexión de tabla para el tipo de tabla CRM debe registrarse mediante RegisterTableConnection o el cmdlet New-NAVTableConnection antes de poder usarse._|* Para finalizaciones de tiempos de espera de sesión, actualice la página para volver a conectarse a Dataverse. El mensaje de error desaparece.<br><br>* Para un problema en el código, por ejemplo, si está utilizando una página personalizada para mostrar datos de una entidad de Dataverse, comuníquese con su socio o soporte de Microsoft. Cuando lo haga, utilice la acción **Copiar detalles** para compartir detalles sobre el error. |

Las siguientes son algunas herramientas en la página Errores de sincronización de integración que pueden ayudarlo a resolver estos problemas manualmente.  

* Los campos **Origen** y **Destino** pueden contener vínculos a la fila donde se encontró el error. Elija el vínculo para investigar el error.  
* Las acciones **Eliminar movs. anteriores a 7 días** y **Eliminar todos los movs.** limpian la lista. Normalmente, estas acciones se utilizan después de resolver la causa de un error que afecta a muchos registros. Sin embargo, preste atención. Estas acciones pueden eliminar errores que todavía son relevantes.
* La acción **Mostrar error de pila de llamadas** muestra información que puede ayudar a identificar la causa del error. Si no puede resolver el error usted mismo y decide enviar una solicitud de soporte, incluya la información en la solicitud de soporte.

## <a name="see-also"></a>Consulte también

[Integración con Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Configuración de cuentas de usuario para la integración con Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurar una conexión a Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md)  
[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
