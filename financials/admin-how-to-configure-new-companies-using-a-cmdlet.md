---
title: "Configuración de nuevas empresas con un Cmdlet | Documentos de Microsoft"
description: "En varios casos se puede cargar e importar un lote un paquete de configuración sin implicar a los usuarios o usar la interfaz de usuario de RapidStart Services. Puede hacerlo con un cmdlet de Windows PowerShell."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b91c3b91e07f5ad96dcfc65152062054fc13c01
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Configuración de nuevas empresas con un Cmdlet
En varios casos se puede cargar e importar un lote un paquete de configuración sin implicar a los usuarios o usar la interfaz de usuario de RapidStart Services. Puede hacerlo con un cmdlet de Windows PowerShell. Entre los escenarios donde puede ser útil se incluyen:  

- Efectuar la importación de datos en múltiples instalaciones de [!INCLUDE[d365fin](includes/d365fin_md.md)].
- Configuración de áreas de aplicación adicionales para varios clientes.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Para implementar un paquete configuración mediante un cmdlet  

1. Preparar un paquete de RapidStart Services. Por ejemplo, puede crear un paquete para importar determinados valores y los nombres de la tabla y los campos donde insertar estos valores.  
2. Coloque el paquete en un equipo donde ejecutará el cmdlet.  
3. Abra el shell de administración de [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4. Introduzca **Invoque -NAVCodeUnit - NAVCodeUnit** y especifique información similar al ejemplo siguiente.  
    ```  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
El cmdlet importa el paquete en cada empresa. Los usuarios pueden empezar a usar la nueva funcionalidad inmediatamente.  

## <a name="see-also"></a>Consulte también  
[Configurar nuevas empresas](admin-how-to-configure-new-companies.md)  
[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Cmdlets de Windows PowerShell](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

