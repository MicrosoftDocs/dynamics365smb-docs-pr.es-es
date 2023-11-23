---
title: Movimiento de datos de Copilot entre zonas geográficas
description: Descubra cómo los datos usados en las funciones de Copilot en Dynamics 365 Business Central se mueven a través de geografías donde Azure OpenAI Service no está disponible de forma predeterminada.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: get-started
ms.date: 11/09/2023
ms.custom: bap-template
---

# Movimiento de datos de Copilot entre zonas geográficas 

Copilot está disponible en todas las [regiones geográficas de Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) admitidas. Sin embargo, Copilot utiliza Microsoft Azure OpenAI Service, que actualmente está disponible para Business Central solo en algunas regiones geográficas, actualmente Estados Unidos y Suiza. Esto significa que si su entorno está ubicado en otro lugar, los datos del Copilot y las funciones de IA generativa deben transmitirse fuera de su región geográfica y podrían procesarse y almacenarse fuera de sus límites de cumplimiento. Los datos incluyen las indicaciones de IA y los datos de su negocio que Copilot utiliza o genera. En este caso, debe optar por permitir el movimiento de datos a una instancia de Azure OpenAI Service en otra geografía. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Si su entorno está ubicado en la misma geografía que Azure OpenAI Service, se conecta automáticamente a Azure OpenAI Service, no hay opción. En Europa, Business Central acepta automáticamente el movimiento de datos, pero los administradores pueden optar por no participar en cualquier momento.

> [!NOTE]
> Es posible que las funciones de Copilot individual e IA generativa no estén disponibles en todas las regiones geográficas de Business Central. Consulte con el editor de cada capacidad para comprender la disponibilidad.
> 
> Funciones de Copilot e IA generativa de editores que no son de Microsoft, como las que se originan a partir de personalizaciones o aplicaciones AppSource que instala, cada una define sus propias regiones de Azure OpenAI Service específicas. Consulte con el editor de la extensión para comprender qué servicios regionales de Azure utiliza la extensión. 

### Geografías de Azure OpenAI Serivce

La siguiente tabla muestra la geografía de Azure OpenAI Service utilizada por Copilot, basada en la geografía de un entorno de Business Central. Esta información es importante a la hora de decidir si optar por el movimiento de datos entre geografías. Puede identificar la geografía de su entorno en el centro de administración de Business Central, donde se denomina *región de Azure* (vea [Gestión de entornos en el centro de administración](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Geografía del entorno de Business Central (región de Azure)| Geografía de Azure OpenAI Service|
| - | - |
|Asia (Este, Sudeste) |Estados Unidos|
|Australia (Sureste)| Estados Unidos |
|Brasil (Sur) |Estados Unidos|
|Canadá (Central, Este)|Estados Unidos|
|Europa (Oeste, Norte)| Suiza |
|Francia (Centro, Sur)|Suiza |
|Alemania (Norte, Oeste central)|Suiza |
|India (Centro, Sur)|Estados Unidos|
|Japón (Este, Oeste)|Estados Unidos|
|Corea (Centro, Sur)|Estados Unidos|
|Noruega (Este, Oeste)|Suiza |
|Sudáfrica (Norte, Oeste)|Estados Unidos|
|Suiza (Norte, Oeste) |Suiza|
|Emiratos Árabes Unidos (Norte, Oeste)|Estados Unidos|
|Reino Unido (Sur, Oeste)|Estados Unidos|
|Estados Unidos (centro, este, centro norte, centro sur, oeste) |Estados Unidos|
<!--
| Business Central environment geography | Azure OpenAI Service geography|
| - | - |
|Asia Pacific|United States|
|Australia| United States |
|Brazil |United States|
|Canada|United States|
|Europe| Switzerland |
|France|Switzerland |
|Germany|Switzerland |
|France|Switzerland |
|India|United States|
|Japan|United States|
|Korea|United States|
|Norway|Switzerland |
|Singapore|United States|
|South Africa|United States|
|Switzerland |Switzerland|
|United Arab Emirates|United States|
|United Kingdom|United States|
|United States|United States|-->

> [!NOTE]
> Una vez que un servicio Azure OpenAI Service esté disponible en su geografía de Business Central, su entorno pasará automáticamente a usar Azure OpenAI Service y la suscripción no son obligatorios ni siquiera posibles.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## Pasos siguientes

Usted opta por permitir el movimiento de datos entre geografías desde la página [Copilot y capacidades de IA](https://businesscentral.dynamics.com/?page=7775). Para obtener más información, vaya a [Permitir el movimiento de datos entre geografías](enable-ai.md#allow-data-movement-across-geographies).
