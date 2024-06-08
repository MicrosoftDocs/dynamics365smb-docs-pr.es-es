---
title: Cambiar el importe anual de los contratos de servicio o las ofertas de contrato
description: puede cambiar el importe que se facturará anualmente en el contrato de servicio o las ofertas de contrato de servicio.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a>Cambiar el importe anual de los contratos de servicio o las ofertas de contrato
Puede cambiar el importe anual del contrato de servicio u oferta de contrato para corregir el importe que se facturará anualmente.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a>Para cambiar el importe anual del contrato de servicio o la oferta de contrato

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , especifique **Contratos servicio** u **Ofertas contrato servicio** y, a continuación, elija el vínculo relacionado.  
2. Elija el contrato o la oferta de contrato.  
3. Elija la acción **Abrir contrato** para abrir el contrato u oferta de contrato para su modificación.  
4. Seleccione la casilla **Permite importes sin saldar** si desea cambiar el importe anual y distribuir la diferencia del importe anual manualmente en la líneas de contrato. En caso contrario, desactive la casilla para distribuir automáticamente la diferencia de importe anual automáticamente en las líneas de contrato después de cambiar el importe anual.  
5. Cambie el contenido del campo **Importe anual**. No puede firmar, es decir, convertir en contrato de servicio si está trabajando en una oferta de contrato ni bloquear el contrato de servicio si tiene un importe anual negativo. Si establece el importe anual en cero, el contenido del campo **Periodo factura** debe ser **Ninguno** al firmar o bloquear el contrato de servicio.  
6. Dependiendo de si activa la casilla **Permite importes sin saldar**, ejecute la distribución manual o automática de la diferencia de importe anual. Las líneas de contrato se actualizarán para que el valor del campo **Importe anual calculado** sea igual al nuevo importe anual.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts"></a>Diferencias de distribución entre cantidades anuales nuevas y calculadas
Si cambia el importe anual de un contrato de servicio o de la oferta de contrato, es posible que desee distribuir la diferencia entre los importes anuales nuevos y calculados en las líneas de contrato. Existen tres formas de distribuir importes:

* Distribución uniforme  
* Distribución basada en Importes de línea  
* Distribución basada en beneficio bruto

### <a name="even-distribution"></a>Distribución uniforme
Si cambia el importe anual del contrato de servicio o de la oferta de contrato, quizás le interese distribuir la diferencia entre los importes anuales nuevos y calculados en las líneas de contrato. La distribución uniforme es uno de los métodos de distribución automática que le pueden ayudar a repartir por igual la diferencia de importes anuales nuevos y calculados entre los importes de líneas en las líneas de contrato. La siguiente lista de los pasos del procedimiento de distribución describe la idea principal de este método:  

1. La diferencia entre los valores de los campos **Importe anual** nuevo e **Importe anual calculado** se divide entre el número de líneas de contrato de la oferta de contrato o el contrato de servicio.  
2. El valor del campo **Importe línea** se actualiza sumando el resultado de la operación anterior.  
3. El contenido de los campos **Importe dto. línea**, **% Descuento línea** y **Bfº bruto** se actualiza en relación con el nuevo valor del campo **Importe dto. línea** de la siguiente forma:   
    * Importe dto. línea = Valor línea - Importe línea.  
    * % Descuento línea = (Importe dto. línea/ Valor línea) * 100.  
    * Bfº bruto = Importe línea - Coste línea.  

 Los pasos se repiten para cada línea de contrato.  

#### <a name="example"></a>Ejemplo:
La casilla de verificación **Permite importes sin saldar** no está activada en el contrato de servicio que contiene tres líneas de contrato con esta información.  

|Producto|Coste línea|Valor línea|% Descuento línea|Importe dto. línea|Importe línea|Bfº bruto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Producto 1|30,00|40,00|0.00|0.00|40,00|10.00|  
|Producto 2|40,00|50.00|10.00|5.00|45.00|5.00|  
|Producto 3|50.00|70.00|10.00|7.00|63.00|13.00|  

