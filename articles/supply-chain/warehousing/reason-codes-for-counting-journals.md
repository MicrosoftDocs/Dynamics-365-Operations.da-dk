---
title: Årsagskoder for lageroptælling
description: Dette emne beskriver, hvordan du konfigurerer og anvender årsagskoder til optællingsopgaver.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: d72b171bfe149b25f5055d5bebef85b49e952295
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228483"
---
# <a name="reason-codes-for-inventory-counting"></a>Årsagskoder for lageroptælling

[!include [banner](../includes/banner.md)]

Med årsagskoder kan du analysere resultaterne af en optællingsproces og eventuelle uoverensstemmelser, der opstår under denne proces. Du kan angive årsagen til optællingen, f.eks. en ødelagt palle eller en regulering af lageret, der er baseret på lagerprøver.

## <a name="recommendation"></a>Anbefaling

Før du konfigurerer systemet, anbefales det, at du definerer en strategi for at arbejde med årsagskoder. Prøv f.eks. at besvare følgende spørgsmål:

- Skal årsagskoder være obligatoriske på lagersteder?
- Årsagskoder skal være obligatoriske eller valgfrie for bestemte varer?
- Hvor mange årsagskoder skal du bruge?
- Hvordan skal brugere af stregkodescannere bruge årsagskoder? Skal årsagskoderne være forvalgte, obligatoriske eller ikke kunne redigeres?
- Kræver lagermedarbejdere andre funktionsmåder for årsagskoder på mobile scannere? Hvis svaret er Ja, kan du oprette flere menupunkter og tildele dem til forskellige personer.

## <a name="where-reason-codes-apply"></a>Hvor anvendes årsagskoder

Du kan oprette flere årsagskodepolitikker, og hver årsagskodepolitik kan have to politikker for årsagskoder for optælling. Politikker for optællingsårsagskoder kan bruges på lagerstedsniveau eller vareniveau.

## <a name="set-up-reason-code-policies"></a>Konfigurere politikker for årsagskoder

1. Vælg **Lagerstyring** \> **Opsætning** \> **Lager** \> **Politikker for optællingsårsagskode**, og opret en ny politik for årsagskoder.
2. I feltet **Type af optællingsårsagskode** skal du vælge enten **Obligatorisk** eller **Valgfrit** for at angive, om valget af en årsagskode skal være en valgfri eller obligatorisk handling i en af følgende optællingskladder:

    - Cyklusoptælling (mobilenhed)
    - Spotoptælling (mobilenhed)
    - Grænseoptælling (mobilenhed)
    - Regulering ind (mobilenhed)
    - Regulering ud (mobilenhed)
    - Optællingskladde (Rich Client)

Du kan også angive årsagskoder for individuelle lagersteder og produkter. Opsætningen af årsagskoder for produkter kan se bort fra opsætningen for lagersteder.

## <a name="mandatory-reason-codes"></a>Obligatoriske årsagskoder

Hvis parameteren **Obligatorisk** er angivet i konfigurationen af årsagskoder for lagersteder eller varer, kan optællingskladden ikke fuldføres og lukkes, før en årsagskode er angivet.

### <a name="set-up-reason-codes-for-warehouses"></a>Konfigurere årsagskoder for lagersteder

1. Vælg **Lagerstyring** \> **Opsætning** \> **Lageropdeling** \> **Lagersteder**.
2. På fanen **Lagersted** i feltet **Politik for optællingsårsagskode** skal du vælge en af følgende indstillinger:

    - **Tom** – Den parameter, der er defineret for varen, bruges til at afgøre, om optællingskladder er obligatoriske for produktet.
    - **Obligatoriske** – Der kræves altid en årsagskode på optællingskladder for lagerstedet.
    - **Valgfri** – Der kræves ikke en årsagskode på optællingskladder for lagerstedet.

### <a name="set-up-reason-codes-for-products"></a>Konfigurere årsagskoder for produkter

1. Vælg **Administration af produktoplysninger** \> **Produkter** \> **Frigivne produkter**.
2. På fanen **Produkt** skal du vælge **Politik for optællingsårsagskode** og derefter vælge en af følgende indstillinger:

    - **Tom** – Den parameter, der er defineret for lagerstedet, bruges til at afgøre, om optællingskladder er obligatoriske for produktet.
    - **Obligatoriske** – Der kræves altid en årsagskode kræves på optællingskladder for produktet. Denne indstilling tilsidesætter enhver indstilling for årsagskoder på lagerstedsniveau.
    - **Valgfri** – Der kræves ikke en årsagskode på optællingskladder for produktet. Denne indstilling tilsidesætter enhver indstilling for årsagskoder på lagerstedsniveau.

