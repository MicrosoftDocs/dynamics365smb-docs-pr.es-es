---
title: Crear nuevas empresas con una guía de configuración asistida
description: 'Es fácil crear una empresa nueva y en blanco en Business Central. Una guía de configuración asistida le ayudará a seguir los pasos, y podrá importar sus datos empresariales.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/14/2023
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.service: dynamics-365-business-central
---
# <a name="create-new-companies-in-"></a>Crear nuevas en empresas en [!INCLUDE[prod_short](includes/prod_short.md)]

En [!INCLUDE[prod_short](includes/prod_short.md)], el contenedor para datos empresariales que pertenece a una unidad de negocio o entidad legal se denomina *empresa*. Cuando se registra en [!INCLUDE[prod_short](includes/prod_short.md)], recibe una empresa de demostración y una empresa vacía, *Mi empresa*. Cambiar entre las empresas es fácil, solo tiene que ir a **Mi configuración** y cambiar a la otra empresa. Pero también puede crear nuevas empresas en [!INCLUDE[prod_short](includes/prod_short.md)], según sus necesidades comerciales.  

> [!NOTE]
> Para crear una nueva empresa, debe tener asignado el conjunto de permisos **Super**.

Al crear una empresa nueva, una guía de configuración asistida le ayuda a obtener los elementos básicos. A continuación, puede importar datos relevantes de su sistema heredado u otra empresa en [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="choose-the-right-template"></a>Elegir la plantilla adecuada

Si decide agregar una empresa al [!INCLUDE[prod_short](includes/prod_short.md)], puede utilizar la guía de configuración asistida **Crear nueva empresa** para comenzar. La guía de configuración está disponible en la página **Empresas** y en la búsqueda en el campo **Empresa** en la página **Mi configuración**.  

La guía de configuración ofrece dos plantillas y una opción en blanco:

- **Evaluación: datos de muestra**  
    Crea una empresa similar a la compañía de demostración con datos de ejemplo y datos de configuración. Este tipo de empresa está a su disposición sin necesidad de cambiar a un período de prueba de 30 días, lo que hacen los otros tipos.  
- **Producción - Solo datos de configuración**  
    Crea una empresa similar a **Mi empresa** con datos de configuración pero sin datos de ejemplo. Podrá usar esta empresa durante un periodo de evaluación de 30 días.  
- **Crear nuevo - No hay datos**  
    Crea una empresa en blanco sin datos de configuración. Podrá usar esta empresa durante un periodo de evaluación de 30 días.  

Si desea empezar fácilmente con una empresa nueva, elija **Producción - Solo datos de configuración** y, a continuación, importe sus propios datos empresariales, como clientes, productos, y proveedores. Seleccione la plantilla **Nuevo** si desea configurar todos los parámetros desde cero. En ese caso, puede utilizar la guía de configuración asistida **Configuración de la empresa** para obtener ayuda con los datos esenciales de configuración.  

> [!NOTE]  
> Al crear una empresa nueva, tarda algunos minutos antes de tener acceso en [!INCLUDE[prod_short](includes/prod_short.md)]. El estado de configuración de la página **Empresas** muestra cuando la nueva empresa está lista. A continuación, puede cambiar a la nueva empresa mediante **Mi configuración**.  

Durante su prueba de 30 días, puede crear todas las nuevas empresas que desee, pero solo estarán disponibles durante la versión de prueba. Para obtener más información, póngase en contacto con su socio [!INCLUDE[prod_short](includes/prod_short.md)]. Consulte también el artículo [Preguntas más frecuentes de la prueba de Dynamics 365 Business Central](trial-faq.md).  

Su administrador puede obtener más información sobre pruebas y suscripciones [aquí](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## <a name="copy-a-company"></a>Copiar una empresa

En la página **Empresas**, puede usar la acción **Copiar** para crear una segunda empresa basada en los contenidos de una empresa existente. Eso es útil, por ejemplo, cuando desea probar una empresa sin interrumpir los datos de producción.

> [!Important]
> No utilice la acción Copiar para realizar una copia de seguridad de una empresa. Para hacer una copia de seguridad, comience exportando la base de datos como un archivo .bacpac. Para obtener más información, consulte [Exportar bases de datos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) en la ayuda para desarrolladores y administradores.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="set-up-the-company"></a>Establecer la empresa

Cuando inicie sesión en una empresa nueva, se ejecutará el asistente **Configuración de la empresa** automáticamente y le ayudará a empezar. Se le pedirá información sobre su empresa, como la dirección, los datos bancarios y el método de cálculo de costes de inventario. Pedimos esta información porque se utiliza como base para muchas áreas en [!INCLUDE[prod_short](includes/prod_short.md)] que no tendrá que configurar manualmente más adelante.  

Por ejemplo, [!INCLUDE [prod_short](includes/prod_short.md)] incluye la dirección de su empresa en las facturas y otros documentos y su información bancaria en los pagos. El método de coste se utiliza para calcular los precios y la valoración del inventario.  

Una vez que tenga los elementos básicos, puede configurar las áreas restantes. A continuación, puede agregar datos empresariales, como clientes y proveedores. Para obtener más información, consulte [Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Empresas y entornos

[!INCLUDE [company_environment](includes/company_environment.md)]

Para más información, vea [Cambiar a otra empresa o entorno](ui-organization-switch.md). Para obtener más información sobre los entornos, consulte [Comprender la infraestructura de Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (solo en inglés).  

## <a name="changing-a-companys-name"></a>Cambiar el nombre de una empresa

Una vez que se ha creado una empresa, no puede cambiar su nombre. Pero puedes cambiar su **Nombre para mostrar**, que es el texto que se mostrará a la empresa a lo largo de la aplicación.  

> [!TIP]
> Puede cambiar el nombre de una empresa si está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en las instalaciones.

## <a name="add-contoso-coffee"></a>Agregar Contoso Coffee

La aplicación Contoso Coffee proporciona datos de demostración que pueden ayudarle a explorar las capacidades avanzadas de [!INCLUDE [prod_short](includes/prod_short.md)]. Encuentre la aplicación en AppSource e instálela en una empresa vacía, por ejemplo, una empresa en un entorno de espacio aislado. Para obtener más información, consulte [Introducción a los datos de demostración de Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).  

## <a name="see-also"></a>Consulte también .

[Personalizar Business Central](ui-customizing-overview.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Comprender la infraestructura de Business Central Online (solo en inglés)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
