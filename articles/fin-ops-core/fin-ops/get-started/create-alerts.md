---
title: Opret påmindelsesregler
description: Dette emne indeholder oplysninger om påmindelser og forklarer, hvordan du opretter en påmindelsesregel, så du får besked om hændelser, f.eks. en dato, der nærmer sig, eller en bestemt ændring, der opstår.
author: tjvass
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 3721416ce720167a6f78e26583de84af9c8d086b
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798421"
---
# <a name="create-alert-rules"></a>Opret påmindelsesregler

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Kom godt i gang

Før du opretter en påmindelsesregel, skal du beslutte, hvornår og i hvilke situationer du vil modtage påmindelser. Når du ved, hvilke hændelser du vil have besked om, skal du finde den side, hvor de data vises, der udløser den pågældende hændelse. Hændelsen kan være en dato, der bliver nået, eller en bestemt ændring, der opstår. Derfor skal du finde den side, hvor datoen er angivet, eller hvor det felt, der ændres, eller posten, der oprettes, bliver vist. Når du har disse oplysninger, kan du oprette påmindelsesreglen.

Når du opretter en påmindelsesregel, skal du skal definere de kriterier, der skal være opfyldte, før der udløses en påmindelse. Kriterier er grundlæggende set sammenhængen mellem en hændelses opståen og opfyldelsen af specifikke betingelser. Når der indtræffer en hændelse, udfører systemet en kontrol i overensstemmelse med de betingelser, der er angivet.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Sørg for, at påmindelsesbatchjobbene kører

Batchjobbene for dataændring og påmindelser om forfaldsdatoer skal køre, for at påmindelsesbetingelserne kan behandles, og beskederne kan sendes. Hvis du vil køre batchjob, skal du gå til **Systemadministration** > **Periodiske opgaver** > **Påmindelser** og tilføje et nyt batchjob til **Ændringsbaserede påmindelser** og/eller **Påmindelser om forfaldsdatoer**. Hvis der er brug for et lang og ofte kørt batchjob, skal du vælge **Gentagelse** og angive **Ingen slutdato** med et **Gentagelsesmønster** på **Minutter** og et **Antal** på **1**.

## <a name="events"></a>Hændelser

Den hændelse, der udløser en påmindelsesregel, kan være en dato eller en bestemt ændring, der opstår. Udløsere for hændelser defineres på oversigtspanelet **Vis påmindelse, når** i dialogboksen **Opret påmindelsesregel**. Hvilke hændelser, der er tilgængelige for et bestemt felt, afhænger af den udløser, der er valgt.

Hvis du f.eks. definerer en påmindelsesregel for feltet **Startdato**, er forfaldsdatohændelser relevante. Derfor er hændelsestypen `is due in` tilgængelige for dette felt. Men til et felt, som f.eks. **Bærer**, kan en forfaldsdato ikke anvendes. Derfor er hændelsestypen `is due in` ikke tilgængelig for dette felt. Derimod er hændelsestypen `has changed` tilgængelig.

## <a name="event-types"></a>Hændelsestyper

Der kan opstå tre typer af hændelser:

- **Hændelser af typen oprette og slette** – Disse hændelser udløser en påmindelse, når en post oprettes eller slettes.
- **Hændelser af typen opdatering** – Disse hændelser udløser en påmindelse, når dataene i et bestemt felt ændres.
- **Hændelser af typen forfaldsdato** – Disse hændelser udløser en påmindelse på en bestemt dato.
    
Ændringer kan aktiveres af brugeren. F.eks. når en bruger ændrer leveringsdatoen for en købsordre. Ændringer kan også forekomme som en del af en proces. F.eks. når feltet **Status** på en side ændres for at afspejle livscyklussen for forskellige processer i systemet.

## <a name="conditions"></a>Årsager

I oversigtspanelet **Påmind mig om** i dialogboksen **Opret påmindelsesregel** kan du bruge betingelser til at styre, hvornår du bliver påmindet om hændelser.

Du kan f.eks. angive, at systemet skal advare dig, når status for købsordrer ændres, men kun, hvis status for en købsordre svarer til et bestemt sæt betingelser. Du ønsker specifikt at blive påmindet, når status for en indkøbsordre er angivet til **modtaget**. Denne statusændring er den hændelse, der udløser påmindelsen.

