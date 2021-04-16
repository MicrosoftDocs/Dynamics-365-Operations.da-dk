---
title: Liste over ER-funktioner i kategorien forretningsdomænespecifik
description: Dette emne indeholder oplysninger om de forretningsdomænespecifikke funktioner, der understøttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3d2055be7a755e35d0e88230e19038cf2d02ccc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748009"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Liste over ER-funktioner i kategorien forretningsdomænespecifik

[!include [banner](../includes/banner.md)]

De domænespecifikke til elektronisk rapportering (ER) kan bruges til at udføre beregninger og dataadgangsanmodninger, der er specifikke for implementeringen af Microsoft Dynamics 365 Finance. Dette emne indeholder en oversigt over disse funktioner.

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