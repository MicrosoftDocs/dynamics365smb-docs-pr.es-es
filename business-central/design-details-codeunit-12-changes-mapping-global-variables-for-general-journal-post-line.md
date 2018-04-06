---
title: "Detalles de diseño: Cambios en unidad de código 12 en la asociación de variables globales para línea de registro en diario general | Documentos de Microsoft"
description: "En esta versión de Business Central se han implementado los siguientes cambios."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: aae8b02b95d3e385030610533f4b1b7f04602d5e
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Cambios en unidad de código 12 cambios: asociación de variables globales para línea de registro en diario general
En esta versión de [!INCLUDE[d365fin](includes/d365fin_md.md)] se han implementado los siguientes cambios.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Comentario**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Registro 98;|GLSetup@1009 : Registro 98;|Invariable|  
|SalesSetup@1010 : Registro 311;||Cambiado a local|  
|PurchSetup@1011 : Registro 312;||Cambiado a local|  
|AccountingPeriod@1012 : Registro 50;||Cambiado a local|  
|GLAcc@1013 : Registro 15;||Cambiado a local|  
|GLEntry@1014 : Registro 17;|GlobalGLEntry@1014 : Registro 17;|Con nombre nuevo|  
|GLEntryTmp@1015: Registro TEMPORAL 17;|TempGLEntryBuf@1010: Registro TEMPORAL 17;|Con nombre nuevo|  
|TempGLEntryVAT@1016: Registro TEMPORAL 17;|TempGLEntryVAT@1016: Registro TEMPORAL 17;|Invariable|  
|OrigGLEntry@1017 : Registro 17;||Eliminado|  
|VATPostingSetup@1019 : Registro 325;||Cambiado a local|  
|Cust@1020 : Registro 18;||Cambiado a local|  
|Vend@1021 : Registro 23;||Cambiado a local|  
|GenJnlLine@1022 : Registro 81;||Cambiado a local|  
|GLReg@1029 : Registro 45;|GLReg@1029 : Registro 45;|Invariable|  
|CustPostingGr@1030 : Registro 92;||Cambiado a local|  
|VendPostingGr@1031 : Registro 93;||Cambiado a local|  
|Currency@1032 : Registro 4;||Cambiado a local|  
|AddCurrency@1033 : Registro 4;|AddCurrency@1033 : Registro 4;|Invariable|  
|ApplnCurrency@1034 : Registro 4;||Cambiado a local|  
|CurrExchRate@1035 : Registro 330;|CurrExchRate@1035 : Registro 330;|Invariable|  
|VATEntry@1038 : Registro 254;|VATEntry@1038 : Registro 254;|Invariable|  
|BankAcc@1039 : Registro 270;||Cambiado a local|  
|BankAccLedgEntry@1040 : Registro 271;||Cambiado a local|  
|CheckLedgEntry@1041 : Registro 272;||Cambiado a local|  
|CheckLedgEntry2@1042 : Registro 272;||Cambiado a local|  
|BankAccPostingGr@1043 : Registro 277;||Cambiado a local|  
|GenJnlTemplate@1044 : Registro 80;||Cambiado a local|  
|TaxJurisdiction@1045 : Registro 320;||Cambiado a local|  
|TaxDetail@1046 : Registro 322;|TaxDetail@1046 : Registro 322;|Invariable|  
|FAGLPostBuf@1047: Registro TEMPORAL 5637;||Cambiado a local|  
|UnrealizedCustLedgEntry@1084 : Registro 21;|UnrealizedCustLedgEntry@1084 : Registro 21;|Invariable|  
|UnrealizedVendLedgEntry@1085 : Registro 25;|UnrealizedVendLedgEntry@1085 : Registro 25;|Invariable|  
|GLEntryVATEntryLink@1087 : Registro 253;|GLEntryVATEntryLink@1087 : Registro 253;|Invariable|  
|TempVATEntry@1088: Registro TEMPORAL 254;|TempVATEntry@1088: Registro TEMPORAL 254;|Invariable|  
|ReversedGLEntryTemp@1089: Registro TEMPORAL 17;||Desplazado a unidad de código 17|  
|CostAccSetup@1092 : Registro 1108;||Cambiado a local|  
|GenJnlCheckLine@1048: Unidad de código 11;|GenJnlCheckLine@1001: Unidad de código 11;|Invariable|  
|ExchAccGLJnlLine@1049: Unidad de código 366;||Cambiado a local|  
|FAJnlPostLine@1050: Unidad de código 5632;||Cambiado a local|  
|SalesTaxCalculate@1051: Unidad de código 398;||Cambiado a local|  
|GenJnlApply@1052: Unidad de código 225;||Cambiado a local|  
|DimMgt@1053: Unidad de código 408;||Cambiado a local|  
|JobPostLine@1028: Unidad de código 1001;||Cambiado a local|  
|TransferGlEntriesToCA@1091: Unidad de código 1105;||Cambiado a local|  
||PaymentToleranceMgt@1002: Unidad de código 426;|Añadido|  
||AddCurrencyCode@1117 : Código[10];|Añadido|  
|FiscalYearStartDate@1054: Fecha;|FiscalYearStartDate@1011: Fecha;|Invariable|  
|NextEntryNo@1055: Entero;|NextEntryNo@1022: Entero;|Invariable|  
|BalanceCheckAmount@1056: Decimal;|BalanceCheckAmount@1056: Decimal;|Invariable|  
|BalanceCheckAmount2@1057: Decimal;|BalanceCheckAmount2@1057: Decimal;|Invariable|  
|BalanceCheckAddCurrAmount@1058: Decimal;|BalanceCheckAddCurrAmount@1058: Decimal;|Invariable|  
|BalanceCheckAddCurrAmount2@1059: Decimal;|BalanceCheckAddCurrAmount2@1059: Decimal;|Invariable|  
|CurrentBalance@1060: Decimal;|CurrentBalance@1060: Decimal;|Invariable|  
|SalesTaxBaseAmount@1061: Decimal;||Cambiado a local|  
|TotalAddCurrAmount@1062: Decimal;|TotalAddCurrAmount@1062: Decimal;|Invariable|  
|TotalAmount@1063: Decimal;|TotalAmount@1063: Decimal;|Invariable|  
|UnrealizedRemainingAmountCust@1086: Decimal;|UnrealizedRemainingAmountCust@1086: Decimal;|Invariable|  
|UnrealizedRemainingAmountVend@1074: Decimal;|UnrealizedRemainingAmountVend@1074: Decimal;|Invariable|  
|NextVATEntryNo@1064: Entero;|NextVATEntryNo@1064: Entero;|Invariable|  
|FirstNewVATEntryNo@1065: Entero;|FirstNewVATEntryNo@1065: Entero;|Invariable|  
|NextTransactionNo@1066: Entero;|NextTransactionNo@1066: Entero;|Invariable|  
|NextConnectionNo@1067: Entero;|NextConnectionNo@1067: Entero;|Invariable|  
|InsertedTempGLEntryVAT@1068: Entero;|InsertedTempGLEntryVAT@1027: Entero;|Invariable|  
|LastDocNo@1069 : Código[20];|LastDocNo@1023 : Código[20];|Invariable|  
|LastLineNo@1070: Entero;||Eliminado|  
|LastDate@1071: Fecha;|LastDate@1021: Fecha;|Invariable|  
|LastDocType@1072: " ,Pago,Factura,Nota de crédito,Documento de interés,Recordatorio,Reembolso"|LastDocType@1025: " ,Pago,Factura,Nota de crédito,Documento de interés,Recordatorio,Reembolso"|Invariable|  
|NextCheckEntryNo@1073: Entero;|NextCheckEntryNo@1028: Entero;|Invariable|  
|AddCurrGLEntryVATAmt@1075: Decimal;|AddCurrGLEntryVATAmt@1017: Decimal;|Invariable|  
|CurrencyDate@1076: Fecha;|CurrencyDate@1020: Fecha;|Invariable|  
|CurrencyFactor@1077: Decimal;|CurrencyFactor@1019: Decimal;|Invariable|  
|UseCurrFactorOnly@1078: Booleano;|UseCurrFactorOnly@1078: Booleano;|Invariable|  
|NonAddCurrCodeOccured@1079: Booleano;|NonAddCurrCodeOccured@1079: Booleano;|Invariable|  
|FADimAlreadyChecked@1080: Booleano;|FADimAlreadyChecked@1080: Booleano;|Invariable|  
|AllApplied@1081: Booleano;||Cambiado a local|  
|OverrideDimErr@1018: Booleano;|OverrideDimErr@1018: Booleano;|Invariable|  
|JobLine@1036: Booleano;|JobLine@1036: Booleano;|Invariable|  
|Prepayment@1037: Booleano;||Eliminado|  
|CheckUnrealizedCust@1082: Booleano;|CheckUnrealizedCust@1082: Booleano;|Invariable|  
|CheckUnrealizedVend@1083: Booleano;|CheckUnrealizedVend@1083: Booleano;|Invariable|  
|GLEntryNo@1090: Entero;|GLEntryNo@1026: Entero;|Invariable|  
||GLSetupRead@1015: Booleano;|Añadido|  
||AmountRoundingPrecision@1012: Decimal;|Añadido|  
||CrCardTransactionEntryNo@1013: Entero;|Añadido|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Cambios en la unidad de código 12: Cambios en los procedimientos de registro en el diario general](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

