---
title: Crear nuevas empresas con una guía de configuración asistida
description: Es fácil crear una empresa nueva y en blanco en Business Central. Una guía de configuración asistida le ayudará a seguir los pasos, y podrá importar sus datos empresariales existentes.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.search.form: 1803, 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f05fcf2fc3137fbdf97940e5b3d73922180253b4
ms.sourcegitcommit: 75a388b1d8917e2bbd49398ef76cf86cf37e6767
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323170"
---
# <a name="creating-new-companies-in-prod_short"></a>Crear nuevas en empresas en [!INCLUDE[prod_short](includes/prod_short.md)]

En [!INCLUDE[prod_short](includes/prod_short.md)], el contenedor para datos empresariales que pertenece a una unidad de negocio o entidad legal se denomina *empresa*. Cuando se registra en [!INCLUDE[prod_short](includes/prod_short.md)], recibe una empresa de demostración y una empresa vacía, *Mi empresa*. Cambiar entre las empresas es fácil, solo tiene que ir a **Mi configuración** y cambiar a la otra empresa. Pero también puede crear nuevas empresas en [!INCLUDE[prod_short](includes/prod_short.md)], según sus necesidades comerciales. Al crear una empresa nueva, una guía de configuración asistida le ayuda a obtener los elementos básicos. A continuación, puede importar datos relevantes de su sistema heredado u otra empresa en [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="creating-a-new-company"></a>Creación de una nueva empresa

Si decide agregar una empresa al [!INCLUDE[prod_short](includes/prod_short.md)], puede utilizar la guía de configuración asistida **Crear nueva empresa** para comenzar. El asistente de configuración está disponible en la página **Empresas** y en la búsqueda en el campo **Empresa** en la página **Mi configuración**.  

El asistente de configuración ofrece tres plantillas y una opción en blanco:

- **Evaluación - Datos de ejemplo**  
    Crea una empresa similar a la compañía de demostración con datos de ejemplo y datos de configuración.  
- **Producción - Solo datos de configuración**  
    Crea una empresa similar a **Mi empresa** con datos de configuración pero sin datos de ejemplo.
- **Evaluación avanzada - Datos de muestra completa** Esto crea una empresa con datos de configuración y datos de muestra completos para todas las funciones, incluidas la Fabricación y la Gestión de servicios.
- **Crear nuevo - No hay datos**  
    Crea una empresa en blanco sin datos de configuración.  

Si desea empezar fácilmente con una empresa nueva, elija **Producción - Solo datos de configuración** y, a continuación, importe sus propios datos empresariales, como clientes, productos, y proveedores. Seleccione la plantilla **Nuevo** si desea configurar todos los parámetros desde cero. En ese caso, puede utilizar la guía de configuración asistida **Configuración de la empresa** para obtener ayuda con los datos esenciales de configuración.  

> [!NOTE]  
> Al crear una empresa nueva, tarda algunos minutos antes de tener acceso en [!INCLUDE[prod_short](includes/prod_short.md)]. El estado de configuración de la página **Empresas** muestra cuando la nueva empresa está lista. A continuación, puede cambiar a la nueva empresa mediante **Mi configuración**.  

Durante su prueba de 30 días, puede crear todas las nuevas empresas que desee, pero solo estarán disponibles durante la versión de prueba. Para obtener más información, póngase en contacto con su socio [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="copying-a-company"></a>Copiar una empresa

En la página **Empresas**, puede usar la acción **Copiar** para crear una segunda empresa basada en los contenidos de una empresa existente. Esto es útil, por ejemplo, cuando desea probar una empresa sin interrumpir los datos de producción.

> [!Important]
> Esta función no se puede utilizar para hacer una copia de seguridad de una empresa. Hacer una copia de seguridad de la empresa comienza exportando la base de datos como un archivo .bacpac. Para obtener más información, consulte [Exportar bases de datos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) en la ayuda para desarrolladores y administradores.

## <a name="company-setup"></a>Configuración de la empresa

Cuando inicie sesión en una empresa nueva, se ejecutará el asistente **Configuración de la empresa** automáticamente y le ayudará a empezar. Se le pedirá información sobre su empresa, como la dirección, los datos bancarios y el método de cálculo de costes de inventario. Pedimos esta información porque se utiliza como base para muchas áreas en [!INCLUDE[prod_short](includes/prod_short.md)] que no tendrá que configurar manualmente más adelante.  

Por ejemplo, la dirección de su empresa se incluye en facturas y otros documentos, su información bancaria se utiliza en los pagos y el método de cálculo de costes se utiliza para calcular los precios, así como la evaluación del inventario.  

Una vez que tenga los elementos básicos, puede configurar las áreas restantes. A continuación, puede agregar datos empresariales, como clientes y proveedores. Para obtener más información, consulte [Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Empresas y entornos

[!INCLUDE [company_environment](includes/company_environment.md)]

Para más información, vea [Cambiar a otra empresa o entorno](ui-organization-switch.md). 

## <a name="changing-a-companys-name"></a>Cambiar el nombre de una empresa

Una vez que se ha creado una empresa, no puede cambiar su nombre. Pero puedes cambiar su **Nombre para mostrar**, que es el texto que se mostrará a la empresa a lo largo de la aplicación.  

> [!TIP]
> Puede cambiar el nombre de una empresa si está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones.

## <a name="see-also"></a>Consulte también

[Personalizar Business Central](ui-customizing-overview.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]