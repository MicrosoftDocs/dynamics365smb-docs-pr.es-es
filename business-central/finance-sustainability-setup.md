---
title: Configuración de sostenibilidad
description: Aprenda a configurar características de sostenibilidad.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Configuración de sostenibilidad  

Para que el módulo de Sostenibilidad funcione correctamente, primero debe configurar algunos controles e instrucciones básicos relacionados con toda la funcionalidad.  

Para configurar un módulo de sostenibilidad, siga los siguientes pasos:  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), icono, escriba **Configuración de sostenibilidad** y luego elija el vínculo relacionado.  
2. En la ficha desplegable **General**, configure los campos obligatorios relacionados con este módulo:   

|  Campo  |  Descripción  |  
|--------|--------------| 
| **Código de unidad de medida de emisiones** | Especifica el código de unidad de medida que se utiliza para registrar la emisión. |
| **Posiciones decimales emisión** | Especifica el número de decimales que se muestran para las cantidades de emisión. La configuración predeterminada, 2:5, especifica que todas las cantidades se muestran con un mínimo de 2 decimales y un máximo de 5 decimales. También puede introducir un número fijo, como 2, lo que también significa que los importes se muestran con dos decimales. |
| **País o región obligatorio** | Especifica si el valor de país o región es obligatorio. Puede usar este campo en diarios sin configurarlo, pero puede seleccionarlo si desea obligar a los usuarios a completar el campo antes de registrar. |
| **Centro de responsabilidad obligatorio** | Especifica si el centro de responsabilidad es obligatorio, ya que el centro de responsabilidad se puede utilizar como una instalación para medir las emisiones basadas en instalaciones. Puede usar este campo en diarios sin configurarlo, pero puede seleccionarlo si desea obligar a los usuarios a completar el campo antes de registrar. |
| **Cambio de base de cálculo de bloques si existen movimientos** | Especifica si el cambio de base de cálculo en la Categoría de cuenta está bloqueado al momento de la entrada de sostenibilidad, lo que significa que esta fórmula ya se aplicó. |
| **Habilitar comprobación de errores en segundo plano** | Especifica si está habilitada la comprobación de errores en segundo plano de las líneas del diario de sostenibilidad. |

3.  En la ficha desplegable **Cálculos**, configure los campos obligatorios relacionados con las fórmulas utilizadas para calcular las emisiones:  

|  Campo  |  Descripción  |  
|--------|--------------| 
| **Posiciones decimales combustible/electricidad** | Especifica el número de decimales que se muestran para los importes de combustible/electricidad. La configuración predeterminada, 2:5, especifica que todas las cantidades se muestran con un mínimo de 2 decimales y un máximo de 5 decimales. También puede introducir un número fijo, como 2, lo que también significa que los importes se muestran con dos decimales. |
| **Posiciones decimales distancia** | Especifica el número de decimales que se muestran para las mediciones de distancia. La configuración predeterminada, 2:5, especifica que todas las cantidades se muestran con un mínimo de 2 decimales y un máximo de 5 decimales. También puede introducir un número fijo, como 2, lo que también significa que los importes se muestran con dos decimales. |
| **N.º decimales para importes personalizados** | Especifica el número de decimales que se muestran para los importes personalizados. La configuración predeterminada, 2:5, especifica que todas las cantidades se muestran con un mínimo de 2 decimales y un máximo de 5 decimales. También puede introducir un número fijo, como 2, lo que también significa que los importes se muestran con dos decimales. |

4.  Termine la configuración en la ficha desplegable **Informes**, relacionada con la presentación de informes a las autoridades:   

|  Campo  |  Descripción  |  
|--------|--------------| 
| **Código de unidad de medida de notificación de emisiones** | Especifica el código de unidad de medida que se utiliza para informar las emisiones, ya que puede utilizar diferentes unidades de medida al informar a las autoridades. Este campo no es aplicable a los informes estándar. |
| **Factor UOM de notificación** | Especifica el factor de unidad de medida que se utiliza para registrar la emisión si utiliza diferentes unidades de medida al informar a las autoridades. |
| **Precisión de redondeo de emisiones** | Especifica el tamaño del intervalo que se usará al redondear cantidades de emisiones al informar a las autoridades. |
| **Tipo de redondeo de emisiones** | Especifica cómo el programa redondea una cantidad de emisión mientras informa a las autoridades, usando opciones: Más cercano, Arriba o Abajo. |

>[!NOTE]
> En la versión 24.0, [!INCLUDE[prod_short](includes/prod_short.md)] no admite informes para ninguna autoridad. Entonces, el campo relacionado con la configuración en la ficha desplegable **Informes** se utilizará para capacidades de generación de informes futuras, pero los socios también pueden utilizarla en versiones localizadas.

## Consulte también  
[Finanzas](finance.md)    
[Información general de administración de la sostenibilidad](finance-manage-sustainability.md)
[Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md)
[Cómo registrar emisiones](finance-sustainability-journal.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