El valor del campo **Importe anual** es igual que el contenido del campo **Importe anual calculado**, que siempre se establece en la suma de los importes de las líneas. En este caso, es igual a lo siguiente: 40 + 45 + 63 = 148.  

Si cambia el **Importe anual** a 139, se calculará el importe que debe sumarse al valor de cada campo **Importe línea**. Este importe se calcula restando el **Importe anual calculado** al valor del nuevo campo de **Importe anual** y dividiendo el resultado entre el número de líneas de contrato del contrato de servicio. En este caso, será igual a lo siguiente: (139 - 148) / 3 = -3. Así, el último valor calculado se suma a cada valor del campo **Importe línea** y a los valores de los campos **% Descuento línea**, **Importe dto. línea** y **Bfº bruto** se actualizan con las fórmulas del procedimiento descrito anteriormente.  

Finalmente, las líneas del contrato tendrán los siguientes datos:  

|Producto|Coste línea|Valor línea|% Descuento línea|Importe dto. línea|Importe línea|Bfº bruto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Producto 1|30,00|40,00|7.50|3.00|37.00|7.00|  
|Producto 2|40,00|50.00|16.00|8.00|42.00|2.00|  
|Producto 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount"></a>Distribución basada en Importe de línea
Si cambia el importe anual del contrato de servicio o de la oferta de contrato, quizás le interese distribuir la diferencia entre los importes anuales nuevos y calculados en las líneas de contrato. La distribución basada en importe de línea es un método automático que le pueden ayudar a repartir la diferencia de importes anuales nuevos y calculados entre los importes de líneas en las líneas de contrato. La distribución se realizará para repartir de forma proporcional el importe de línea en el importe anual calculado. La siguiente lista de los pasos del procedimiento de distribución para cada línea de contrato describe la idea principal de este método:  

1. La contribución del porcentaje del importe de línea se calcula del siguiente modo: el contenido del campo **Importe línea** se divide entre los valores del campo **Importe anual calculado** en todas las líneas de contrato.  
2. El valor del campo **Importe línea** se actualiza sumándole la diferencia entre los importes anuales nuevos y calculados, que se multiplica por la contribución del porcentaje de importe de línea.  
3. El contenido de los campos **Importe dto. línea**, **% Descuento línea** y **Bfº bruto** se actualiza en relación con el nuevo valor del campo **Importe dto. línea** de la siguiente forma:  

    * Importe dto. línea = Valor línea - Importe línea  
    * % Descuento línea = Importe dto. línea / Valor línea * 100  
    * Bfº bruto = Importe línea - Coste línea  

Los pasos se repiten para cada línea de contrato.  

#### <a name="example-1"></a>Ejemplo:
La casilla de verificación **Permite importes sin saldar** no está activada en el contrato de servicio que contiene tres líneas de contrato con esta información.  

|Producto|Coste línea|Valor línea|% Descuento línea|Importe dto. línea|Importe línea|Bfº bruto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Producto 1|15.00|17.00|3.00|0.51|25.00|1.49|  
|Producto 2|20,00|23.00|Ninguno|0.00|55.10|3.00|  
|Producto 3|24.00|27.00|3.00|0.81|112.70|2.19|  

El valor del campo **Importe anual** es igual que el contenido del campo **Importe anual calculado**, que siempre se establece en la suma de los importes de las líneas. En este caso, es igual a lo siguiente: 16,49 + 23,00 + 26,19 = 65,68.  

Si cambia el **Importe anual** a 60, se calcularán las contribuciones del porcentaje de las ganancias para cada línea de contrato:  

* Producto 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Producto 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Producto 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557  

El valor del campo **Importe línea** se actualiza en cada línea de contrato mediante la siguiente fórmula: Importe línea = Importe línea + diferencia entre los importes anuales nuevos y calculados * Porcentaje de contribución. Después de eso, los valores de los campos **Importe dto. línea**, **% Descuento línea** y **Bfº bruto** se actualizan con las fórmulas descritas en el procedimiento anterior.  

