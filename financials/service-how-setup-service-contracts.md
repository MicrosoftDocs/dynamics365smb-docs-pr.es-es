---
title: Configurar contratos de servicio | Documentos de Microsoft
description: "Aprenda cómo configurar contratos de servicio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 203f6ef7f156bdccaa491fdac761711fd32c317e
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---

# <a name="how-to-set-up-service-contracts"></a>Cómo configurar contratos de servicio
Antes de que pueda trabajar con contratos, debe configurar las opciones siguientes: 

* **Grupos contrato servicio**, que reúne contratos de servicio relacionados.
* Los **grupos de cuentas de contratos de servicio**, que se utilizan para agrupar las cuentas de contratos de servicio que se utilizan para agrupar las cuentas de contratos de servicio con las facturas de servicio creadas para los contratos de servicio. Asigne estos grupos a los contratos de servicio.  
* **Plantillas de contratos** que definen las disposiciones del contrato de contratos que incluyen los detalles del contrato de servicio más utilizados. Puede utilizar plantillas cuando cree ofertas de contrato de servicio. Al crear una oferta de contrato, los campos contienen automáticamente el contenido de los campos de la plantilla.
* Las **Plantillas de clientes** que le permiten crear ofertas para contactos o clientes potenciales que no están registrados como clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Para configurar un grupo de contratos de servicio  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos contrato servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Elija la casilla **Sólo dto. en pedidos contrat.** si desea que los descuentos de contrato o servicio sean válidos únicamente para pedidos de servicio de contrato, como el mantenimiento.  

## <a name="to-set-up-a-service-contract-account-group"></a>Para configurar un grupo de cuentas de contratos de servicio  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos contables contr. serv.** y, a continuación, seleccione el vínculo relacionado.  
2. Cree un grupo de cuentas de contratos de servicio nuevo.   
3. Rellene los campos **Código** y **Descripción**. Estos campos describen el grupo de cuentas de servicio.  
4. Rellene el campo **Cuenta contrato no prepago**, elija el número de la cuenta contable de no prepago.  
5. En el campo **Cuenta contrato no prepago**, elija el número de la cuenta contable de prepago.  

## <a name="to-set-up-a-contract-template"></a>Para configurar una plantilla de contrato  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas contrato servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Cree una plantilla de contrato de servicio nueva.  
3. En el campo **N.º**, introduzca un número para la plantilla de contrato.  
  
     Si ha configurado series numéricas para plantillas de contrato en la ventana **Config. gestión servicio**, también puede presionar la tecla Enter para especificar el siguiente número de plantilla de contrato disponible. Rellene el resto de los campos en caso necesario.  
  
4. En la ficha desplegable **Factura**, rellene el campo **Código de grupo de cuentas de contrato de servicio**, **Período de factura**, etc. Rellene el resto de los campos en caso necesario.  
5. Elija la acción **Descuentos servicio** para agregar descuentos de contrato.  

## <a name="to-set-up-a-customer-template"></a>Para configurar una plantilla de cliente  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas cliente** y, a continuación, seleccione el vínculo relacionado.  
2. Cree una ficha de plantilla de cliente nueva.  
3. En la ficha desplegable **General**, escriba un nombre y una descripción para la plantilla de cliente en los campos **Código** y **Descripción** respectivamente. 
4. Para definir los criterios de búsqueda, rellene los otros campos, como **Cód. país/región**, **Cód. territorio** y **Cód. idioma**.  
5. Rellene los campos **Grupo contable negocio** y **Grupo contable cliente**.  

## <a name="see-also"></a>Consulte también
[Configurar la gestión de servicios](service-setup-service.md)