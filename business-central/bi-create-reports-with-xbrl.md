---
title: "Cómo crear informes con XBRL | Documentos de Microsoft"
description: "XBRL, siglas en inglés de eXtensible Business Reporting Language (Lenguaje ampliado para informes comerciales), es un lenguaje basado en XML para etiquetar datos financieros que permite a las empresas procesar y compartir sus datos de manera eficiente y precisa."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 2b17ad5dabed505b358b8c2be6414b17228724b8
ms.contentlocale: es-es
ms.lasthandoff: 11/29/2018

---
# <a name="create-reports-with-xbrl"></a>Crear informes con XBRL
XBRL, siglas en inglés de eXtensible Business Reporting Language (Lenguaje ampliado para informes comerciales), es un lenguaje basado en XML para etiquetar datos financieros que permite a las empresas procesar y compartir sus datos de manera eficiente y precisa. La iniciativa XBRL permite los informes financieros mundiales a numerosas empresas de software ERP y organizaciones internacionales de contabilidad. El objetivo de la iniciativa es proporcionar una norma para informes uniformes sobre información financiera para bancos, inversores y autoridades. Estos informes comerciales pueden incluir:  

 • Resultados financieros  
 • Información financiera  
 • Información no financiera  
 • Declaraciones obligatorias, como resultados financieros anuales y trimestrales  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] permite a las empresas implementar datos en XBRL y aprovechar la flexibilidad y automatización que proporciona tanto para recopilar como para compartir datos.  

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language (Lenguaje ampliado para informes comerciales)
XBRL (e **X**tensible **B**usiness **R**eporting **L**anguage, Lenguaje ampliado para informes comerciales) es un lenguaje basado en XML para información financiera. XBRL proporciona un estándar de información uniforme para todos los usuarios de la cadena de suministro de información financiera; como empresas públicas y privadas, profesionales contables, auditores, analistas, inversores, mercados de capital y entidades de crédito, y otros como desarrolladores de software e intermediarios de datos.  

El sitio Web www.xbrl.org mantiene las taxonomías. Para obtener más información o descargar taxonomías visite el sitio Web de XBRL.  

Si alguien desea su información financiera, le proporcionará una taxonomía (un documento XML) que contiene uno o varios esquemas, cada uno con una o varias líneas. Las líneas corresponden a operaciones financieras individuales que requiere el remitente. Importe esta taxonomía en el sistema y rellene los esquemas introduciendo las cuentas que corresponden a cada línea, el tipo de periodo, por ejemplo, el saldo del periodo o el saldo a la fecha. En algunos casos puede introducir una constante, por ejemplo, el número de empleados. Ahora ya puede enviar el documento de instancia (un documento XML) a quien le ha solicitado la información. La idea es que esto puede ser un evento periódico, por lo que si no ha hecho cambios en la taxonomía, sólo tiene que exportar los nuevos documentos de instancia para los nuevos periodos cuando se lo soliciten.  

## <a name="xbrl-is-comprised-of-the-following-components"></a>XBRL consta de los siguientes componentes:  
La **especificación** XBRL explica lo que es XBRL, cómo generar documentos de instancia XBRL y taxonomías XBRL. La especificación XBRL explica XBRL en términos técnicos y está pensada para un público técnico.  

El **esquema** XBRL son los componentes del núcleo de nivel inferior de XBRL. El esquema es el archivo XSD físico que expresa cómo se generan los documentos de instancia y las taxonomías.  

Las **bases de enlaces** XBRL son los archivos XML físicos que contiene diversa información sobre los elementos definidos en el esquema XBRL, como las etiquetas en uno o varios idiomas, cómo se relacionan entre sí, cómo resumen elementos, etc...  

Una **taxonomía** XBRL es un "vocabulario" o "diccionario" creado por un grupo, compatible con la especificación XBRL, para intercambiar información de negocios.  

Un **documento de instancia** XBRL es un informe de negocios, como un extracto financiero preparado para la especificación XBRL. La taxonomía explica el significado de los valores del documento de instancia. Un documento de instancia es inútil a menos que conozca la taxonomía para la que está preparada.  

## <a name="layered-taxonomies"></a>Taxonomías por niveles  
Una taxonomía puede componerse de una taxonomía base, por ejemplo, us-gaap o IAS y, a continuación, tener una o varias extensiones. Para reflejar esto, una taxonomía hace referencia a uno o varios esquemas que son taxonomías separadas. Cuando se cargan las taxonomías adicionales en la base de datos, los elementos nuevos simplemente se agregan al final de los elementos existentes.  

## <a name="linkbases"></a>Base de enlaces  
 En XBRL (especif. 2), la taxonomía se describe en varios archivos XML. El archivo XML principal es el propio archivo de esquema de la taxonomía (archivo .xsd) que sólo contiene una lista desordenada de elementos u operaciones que se van a comunicar. Además, normalmente hay algunos archivos de base de enlaces (.xml) asociados. Los archivos de base de enlaces contienen datos que complementan la taxonomía básica (archivo .xsd). Existen seis tipos de archivos de base de enlaces de los cuales cuatro afectan a Nombre producto XBRL. Son:  

-   Base de enlaces de etiqueta: Esta base de enlaces contiene etiquetas o nombres de los elementos. El archivo puede contener etiquetas en diferentes idiomas que se identifican con una propiedad XML denominada 'lang'. El identificador de idioma XML contiene, normalmente, una abreviatura de dos letras y, por lo tanto, es fácil saber qué significa la abreviatura, no existe ninguna conexión con el código de idioma de Windows ni con los códigos de idioma definidos en los datos de demostración. Cuando el usuario busque los idiomas de una taxonomía específica, verá todas las etiquetas del primer elemento de la taxonomía, lo que significa que, a continuación, podrá ver un ejemplo de cada idioma. Una taxonomía puede tener varias bases de enlaces de etiquetas adjuntas siempre que estas bases contengan diferentes idiomas.  

