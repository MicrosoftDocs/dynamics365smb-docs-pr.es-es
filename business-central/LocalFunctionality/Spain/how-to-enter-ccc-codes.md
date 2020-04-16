---
title: Introducción de códigos CCC
description: El Código Cuenta Cliente (CCC) es un código de identificación de cuentas bancarias único. Los siguientes campos de componentes componen la estructura de código CCC de 20 dígitos (España) o 21 dígitos (Portugal).
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1eebd4d936a13d6bfa197f79bcaf2dd67211fe07
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189187"
---
# <a name="enter-ccc-codes"></a>Introducir códigos CCC
El Código Cuenta Cliente (CCC) es un código de identificación de cuentas bancarias único. Los siguientes campos de componentes componen la estructura de código CCC de 20 dígitos (España) o 21 dígitos (Portugal).  

Si modifica la estructura del código CCC, el campo **Nº CCC** se actualiza automáticamente. De igual forma, si modifica el campo **Nº CCC** la estructura del código CCC se actualiza automáticamente.  

## <a name="to-enter-ccc-codes"></a>Para introducir códigos CCC  

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Información de empresa** y, a continuación, seleccione el vínculo relacionado.  
2.  Rellene los campos de la ficha desplegable **Pagos**, tal como se describe en la tabla siguiente  

    |Campo|Description|  
    |---------------------------------|--------------|---------------------------------------|  
    |**CCC Cód. banco**|1-4|Identifica el banco en el que se ha abierto la cuenta.|  
    |**CCC Cód. oficina**|5-8|Identifica el código de la oficina. Si el banco no utiliza esta referencia, pueden ser ceros.|  
    |**CCC Dígito control**|9-10|Identifica los dígitos de control.|  
    |**CCC Nº cuenta**|11-20 (España)<br /><br /> 11-21 (Portugal)|Identifica el número de cuenta, que se puede ajustar con ceros a la izquierda.|  

## <a name="see-also"></a>Consulte también  
[Funcionalidad local para España](spain-local-functionality.md)
