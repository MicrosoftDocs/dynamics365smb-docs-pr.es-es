---
title: Configuración de sostenibilidad
description: Aprenda a configurar características de sostenibilidad.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Configuración de sostenibilidad

Antes de que el módulo de sostenibilidad pueda funcionar correctamente, debe configurar algunos controles e instrucciones básicos relacionados con toda la funcionalidad.

Para configurar un módulo de sostenibilidad, siga los pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de sostenibilidad** y luego seleccione el vínculo relacionado.
2. En la ficha desplegable **General**, configure los campos obligatorios relacionados con el módulo de sostenibilidad.

    | Campo | Descripción |
    |-------|-------------|
    | **Código de unidad de medida de emisiones** | Especifique el código de unidad de medida que se utiliza para registrar las emisiones. |
    | **Posiciones decimales emisión** | Especifique el número de decimales que se muestran para las cantidades de emisión. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |
    | **País o región obligatorio** | Especifique si el valor de país o región es obligatorio. Los usuarios pueden configurar el campo de país o región en los diarios incluso si no selecciona este campo. Sin embargo, al seleccionarlo, requiere que los usuarios configuren el campo de país o región antes de publicar. |
    | **Centro de responsabilidad obligatorio** | Especifique si el centro de responsabilidad es obligatorio. El centro de responsabilidad se puede utilizar como una instalación, de modo que se puedan medir las emisiones basadas en las instalaciones. Los usuarios pueden configurar el centro de responsabilidad en los diarios incluso si no selecciona este campo. Sin embargo, al seleccionarlo, requiere que los usuarios configuren el centro de responsabilidad antes de publicar. |
    | **Cambio de base de cálculo de bloques si existen movimientos** | Especifique si los cambios en la base de cálculo (fórmula) a nivel de categoría de cuenta se bloquean en el momento de la entrada de sostenibilidad, cuando la fórmula ya se ha aplicado. |
    | **Habilitar comprobación de errores en segundo plano** | Especifique si está habilitada la comprobación de errores en segundo plano de las líneas del diario de sostenibilidad. |

    > [!NOTE]
    > Después de activar o desactivar la comprobación de errores en segundo plano en los diarios, deberá volver a iniciar sesión antes de iniciar la nueva configuración.

3. En la ficha desplegable **Cálculos**, configure los campos obligatorios relacionados con las fórmulas que se utilizan para calcular las emisiones.

    | Campo | Descripción |
    |-------|-------------|
    | **Posiciones decimales combustible/electricidad** | Especifique el número de decimales que se muestran para los importes de combustible/electricidad. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |
    | **Posiciones decimales distancia** | Especifique el número de decimales que se muestran para las mediciones de distancia. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |
    | **N.º decimales para importes personalizados** | Especifique el número de decimales que se muestran para los importes personalizados. El ajuste predeterminado es *2:5*, indica que se muestran un mínimo de dos decimales y un máximo de cinco decimales para todos los importes. También puede introducir un número fijo. Por ejemplo, si introduce *2*, se muestran dos decimales para todos los importes. |

4. En la ficha desplegable **Informes**, complete la configuración configurando los campos relacionados con la presentación de informes a las autoridades.

    > [!NOTE]
    > En la versión 24.0, [!INCLUDE[prod_short](includes/prod_short.md)] no admite informes para ninguna autoridad. Por lo tanto, los campos que están relacionados con la configuración de esta funcionalidad en la ficha desplegable **Informes** están destinados a futuras capacidades de generación de informes. Sin embargo, los partners también pueden utilizar estos campos en versiones localizadas.

    | Campo | Descripción |
    |-------|-------------|
    | **Código de unidad de medida de notificación de emisiones** | Especifique el código de unidad de medida que se utiliza para informar de las emisiones, ya que puede utilizar diferentes unidades de medida al informar a las autoridades. Este campo no es aplicable a los informes estándar. |
    | **Factor UOM de notificación** | Especifique el factor de unidad de medida que se utiliza para registrar la emisión si utiliza diferentes unidades de medida al informar a las autoridades. |
    | **Precisión de redondeo de emisiones** | Especifique el tamaño del intervalo que se usará al redondear cantidades de emisiones al informar a las autoridades. |
    | **Tipo de redondeo de emisiones** | Especifique cómo el programa redondea las cantidades de emisiones cuando informa a las autoridades. Las siguientes opciones están disponibles: **Más cercano**, **Hacia arriba** y **Hacia abajo**. |

## <a name="see-also"></a>Consulte también

[Finanzas](finance.md)  
[Información general de la administración de la sostenibilidad](finance-manage-sustainability.md)  
[Plan de cuentas y libro mayor de sostenibilidad](finance-sustainability-accounts-ledger.md)  
[Registrar entradas de sostenibilidad](finance-sustainability-journal.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
