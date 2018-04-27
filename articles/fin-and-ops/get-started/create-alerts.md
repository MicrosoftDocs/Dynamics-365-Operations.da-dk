---
title: "Oprette påmindelser"
description: "Dette emne indeholder oplysninger om påmindelser og forklarer, hvordan du opretter en påmindelsesregel, så du får besked om hændelser, f.eks. en dato, der nærmer sig, eller en bestemt ændring, der opstår."
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: 5bcd02e08a4ce5b601615b39bf95362cf92d3fec
ms.contentlocale: da-dk
ms.lasthandoff: 03/23/2018

---

# <a name="create-alerts"></a>Oprette påmindelser

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [banner](../includes/pre-release.md)]

## <a name="getting-started"></a>Kom godt i gang
Før du opretter en påmindelsesregel, skal du beslutte, hvornår og i hvilke situationer du vil modtage påmindelser. Når du ved, hvilke hændelser du vil have besked om, skal du i Microsoft Dynamics 365 for Finance and Operations finde den side, hvor de data vises, der udløser den pågældende hændelse. Hændelsen kan være en dato, der bliver nået, eller en bestemt ændring, der opstår. Derfor skal du finde den side, hvor datoen er angivet, eller hvor det felt, der ændres, eller posten, der oprettes, bliver vist. Når du har disse oplysninger, kan du oprette påmindelsesreglen.

Når du opretter en påmindelsesregel, skal du skal definere de kriterier, der skal være opfyldte, før der udløses en påmindelse. Du kan opfatte kriterier som sammenhængen mellem en hændelses opståen og overholdelse af specifikke betingelser. Når der indtræffer en hændelse, udfører systemet en kontrol i overensstemmelse med de betingelser, der er angivet i Finance and Operations.

## <a name="events"></a>Hændelser
Den hændelse, der udløser en påmindelsesregel, kan være en dato eller en bestemt ændring, der opstår. Udløsere for hændelser defineres på oversigtspanelet **Vis påmindelse, når** i dialogboksen **Opret påmindelsesregel**. Hvilke hændelser, der er tilgængelige for et bestemt felt, afhænger af den udløser, der er valgt.

Hvis du f.eks. definerer en påmindelsesregel for feltet **Startdato**, er forfaldsdatohændelser relevante. Derfor er hændelsestypen **forfalder om** tilgængelig for dette felt. Men til et felt, som f.eks. **Bærer**, kan en forfaldsdato ikke anvendes. Derfor er hændelsestypen **forfalder om** ikke tilgængelig for dette felt. I stedet er hændelsestypen **er ændret** tilgængelig.

## <a name="event-types"></a>Hændelsestyper
Der kan opstå tre typer af hændelser:

- **Hændelser af typen oprette og slette** – Disse hændelser udløser en påmindelse, når en post oprettes eller slettes.
- **Hændelser af typen opdatering** – Disse hændelser udløser en påmindelse, når dataene i et bestemt felt ændres.
- **Hændelser af typen forfaldsdato** – Disse hændelser udløser en påmindelse på en bestemt dato.
    
Ændringer kan aktiveres af brugeren. F.eks. når en bruger ændrer leveringsdatoen for en købsordre. Ændringer kan også forekomme som en del af en proces. F.eks. når feltet **Status** på en side ændres for at afspejle livscyklussen for forskellige processer i systemet.

## <a name="conditions"></a>Årsager
I oversigtspanelet **Påmind mig i** i dialogboksen **Opret påmindelsesregel** kan du bruge betingelser til at styre, hvornår du bliver påmindet om hændelser.

Du kan f.eks. angive, at systemet skal advare dig, når status for købsordrer ændres, men kun, hvis status for en købsordre svarer til et bestemt sæt betingelser. Du ønsker specifikt at blive påmindet, når status for en indkøbsordre er angivet til **modtaget**. Denne statusændring er den hændelse, der udløser påmindelsen.

Derefter skal du beslutte, hvilke indkøbsordrer du vil have besked om. Du kan f.eks. vælge en af følgende indstillinger. Disse indstillinger definerer betingelserne for påmindelsesreglen.

- **Aktuelt valgte post** – Du modtager en påmindelse, når status for en bestemt købsordre ændres til **modtaget**.
- **Alle poster** – du modtager en påmindelse, når status for en indkøbsordre ændres for en vare i den aktive sidevisning. Du kan bruge den avancerede filtrering, der findes på siden, til at oprette regler for et bestemt sæt poster. Du kan for eksempel oprette en påmindelse, der udløses for alle indkøbsordrer for kunderne i en specifik kundegruppe.
    
## <a name="expiry-of-rule"></a>Reglens udløb
I oversigtspanelet **Påmind mig indtil** i dialogboksen **Opret påmindelsesregel** kan du angive, hvor længe reglen skal være aktiv.

## <a name="alert-contents"></a>Påmindelsens indhold
I oversigtspanelet **Vis påmindelse med** i dialogboksen **Opret påmindelsesregel** kan du angive den emnetekst og meddelelsestekst, der skal bruges i advarselsmeddelelserne.

## <a name="user-id"></a>Bruger-id
I oversigtspanelet **Vis påmindelse med** i dialogboksen **Opret påmindelsesregel** kan du angive, hvilken bruger der skal modtage påmindelserne. Dit bruger-ID er som standard markeret. Denne indstilling er begrænset til administratorer i organisationen.

## <a name="create-an-alert-rule"></a>Opret en påmindelsesregel
1. Åbn den side, der indeholder de data, der skal overvåges.
2. I handlingsruden under fanen **Indstillinger** i gruppen **Del** skal du vælge **Opret påmindelsesregel**.
3. Vælg det felt, der skal overvåges, i dialogboksen **Opret påmindelsesregel** i feltet **Felt**.
4. Vælg typen af hændelse, i feltet **Hændelse**.
5. I oversigtspanelet **Påmind mig i** skal du vælge en indstilling.
6. Hvis påmindelsesreglen skal blive inaktiv pr. en bestemt dato, skal du vælge en slutdato i oversigtspanelet **Påmind mig indtil**.
7. I oversigtspanelet **Vis påmindelse med** i feltet **Emne** skal du acceptere standardemneoverskriften til mailen i feltet eller angive et nyt emne. Teksten bruges som emneoverskrift i den e-mail, du modtager, når påmindelsen udløses.
8. Skriv en meddelelse efter eget valg i feltet **Meddelelse**. Teksten bruges som den meddelelse, du modtager, når påmindelsen udløses.
9. Vælg **OK** for at gemme indstillingerne og oprette påmindelsesreglen.