Finalmente, las líneas del contrato tendrán los siguientes datos:  

|Producto|Coste línea|Valor línea|% Descuento línea|Importe dto. línea|Importe línea|Bfº bruto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Producto 1|15.00|17.00|11.41|1.94|15.06|0.06|  
|Producto 2|20,00|23.00|8.65|1.99|21.01|1.01|  
|Producto 3|24.00|27.00|11.37|3.07|23.93|-0,07|  

### <a name="distribution-based-on-profit"></a>Distribución basada en beneficio bruto
Si cambia el importe anual del contrato de servicio o de la oferta de contrato, quizás le interese distribuir la diferencia entre los importes anuales nuevos y calculados en las líneas de contrato. La distribución basada en beneficio es uno de los métodos automáticos que le pueden ayudar a repartir la diferencia de importes anuales nuevos y calculados entre los importes de líneas en las líneas de contrato. Esta distribución se realizará un reparto de beneficios de forma proporcional en el contrato total o en el beneficio de la oferta de contrato. La siguiente lista de los pasos del procedimiento de distribución para cada línea de contrato describe la idea principal de este método:  

1. La contribución del porcentaje de beneficio se calcula del siguiente modo: el contenido del campo **Bfº bruto** se divide entre la suma de los valores del campo **Bfº bruto** en todas las líneas de contrato.  
2. El valor del campo **Importe línea** se actualiza sumándole la diferencia entre los importes anuales nuevos y calculados, que se multiplica por la contribución del porcentaje de beneficio.  
3. El contenido de los campos Importe dto. línea, % Descuento línea y Bfº bruto se actualiza en relación con el nuevo valor del campo **Importe de línea** de la siguiente forma:  

    * Importe dto. línea = Valor línea - Importe línea  
    * % Descuento línea = Importe dto. línea / Valor línea * 100  
    * Bfº bruto = Importe línea - Coste línea  

#### <a name="example-2"></a>Ejemplo
La casilla de verificación **Permite importes sin saldar** no está activada en el contrato de servicio que contiene tres líneas de contrato con esta información.  

|Producto|Coste línea|Valor línea|% Descuento línea|Importe dto. línea|Importe línea|Bfº bruto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Producto 1|20,00|25.00|0.00|0.00|25.00|5.00|  
|Producto 2|50.00|58.00|5.00|2.90|55.10|5.10|  
|Producto 3|100.00|115.00|2.00|2.30|112.70|12.70|  

El valor del campo **Importe anual** es igual que el contenido del campo **Importe anual calculado**, que siempre se establece en la suma de los importes de las líneas. En este caso, es igual a lo siguiente: 25,00 + 55,10 + 112,70 = 192,80.  

 Si cambia el **Importe anual** a 180, se calcularán las contribuciones del porcentaje de las ganancias para cada línea de contrato:  

* Producto 1 – 5 / (5 + 5,1 +1 2,7) = 0,2193 %  
* Producto 2 – 5,1 / (5 + 5,1 + 12,7) = 0,2237  
* Producto 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557  

El valor del campo **Importe línea** se actualiza en cada línea de contrato mediante la siguiente fórmula: Importe línea = Importe línea + diferencia entre los importes anuales nuevos y calculados * Porcentaje de contribución. Después de eso, los valores de los campos **Importe dto. línea**, **% Descuento línea** y **Bfº bruto** se actualizan con las fórmulas del paso 3 del procedimiento descrito anteriormente.  

Finalmente, las líneas del contrato tendrán los siguientes datos:  

|Producto|Coste línea|Valor línea|% Descuento línea|Importe dto. línea|Importe línea|Bfº bruto|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Producto 1|20,00|25.00|11.24|2.81|22.19|2.19|  
|Producto 2|50.00|58.00|9.93|5.76|52.24|2.24|  
|Producto 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also"></a>Consulte también
[Creación de contratos de servicio y ofertas de contrato de servicio](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Configurar la gestión de servicios](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