-   Base de enlaces de presentación: Esta base de enlaces contiene información sobre la estructura de los elementos, o más exactamente, cómo sugiere el emisor de la taxonomía que el sistema la presente al usuario. La base de enlaces contiene una serie de enlaces que conectan dos elementos como padre e hijo. Al aplicar estos enlaces, los elementos pueden mostrarse de forma jerárquica. Tenga en cuenta que la base de enlaces de presentación sólo se ocupa de: la presentación de elementos al usuario.  

-   Base de enlaces de cálculo: Esta base de enlaces contiene información sobre los elementos que se distribuyen a otros elementos. La estructura es muy parecida a la de la base de enlaces de presentación, excepto que cada enlace o 'arc', como se denominan, tiene una propiedad Weight. La propiedad Weight puede ser 1 o –1, que indica si el elemento debe agregarse o eliminarse de su elemento padre. Tenga en cuenta que las distribuciones no tienen que mantenerse necesariamente con la presentación visual.  

-   Base de enlaces de referencia: Esta base de enlaces es un archivo xml que contiene información adicional acerca de los datos que requiere el emisor de la taxonomía.

## <a name="to-set-up-xbrl-lines"></a>Para configurar líneas XBRL  
Después de importar o actualizar la taxonomía, las líneas de los esquema deben rellenarse con toda la información necesaria. Esta información incluirá información básica de la empresa, extractos financieros reales, notas a los extractos financieros, esquemas adicionales y otra información necesaria para satisfacer los requisitos de información financiera particular.  

Configure las líneas XBRL asignando los datos de la texto a sus datos contables.  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Taxonomías XBRL** y luego elija el enlace relacionado.  
2.  En la página **Taxonomías XBRL**, seleccione una taxonomía de la lista.  
3.  Seleccione la acción **Líneas**.  
4.  Seleccione una línea y rellene los campos.   
5.  Para obtener más información acerca de lo que tiene que rellenar, elija la acción **Información**.  
6.  Para configurar la asignación de las cuentas contables del plan de cuentas a las líneas XBRL, elija la acción **Lín. contabilidad asignadas**.  
7.  Para agregar notas a los extractos financieros, elija la acción **Notas**.  

> [!NOTE]  
>  Sólo puede exportar datos que coincidan con el tipo de datos que ha seleccionado en el campo **Tipo procedencia mov.**, incluidas la descripción y las notas.  

> [!NOTE]  
>  Las líneas sin importancia pueden marcarse como tipo de línea **NO APLICABLE** para que las líneas no se exporten.

 ## <a name="to-import-an-xbrl-taxonomy"></a>Para importar taxonomías XBRL  
El primer paso para trabajar con la funcionalidad XBRL es importar la taxonomía en la base de datos de la empresa. Una taxonomía se compone de uno o varios esquemas y algunas bases de enlaces. Una vez haya completado la importación de los esquemas y las bases de enlaces y haya aplicado las bases de enlaces linkbases a los esquemas, puede configurar las líneas y asignar las cuentas contables del pan de cuentas a las líneas apropiadas de la taxonomía.  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Taxonomías XBRL** y luego elija el enlace relacionado.  
2.  En la página **Taxonomías XBRL**, cree una línea nueva y escriba el nombre y la descripción de la taxonomía.  
3.  Elija la acción **Esquemas** y, a continuación, inserte la descripción del esquema.  
4.  Para importar el esquema, en la página **Esquemas XBRL**, elija la acción **Importar** y seleccione una carpeta y un archivo XSD. Elija el botón **Abrir**.  
5.  Para importar la base de enlaces, en la página **Esquemas XBRL**, elija la acción **Base de enlaces** y seleccione una carpeta y un archivo XML. Elija el botón **Abrir**.  
6.  Ahora puede elegir entre aplicar la base de enlaces al esquema. Repita el proceso hasta que haya importado todas las bases de enlaces.  
7. Seleccione la acción **Aplicar a taxonomía** para aplicar la base de enlaces al esquema.  

> [!IMPORTANT]  
>  En vez de aplicar las base de enlaces individualmente justo después de importar, puede esperar hasta que haya importado todas las bases de enlaces y, a continuación, aplicarlas todas simultáneamente. Para hacerlo, seleccione **No** cuando el sistema le pregunte si desea aplicar las bases de enlaces recién importadas al esquema. Seleccione las líneas con las bases de enlaces que desea aplicar.  

## <a name="to-update-an-xbrl-taxonomy"></a>Para actualizar una taxonomía XBRL  
Cuando una taxonomía cambie, también tiene que actualizar la taxonomía actual. La razón para la actualización puede ser un cambio en el esquema, un cambio en la base de enlaces o una nueva base de enlaces. Después de actualizar la taxonomía, sólo tiene que asignar las líneas de las líneas nuevas o modificadas.  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Taxonomías XBRL** y luego elija el enlace relacionado.  
2.  En la página **Taxonomías XBRL**, seleccione la acción **Esquemas**.  
3.  Para actualizar un esquema, seleccione el esquema que desea actualizar y elija la acción **Importar**.  
4.  Para actualizar o agregar una base de enlaces nueva, elija la acción **Bases de enlaces**.  
5.  Seleccione la base de enlaces correspondiente o pulse Ctrl+N para crear una nueva línea, seleccione el tipo de base de enlaces y, a continuación, inserte una descripción.  
6.  Para importar la base de enlaces, elija la acción **Importar**.  
7.  Elija el botón **Sí** para aplicar la base de enlaces al esquema.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)    
[Inteligencia empresarial](bi.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

