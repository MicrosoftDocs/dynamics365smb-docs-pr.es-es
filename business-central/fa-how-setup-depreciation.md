---
title: Configurar Amortización A/F
description: 'Existen varios métodos de amortización. En Business Central, usted define el método de amortización de un activo en la página **Tarjeta de activo fijo**.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Configurar la amortización de los activos fijos

Puede utilizar varios métodos de amortización para preparar extractos financieros y devoluciones de impuestos. Muchas grandes empresas utilizan amortizaciones en línea en sus extractos financieros porque les suele permitir obtener ganancias mayores. Sin embargo, en casos de devolución de impuestos, muchas empresas utilizan un método de amortización acelerado, como la amortización regresiva. Usted define el método de depreciación de un activo con el campo **Método de amortización** en la página **Tarjeta de activo fijo**. Para obtener más información sobre lo que hacen los diferentes métodos, vea [Métodos de amortización](fa-depreciation-methods.md).

Puede configurar libros de amortización, en los que usted define las diferentes formas en que se debe calcular la amortización para sus diferentes activos fijos. Cada libro de amortización especifica términos de amortización individuales. Por ejemplo, se puede especificar que un activo debe amortizarse en un periodo de tres años en un libro, y en un periodo de cinco años en otro libro.

Cuando cree los libros de amortización pertinentes, debe asignar uno o más a cada activo. Un libro de amortización que se asigna a un activo se le conoce como un libro de amortización de activo. Puede establecer un número ilimitado de libros de amortización para un activo.  

## Para crear un libro de amortización

En un libro de amortización de activos puede especificar la forma en que se amortizarán los activos. Para aplicar distintos métodos de amortización, puede configurar varios libros de amortización.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros amortización** y luego elija el enlace relacionado.
2. En la página **Lista libros amortización**, elija la acción **Nuevo**.
3. En la página **Ficha libro amortización**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Puede registrar transacciones de activos en las páginas **A/F Diario general** o **Diario activos fijos**, dependiendo de si las transacciones son para la información financiera o la gestión interna. Vaya al siguiente paso para indicar qué tipo de diario se utiliza para las distintas actividades de activo de forma predeterminada.
4. En la ficha desplegable **Integración**, seleccione la casilla de las transacciones de cada actividad de activo que desee registrar en la página **A/F Diario general**.
5. Repita los pasos del 2 al 4 para cada método de amortización o de registro que desee asignar a los activos fijos en un libro de amortización.

> [!IMPORTANT]
> Elija el campo **Utilizar el redondeo en amortización periódica** para redondear los importes de depreciación periódica calculados a números enteros. Por ejemplo, si su empresa también utiliza el redondeo de facturas a números enteros en la págin **Configuración de contabilidad**, redondear también los importes de depreciación a números enteros puede ayudar a proporcionar transparencia.

Por ejemplo, si se deshace de un activo fijo donde el libro de amortización no especifica el redondeo, pero la configuración de contabilidad de la empresa requiere redondeo, entonces, cuando se deshaga del activo fijo, verá un mensaje de error que indica que se debe redondear una cantidad en un movimiento.  

## Para asignar un libro de amortización a un activo fijo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo fijo para el que desee configurar un libro de amortización de activos fijos.
3. En la ficha desplegable **Ficha libros amortización**, rellene los campos según sea necesario.
4. Si necesita asignar más de un libro de amortización al activo, elija la acción **Añadir más libros amortización**.
5. Opcionalmente, elija la acción **Libros amortización** para especificar uno o más libros de amortización de activos.

    > [!NOTE]  
    >   Cuando utilice el método de amortización manual, debe introducir la amortización de forma manual en el diario general de activos. La función **Calcular amortización** ignora los activos que utilizan el método de amortización manual. Puede utilizar este método para activos no sujetos a amortización como, por ejemplo, los terrenos.

    > [!NOTE]  
    > Cuando utiliza el método de amortización definido por el usuario, debe asignar el libro de amortización de una manera diferente. Para más información, vea [Configurar el método de amortización definido por el usuario](fa-how-setup-user-defined-depreciation-method.md).

## Para asignar un libro de amortización a varios activos con un solo proceso

Si desea asignar un libro de amortización a varios activos fijos, puede utilizar el proceso **A/F Crear libros amortización** para crear los libros necesarios de activos fijos.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo al que desea asignarle un libro de amortización y, a continuación, elija la acción **Editar**.
3. En la página **Ficha libro amortización**, elija la acción **A/F Crear libros amortización**.
4. En la página **A/F Crear libros amortización**, rellene el campo **Libro amortización**.
5. Elija el campo **A/F Copiar desde nº** y, a continuación, seleccione el número de activo que desee utilizar como base para crear nuevos libros de amortización de activos fijos.

    Si rellena este campo, los campos de amortización de los nuevos libros de amortización de activos fijos contendrán la misma información que los campos correspondientes del libro desde el que va a copiarlos. Deje este campo en blanco si desea crear libros de amortización de activos fijos con los campos de amortización vacíos.  
6. En la ficha desplegable **Activo**, puede establecer un filtro para seleccionar los activos para los que desee crear los libros de amortización de activos.
7. Elija el botón **Aceptar**.

## Para configurar los tipos de registro de amortización

Para cada libro de amortización, debe configurar el modo en que desea que [!INCLUDE[prod_short](includes/prod_short.md)] administre los distintos tipos de registro. Por ejemplo, si el registro debe ser débito o abono, y si el tipo de registro se debe incluir en la base de amortización.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros amortización** y luego elija el enlace relacionado.  
2. Seleccione el libro de amortización que desea configurar y, a continuación, elija la acción **A/F Config. tipo registro**.
3. En la página **A/F Config. tipo registro**, rellene los campos según sea necesario.

    > [!NOTE]  
    >   En la página **Config. tipos registro A/F** no puede insertar ni borrar líneas. Sólo puede modificar las líneas existentes.

Se recomienda que no cambie la configuración de los libros de amortización de los movimientos que ya se han registrado. Los cambios no afectarán a los movimientos ya registrados, lo que provocaría estadísticas del libro de amortización erróneas.

## Para configurar las plantillas y los procesos predeterminados para la amortización de activos

Puede definir para cada libro de amortización una configuración predeterminada para libros y secciones. Estos valores predeterminados se usan para duplicar líneas de un diario a otro, crear líneas de diario con los procesos **Calcular amortización** o **Ajustar valores activos fijos** o duplicar los costes de adquisición en el diario de seguros.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros amortización** y luego elija el enlace relacionado.  
2. Seleccione el libro de amortización en el que desea definir los diarios predeterminados y, a continuación, elija la acción **Configuración del diario A/F**.  
3. Si desea tener una configuración predeterminada para cada usuario, elija el campo **Id. usuario** y selecciónela desde la página **Usuarios**.  
4. En el resto de campos, seleccione la sección o plantilla del diario que debe usarse de forma predeterminada.  

## Amortización de campo Ejercicio 365 días

Cuando el proceso Calcular amortización calcula las amortizaciones, el proceso normalmente utiliza un año estándar de 360 días en el que cada uno de los 12 meses tiene 30 días.

Si selecciona este campo, el proceso Calcular amortización utiliza un calendario de 365 en el que cada mes se calcula con el mismo número de días que en el calendario. La única excepción es el febrero en años bisiestos, que el proceso trata como que tiene 28 días en lugar de 29. Por eso, todos los años, incluso los bisiestos, consta que tienen 365 días.

## Consulte también .

[Configuración de activos fijos](fa-setup.md)  
[Activos fijos](fa-manage.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
