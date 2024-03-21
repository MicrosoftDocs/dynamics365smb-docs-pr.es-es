---
title: Exportar los datos de Business Central a Excel
description: 'Puede exportar los informes financieros y los datos de inteligencia empresarial desde Business Central a Excel, o abrir los datos en Excel.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, reporting, financial report, business intelligence, BI, Excel'
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="export-your-business-data-to-excel"></a>Exportar sus datos empresariales a Excel

Excel es una potente herramienta para trabajar con datos. Puede abrir cualquier lista en Excel desde [!INCLUDE[prod_short](includes/prod_short.md)]. Incluso puede modificar los datos en Excel y después volver a enviarlos a [!INCLUDE [prod_short](includes/prod_short.md)]. La misma capacidad le facilita llevar sus datos con usted si decide cancelar su suscripción.

## <a name="opening-lists-in-excel"></a>Abrir listas en Excel

Puede abrir los datos en Excel desde cualquier diario, lista u hoja de trabajo. Abra solo la página que desee y, a continuación, elija **Abrir en Excel**. Por ejemplo, abra la lista de clientes (busque **Clientes**) y elija **Abrir en Excel**. El explorador le indicaŕa que abra o guardar el libro de Excel generado.  

> [!NOTE]
> Use esta opción cuando no desee realizar cambios y publicar esos cambios de nuevo en [!INCLUDE[prod_short](includes/prod_short.md)].  

Cada lista incluye algunas columnas. La exportación a Excel incluye las columnas que se encuentran en su vista actual. Cambie las columnas abriendo el menú contextual para cualquier columna y luego especificando qué columnas desea ver. La lista de columnas es diferente para la mayoría de las listas. Las columnas reflejan la estructura de la base de datos que almacena sus datos. Si no está seguro de qué tipo de datos contiene una determinada columna, agréguela a su vista. Siempre puede volver a eliminarla.  

### <a name="edit-data-in-excel"></a>Editar datos en Excel

Su experiencia de [!INCLUDE[prod_short](includes/prod_short.md)] incluye un complemento para Excel para que pueda editar datos en Excel. Para obtener más información, consulte [Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Exportar datos a otros sistemas financieros

Si decida cancelar la suscripción de [!INCLUDE[prod_short](includes/prod_short.md)], puede exportar los datos a Excel y llevárselos a su próximo sistema financiero.  

Puede exportar todas las páginas, pero puede que sea más de lo que necesita realmente. Por lo tanto, considere la posibilidad de exportar las páginas esenciales siguientes y recuerde agregar todas las columnas como se ha descrito anteriormente:  

* Plan de cuentas  
* Clientes  
* Proveedores  
* Bancos  
* Artículos  

Si también desea todas las transacciones financieras, es una gran cantidad de datos, por lo que la exportación suele tardar varios minutos. Las transacciones financieras se muestran en la página **Movs. contabilidad**.  

Le recomendamos que también considere la posibilidad de exportar los datos de las páginas siguientes:  

* Movs. clientes  
* Movs. proveedores  
* Movs. bancos  
* Movs. productos  
* Configuración grupos contables  
* Grupos contables clientes  
* Grupos contables proveedores  
* Grupos contables producto  
* Grupo contable banco  
* Presupuestos contables  
* Movs. pptos. contabilidad  
* Ofertas venta  
* Facturas venta  
* Facturas compra  
* Contactos  
* Vendedores  

> [!NOTE]  
> Si ha configurado varias empresas en [!INCLUDE[prod_short](includes/prod_short.md)], debe exportar los datos correspondientes de cada empresa.

> [!NOTE]
> Debe tener al menos uno de los siguientes permisos para abrir o editar datos en Excel:
>
> * Conjunto de permisos *Acción de exportación de Excel D365*  
> * Permiso del sistema 6110 *Permitir que la acción se exporte a Excel*.  

Para obtener más información, consulte [Para obtener un resumen de los permisos de un usuario](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-also"></a>Consulte también
[Cancelar la suscripción de [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Finanzas](finance.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
