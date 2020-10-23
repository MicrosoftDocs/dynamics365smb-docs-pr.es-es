---
title: Administración de valores de opciones que faltan
description: Aprenda a evitar que falle la sincronización completa porque las opciones difieren en los campos asignados.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 9148217400da88506e41b460157fe00be596a7c5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911679"
---
# <a name="handling-missing-option-values"></a>Administración de valores de opciones que faltan
[!INCLUDE[d365fin](includes/cds_long_md.md)] contiene solo tres campos de conjunto de opciones que contienen valores de opciones que puede asignar a campos [!INCLUDE[d365fin](includes/d365fin_md.md)] de tipo de opción<!-- Option type, not enum? @Onat can you vertify this? --> para sincronización automática. Durante la sincronización, las opciones no asignadas se ignoran y las opciones que faltan se anexan a la tabla [!INCLUDE[d365fin](includes/d365fin_md.md)] relacionada y se agregan la tabla de sistema **Asignación de opciones de CDS** para su administración manual más tarde. Por ejemplo, agregando las opciones que faltan en cualquiera de los productos y luego actualizando la asignación. Esta sección describe cómo funciona.

La página **Asignación de tablas de integración** contiene tres mapas de campos con uno o más valores de opciones asignados. Después de una sincronización completa, la página **Asignación de opciones de CDS** contiene las opciones no asignadas en los tres campos respectivamente.

|         Registro             | Valor de opción | Título del valor de opción |
|----------------------------|--------------|----------------------|
| Condiciones de pago: NET30       | 1            | Neto 30               |
| Condiciones de pago: 2%10NET30   | 2            | 2% 10; Neto 30        |
| Condiciones de pago: NET45       | 3            | Neto 45               |
| Condiciones de pago: NET60       | 4            | Neto 60               |
| Condiciones de envío: FOB       | 1            | FOB                  |
| Condiciones de envío: NOCHARGE  | 2            | Sin cargo            |
| Transportista: AIRBORNE   | 1            | Airborne             |
| Transportista: DHL        | 2            | DHL                  |
| Transportista: FEDEX      | 3            | FedEx                |
| Transportista: UPS        | 4            | UPS                  |
| Transportista: POSTALMAIL | 5            | Correo postal          |
| Transportista: FULLLOAD   | 6            | Carga completa            |
| Transportista: WILLCALL   | 7            | Recogida a cargo del cliente            |

El contenido de la página **Asignación de opciones de CDS** se basa en los valores de enumeración de la tabla **Cuenta de CDS**. En [!INCLUDE[d365fin](includes/cds_long_md.md)], los siguientes campos en la entidad de cuenta se asignan a campos en los registros de clientes y proveedores:

- **Dirección 1: Términos de flete** del tipo de datos Enum, donde los valores se definen de la siguiente manera:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Dirección 1: Método de envío** del tipo de datos Enum, donde los valores se definen de la siguiente manera:

