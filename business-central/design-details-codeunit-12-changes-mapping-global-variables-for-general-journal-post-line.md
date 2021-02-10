---
title: Cambios en la asignación de variables globales para la contabilización en la codeunit 12
description: En versiones anteriores, se cambió la codeunit 12 para ayudar a mejorar el rendimiento en la publicación del diario general. Obtenga información sobre los cambios en las variables globales.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/28/2020
ms.author: edupont
ms.openlocfilehash: 0fc79ba982e17b9295f0f611ca34b4eb615001f3
ms.sourcegitcommit: a95681db16e81af109b34f8e5d88028c1552c6a2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367764"
---
# <a name="historical-changes-to-codeunit-12-mapping-global-variables-for-general-journal-post-line"></a>Cambios históricos en la codeunit 12: Asociación de variables globales para línea de registro en diario general

En las versiones de [!INCLUDE [navnow_md](includes/navnow_md.md)] se han implementado los siguientes cambios.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Comentario**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Invariable|  
|SalesSetup@1010 : Record 311;||Cambiado a local|  
|PurchSetup@1011 : Record 312;||Cambiado a local|  
|AccountingPeriod@1012 : Record 50;||Cambiado a local|  
|GLAcc@1013 : Record 15;||Cambiado a local|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Con nombre nuevo|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Con nombre nuevo|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Invariable|  
|OrigGLEntry@1017 : Record 17;||Eliminado|  
|VATPostingSetup@1019 : Record 325;||Cambiado a local|  
|Cust@1020 : Record 18;||Cambiado a local|  
|Vend@1021 : Record 23;||Cambiado a local|  
|GenJnlLine@1022 : Record 81;||Cambiado a local|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Invariable|  
|CustPostingGr@1030 : Record 92;||Cambiado a local|  
|VendPostingGr@1031 : Record 93;||Cambiado a local|  
|Currency@1032 : Record 4;||Cambiado a local|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Invariable|  
|ApplnCurrency@1034 : Record 4;||Cambiado a local|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Invariable|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Invariable|  
|BankAcc@1039 : Record 270;||Cambiado a local|  
|BankAccLedgEntry@1040 : Record 271;||Cambiado a local|  
|CheckLedgEntry@1041 : Record 272;||Cambiado a local|  
|CheckLedgEntry2@1042 : Record 272;||Cambiado a local|  
|BankAccPostingGr@1043 : Record 277;||Cambiado a local|  
|GenJnlTemplate@1044 : Record 80;||Cambiado a local|  
|TaxJurisdiction@1045 : Record 320;||Cambiado a local|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Invariable|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Cambiado a local|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Invariable|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Invariable|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Invariable|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Invariable|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Desplazado a codeunit 17|  
|CostAccSetup@1092 : Record 1108;||Cambiado a local|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Invariable|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Cambiado a local|  
|FAJnlPostLine@1050 : Codeunit 5632;||Cambiado a local|  
|SalesTaxCalculate@1051 : Codeunit 398;||Cambiado a local|  
|GenJnlApply@1052 : Codeunit 225;||Cambiado a local|  
|DimMgt@1053 : Codeunit 408;||Cambiado a local|  
|JobPostLine@1028 : Codeunit 1001;||Cambiado a local|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Cambiado a local|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Añadido|  
||AddCurrencyCode@1117 : Code[10];|Añadido|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Invariable|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Invariable|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Invariable|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Invariable|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Invariable|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Invariable|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Invariable|  
|SalesTaxBaseAmount@1061 : Decimal;||Cambiado a local|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Invariable|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Invariable|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Invariable|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Invariable|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Invariable|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Invariable|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Invariable|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Invariable|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Invariable|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Invariable|  
|LastLineNo@1070 : Integer;||Eliminado|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Invariable|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Invariable|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Invariable|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Invariable|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Invariable|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Invariable|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Invariable|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Invariable|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Invariable|  
|AllApplied@1081 : Boolean;||Cambiado a local|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Invariable|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Invariable|  
|Prepayment@1037 : Boolean;||Eliminado|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Invariable|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Invariable|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Invariable|  
||GLSetupRead@1015 : Boolean;|Añadido|  
||AmountRoundingPrecision@1012 : Decimal;|Añadido|  
||CrCardTransactionEntryNo@1013 : Integer;|Añadido|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Cambios en la codeunit 12: Cambios en los procedimientos de registro en el diario general](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)
