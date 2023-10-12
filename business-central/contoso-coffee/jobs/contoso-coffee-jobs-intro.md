---
title: Introducción a la Administración de proyecto de Contoso Coffee
description: Este artículo le presenta los datos de demostración de Consoso Coffee para trabajos y gestión de proyectos.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Introducción a la Administración de proyecto y trabajos de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para Business Central agregan datos de demostración que puede usar para aprender a usar las capacidades de trabajos y gestión de proyectos de Business Central.

Esta aplicación proporciona varios elementos que se utilizan para los tutoriales principales:

- Recursos con capacidades y zonas asignadas
- Artículos configurados para crear artículos de servicio

> [!IMPORTANT]
> Antes de ejecutar cualquiera de los escenarios para Contoso Coffee, registre las líneas del diario de productos con saldos iniciales. Para ver más requisitos, consulte la sección [Configurar datos de Contoso Coffee](#set-up-contoso-coffee-jobs-and-project-management-data).
>
> 
## Configurar los datos de la Administración de proyecto y trabajos de Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Una vez que las aplicaciones correspondientes estén instaladas, vaya a la página [Datos de demostración de Contoso Coffee para trabajos](https://businesscentral.dynamics.com/?page=4767) en [!INCLUDE [prod_short](../../includes/prod_short.md)] y cambie la configuración predeterminada para adaptarla a sus necesidades. En las siguientes tablas se describen las configuraciones:  

|Campo  |Descripción  |
|---------|---------|
|**Año inicial** |Especifica el primer año en el que desea usar los datos de demostración de Contoso Coffee. Según la configuración de la empresa, el año es un año natural o un año fiscal.|
|**Nº cliente**  |El cliente que se utilizará para los escenarios en las operaciones de venta.|
|**N.º de producto 1**  |El producto que se usará para los escenarios de contrato.|
|**N.º de producto 2**  |El producto que se usará para los escenarios de sustitución.|
|**N.º recurso local 1**  |El recurso que se usará para los escenarios de contrato.|
|**N.º recurso remoto 1**  |El recurso que se usará para los escenarios de sustitución.|
|**Grupo contable cliente**|Especifica un código de negocio para clientes nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**Grupo contable de negocio general de clientes**|Especifica un código de negocio para clientes nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**NAC: grupo contable de negocio general**|Especifica un código de negocio para clientes y proveedores nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**Reventa: grupo contable inventario**    |Especifica un código para productos que se deben usar para registrar la reventa.|
|**Mercadería: grupo contable de producto general**    |Especifica un código para productos que se deben usar para registrar la venta minorista.|
|**Grupo registro IVA producto**    |Especifica un código de producto de IVA para contabilizar el IVA si el IVA está habilitado.|
|**Factor precio**     |Especifica un factor para convertir un precio de USD/EUR a la divisa local. *1* significa que el precio es la misma cantidad en cualquier divisa. Se utilizará un número mayor para obtener el precio en la divisa local. |
|**Precisión redondeo**  |Define cómo se redondean las cantidades calculadas de consumo cuando se introducen en las líneas del diario de consumo. Las cantidades inferiores a 0,5 se redondean hacia abajo. Las cantidades iguales o superiores a 0,5 se redondean hacia arriba.|

Una vez que esté listo, elija la acción **Crear datos de demostración** acción. Se tarda unos minutos en agregar los datos a la base de datos subyacente, pero luego ya está listo para ejecutar los distintos escenarios.  

## Consulte también .
