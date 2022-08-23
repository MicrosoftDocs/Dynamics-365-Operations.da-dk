---
title: Liste over ER-funktioner i kategorien forretningsdomænespecifik
description: Denne artikel indeholder oplysninger om de forretningsdomænespecifikke funktioner, der understøttes i elektronisk rapportering (ER).
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b1ac46cf10d57b40af1fa99021156ad97a17ba20
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272676"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Liste over ER-funktioner i kategorien forretningsdomænespecifik

[!include [banner](../includes/banner.md)]

De domænespecifikke til elektronisk rapportering (ER) kan bruges til at udføre beregninger og dataadgangsanmodninger, der er specifikke for implementeringen af Microsoft Dynamics 365 Finance. Denne artikel indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion| Beskrivelse |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer en kreditorreference som et MOD10-udtryk, der er baseret på cifrene i det angivne fakturanummer. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer et enkelt økonomisk dimensions-ID, der er hentet fra den angivne streng. Den angivne streng præsenterer alle dimensioner som en kommasepareret liste over ID'er. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Denne funktion returnerer en *Reel* værdi, som repræsenterer resultatet af konverteringen af det angivne pengebeløb fra den angivne kildevaluta til den angivne målvaluta ved hjælp af indstillingerne for det angivne firma på den angivne dato. |
| [CurCredRef](er-functions-other-curcredref.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer en kreditorreference, der er baseret på cifrene i det angivne fakturanummer. |
| [FA_Balance](er-functions-other-fabalance.md) | Denne funktion returnerer en *Container (post)*-værdi, der består af data for anlægsaktivsaldoen for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og rapporteringsdato. |
| [FA_Sum](er-functions-other-fasum.md) | Denne funktion returnerer en *Container (post)*-værdi, der består af data for anlægsaktivbeløbene for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og datoperioder. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på. |
| [ISOCredRef](er-functions-other-isocredref.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer en ISO-kreditorreference, der er baseret på cifrene og bogstaverne i det angivne fakturanummer. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Denne funktion returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne streng repræsenterer et gyldigt internationalt bankkontonummer (IBAN). Ellers returneres en *Boolesk* værdi på **FALSK**. |
| [Mod_97](er-functions-other-mod97.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer en kreditorreference som et MOD97-udtryk, der er baseret på cifrene i det angivne fakturanummer. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer den nye genererede værdi for en nummerserie, der er baseret på den angivne nummerserie, omfang og område-ID. Område-ID'et er lig med den firmakode, der leveres af den kontekst, som ER-formatet køres under. |
| [RoundAmount](er-functions-other-roundamount.md) | Denne funktion returnerer en *Reel* værdi, som repræsenterer resultatet af afrunding af det angivne beløb til det angivne antal decimaler i henhold til den angivne afrundingsregel. |
| [TableName2ID](er-functions-other-tablename2id.md) | Denne funktion returnerer en numerisk gengivelse af tabel-ID'et for det angivne tabelnavn som en værdi angivet som et *Heltal*. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
