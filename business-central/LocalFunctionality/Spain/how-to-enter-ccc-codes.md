---
title: 'Cómo introducir códigos CCC [ES]'
description: Aprenda a ingresar el código de identificación de cuenta bancaria único Código Cuenta Cliente (CCC) utilizando la versión en español de Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/21/2021
ms.author: edupont
---
# <a name="enter-ccc-codes-in-the-spanish-version"></a><a name="enter-ccc-codes-in-the-spanish-version"></a>Ingrese códigos CCC en la versión en español
El Código Cuenta Cliente (CCC) es un código de identificación de cuentas bancarias único. Los siguientes campos de componentes componen la estructura de código CCC de 20 dígitos (España) o 21 dígitos (Portugal).  

Si modifica la estructura del código CCC, el campo **Nº CCC** se actualiza automáticamente. De igual forma, si modifica el campo **Nº CCC** la estructura del código CCC se actualiza automáticamente.  

## <a name="to-enter-ccc-codes"></a><a name="to-enter-ccc-codes"></a>Para introducir códigos CCC

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información empresa** y luego elija el enlace relacionado.  
2.  Rellene los campos de la ficha desplegable **Pagos**, tal como se describe en la tabla siguiente  

    |Campo|Posición|Descripción|  
    |---------------------------------|--------------|---------------------------------------|  
    |**CCC Cód. banco**|1-4|Identifica el banco en el que se ha abierto la cuenta.|  
    |**CCC Cód. oficina**|5-8|Identifica el código de la oficina. Si el banco no utiliza esta referencia, pueden ser ceros.|  
    |**CCC Dígito control**|9-10|Identifica los dígitos de control.|  
    |**CCC Nº cuenta**|11-20 (España)<br /><br /> 11-21 (Portugal)|Identifica el número de cuenta, que se puede ajustar con ceros a la izquierda.|  

## <a name="see-also"></a><a name="see-also"></a>Consulte también
[Funcionalidad local para España](spain-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
