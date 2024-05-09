---
title: Informe de prácticas de pago
description: Aprenda cómo crear fácilmente el informe de prácticas de pago para proveedores y clientes.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
--- 

# Informe de prácticas de pago  

Algunos países/regiones exigen que las empresas informen de los plazos de pago de sus proveedores según lo definido por las autoridades locales. Estos informes pueden basarse en diferentes orígenes y pueden clasificar a los proveedores según su tamaño o condiciones de pago definidas, proporcionando informes para los proveedores para lo siguiente según lo requieran las autoridades locales:  

- El promedio de periodo de pago acordado.  
- El plazo medio de pago real.   
- La proporción de facturas pagadas después del final del período de pago acordado. 

Los usuarios pueden seleccionar el período para el cual desean ejecutar un cálculo y buscar detalles según la agrupación que elijan. Para cada una de estas agrupaciones, puede encontrar entradas con orígenes. 

> [!NOTE]
> Hasta ahora, estos informes son obligatorios en algunos países o regiones, pero se trata de una característica global y se puede utilizar en todas partes. Actualmente, las empresas suecas con 250 o más empleados deben informar cada año a la Oficina de Registro de Empresas de Suecia qué plazos de pago tienen para las compras a empresas más pequeñas que ellas. Existen leyes similares en el Reino Unido, Australia y Nueva Zelanda.  

## Genere el informe 

Para ejecutar el informe de **Prácticas de pago**, siga los siguientes pasos:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Prácticas de pago** y luego seleccione el vínculo relacionado. 
2. Seleccione **Nuevo**.
3. En la ficha desplegable **General**, introduzca valores en los siguientes campos:

   | Campo | Descripción |
   |---------|-----------------------------------|
   | N.º | Especifique el número de la entrada o registro del informe. |
   | Tipo de agregación | Especifique cómo se agregan los datos. Si elige la opción **Período** el informe se basará en diferentes períodos, pero si elige la opción **Tamaño de la empresa**, el informe se crea en función del tamaño de la empresa configurado en el campo **Código de tamaño de la empresa** en la tarjeta **Proveedor**. |
   | Tipo de cabecera | Especifica el origen de las entradas en la práctica de pago y puede elegir Proveedores, Clientes o ambos. |
   | Fecha inicial | Especifica la fecha de inicio de la práctica de pago. |
   | Fecha final | Especifica la fecha final de la práctica de pago. |

> [!NOTE]
> Si decide utilizar la opción **Tamaño de empresa** , primero debe crear entradas en la página **Tamaños de empresa** y agréguelos a todos los proveedores que desee rastrear mediante este método.

4. Una vez que complete todos los campos en el encabezado, deberá ejecutar la acción **Generar** para generar datos en las líneas y estadísticas para el tipo de informe seleccionado.
5. Según el **Tipo de agregación** obtendrá diferentes líneas. Puede cambiar algunos valores manualmente, pero en este caso cada línea modificada y todo el informe se marcarán como **Modificado manualmente**.
6. Desde todos los campos calculados, puede profundizar para ver cómo se ha calculado este resultado, abriendo la página **Lista de datos de prácticas de pago**.
7. Si desea imprimir el documento, puede hacerlo ejecutando la acción **Imprimir**.

## Consulte también

[Informes financieros](finance-reports.md)  
[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Informes y análisis de cobros](receivables-reports.md)  
[Informes y análisis de pagos](payables-reports.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Finanzas](finance.md)  
[Información general de la funcionalidad local](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
