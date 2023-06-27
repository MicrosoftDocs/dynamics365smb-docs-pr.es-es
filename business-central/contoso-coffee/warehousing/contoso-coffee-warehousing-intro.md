---
title: Introducción a Contoso Coffee
description: Descripción general de escenarios sobre cómo los datos de demostración de Contoso Coffee pueden ayudarle a aprender a usar las capacidades de almacenamiento en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-warehousing"></a><a name="introduction-to-contoso-coffee-warehousing"></a>Introducción al almacenamiento de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para Business Central agregan datos de demostración que puede usar para aprender a usar las capacidades de almacenamiento en Business Central. Puede configurar las características del almacén de varias maneras, consulte [Descripción general de las diferentes opciones de configuración](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

La aplicación proporciona tres almacenes optimizados para diferentes escenarios:

- **PLATA**  

  Este almacén está configurado para usar ubicaciones. Se puede configurar fácilmente para admitir funciones básicas o avanzadas. 

- **AMARILLO**  

  Este almacén utiliza la configuración de almacén avanzada, pero no utiliza ubicaciones. Se puede reconfigurar para admitir configuraciones básicas.

- **BLANCO**  

  Esta ubicación utiliza la configuración de almacén avanzado con ubicaciones y almacenamientos dirigidos, lo que permite reglas más avanzadas sobre cómo se mueven los productos en el almacén.

## <a name="set-up-contoso-coffee-warehousing-data"></a><a name="set-up-contoso-coffee-warehousing-data"></a>Configurar datos de Contoso Coffee para almacenamiento

Para usar los datos de demostración de Contoso Coffee para almacenamiento, debe instalar dos aplicaciones en la empresa correspondiente en [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Conjunto de datos de demostración de Contoso Coffee**  

    Esta aplicación ofrece datos de demostración para la aplicación base.  
- **Conjunto de datos de demostración de Contoso Coffee (ID de país)**  

    Esta aplicación agrega contenido específico del país sobre la aplicación base.

Agregue las aplicaciones a una empresa vacía en una suscripción pagada o como parte de una prueba. Por ejemplo, cree una nueva empresa sin datos de muestra de la guía de configuración asistida **Crear nueva empresa** que puede abrir desde la lista **Empresas**. A continuación, agregue las aplicaciones del [mercado](../../ui-extensions-install-uninstall.md#install) en caso de que no se indiquen en la página **Administración de extensiones**.  

Una vez que las aplicaciones correspondientes estén instaladas, vaya a la página [Datos de demostración de Contoso Coffee para almacenamiento](https://businesscentral.dynamics.com/?page=4761) en [!INCLUDE [prod_short](../../includes/prod_short.md)] y cambie la configuración predeterminada para adaptarla a sus necesidades. En la siguiente tabla se describen las configuraciones:  

|Campo  |Descripción  |
|---------|---------|
|**Año inicial** |Especifica el primer año en el que desea usar los datos de demostración de Contoso Coffee. Según la configuración de la empresa, el año es un año natural o un año fiscal.|
|**Ubicación almacén**  |El almacén a utilizar para escenarios de almacén básico.|
|**Logística de almacén avanzado**  |El almacén a utilizar para escenarios de logística sencilla.|
|**Almacenamiento y recogida dirigidos por almacén**  |El almacén a utilizar para escenarios de logística avanzada.|
|**Ubicación en tránsito**  |La ubicación que se usará para el almacén de tránsito en escenarios de transferencia.|
|**Nº cliente**  |El cliente a utilizar para los escenarios básicos y sencillos en las operaciones de venta.|
|**N.º proveedor**  |El proveedor que se utilizará para todos los escenarios en las operaciones de compra.|
|**N.º de producto principal**  |El producto que se utilizará para todos los escenarios en las operaciones de venta.|
|**N.º de producto 1**  |El producto principal que se usará para todos los escenarios.|
|**N.º de producto 2**  |El producto adicional que se usará para todos los escenarios.|
|**Grupo contable cliente**|Especifica un código de negocio para clientes nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**Grupo contable de negocio general de clientes**|Especifica un código de negocio para clientes nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**Grupo contable proveedor**|Especifica un código de negocio para clientes y proveedores nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**Grupo contable de negocio general para proveedores**|Especifica un código de negocio para clientes y proveedores nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**Nacional: grupo contable de negocio de IVA**|Especifica un código comercial de IVA para clientes y proveedores, para contabilizar el IVA si el IVA está habilitado.|
|**Reventa - Grupo contable inventario**    |Especifica un código para productos que se deben usar para registrar la reventa.|
|**Mercadería: grupo contable de producto general**    |Especifica un código para productos que se deben usar para registrar la venta minorista.|
|**Grupo registro IVA producto**    |Especifica un código de producto de IVA para contabilizar el IVA si el IVA está habilitado.|
|**Factor precio**     |Especifica un factor para convertir un precio de USD/EUR a la divisa local. *1* significa que el precio es la misma cantidad en cualquier divisa. Se utilizará un número mayor para obtener el precio en la divisa local. |
|**Precisión redondeo**  |Define cómo se redondean las cantidades calculadas de consumo cuando se introducen en las líneas del diario de consumo. Las cantidades inferiores a 0,5 se redondean hacia abajo. Las cantidades iguales o superiores a 0,5 se redondean hacia arriba.|

Una vez que esté listo, elija la acción **Crear datos de demostración** acción. Se tarda unos minutos en agregar los datos a la base de datos subyacente, pero luego ya está listo para ejecutar los distintos escenarios.  

> [!IMPORTANT]
> Si está ejecutando los escenarios, es posible que desee verificar que su usuario se haya agregado para los almacenes seleccionados. Para obtener más información, vea [Configurar los empleados de almacén](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a><a name="scenarios"></a>Escenarios

Los datos de demostración de almacenamiento de Contoso Coffee admiten actualmente los siguientes escenarios de pruebas y entrenamiento:

1.  [Tutorial de flujo entrante y saliente en las configuraciones de almacén básico](warehouse-basic-flow-putaway-pick.md)
2.  [Tutorial de flujo entrante y saliente en las configuraciones de almacén mixto](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Tutorial del flujo de entrada y salida en Configuración avanzada de almacén con ubicación y selección dirigidas](warehouse-directed-flow.md)

Lea los pasos para cada escenario en el artículo correspondiente.  

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Configuración de inventario](../../inventory-setup-inventory.md) 
[Cómo configurar almacenes](../../inventory-how-setup-locations.md) 
[Almacenamiento](../../warehouse-manage-warehouse.md) 
[Detalles de diseño](../../design-details-warehouse-overview.md) 
