---
title: Introducción a la fabricación de Contoso Coffee
description: Descripción general de escenarios sobre cómo los datos de demostración de Contoso Coffee pueden ayudarle a aprender a usar las capacidades de fabricación en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a><a name="introduction-to-contoso-coffee-manufacturing"></a>Introducción a la fabricación de Contoso Coffee

Contoso Coffee es una empresa ficticia que produce cafeteras comerciales y de consumo. La aplicaciones **Contoso Coffee** para Business Central agregan datos de demostración que puede usar para aprender a usar las capacidades de fabricación en Business Central.  

La aplicación proporciona cuatro productos optimizados para diferentes escenarios:

- **SP-SCM1009 Airpot**  

  Este producto es una lista de materiales (L.M.) con un producto semiterminado, **Ruta**. Úselo para demostrar el flujo de producción estándar. Está configurado con rutas alternativas que puede usar para demostrar varios escenarios que implican a subcontratistas. El método de coste es *Estándar*.  

- **SP-SCM1011 Airpot Duo**  

  Este producto requiere seguimiento de artículos y tiene un componente que también requiere seguimiento de artículos. El método de coste es *Específico*.  

- **SP-SCM1004 Autodrip**  

  Este producto es una L.M. con un producto semiterminado, **Ruta**. Le recomendamos que demuestre los diversos métodos de baja tanto para componentes como para operaciones. El método de coste es *Estándar*.

- **SP-SCM1006 AutoDripLite**

  Este producto tiene tres variantes y tres listas de materiales (L.M.) que se pueden asignar a unidades de almacenamiento. El producto utiliza el concepto de L.M. ficticia. El método de coste es *Estándar*.

Las actividades de fabricación para todos los escenarios utilizan la ubicación *NORTE*.  

> [!IMPORTANT]
> Antes de ejecutar cualquiera de los escenarios para Contoso Coffee, registre las líneas del diario de productos con saldos iniciales. Para ver más requisitos, consulte la sección [Configurar datos de Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## <a name="set-up-contoso-coffee-manufacturing-data"></a><a name="set-up-contoso-coffee-manufacturing-data"></a>Configuración de datos de demostración de Contoso Coffee para fabricación

Para usar los datos de demostración de Contoso Coffee para fabricación, debe instalar dos aplicaciones en la empresa correspondiente en [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Conjunto de datos de demostración de Contoso Coffee**  

    Esta aplicación ofrece datos de demostración para la aplicación base.  
- **Conjunto de datos de demostración de Contoso Coffee (ID de país)**  

    Esta aplicación agrega contenido específico del país sobre la aplicación base.

Agregue las aplicaciones a una empresa vacía en una suscripción pagada o como parte de una prueba. Por ejemplo, cree una nueva empresa sin datos de muestra de la guía de configuración asistida **Crear nueva empresa** que puede abrir desde la lista **Empresas**. A continuación, agregue las aplicaciones del [mercado](../../ui-extensions-install-uninstall.md#install) en caso de que no se indiquen en la página **Administración de extensiones**.  

Una vez que las aplicaciones correspondientes estén instaladas, vaya a la página [Datos de demostración de Contoso Coffee](https://businesscentral.dynamics.com/?page=4760) en [!INCLUDE [prod_short](../../includes/prod_short.md)] y cambie la configuración predeterminada para adaptarla a sus necesidades. En la siguiente tabla se describen las configuraciones:  

|Campo  |Descripción  |
|---------|---------|
|**Año inicial** |Especifica el primer año en el que desea usar los datos de demostración de Contoso Coffee. Según la configuración de la empresa, el año es un año natural o un año fiscal.|
|**Almacén de fabricación** |Especifica el almacén que desea usar para las operaciones de producción. El valor predeterminado es *NORTE*, pero puede cambiarlo para adaptarlo a sus necesidades.|
|**Tipo de empresa**    |Especifica si la empresa actual debe declarar el IVA o el impuesto de venta. |
|**NAC: grupo contable de negocio general**|Especifica un código de negocio para clientes y proveedores nacionales. Los códigos de negocio se utilizan cuando se registran las transacciones. |
|**Capacidad: grupo contable de producto general**    |Especifica un código para productos o recursos que se deben usar para registrar la capacidad.|
|**Mercadería: grupo contable de producto general**    |Especifica un código para productos o recursos que se deben usar para registrar la mercadería.|
|**Materia prima: grupo contable de producto general**    |Especifica un código para productos o recursos que se deben usar para registrar las materias primas. |
|**Código base IVA**    |Especifica un grupo de productos de IVA existente que se utilizará para los productos.|
|**Código terminado**    |Especifica un grupo de productos existente que se utilizará para los productos terminados.|
|**Factor precio**     |Especifica un factor para convertir un precio de USD/EUR a la divisa local. *1* significa que el precio es la misma cantidad en cualquier divisa. Se utilizará un número mayor para obtener el precio en la divisa local. |
|**Precisión redondeo**  |Define cómo se redondean las cantidades calculadas de consumo cuando se introducen en las líneas del diario de consumo. Las cantidades inferiores a 0,5 se redondean hacia abajo. Las cantidades iguales o superiores a 0,5 se redondean hacia arriba.|

Una vez que esté listo, elija la acción **Crear datos de demostración** acción. Se tarda unos minutos en agregar los datos a la base de datos subyacente, pero luego ya está listo para ejecutar los distintos escenarios.  

## <a name="scenarios"></a><a name="scenarios"></a>Escenarios

Los datos de fabricación de Contoso Coffee admiten actualmente los siguientes escenarios de fabricación para pruebas y entrenamiento:

1. [Crear una nueva L.M. de producción y una versión de L.M.](create-new-production-bom-version.md)  
2. [Crear una nueva ruta](create-new-routing.md)  
3. [Crear una nueva orden de producción planificada en firme y cambiarla](create-firm-planned-production-order-change.md)  
4. [Combinar la baja automática y la manual](combine-automatic-manual-flushing.md)  
5. [Utilizar la planificación de pedidos para crear y reservar suministros](order-planning-create-reserve-supply.md)  
6. [Configurar y procesar una operación de subcontratación](set-up-process-subcontracting-operation.md)  
7. [Configurar nueva capacidad](set-up-new-capacity.md)  
8. [Previsión de la demanda de variantes de producto con diferentes L.M. asignadas](variants.md)  

Lea los pasos para cada escenario en el artículo correspondiente.  

> [!IMPORTANT]
> Estos tutoriales requieren que la experiencia del usuario esté establecida en *Premium* en la página **Información empresa**.

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Fabricación](../../production-manage-manufacturing.md)  
[Informes y análisis de producción en Business Central](../../production-reports.md)  
