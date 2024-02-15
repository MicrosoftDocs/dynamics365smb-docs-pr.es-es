---
title: Movimiento de datos de Copilot entre zonas geográficas
description: Descubra cómo los datos usados en las funciones de Copilot en Dynamics 365 Business Central se mueven a través de geografías donde Azure OpenAI Service no está disponible de forma predeterminada.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 11/30/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="copilot-data-movement-across-geographies"></a>Movimiento de datos de Copilot entre zonas geográficas

Copilot está disponible en todos los [países o regiones de Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) admitidos. Sin embargo, Copilot utiliza Microsoft Azure OpenAI Service, que actualmente está disponible para Business Central solo en algunas regiones geográficas. Esto significa que si su entorno está ubicado en otro lugar, los datos del Copilot y las funciones de IA generativa deben transmitirse fuera de su región geográfica y podrían procesarse y almacenarse fuera de sus límites de cumplimiento. Los datos incluyen las indicaciones de IA y los datos de su negocio que Copilot utiliza o genera. En este caso, debe optar por permitir el movimiento de datos a una instancia de Azure OpenAI Service en otra geografía. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Si su entorno está ubicado en la misma región que Azure OpenAI Service, se conecta automáticamente a Azure OpenAI Service, no hay opción y no hace falta ninguna configuración puntual.

> [!NOTE]
> Es posible que las funciones de Copilot individual e IA generativa no estén disponibles en todos los países o regiones del entorno de Business Central. Consulte con el editor de cada capacidad para comprender la disponibilidad.
> 
> Funciones de Copilot e IA generativa de editores que no son de Microsoft, como las que se originan a partir de personalizaciones o aplicaciones AppSource que instala, cada una define sus propias regiones de Azure OpenAI Service específicas. Consulte con el editor de la extensión para comprender qué servicios regionales de Azure utiliza la extensión. 

### <a name="azure-openai-service-geographies"></a>Geografías de Azure OpenAI Serivce

La siguiente tabla muestra la geografía de Azure OpenAI Service utilizada por Copilot, basada en la región de Azure de un entorno de Business Central. Esta información es importante a la hora de decidir si optar por el movimiento de datos entre geografías. Puede identificar la región de Azure de su entorno en el centro de administración de Business Central, donde se denomina región de Azure (vea [Gestión de entornos en el centro de administración](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Región de Azure del entorno| Geografía de Azure OpenAI Service|Se requiere una acción del administrador para desbloquear Copilot| 
| - | - | - |
|Asia (Este, Sudeste) |Estados Unidos|Sí|
|Australia (Sureste)| Estados Unidos |Sí |
|Brasil (Sur) |Estados Unidos|Sí|
|Canadá (Central, Este)|Estados Unidos|Sí|
|Europa (Oeste, Norte)| Suecia o Suiza |Sí|
|Francia (Centro, Sur)| Suecia o Suiza |Sí|
|Alemania (Norte, Oeste central)| Suecia o Suiza |Sí|
|India (Centro, Sur)|Estados Unidos|Sí|
|Japón (Este, Oeste)|Estados Unidos|Sí|
|Corea (Centro, Sur)|Estados Unidos|Sí|
|Noruega (Este, Oeste)|Suecia o Suiza |Sí|
|Sudáfrica (Norte, Oeste)|Estados Unidos|Sí|
|Suiza (Norte, Oeste) |Suecia o Suiza |Sí|
|Emiratos Árabes Unidos (Norte, Oeste)|Estados Unidos|Sí|
|Reino Unido (Sur, Oeste)|Reino Unido|Sí|
|Estados Unidos (centro, este, centro norte, centro sur, oeste) |Estados Unidos|No|

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

## <a name="next-steps"></a>Pasos siguientes

Usted opta por permitir el movimiento de datos entre geografías desde la página [Copilot y capacidades de IA](https://businesscentral.dynamics.com/?page=7775). Para obtener más información, vaya a [Permitir el movimiento de datos entre geografías](enable-ai.md#allow-data-movement-across-geographies).
