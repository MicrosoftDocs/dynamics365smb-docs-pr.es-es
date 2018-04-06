---
title: Como crear una empresa nueva | Documentos de Microsoft
description: "Para usar las tablas y páginas de RapidStart Service creadas que no tienen datos."
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
ms.openlocfilehash: 8c07b7c4e6b1c82004295a187184a6f3ccb4c7c7
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a>Cree una nueva empresa
Para usar RapidStart Services para [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe crear una nueva empresa para la que desee realizar una implementación de cliente. Al crear una empresa nueva, se crean las tablas y páginas estándar de [!INCLUDE[d365fin](includes/d365fin_md.md)], pero no existen datos en ellas.

Además, puede aplicar datos específicos de configuración a la empresa después de inicializarla. La información se proporciona en un paquete de configuración, un archivo .rapidstart, que entrega contenido en formato comprimido.  

La empresa de demostración CRONUS incluye paquetes de configuración de ejemplo, incluidos los archivos específicos del país o la región. Utilice los procedimientos siguientes para utilizar el paquete de configuración de ejemplo con una nueva empresa.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Utilizar el paquete de configuración BASICCONFIG de ejemplo  
1. Abra la empresa CRONUS España S.A. Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).
2. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Paquetes de configuración** y, a continuación, seleccione el vínculo relacionado.  
3. Elija el paquete BASICCONFIG de la lista y, a continuación, seleccione la acción **Exportar paquete**.  

Utilice el procedimiento siguiente para crear una nueva empresa y utilizar el paquete BASICCONFIG como parte del proceso.  

## <a name="to-create-a-new-company"></a>Para crear una nueva empresa  
1. Cree una nueva empresa. Para obtener más información, consulte [Crear nuevas empresas en [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).
2. Desde el área de trabajo del implementador de RapidStart Services, ahora puede importar el paquete de configuración que exportó de la empresa CRONUS España S.A.

Después de crear una empresa nueva, algunas tablas se rellenan automáticamente, incluso si no se aplica ningún plantilla de empresa. Por ejemplo, puede revisar los códigos estándar para registrar y tratar las transacciones por lotes en la ventana **Código origen**. Si proporciona una versión local de [!INCLUDE[d365fin](includes/d365fin_md.md)], debe revisar esta tabla y tener en cuenta cualquier problema de idioma local.

## <a name="about-data-tables"></a>Acerca de las tablas de datos
Las tablas de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] se proporcionan en dos tipos básicos: principal y configuración. Cuando está estableciendo la configuración de una empresa, puede usar estos tipos para centrar la estrategia de configuración.  

### <a name="master-data-tables"></a>Tablas de datos maestros  
En la tabla siguiente se enumeran todas las tablas de datos maestros. Cuando se inicializa una nueva empresa, estas tablas están vacías.  

|Tabla nº|Nombre de tabla|  
|-------------------|--------------------|  
|15|Cuenta|  
|18|Cliente|  
|23|Proveedor|  
|27|Artículo|  
|5050|Contacto|  

### <a name="setup-data-tables"></a>Tablas de datos de configuración  
En la tabla siguiente se enumeran algunas tablas de datos de configuración, en las que se captura información de configuración en el cuestionario de configuración. Estas tablas contienen información de línea en el momento de crear la empresa.  

|Tabla nº|Nombre de tabla|  
|-------------------|--------------------|  
|98|Configuración de contabilidad|  
|311|Configuración de ventas y cobros|  
|312|Configuración de compras y pagos|  
|313|Configuración de inventario|  

Además de las tablas de datos de configuración, [!INCLUDE[d365fin](includes/d365fin_md.md)] también incluye tablas de datos de tipo de configuración que especifican información básica acerca de la empresa y sus procesos empresariales. En la tabla siguiente aparecen algunos.  

|Tabla nº|Nombre de tabla|  
|-------------------|--------------------|  
|3|Términos de pago|  
|4|Divisa|  
|6|Grupos precio cliente|  
|5700|Ud. de almacenam.|

  

## <a name="see-also"></a>Consulte también  
[Aplicar la configuración a nuevas empresas](admin-apply-configuration-to-new-companies.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)

