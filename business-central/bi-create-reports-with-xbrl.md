---
title: Cómo crear informes con XBRL
description: XBRL es un lenguaje basado en XML para etiquetar datos financieros que permite a las empresas procesar y compartir sus datos de manera eficiente y precisa.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: edupont
---
# <a name="create-reports-with-xbrl" />Crear informes con XBRL

> [!NOTE]
> Estamos en proceso de eliminar las características para informes XBRL de [!INCLUDE[prod_short](includes/prod_short.md)]. Más información en [Cambios en el primer lanzamiento de versiones de 2022](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL, siglas en inglés de e**X**tensible **B**usiness **R**eporting **L**anguage (Lenguaje ampliado para informes comerciales), es un lenguaje basado en el lenguaje de marcado extensible (XML) para etiquetar datos financieros que permite a las empresas procesar y compartir sus datos de manera eficiente y precisa. La iniciativa XBRL permite los informes financieros mundiales a numerosas empresas de software de planificación de recursos empresariales (ERP) y organizaciones internacionales de contabilidad. El objetivo de la iniciativa es proporcionar una norma para informes uniformes sobre información financiera para bancos, inversores y autoridades. Estos informes comerciales pueden incluir:  

* Informes financieros  
* Información financiera  
* Información no financiera  
* Declaraciones obligatorias, como resultados financieros anuales y trimestrales  

> [!NOTE]
> Puede importar esquemas relacionados con la contabilidad general y crear documentos de instancia XBRL asignando datos de contabilidad general (G/L) del plan de cuentas a elementos de taxonomías que fueron diseñados para informes financieros, como balances, balances de ingresos, etc.
>
> Las capacidades de XBRL en Business Central admiten taxonomías para la especificación 2.1. Sin embargo, las taxonomías pueden contener elementos no admitidos, como bases de enlaces de fórmulas o iXBRL (XBRL en línea), o tener otras diferencias estructurales. Le recomendamos que valide la capacidad XBRL antes de usarla para generar informes.
>
> El soporte completo para taxonomías puede requerir etiquetado y herramientas XBRL de terceros. La organización XBRL International tiene una lista de herramientas y servicios; dependiendo de los requisitos de generación de informes XBRL para una taxonomía determinada, es posible que desee explorar esos recursos. Más información en [Primeros pasos para empresas](https://go.microsoft.com/fwlink/?linkid=2153466) y [Herramientas y servicios](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language" />eXtensible Business Reporting Language (Lenguaje ampliado para informes comerciales)

El sitio Web www.xbrl.org mantiene las taxonomías de XBRL. Para obtener más información y descargar taxonomías visite el sitio Web de XBRL.  

Digamos que alguien quiere información financiera de usted. Proporcionan una taxonomía (un documento XML) que contiene uno o varios esquemas, cada uno con una o varias líneas. Las líneas corresponden a operaciones financieras individuales que requiere el remitente. Importe esta taxonomía y luego rellene los esquemas introduciendo las cuentas que corresponden a cada línea y el cálculo que se desea, como el saldo del periodo o el saldo a la fecha. En algunos casos puede introducir una constante, por ejemplo, el número de empleados. Ahora ya puede enviar el documento de instancia (un documento XML) al solicitante. La idea es que esto puede ser un evento periódico, por lo que si no ha hecho cambios en la taxonomía, sólo tiene que exportar los nuevos documentos de instancia para los nuevos periodos cuando se lo soliciten.

## <a name="xbrl-comprises-the-following-components" />XBRL consta de los siguientes componentes

La **especificación** XBRL explica lo que es XBRL y cómo generar documentos de instancia y taxonomías XBRL. La especificación XBRL explica XBRL en términos técnicos y está pensada para un público técnico.  

El **esquema** XBRL son los componentes del núcleo de nivel inferior de XBRL. El esquema es el archivo XSD físico (también llamado definición de esquema XML) que expresa cómo se generan los documentos de instancia y las taxonomías.

Las **bases de enlaces** XBRL son los archivos XML físicos que contienen información sobre los elementos definidos en el esquema XBRL, como las etiquetas en uno o varios idiomas, cómo se relacionan entre sí, cómo resumen elementos, etc.  

Una **taxonomía** XBRL es un "vocabulario" o "diccionario" creado por un grupo, compatible con la especificación XBRL, que permite el intercambio de información de negocios.  

Un **documento de instancia** XBRL es un informe de negocios, como un extracto financiero preparado para la especificación XBRL. La taxonomía explica el significado de los valores del documento de instancia. De hecho, un documento de instancia es inútil a menos que conozca la taxonomía para la que está preparada.  

## <a name="layered-taxonomies" />Taxonomías por niveles

Una taxonomía puede constar de una taxonomía base, por ejemplo US GAAP (principios de contabilidad generalmente aceptados de los Estados Unidos) o IAS (normas contables internacionales), y luego tener una o más extensiones. Para reflejar esto, una taxonomía hace referencia a uno o varios esquemas, cada uno de los cuales son taxonomías propiamente dichas. Cuando se cargan las taxonomías adicionales en la base de datos, los elementos nuevos simplemente se agregan al final de los elementos existentes.  

## <a name="linkbases" />Base de enlaces

En XBRL (especif. 2), la taxonomía se describe en varios archivos XML. El archivo XML principal es el propio archivo de esquema de la taxonomía (archivo .xsd) que sólo contiene una lista desordenada de elementos u operaciones que se van a comunicar. Además, normalmente hay algunos archivos de base de enlaces (.xml). Los archivos de base de enlaces contienen datos que complementan la taxonomía básica (archivo .xsd). Existen seis tipos de archivos de base de enlaces de los cuales cuatro afectan a [!INCLUDE[prod_short](includes/prod_short.md)]. Son:

* Base de enlaces de etiqueta: Esta base de enlaces contiene etiquetas o nombres de los elementos. El archivo puede contener etiquetas en diferentes idiomas que se identifican con una propiedad XML denominada 'lang'. El identificador de idioma XML contiene, normalmente, una abreviatura de dos letras y, por lo tanto, es fácil saber qué significa la abreviatura, no existe ninguna conexión con el código de idioma de Microsoft Windows ni con los códigos de idioma definidos en los datos de demostración. Por tanto, cuando busque los idiomas de una taxonomía específica, verá todas las etiquetas del primer elemento de la taxonomía, lo que significa que, a continuación, podrá ver un ejemplo de cada idioma. Una taxonomía puede tener varias bases de enlaces de etiquetas adjuntas siempre que esas bases contengan diferentes idiomas.  
* Base de enlaces de presentación: Esta base de enlaces contiene información sobre la estructura de los elementos, o más exactamente, cómo sugiere el emisor de la taxonomía que la aplicación la presente al usuario. La base de enlaces contiene una serie de enlaces que conectan dos elementos como padre e hijo. Al aplicar estos enlaces, los elementos pueden mostrarse de forma jerárquica. Tenga en cuenta que la base de enlaces de presentación sólo se ocupa de: la presentación de elementos al usuario.
* Base de enlaces de cálculo: Esta base de enlaces contiene información sobre cómo se distribuyen los elementos. La estructura es muy parecida a la de la base de enlaces de presentación, excepto que cada enlace o 'arc', como se denominan, tiene una propiedad Weight. La propiedad Weight puede ser 1 o –1, que indica si el elemento debe agregarse o eliminarse de su elemento padre. Tenga en cuenta que las distribuciones no se alinean necesariamente con la presentación visual.  
* Base de enlaces de referencia: Esta base de enlaces es un archivo xml que contiene información adicional acerca de los datos que requiere el emisor de la taxonomía.

## <a name="set-up-xbrl-lines" />Configurar líneas XBRL

Después de importar o actualizar la taxonomía, las líneas de los esquema deben rellenarse con toda la información necesaria para satisfacer los requisitos de informes financieros concretos. Esta información incuye información básica de la empresa, los extractos financieros reales, los informes contables, las notas a los extractos financieros, esquemas de cuentas suplementarios, etc.  

Configure las líneas XBRL asignando los datos de la texto a sus datos contables.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Taxonomías XBRL** y luego elija el enlace relacionado.  
2. En la página **Taxonomías XBRL**, seleccione una taxonomía de la lista.  
3. Seleccione la acción **Líneas**.  
4. Seleccione una línea y rellene los campos.  
5. Para obtener más información acerca de lo que tiene que rellenar, elija la acción **Información**.  
6. Para configurar la asignación de las cuentas contables del plan de cuentas a las líneas XBRL, elija la acción **Lín. contabilidad asignadas**.  
7. Para agregar notas a los extractos financieros, elija la acción **Notas**.  

   > [!TIP]
   > Para excluir líneas de los datos exportados, elija **NO APLICA** como tipo de fuente.

   > [!NOTE]  
   > Solo puede exportar datos que correspondan a la selección en el campo **tipo de fuente**. Esto incluye descripciones y notas.  

   > [!NOTE]  
   > Las taxonomías pueden contener elementos que [!INCLUDE[prod_short](includes/prod_short.md)] no soporta. Si un elemento no es compatible, el campo **Tipo de fuente** mostrará **No aplica** y el campo **Descripción** mostrará un mensaje de error, como **Tipo inesperado: "tipo específico no reconocido"**. Si debe exportar el elemento, elija un tipo de fuente coincidente. Normalmente, se trata de una constante o una descripción. De esta forma, podrá ingresar y exportar datos; sin embargo, dichos elementos pueden tener reglas de validación que no se pueden verificar antes de exportar.

## <a name="import-an-xbrl-taxonomy" />Importar taxonomías XBRL

El primer paso para trabajar con la funcionalidad XBRL es importar una taxonomía en la base de datos de la empresa. Una taxonomía se compone de uno o varios esquemas y algunas bases de enlaces. Una vez haya completado la importación de los esquemas y las bases de enlaces y haya aplicado las bases de enlaces linkbases a los esquemas, puede configurar las líneas y asignar las cuentas contables del pan de cuentas a las líneas apropiadas de la taxonomía.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Taxonomías XBRL** y luego elija el enlace relacionado.  
2. En la página **Taxonomías XBRL**, cree una línea nueva y escriba el nombre y la descripción de la taxonomía.  
3. Elija la acción **Esquemas** y, a continuación, inserte la descripción del esquema.  
4. Para importar el esquema, en la página **Esquemas XBRL** , elija la acción **Importar** y luego realice uno de los siguientes pasos para subir el archivo:

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Para importar la base de vínculos, en la página **Esquemas XBRL**, elija la acción **Bases de vínculos** y luego realice uno de los siguientes pasos para subir el archivo:

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. Ahora puede elegir entre aplicar la base de enlaces al esquema. Repita el proceso hasta que haya importado todas las bases de enlaces.  
7. Seleccione la acción **Aplicar a taxonomía** para aplicar la base de enlaces al esquema.  

> [!IMPORTANT]  
> En vez de aplicar las base de enlaces individualmente justo después de importar, puede esperar hasta que haya importado todas las bases de enlaces y, a continuación, aplicarlas todas simultáneamente. Para hacerlo, seleccione el botón **No** cuando el sistema le pregunte si desea aplicar las bases de enlaces recién importadas al esquema. Seleccione las líneas con las bases de enlaces que desea aplicar.  

## <a name="update-an-xbrl-taxonomy" />Actualizar una taxonomía XBRL

Cuando una taxonomía cambie, también tiene que actualizar la taxonomía actual. La razón para la actualización puede ser un cambio en el esquema, un cambio en la base de enlaces o una nueva base de enlaces. Después de actualizar la taxonomía, sólo tiene que asignar las líneas de las líneas nuevas o modificadas.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Taxonomías XBRL** y luego elija el enlace relacionado.  
2. En la página **Taxonomías XBRL**, seleccione la acción **Esquemas**.  
3. Para actualizar un esquema, seleccione el esquema que desea actualizar y elija la acción **Importar**.  
4. Para actualizar o agregar una base de enlaces nueva, elija la acción **Bases de enlaces**.  
5. Seleccione la base de enlaces correspondiente o seleccione <kbd>Ctrl</kbd>+<kbd>N</kbd> para crear una nueva línea, seleccione el tipo de base de enlaces y, a continuación, inserte una descripción.  
6. Para importar la base de enlaces, elija la acción **Importar**.  
7. Elija **Sí** para aplicar la base de enlaces al esquema.  

## <a name="see-related-training-at-microsoft-learnlearnmodulesxbrl-reports-dynamics--business-centralindex" />Consulte la formación relacionada en [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index)

## <a name="see-also" />Consulte también .

[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
