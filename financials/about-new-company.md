---
title: "Crear nuevas empresas con una guía de configuración asistida | Documentos de Microsoft"
description: "Es fácil crear una empresa nueva y en blanco en Dynamics 365 for Financials. Una guía de configuración asistida le ayudará a seguir los pasos, y podrá importar sus datos empresariales existentes."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 07/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: 3ff3c7af87033595d64e583b62b0e0242b22d2f1
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="creating-new-companies-in-included365finlongincludesd365finlongmdmd"></a>Crear nuevas en empresas en [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
En [!INCLUDE[d365fin](includes/d365fin_md.md)], los contenedores para datos empresariales que pertenecen a una unidad de negocio o entidad legal se denominan *empresa*. Cuando se registra en [!INCLUDE[d365fin](includes/d365fin_md.md)], recibe una empresa de demostración y una empresa vacía, *Mi empresa*. Cambiar entre las empresas es fácil, solo tiene que ir a **Mi configuración** y cambiarse a la otra empresa. Pero también puede crear nuevas empresas en [!INCLUDE[d365fin](includes/d365fin_md.md)], en función de sus necesidades comerciales. Al crear una empresa nueva, una guía de configuración asistida le ayuda a obtener los elementos básicos. A continuación, puede importar datos relevantes de su sistema heredado u otra empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="create-new-company"></a>Crear nueva empresa
Si decide agregar una empresa al [!INCLUDE[d365fin](includes/d365fin_md.md)], puede utilizar el asistente de configuración asistida **Crear nueva empresa** para comenzar. El asistente de configuración está disponible en la ventana **Empresas** y en la búsqueda en el campo **Empresa** en **Mi configuración**.  

El asistente de configuración ofrece tres plantillas :

-   **Evaluación de Suite**  
    Crea una empresa similar a la compañía de demostración con datos de ejemplo y datos de configuración.  
-   **Producción de Suite**  
    Crea una empresa similar a **Mi empresa** con datos de configuración pero sin datos de ejemplo.  
-   **Nuevo**  
    Crea una empresa en blanco sin datos de configuración.  

Si desea empezar fácilmente con una empresa nueva, elija **Producción de Suite** y, a continuación, importe sus propios datos empresariales, como clientes, productos, y proveedores. Seleccione la plantilla **Nuevo** si desea configurar todos los parámetros desde cero. En ese caso, puede utilizar el asistente de configuración asistida **Configuración de la empresa** para obtener ayuda con los datos esenciales de configuración.  

> [!NOTE]  
>   Al crear una empresa nueva, tarda algunos minutos antes de tener acceso en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El estado de configuración de la ventana **Empresas** muestra cuando la nueva empresa está lista. A continuación, puede cambiar a la nueva empresa mediante **Mi configuración**.  

Durante su prueba de 30 días, puede crear todas las nuevas empresas que desee, pero solo estarán disponibles durante la versión de prueba. Para obtener más información, póngase en contacto con su socio [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="company-setup"></a>Configuración de la empresa
Cuando inicie sesión en una empresa nueva, se ejecutará el asistente **Configuración de la empresa** automáticamente y le ayudará a empezar. Se le pedirá información sobre su empresa, como la dirección, los datos bancarios y el método de cálculo de costes de inventario. Pedimos esta información porque se utiliza como base para muchas áreas en [!INCLUDE[d365fin](includes/d365fin_md.md)] que no tendrá que configurar manualmente más adelante.  

Por ejemplo, la dirección de su empresa se incluye en facturas y otros documentos, su información bancaria se utiliza en los pagos y el método de cálculo de costes se utiliza para calcular los precios, así como la evaluación del inventario.  

Una vez que tenga los elementos básicos, puede configurar las áreas restantes. A continuación, puede agregar datos empresariales, como clientes y proveedores. Para obtener más información, consulte [Configurar Dynamics 365 for Financials](setup.md).  

## <a name="see-also"></a>Consulte también
[Configurar Dynamics 365 for Financials](setup.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

