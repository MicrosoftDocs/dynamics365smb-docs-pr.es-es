---
title: Asignar o editar los permisos de usuario | Documentos de Microsoft
description: "Describe cómo agregar usuarios de Office 365 a Business Central y asignarles permisos, derechos de acceso y opciones de seguridad."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 05/24/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: 443c04799e9aa2b9aa4ede15006ecb5e9773ce6b
ms.contentlocale: es-es
ms.lasthandoff: 05/28/2018

---
# <a name="manage-users-and-permissions"></a>Gestionar usuarios y permisos
Para agregar usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador de Office 365 de la empresa primero debe crear los usuarios en el centro de administración de Office 365. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Una vez se hayan creado los usuarios en Office 365, se pueden importar en la ventana **Usuarios** mediante la acción **Obtener usuarios desde Office 365**. A los usuarios se les asignan conjuntos de permisos según el plan asignado al usuario en Office 365.

Después podrá asignar conjuntos de permisos a los usuarios para definir a qué objetos de base de datos y, por lo tanto, a qué elementos de la interfaz de usuario, tienen acceso y en qué empresas. Puede agregar usuarios a grupos de usuarios. Esto facilita asignar los mismos conjuntos de permisos a varios usuarios.

Un conjunto de permisos es una colección de permisos para objetos específicos de la base de datos. A todos los usuarios se les debe asignar uno o varios conjuntos de permisos antes de que pueden acceder a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Un número de conjuntos de permisos predefinidos se proporcionan de forma predeterminada.  

Los administradores pueden usar la ventana **Configuración usuarios** para definir periodos de tiempo durante los que los usuarios especificados pueden registrar, así como especificar si el sistema registra la cantidad de tiempo que los usuarios tienen iniciada la sesión.

Otro sistema que define qué usuarios pueden acceder es la configuración de Experiencia. Para obtener más información, consulte [Cambiar las funciones que se muestran](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Para asignar permisos a un usuario
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Usuarios** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el usuario al que desea asignar el permiso.
Los conjuntos de permisos ya asignados al usuario se muestran en el cuadro informativo **Conjuntos de permisos**.
3. Seleccione la acción **Editar** para abrir la ventana **Ficha de usuario**.
4. En la ficha desplegable **Conjuntos de permisos de usuario**, en una línea nueva, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Para agrupar usuarios en grupos de usuarios
Puede configurar grupos de usuarios para administrar conjuntos de permisos para grupos de usuarios en su empresa.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de usuarios** y, a continuación, seleccione el vínculo relacionado.
2. Alternativamente, en la ventana **Usuarios**, seleccione la acción **Grupos de usuarios**.
3. En la ventana **Grupo usuarios**, seleccione la acción **Miembros de grupo de usuarios**.
6. En la ventana **Miembros de grupo de usuarios**, seleccione la acción **Añadir usuarios**.
7. Para agregar conjuntos de permisos nuevos o adicionales, en la ventana **Grupos de usuarios**, seleccione la acción **Conjuntos de permisos de grupo de usuarios**.
8. En la ventana **Conjuntos de permisos de grupo de usuarios**, en una línea nueva, rellene los campos según sea necesario seleccionando entre los conjuntos de permisos existentes.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Para copiar un grupo de usuarios y todos los conjuntos de permisos
Para definir rápidamente un nuevo grupo de usuarios, puede copiar todos los conjuntos de permisos de un grupo de usuarios existente al nuevo grupo de usuarios.

No copian los miembros del grupo de usuarios al nuevo grupo de usuarios. Debe añadirlos manualmente posteriormente.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de usuarios** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el grupo de usuarios que desea copiar y, a continuación, seleccione la acción **Copiar el grupo de usuarios**.
3. En el campo **Nuevo código de grupo de usuarios**, introduzca el nombre del grupo y después seleccione el botón **Aceptar**.

El nuevo grupo de usuarios se agrega a la ventana **Grupos de usuarios**. Empiece a agregar usuarios. Para obtener más información, consulte la sección "Para agrupar usuarios en grupos de usuarios".

## <a name="to-set-up-user-time-constraints"></a>Para configurar restricciones de tiempo de usuarios
Los administradores pueden definir periodos de tiempo durante los que los usuarios especificados pueden registrar, así como especificar si el sistema registra la cantidad de tiempo que los usuarios tienen iniciada la sesión. Los administradores también pueden asignar centros de responsabilidad a los usuarios. Para obtener más información, consulte [Trabajar con centros de responsabilidad](inventory-responsibility-centers.md).

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración usuarios** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Configuración usuarios** que se abre, seleccione la acción **Nuevo**.
3. En el campo **Id. usuario**, escriba el identificador de un usuario o elija el campo para ver todos los usuarios de Windows actuales en el sistema.
4. Rellene los campos según sea necesario.

## <a name="see-also"></a>Consulte también
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Administración](admin-setup-and-administration.md)  
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