```
enum 5336 "CDS Shipping Agent Code"
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Condiciones de pago** del tipo de datos Enum, donde los valores se definen de la siguiente manera:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Todas las enumeraciones [!INCLUDE[d365fin](includes/d365fin_md.md)] anteriores se asignan a conjuntos de opciones de [!INCLUDE[d365fin](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-d365fin"></a>Extensión de conjuntos de opciones en [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Cree una nueva extensión AL.

2. Agregue una extensión Enum para las opciones que desea extender. Asegúrese de usar el mismo valor. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Debe usar los mismos valores de id. de opción de [!INCLUDE[d365fin](includes/cds_long_md.md)] cuando extiende la enumeración [!INCLUDE[d365fin](includes/d365fin_md.md)]. De lo contrario, se producirá un error de sincronización.

> [!IMPORTANT]  
> No utilice el carácter "," en los valores y títulos de Enum. Actualmente, esto no es compatible con el tiempo de ejecución [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Los primeros diez caracteres de los nuevos nombres de valores de opciones y títulos deben ser únicos. Por ejemplo, dos opciones llamadas "Transferir 20 días hábiles" y "Transferir 20 días naturales" causarán un error porque ambos tienen los mismos 10 primeros caracteres, "Transferir 2". Nómbrelos, por ejemplo, "TRF20 DH" y "TRF20 DN".

### <a name="update-d365fin-option-mapping"></a>Actualizar la asignación de opciones [!INCLUDE[d365fin](includes/cds_long_md.md)]
Ahora puede recrear la asignación entre las opciones [!INCLUDE[d365fin](includes/cds_long_md.md)] y los registros [!INCLUDE[d365fin](includes/d365fin_md.md)].

En la página **Asignación de tablas de integración**, elija la línea para la asignación **Condiciones de pago** y luego elija la acción **Sincronizar registros modificados**. La página **Asignación de opciones de CDS** se actualiza con los registros adicionales siguientes.

|         Registro                 | Valor de opción   | Título del valor de opción |
|--------------------------------|----------------|----------------------|
| Condiciones de pago: NET30           | 1              | Neto 30               |
| Condiciones de pago: 2%10NET30       | 2              | 2% 10; Neto 30        |
| Condiciones de pago: NET45           | 3              | Neto 45               |
| Condiciones de pago: NET60           | 4              | Neto 60               | 
| **Condiciones de pago: CASH PAYME**  | **779800001**  | **Pago efectivo**     |
| **Condiciones de pago: TRANSFER**    | **779800002**  | **Transferencia**         |

La tabla **Condiciones de pago** de [!INCLUDE[d365fin](includes/d365fin_md.md)] tendrá nuevos registros para las opciones [!INCLUDE[d365fin](includes/cds_long_md.md)]. En la siguiente tabla, las nuevas opciones están en negrita. Las filas en cursiva representan todas las opciones que ahora se pueden sincronizar. Las filas restantes representan opciones que no están en uso y se ignorarán durante la sincronización. Puede eliminarlas o ampliar las opciones de CDS con los mismos nombres.

| Code       | Cálculo de fecha de vencimiento | Fecha cálculo dto. P.P. | % descuento | Calc. dto. P.P. en abonos | Descripción       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 DÍAS    | 10D                  |                           | 0.         | FALSE                         | Neto 10 días       |
| 14 DÍAS    | 14D                  |                           | 0.         | FALSE                         | Neto 14 días       |
| 15 DÍAS    | 15D                  |                           | 0.         | FALSE                         | Neto 15 días       |
| 1M(8D)     | 1M                   | 8D                        | 2.         | FALSE                         | 1 mes/2% 8 días |
| 2 DÍAS     | 2D                   |                           | 0.         | FALSE                         | Neto 2 días        |
| *2%10NET30* |                      |                           | 0.         | FALSE                         |                   |
| 21 DÍAS    | 21D                  |                           | 0.         | FALSE                         | Neto 21 días       |
| 30 DÍAS    | 30D                  |                           | 0.         | FALSE                         | Neto 30 días       |
| 60 DÍAS    | 60D                  |                           | 0.         | FALSE                         | Neto 60 días       |
| 7 DÍAS     | 7D                   |                           | 0.         | FALSE                         | Neto 7 días        |
| ***CASH PAYME*** |                      |                           | 0.         | FALSE                         |                   |
| PM         | PM                   |                           | 0.         | FALSE                         | Mes actual     |
| COD        | 0D                   |                           | 0.         | FALSE                         | Contado  |
| *NET30*      |                      |                           | 0.         | FALSE                         |                   |
| *NET45*      |                      |                           | 0.         | FALSE                         |                   |
| *NET60*      |                      |                           | 0.         | FALSE                         |                   |
| ***TRANSFER*** |                      |                           | 0.         | FALSE                         |                   |

## <a name="see-also"></a>Consulte también
