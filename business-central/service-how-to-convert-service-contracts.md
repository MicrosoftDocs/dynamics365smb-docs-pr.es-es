---
title: Convertir contratos de servicio
description: Este tema describe diversos métodos alternativos que puede usar para convertir contratos de servicio que incluyan importes de IVA.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 715f532745b74b0fb49e8dff10a355fda71a0271
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134852"
---
# <a name="convert-service-contracts-that-include-vat-amounts"></a>Convertir contratos de servicio que incluyen importes de IVA
Como la herramienta de cambio de tasa de IVA no puede convertir contratos de servicio, estos acuerdos deben convertirse manualmente. Este tema describe diversos métodos alternativos que puede usar para la conversión de contrato de servicio.  

> [!NOTE]  
>  Este tema proporciona a un flujo de trabajo de niveles más altos.  

 El procedimiento siguiente describe cómo corregir una factura para un contrato de servicio prepago que se ha creado un año atrás.  

> [!NOTE]  
>  Para este ejemplo, debe cambiar la fecha de trabajo a 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>Para corregir una factura para un contrato de servicio prepago  
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de contratos** y luego elija el enlace relacionado.  
2. En **Listas**, seleccione **Contratos de servicio**.  
3. Cree un contrato de servicio de prepago nuevo. Introduzca una fecha de inicio de **01.01.2017** y un año de periodo de factura para el cliente **20000**.  
4. Para firmar el contrato, elija la acción **Firmar contrato**.  
5. Crear una factura de servicio.
6. La factura aparece como una factura sin registrar del servicio. Para ver la factura del servicio, elija las acciones **Servicio**, **Administración de contratos** y **Facturas de servicio**.  
7. Registre la factura de servicio.  

> [!NOTE]  
>  No cambie la factura sin registrar del servicio. Puesto que se crean los movimientos de servicio cuando se crea la factura, un cambio en la factura sin registrar no cambiará los movimientos ya creados del servicio. Sin embargo, se crean las entradas de IVA cuando se registra la factura. Esto le permite modificar el grupo contable general del producto y el grupo contable del producto de GSP en la factura sin registrar del servicio.  

### <a name="to-create-a-credit-memo-for-vat-difference"></a>Para crear un abono para la diferencia de IVA  
El procedimiento siguiente describe cómo crear un abono que incluya sólo la diferencia de IVA para el periodo ya facturado, con fecha de inicio en **01.07.2017**. En este ejemplo, el importe de IVA se registra sólo en el módulo Gestión financiera, no en el módulo Gestión del servicio. Los movimientos de IVA que están vinculados al movimiento del servicio no se corregirán.  

1. Cree una nueva cuenta para la diferencia de IVA. Esta cuenta se utilizará para el registro directo de corrección de IVA.  
2. Agregue una nueva línea a la configuración de registro de IVA.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a>Para crear las fechas de vencimiento de contrato en las líneas de contrato  
El procedimiento siguiente describe cómo crear nuevos contratos trabajando con las fechas de vencimiento del contrato en las líneas de contrato de servicio.  

1. En la página **Contrato servicio**, establezca la fecha de vencimiento de contrato en **30.06.2017**.  
2. Elija la acción **Crear abono** para crear automáticamente un abono para el periodo de julio de 2017 a diciembre de 2017.  
3. Como el contrato ha expirado, deberá crear un nuevo contrato para el periodo con la nuevo tasa de IVA para el periodo del 1 de julio de 2017 al 31 de diciembre de 2017.  

### <a name="to-create-a-new-credit-memo"></a>Para crear un abono nuevo  
El procedimiento siguiente describe cómo crear un nuevo abono con el trabajo por lotes de **Traer movs. contrato prepago**. Los movimientos que no desea corregir desde enero de 2017 a junio de 2017 serán eliminados.  

1. Ejecute la herramienta de cambio de tasa de IVA el 1 de julio de 2017. Se cambia el grupo contable general de producto o el grupo contable de IVA de producto. Para obtener más información, consulte [Trabajar con el IVA por ventas y compras](finance-work-with-vat.md).  
2. Una vez ejecutada la herramienta de cambio de tasa de IVA, introduzca una fecha de vencimiento de contrato para el contrato de servicio. Ahora puede eliminar la línea de contrato de servicio y crear una nueva línea que se idéntica a la anterior.  
3. Cree una nueva factura para el periodo de enero de 2017 a diciembre de 2012 con la nueva tasa de IVA.  
4. Para crear otro abono, en la página **Abonos de servicio**, seleccione la acción **Nuevo** para crear un nuevo abono de servicio.  
5. Elija la acción **Traer movs. contrato prepag.**  
6. Después de que la conversión esté completa, los movimientos de IVA y del servicio estarán correctos.  

## <a name="see-also"></a>Consulte también  
[Trabajar con contratos de servicio y ofertas de contrato de servicio](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Finanzas](finance.md)  
[Crear informes de IVA para las autoridades fiscales](finance-how-report-vat.md)  
[Trabajar con el IVA por ventas y compras](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]