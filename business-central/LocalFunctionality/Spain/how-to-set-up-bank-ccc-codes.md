---
title: 'Configurar códigos CCC bancarios [ES]'
description: 'El Código Cuenta Cliente (CCC) es un código de cuenta único usado por los bancos para identificar a sus clientes. El código CCC se imprime en los documentos bancarios, como cheques y extractos.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/12/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-bank-ccc-codes-in-the-spanish-version"></a>Configurar códigos CCC bancarios en la versión de español

El Código Cuenta Cliente (CCC) es un código de cuenta único usado por los bancos españoles para identificar a sus clientes. El código CCC se imprime en los documentos bancarios, como cheques y extractos.  

Se pueden configurar códigos CCC en las siguientes ubicaciones:  

- Página **Ficha banco**  
- Página **Información de empresa**  
- Página **Ficha banco cliente**  
- Página **Ficha banco proveedor**  

El procedimiento siguiente describe cómo configurar códigos CCC de banco para su empresa.  

## <a name="to-enter-ccc-codes"></a>Para introducir códigos CCC

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información empresa** y luego elija el enlace relacionado.  
2. Rellene los campos de la ficha desplegable **Pagos**, tal como se describe en la tabla siguiente.  

    |Campo           |Posición |Descripción                            |  
    |----------------|---------|---------------------------------------|  
    |**CCC Cód. banco**|1-4|Identifica el banco que abrió la cuenta.|  
    |**CCC Cód. oficina**|5-8|Identifica el código de la oficina. Si el banco no utiliza esta referencia, el código de la oficina pueden ser ceros.|  
    |**CCC Dígito control**|9-10|Identifica los dígitos de control.|  
    |**CCC Nº cuenta**|11-20 (España)<br /><br /> 11-21 (Portugal)|Identifica el número de cuenta, que se puede ajustar con ceros a la izquierda.|  

El siguiente procedimiento describe cómo configurar códigos bancarios CCC para cuentas bancarias de clientes existentes, pero los mismos pasos se aplican a proveedores, cuentas bancarias e información de la compañía.  

## <a name="to-set-up-bank-ccc-codes-for-a-customer-bank-account"></a>Para configurar códigos CCC de banco de un banco cliente

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ficha banco cliente** y luego elija el enlace relacionado.  
2  En la ficha desplegable **Transferencia**, escriba la información en los campos CCC relevantes.  

    > [!NOTE]  
    >  Debe configurar información de la empresa en la ficha desplegable **Pagos**.  

3. Elija el botón **Aceptar**.  

## <a name="see-also"></a>Consulte también

[Configurar cuentas bancarias](../../bank-how-setup-bank-accounts.md) 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
