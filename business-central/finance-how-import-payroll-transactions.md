---
title: Importar transacciones de nómina
description: 'Para administrar los salarios, se importan y registran transacciones financieras desde el proveedor de nóminas a la contabilidad, mediante una extensión de nóminas como Ceridian.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Ceridian, Quickbooks, salary'
ms.search.form: '1660, 1661, 36601'
ms.date: 06/16/2021
ms.author: edupont
---
# Importación de transacciones de nómina

Para contabilizar los pagos de salario y transacciones relacionadas, deberá importar y registrar las transacciones financieras de salario creadas para el proveedor de nóminas al libro mayor. Para hacer esto, primero importe un archivo que recibirá del proveedor de nóminas en la página **Diario general**. A continuación asigne las cuentas externas del archivo de nóminas a las cuentas correspondientes. Por último, registre operaciones de nóminas según la asignación de cuentas.

> [!NOTE]  
> Para utilizar esta funcionalidad, se debe instalar y habilitar la extensión para importar nóminas. Las extensiones Nómina de Ceridian e Importación del archivo de nómina de QuickBooks están preinstaladas en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] mediante extensiones](ui-extensions.md).

## Para importar un archivo de nómina

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales**, y luego elija el enlace relacionado.
2. En la sección del diario general correspondiente, elija la acción **Importar transacciones de nómina**. Se abre una guía de configuración asistida.
3. Realice los pasos de la página **Importar transacciones de nómina**.

    > [!TIP]  
    >   En el paso de la asignación de los registros de nóminas externos a sus cuentas de contabilidad, las asignaciones que cree se recordarán la próxima vez que importe los mismos registros. Esto le ahorrará tiempo al no tener que rellenar manualmente el campo **Número de cuenta** en el diario general cada vez que haya importado transacciones de nóminas periódicas.   

    Cuando elige el botón **Aceptar** en la guía de configuración asistida, la página **Diario general** incluye las líneas que representan transacciones que contiene el archivo de nóminas y con las cuentas correspondientes rellenadas previamente en los campos **Cuentas G/L** según las asignaciones que ha creado en la guía.
4. Edite o registre las líneas de diario como cualquier otra transacción de contabilidad. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).   

## Consulte también

[Finanzas](finance.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]