---
title: "Configurar cuentas bancarias para realizar pagos electrónicos"
description: "En Business Central, puede configurar cuentas bancarias para realizar pagos electrónicos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 22be19a5009f56f52b61601bfa7069f0e7ea2546
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-bank-accounts-for-electronic-payments"></a>Configurar cuentas bancarias para realizar pagos electrónicos
En [!INCLUDE[d365fin](../../includes/d365fin_md.md)], puede configurar cuentas bancarias para realizar pagos electrónicos.  

## <a name="to-set-up-bank-accounts-for-electronic-payments"></a>Para configurar cuentas bancarias para realizar pagos electrónicos  

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ficha banco** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **Transferencia**, asegúrese de que los campos **CCC Cód. banco**, **CCC Cód. oficina**, **CCC Dígito control** y **CCC Nº cuenta** se rellenan correctamente.  
3.  En la ficha desplegable **Transferencia**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ruta archivo exp. pago elec.**|Introduzca la ruta de acceso completa del archivo de pago electrónico, empiece con la letra de la unidad y acabe con una barra diagonal inversa (\). El nombre no se escribe aquí. Debe utilizar el directorio donde [!INCLUDE[d365fin](../../includes/d365fin_md.md)] se encuentra instalado. Por ejemplo, podría escribir **C:NAV** en este campo. Puede escribir 100 caracteres como máximo.|  
    |**Nom. arch. exp. últ. pago elec.**|Especifique el nombre del archivo con la extensión de nombre de archivo .txt, sin la ruta. Debido a que el nombre del archivo se incrementará cada vez que se exporte un archivo de pago electrónico, este nombre de archivo debe tener dígitos. De esta forma se creará un registro permanente de cada archivo que haya exportado al banco. Por ejemplo, **DD000000.txt** podría ser la primera entrada de este campo. Puede escribir 50 caracteres como máximo.|  

4.  En la ficha desplegable **Registrando**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nº último aviso pago**|Especifique una serie de números distinta a la serie de números de los cheques. Esto es necesario para que los números no entren en conflicto entre sí. El aviso de pago se imprime en papel en blanco de forma que resulte fácil enviarlo al proveedor.|  

## <a name="to-set-up-vendor-bank-accounts-for-electronic-payments"></a>Para configurar cuentas bancarias para realizar pagos electrónicos  

1.  Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ficha banco proveedor** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **General**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Usar para pagos electrónicos**|Especifica si debe usarse esta cuenta bancaria del proveedor para los pagos electrónicos. Para realizar pagos electrónicos solo se puede seleccionar una cuenta de banco por proveedor.|  

3.  En la ficha desplegable **Transferencia**, asegúrese de que los campos **CCC Cód. banco**, **CCC Cód. oficina**, **CCC Dígito control** y **CCC Nº cuenta** se rellenan correctamente.  

## <a name="see-also"></a>Consulte también  
 [Pagos electrónicos – AEB N34.1](electronic-payments-aeb-n341.md)