Derefter skal du beslutte, hvilke indkøbsordrer du vil have besked om. Du kan f.eks. vælge en af følgende indstillinger. Disse indstillinger definerer betingelserne for påmindelsesreglen.

- **Aktuelt valgte post** – Du modtager en påmindelse, når status for en bestemt købsordre ændres til **modtaget**.
- **Alle poster** – du modtager en påmindelse, når status for en indkøbsordre ændres for en vare i den aktive sidevisning. Du kan bruge den avancerede filtrering, der findes på siden, til at oprette regler for et bestemt sæt poster. Du kan for eksempel oprette en påmindelse, der udløses for alle indkøbsordrer for kunderne i en specifik kundegruppe.
    
## <a name="expiry-of-rule"></a>Reglens udløb

I oversigtspanelet **Påmind mig indtil** i dialogboksen **Opret påmindelsesregel** kan du angive, hvor længe reglen skal være aktiv.

## <a name="alert-contents"></a>Påmindelsens indhold

I oversigtspanelet **Vis påmindelse med** i dialogboksen **Opret påmindelsesregel** kan du angive den emnetekst og meddelelsestekst, der skal bruges i advarselsmeddelelserne.

## <a name="user-id"></a>Bruger-id

I oversigtspanelet **Vis påmindelse med** i dialogboksen **Opret påmindelsesregel** kan du angive, hvilken bruger der skal modtage påmindelserne. Dit bruger-ID er som standard markeret. Muligheden for at ændre den bruger, der modtager påmindelsen, er begrænset til organisationens administratorer.

## <a name="alerts-as-business-events"></a>Påmindelser som forretningshændelser

Du kan sende påmindelser eksternt ved hjælp af rammen for forretningshændelser. Når du opretter en påmindelse, skal du angive **Hele organisationen** til **Nej** og angive **Send eksternt** til **Ja**. Når du har den påmindelse, som skal udløse forretningshændelsen, kan du udløse et i Power Automate indbygget flow, som anvender udløseren **Når der indtræffer en forretningshændelse** på forbindelsen Finance and Operations, eller eksplicit sender hændelsen til en forretningshændelses slutpunkt via **Forretningshændelseskataloget**.

## <a name="create-an-alert-rule"></a>Opret en påmindelsesregel

0. Sørg for, at påmindelsesbatchjobbene kører (se ovenfor).
1. Åbn den side, der indeholder de data, der skal overvåges.
2. I handlingsruden under fanen **Indstillinger** i gruppen **Del** skal du vælge **Opret påmindelsesregel**.
3. Vælg det felt, der skal overvåges, i dialogboksen **Opret påmindelsesregel** i feltet **Felt**.
4. Vælg typen af hændelse, i feltet **Hændelse**.
5. I oversigtspanelet **Påmind mig om** skal du vælge den ønskede indstilling. Hvis du vil sende påmindelsen som en forretningshændelse, skal du angive værdien af **Hele organisationen** til **Nej**.
6. Hvis påmindelsesreglen skal blive inaktiv pr. en bestemt dato, skal du vælge en slutdato i oversigtspanelet **Påmind mig indtil**.
7. I oversigtspanelet **Vis påmindelse med** i feltet **Emne** skal du acceptere standardemneoverskriften til mailen i feltet eller angive et nyt emne. Teksten bliver emneoverskriften i den mail, du modtager, når påmindelsen udløses. Hvis du vil sende påmindelsen som en forretningshændelse, skal du angive **Send eksternt** til **Ja**.
8. Skriv en meddelelse efter eget valg i feltet **Meddelelse**. Teksten bliver den meddelelse, du modtager, når påmindelsen udløses.
9. Vælg **OK** for at gemme indstillingerne og oprette påmindelsesreglen.

## <a name="limitations-and-workarounds"></a>Begrænsninger og løsninger

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Løsning til oprettelse af påmindelser til sekundære datakilder i en formular
Der kan ikke oprette påmindelser for visse sekundære datakilder i formularer. Når du f.eks. opretter påmindelser i formularen debitor- eller kreditorposteringsprofiler, er det kun felterne i hovedet (CustLedger eller VendLedger), der er tilgængelige, og ikke dimensions kontiene. Løsningen på denne begrænsning er at bruge **SysTableBrowser** til at åbne den pågældende tabel som primær datakilde. 
1. Åbn tabellen i formularen **SysTableBrowser**.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Opret en påmindelse fra formularen SysTableBrowser.

