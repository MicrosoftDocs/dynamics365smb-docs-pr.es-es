---
title: "Contratos múltiples | Documentos de Microsoft"
description: "Dependiendo de los acuerdos de nivel de servicio con un cliente, es posible que tenga que gestionar un producto de servicio en más de un contrato de servicio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6e4f0bad058bd928f65214f04f978bf3b387cbb8
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="multiple-contracts"></a>Contratos múltiples
Dependiendo de los acuerdos de nivel de servicio con un cliente, es posible que tenga que gestionar un producto de servicio en más de un contrato de servicio.  
  
El control de artículos de servicio de múltiples contratos permite hacer lo siguiente:  
  
* Emitir diferentes contratos para el mismo producto de servicio.  
* Dar servicio a sus componentes por separado.  
* Considerar las diferentes cualificaciones solicitadas para dar servicio a distintos aspectos de un producto de servicio, como los componentes mecánicos y el software.  
* Especificar diferentes tiempos y frecuencias de respuesta al dar servicio a distintos componentes de un producto.  
* Dirigir los diferentes tipos de actividades que se van a realizar en un producto de servicio cuando requiera distintos tipos de servicio en periodos diferentes.  
* Seleccionar y asignar un número de contrato adecuado a una línea de producto de servicio al crear un pedido de servicio.  
* Gestionar información financiera importante sobre productos de servicio y acuerdos de nivel de servicio.  
  
Puede considerar los siguientes ejemplos de uso de la funcionalidad de múltiples contratos.  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Creación de múltiples contratos por producto de servicio  
Puede crear manualmente un contrato de servicio u oferta de contrato para productos de servicio registrados en contratos no cancelados propiedad del mismo cliente. Para hacerlo, siga el procedimiento estándar para crear contratos de servicio y ofertas de contrato de servicio. Para obtener más información, consulte [Trabajar con contratos de servicio y ofertas de contrato de servicio](service-how-to-create-service-contracts-and-service-contract-quotes.md).  
  
Cuando se agrega un producto de servicio a una línea de contrato que ya está registrado en otro contrato de servicio u oferta de contrato, se muestra un mensaje de advertencia que indica que el producto de servicio ya pertenece a uno o varios contratos de servicio u ofertas de contrato. Si confirma este mensaje, toda la información pertinente del producto de servicio se copiará en la línea de contrato recién creada.  
  
## <a name="copying-documents"></a>Copiar documentos  
Puede crear automáticamente un contrato de servicio u oferta de contrato para productos de servicio ya registrados en otros contratos de servicio u ofertas de contratos mediante la acción **Copiar documento**.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Creación de pedidos de servicios para múltiples contratos  
Puede crear un pedido de servicio manualmente para un producto de servicio que esté registrado en múltiples contratos activos. Un contrato de servicio está activo cuando está firmado y no ha caducado.  
  
## <a name="see-also"></a>Consulte también  
[Cumplimiento de contratos de servicio](service-fulfill-service-contracts.md)  
[Crear pedidos de servicio](service-how-to-create-service-orders.md)  