### <a name="use-reason-codes-in-counting-journals"></a>Bruge årsagskoder i optællingskladder

I en optællingskladde kan du tilføje årsagskoder for optælling af følgende typer:

- Cyklusoptælling
- Spotoptælling
- Grænseoptælling
- Regulering ind
- Regulering ud

Årsagskoder føjes til kladdelinjerne i optællingskladder af typen **Optællingskladde**.

1. Vælg **Lagerstyring** \> **Kladdeposteringer** \> **Vareoptælling** \> **Optælling**.
2. I linjedetaljerne i optællingskladden, i feltet **Optællingsårsagskode** skal du vælge en indstilling.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Få vist optællingshistorikken, sådan som den er registreret af årsagskoder

- Vælg **Lagerstyring** \> **Forespørgsler og rapporter** \> **Optællingshistorik**, få derefter vist den optællingshistorik i feltet **Optællingsårsagskode**, som er registreret gennem en årsagskode.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Bruge en årsagskode til en regulering af antal

1. På siden **Disponibel lagerbeholdning** skal du vælge **Juster antal**. Du kan åbne siden **Disponibel lagerbeholdning** på flere måder. Vælg f.eks. **Lagerstyring** \> **Forespørgsler og rapporter** \> **Disponibel lagerbeholdning**.
2. Vælg **Juster antal**, og vælg derefter en årsagskode i feltet **Optællingsårsagskode**.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Konfigurere årsagskoder for mobilenheds menupunkter

Du kan konfigurere årsagskoder for enhver type optælling i et menupunkt på en mobilenhed. Konfigurationen af menupunktet på mobilenheden indeholder følgende oplysninger:

- Om årsagskoden vises for mobilenhedens arbejder under optælling.
- Den standardårsagskode, der vises i en mobilenheds menupunkt.
- Om brugeren kan redigere årsagskoden.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Konfigurere årsagskoder på en mobilenhed

1. Vælg **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Menupunkter i mobilenhed**.
2. På fanen **Cyklusoptælling** skal du vælge **Cyklusoptælling**.
3. I feltet **Standardkode for optællingsårsag** skal du angive den standardårsagskode, der skal registreres, når optællingen udføres ved hjælp af mobilenhedens menupunkt.
4. I feltet **Vis optællingsårsagskode** skal du vælge **Linje** for at vise årsagskoden efter registrering af hver afvigelse. Alternativt skal du vælge **Skjul**, hvis årsagskoden ikke skal vises.
5. Angiv indstillingen **Rediger optællingsårsagskode** til enten **Ja** eller **Nej**. Hvis du angiver denne indstilling til **Ja**, kan arbejderen redigere årsagskoden, når den vises på mobileenheden under optælling.

> [!NOTE]
> Knappen **Cyklusoptælling** kan aktiveres i menupunktet på enhver mobilenhed, hvor optælling kan udføres. Eksemplet omfatter menupunkter for spotoptællinger, brugerstyret arbejde og systemstyret arbejde.

## <a name="cycle-count-approvals"></a>Godkendelse af cyklusoptælling

Før antallet godkendes, kan brugeren ændre den årsagskode, der er tilknyttet optællingen. Når optællingen er godkendt, angives årsagskoden i optællingskladdens linjer.

### <a name="modify-cycle-count-approvals"></a>Rediger godkendelse af cyklusoptælling

1. Vælg **Lokationsstyring** \> **Cyklusoptælling** \> **Ventende gennemsyn af cyklusoptællingsarbejde**.
2. Vælg **Cyklusoptælling**, og vælg derefter en ny årsagskode i feltet **Årsagskode**.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Redigere mobilenhedens menupunkt for Regulering ind og Regulering ud

1. Vælg **Lokationsstyring** \> **Opsætning** \> **Mobilenhed** \> **Menupunkter i mobilenhed**, og vælg derefter **Regulering ind og ud**.
2. Angiv indstillingen **Brug eksisterende arbejde** til **Nej**.
3. I feltet **Arbejdsoprettelsesproces** skal du vælge **Regulering ind**.

Følgende felter føjes til mobilenhedens menupunkt, når **Regulering ind** eller **Regulering ud** er valgt under oprettelsen af arbejdsoprettelsesprocessen:

- Standardkode for optællingsårsag
- Vis optællingsårsagskode
- Rediger optællingsårsagskode


[!INCLUDE[footer-include](../../includes/footer-banner.md)]