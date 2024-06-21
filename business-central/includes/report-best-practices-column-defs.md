---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

## Procedimientos recomendados para trabajar con definiciones de columna

Las definiciones de columnas no tienen versiones. Cuando cambia la definición de una columna, la versión anterior se reemplaza si el cambio se guarda en la base de datos. La siguiente lista contiene algunos procedimientos recomendados para trabajar con definiciones de columna:

- Si agrega una definición de columna, elija un buen código y complete el campo de descripción con un texto significativo mientras aún sabe para qué usa la definición de columna. Esta información ayuda a sus compañeros de trabajo (y a usted mismo en el futuro) a trabajar con el informe financiero y tal vez a cambiar la definición de columna.
- Antes de cambiar la definición de columna, considere la posibilidad de hacer una copia de seguridad del mismo, por si acaso su cambio no funciona como esperaba. Puede limitarse a copiar la definición (dándole un buen nombre) o exportarla. Para obtener más información, vaya a [Importar o exportar definiciones de columna](#import-or-export-financial-report-column-definitions).
- Si necesita una copia nueva de una definición que [!INCLUDE [prod_short](prod_short.md)] proporciona, una manera fácil de obtenerla es crear una nueva empresa que solo contenga datos de configuración. Luego, exporte la definición e impórtela en la empresa donde la definición necesita una actualización.