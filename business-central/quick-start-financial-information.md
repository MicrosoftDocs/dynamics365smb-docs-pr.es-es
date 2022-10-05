---
title: Inicio rápido de información financiera
description: Prepare su empresa para hacer negocios configurando la información financiera en Business Central.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: ''
ms.date: 08/25/2022
ms.author: a-reishima
ms.openlocfilehash: 6d8383015e977acffe94555eec00bfb8f104085d
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2022
ms.locfileid: "9586081"
---
# <a name="financial-information-quick-start"></a>Inicio rápido de información financiera

Después de especificar la información básica de la empresa en [!INCLUDE[prod_short](includes/prod_short.md)], uno de los siguientes pasos es completar la sección financiera. Lo hace no solo para recibir o realizar pagos, sino también para gestionar e informar adecuadamente de los números de su negocio.

## <a name="the-chart-of-accounts"></a>Plan de cuentas

El plan de cuentas ofrece una descripción general de las finanzas de la empresa, enumerando las cuentas en grupos estructurados como activos, pasivos, ingresos, coste de los bienes vendidos y gastos. [!INCLUDE[prod_short](includes/prod_short.md)] incluye un plan de cuentas estándar que puede adaptar a las prácticas contables de su empresa.

## <a name="set-up-the-chart-of-accounts"></a>Configurar el plan de cuentas

El siguiente vídeo le muestra cómo configurar el plan de cuentas en [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts"></a>Añadir una cuenta al plan de cuentas

Para agregar una cuenta no incluida de manera predeterminada en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, los servicios de jardinería, solo tiene que seguir estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el vínculo relacionado.
2. Elija la acción **Nuevo** para abrir la página **Ficha cuenta**.
3. Introduzca los siguientes datos en los campos correspondientes de la ficha desplegable **General**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Campo | Datos |
   | --- | --- |
   | **Nº** | 61250 |
   | **Nombre** | Servicios de jardinería |
   | **Ingresos/Saldo** | Extracto de ingresos |
   | **Categoría de cuenta** | Gasto |
   | **Subcategoría de cuenta** | Gastos en reparaciones y mantenimiento |
   | **Debe/Haber** | Ambos |
   | **Tipo mov.** | Registrar |

4. En la ficha desplegable **Registro**, escriba los siguientes datos:

   | Campo | Datos |
   | --- | --- |
   | **Tipo de registro general** | Compra |
   | **Grupo contable negocio** | Nac. |
   | **Grupo contable producto** | Servicios |

5. Rellene el resto de los campos de la página **Ficha cuenta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts"></a>Obtener una visión general del plan de cuentas

Si necesita una vista más compacta del plan de cuentas, sin columnas para los grupos de contabilización, el tipo de contabilización o el tipo de coste, por ejemplo **Introducción al plan de cuentas** recopila la información principal de cada cuenta en una tabla más pequeña. Además, puede contraer o expandir los grupos para ocultar las cuentas que hay en ellos.

Para mostrar la vista general, elija la acción **Introducción al plan de cuentas** de la página **Plan de cuentas** o busque la función usando ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer").

Obtenga más información sobre el plan de cuentas y el libro mayor en [Descripción de contabilidad y plan de cuentas](finance-general-ledger.md).

## <a name="set-up-bank-accounts"></a>Configurar cuentas bancarias

Las cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)] registran las transacciones bancarias y están asociadas a las entradas del plan de cuentas. El siguiente vídeo le muestra cómo configurar cuentas bancarias.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el vínculo relacionado.
2. En la página **Cuentas bancarias**, elija la acción **Nuevo**.
3. En el campo **N.º**, , se introducirá automáticamente un identificador como *B010* si hay una lista de series numeradas establecida para las cuentas bancarias. Si no, introduzca una combinación única.

   El campo es diferente del campo **N.º cuenta bancaria** también disponible en la ficha desplegable **General**.
4. Rellene los campos de la página **Ficha de cuenta bancaria** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también .

[Configurar el plan de cuentas](finance-setup-chart-accounts.md)  
[Configurar cuentas bancarias](bank-how-setup-bank-accounts.md)  
[Ejecutar e imprimir informes](ui-work-report.md)  
[Inicio rápido de Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
