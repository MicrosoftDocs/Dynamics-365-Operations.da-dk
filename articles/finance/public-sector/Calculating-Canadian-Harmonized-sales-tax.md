---
title: Canadisk harmoniseret moms (Harmonized Sales Tax - HST)
description: Denne artikel giver oplysninger om funktionerne til at understøtte harmoniseret moms for den offentlige sektor.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNCanadianHSTTaxFeature
audience: Application User
ms.devlang: ''
ms.reviewer: twheeloc
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: twheeloc
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 61b519ac2575853b8fb0a65c308e09c81e8051f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856446"
---
# <a name="calculating-canadian-harmonized-sales-tax"></a>Beregning af canadisk harmoniseret moms

[!include [banner](../includes/banner.md)]

Denne funktion giver din organisation mulighed for at overholde de canadiske harmoniserede momsregler (HST). HST hjælper offentlige institutioner med at overholde canadiske momspolitikker. HST bruges af visse canadiske provinser og er en kombination af moms på varer og ydelser og provinsmoms.
Dele af HST kan genvindes af offentlige myndigheder, hvis momsen er betalt til kreditorer, afhængigt af købets formål. Formålet er angivet af de økonomiske dimensionsværdier og hovedkontoen på en posteringslinje i et købsdokument (f.eks. en indkøbsrekvisition, en indkøbsordre eller en kreditorfaktura).
Bemærk! Denne funktionalitet gælder ikke for kreditorfakturakladden.

## <a name="enabling-the-hst-feature"></a>Aktivere funktionen HST

1. Gå til **Finans > Opsætning Finans > Finansparametre > Momsgruppe**.
2. Indstil **Anvend canadiske harmoniserede momsregler** til **Ja**, hvis du vil aktivere funktionen.

## <a name="define-the-dimensions-for-hst-rules"></a>Definere dimensionerne for HST-regler

1. Gå til **Moms > Indirekte moms > Moms**, og klik derefter på **Harmoniserede momsdimensioner**. 
2. På siden **Harmoniserede momsdimensioner** skal du vælge og prioritere de økonomiske dimensioner (sammen med hovedkontoen, hvis det er relevant), du vil bruge til HST. De økonomiske dimensioner i kontostrukturer knyttes til kontoplanen. Dimensionernes prioritet er en hjælp til at diktere den moms, der anvendes, hvis der er flere muligheder. 



> [!Note] 
> Kun de økonomiske dimensioner, der bruges i den aktuelle juridiske enhed, vil være tilgængelige.

## <a name="set-up-hst-rules"></a>Konfigurere HST-regler

Når du har defineret dimensionerne for HST, skal du konfigurere de finansdimensionsregler, der gælder. HST-regler tildeler momskoder ud fra dokumentlinjers kontofordelinger. Det skyldes, at der kan anvendes forskellige momskoder baseret på formålet med købet.
1. Gå til **Moms > Indirekte moms > Moms**, og klik derefter på **Harmoniserede momsregler**. 
2. På siden **Harmoniserede momsregler** vises de dimensioner, du har valgt til HST, i prioriteret rækkefølge fra venstre mod højre. De resterende kolonner gælder for momskoder, der er tilknyttet denne dimensionskombination. 
3. Vælg **Ny** i handlingsruden for at oprette en ny post.
4. Definer dimensionsværdierne. 

### <a name="notes"></a>Noter:
- Der kan ikke være identiske indstillinger for to rækker.
- Du kan slette eller redigere eksisterende regler.
- Du kan vælge at lade et segment være tomt. Det fungerer som "joker". En fuldstændigt tom række gælder for alle kontokombinationer, hvor der ikke er anvendt en mere specifik regel. Du kan tilføje én række med alle tomme økonomiske dimensioner, hvis der er momskoder, som skal anvendes, når ingen regler matcher.

5. Vælg op til fem momskoder, der kan anvendes i forhold til de dimensioner, der er valgt til HST. Bemærk! For at kunne anvendes skal de momskoder, der er defineret her, være til stede i HST-reglen og i både den **Momsgruppe** og **Varemomsgruppe**, der er valgt på linjerne i transaktionsdokumentet. 
6. Klik på **Gem** for at gemme ændringerne. 

### <a name="notes"></a>Noter:
- Når du har defineret reglerne for HST, kan du ikke redigere eksisterende dimensioner for HST. Hvis du vil foretage ændringer, skal du først fjerne alle regler og momskoder i formularen **Harmoniserede momsregler**.
- Der kan anvendes mere end én momskode på en regel.
- Der gælder kun én regel for en kontofordeling.
- Der kan gælde mere end én regel for en linje i et transaktionsdokument med flere fordelinger.

## <a name="how-rules-are-applied"></a>Sådan anvendes regler

Den rækkefølge, som reglerne anvendes i, er noget kompleks. Følgende grafik viser princippet:

> [![Definere HST-regler.](./media/define-hst-rules.png)](./media/define-hst-rules.png)

De momskoder, der er valgt for dimensionslinjen, er som følger, hvis posteringen bruger en momsgruppe og varemomsgruppe med alle de momskoder, der er medtaget.

|Økonomiske dimensioner                     | Momskoder|
|-----------------------------------------|-----------------|   
|Fond 101, enhver division med undtagelse af 111 og 121| Tax1            |
|   Fond 101, division 111                  |   Tax1, Tax2, Tax3|
|   Fond 101, division 121                  | Tax2, Tax3      |
|   Fond 303, enhver division med undtagelse af 141         | Tax1, Tax2, Tax3|
|   Fond 303, division 141                  | Tax1            |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
