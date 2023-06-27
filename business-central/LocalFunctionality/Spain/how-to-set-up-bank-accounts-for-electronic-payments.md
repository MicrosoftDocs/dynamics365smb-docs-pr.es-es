---
title: 'Cuentas bancarias para pagos electrónicos [ES]'
description: Aprenda a utilizar Business Central para configurar cuentas bancarias y cuentas bancarias de proveedores para realizar pagos electrónicos.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-bank-accounts-for-electronic-payments-in-the-spanish-version"></a><a name="set-up-bank-accounts-for-electronic-payments-in-the-spanish-version"></a>Configurar cuentas bancarias para pagos electrónicos en la versión en español
En [!INCLUDE[prod_short](../../includes/prod_short.md)], puede configurar cuentas bancarias para realizar pagos electrónicos.  

## <a name="to-set-up-bank-accounts-for-electronic-payments"></a><a name="to-set-up-bank-accounts-for-electronic-payments"></a>Para configurar cuentas bancarias para realizar pagos electrónicos

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ficha banco** y luego elija el enlace relacionado.  
2.  En la ficha desplegable **Transferencia**, asegúrese de que los campos **CCC Cód. banco**, **CCC Cód. oficina**, **CCC Dígito control** y **CCC Nº cuenta** se rellenan correctamente.  
3.  En la ficha desplegable **Transferencia**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ruta archivo exp. pago elec.**|Introduzca la ruta de acceso completa del archivo de pago electrónico, empiece con la letra de la unidad y acabe con una barra diagonal inversa (\). El nombre no se escribe aquí. Debe utilizar el directorio donde [!INCLUDE[prod_short](../../includes/prod_short.md)] se encuentra instalado. Por ejemplo, podría escribir **C:NAV** en este campo. Puede escribir 100 caracteres como máximo.|  
    |**Nom. arch. exp. últ. pago elec.**|Especifique el nombre del archivo con la extensión de nombre de archivo .txt, sin la ruta. Debido a que el nombre del archivo se incrementará cada vez que se exporte un archivo de pago electrónico, este nombre de archivo debe tener dígitos. De esta forma se creará un registro permanente de cada archivo que haya exportado al banco. Por ejemplo, **DD000000.txt** podría ser la primera entrada de este campo. Puede escribir 50 caracteres como máximo.|  

4.  En la ficha desplegable **Registrando**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nº último aviso pago**|Especifique una serie de números distinta a la serie de números de los cheques. Esto es necesario para que los números no entren en conflicto entre sí. El aviso de pago se imprime en papel en blanco de forma que resulte fácil enviarlo al proveedor.|  

## <a name="to-set-up-vendor-bank-accounts-for-electronic-payments"></a><a name="to-set-up-vendor-bank-accounts-for-electronic-payments"></a>Para configurar cuentas bancarias para realizar pagos electrónicos

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ficha banco proveedor** y luego elija el enlace relacionado.  
2.  En la ficha desplegable **General**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Usar para pagos electrónicos**|Especifica si debe usarse esta cuenta bancaria del proveedor para los pagos electrónicos. Para realizar pagos electrónicos solo se puede seleccionar una cuenta de banco por proveedor.|  

3.  En la ficha desplegable **Transferencia**, asegúrese de que los campos **CCC Cód. banco**, **CCC Cód. oficina**, **CCC Dígito control** y **CCC Nº cuenta** se rellenan correctamente.  

## <a name="see-also"></a><a name="see-also"></a>Consulte también
 [Pagos electrónicos – AEB N34.1](electronic-payments-aeb-n341.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
