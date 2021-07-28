---
title: Aktivere og konfigurere automatiske gebyrer efter kanal
description: I dette emne beskrives, hvordan du aktiverer og konfigurerer automatiske gebyrer efter kanal i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: c38717ca9c57913ea22f2dd7712b49f39d2e556e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349692"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>Aktivere og konfigurere automatiske gebyrer efter kanal

I dette emne beskrives, hvordan du aktiverer og konfigurerer automatiske gebyrer (autogebyr) efter kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overblik

Der kan være tilfælde, hvor du skal anvende genbrugsgebyrer eller andre gebyrer på en gruppe af produkter, der sælges i alle eller nogle butikker i en bestemt stat (f.eks. Californien). Funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** i Commerce giver dig mulighed for at angive automatiske gebyrer efter kanal (f.eks. en specifik fysisk vare- og en fysisk kanal). Denne funktion er tilgængelig i Dynamics 365 Commerce version 10.0.10 og nyere.

Hvis du vil aktivere og konfigurere automatiske gebyrer efter kanal, skal du udføre følgende opgaver:

- Slå funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** til.
- Konfigurer formålet med organisationshierarkier.
- Definer automatiske gebyrer efter kanal.

> [!NOTE]
> Funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** virker kun, hvis funktionen til avancerede automatiske gebyrer også er slået til. Du kan få flere oplysninger om, hvordan du aktiverer funktionen avancerede automatiske gebyrer, i [Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>Slå funktionen Aktivér filtrering af automatiske gebyrer efter kanal til

Hvis du vil aktivere automatiske gebyrer efter kanal i Commerce, skal du følge disse trin.

1. Gå til **Systemadministrator \> Arbejdsområder \> Funktionsstyring**.
1. Find og vælg **Aktivér filtrering af automatiske gebyrer efter kanal** i listen **Funktionsnavn** på fanen **Ikke aktiveret**.
1. Vælg **Aktivér nu** i nederste højre hjørne. Når funktionen er slået til, vises den på listen under fanen **Alle**.
1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Find og vælg jobbet **1110** (**Global konfiguration**) i venstre rude.
1. Vælg **Kør nu** i handlingsruden for at overføre konfigurationsændringerne.

> [!WARNING]
> Hvis du slår funktionen **Aktivér filtrering af automatiske gebyrer for kanal** fra, efter at du allerede har brugt den, vises feltet **Detailkanalrelation** under **Automatiske gebyrer** ikke længere, og du mister alle eksisterende konfigurationer. Hvis fjernelse af konfigurationerne af **Detailkanalrelationer** medfører, at automatiske gebyrregler duplikeres, vil et forsøg på at slå funktionen fra mislykkes. Før du slår for funktionen fra, skal du gennemgå alle regler for automatisk gebyrer og foretage eventuelle nødvendige ændringer.

## <a name="configure-the-organization-hierarchy-purpose"></a>Konfigurer formålet med organisationshierarkier

Der er oprettet et nyt formål med organisationshierarki, som hedder **Opkræv automatisk detailgebyr** for at administrere hierarkiet for automatiske gebyrer efter kanal.

Hvis du vil tildele et standardhierarki til et formål med organisationshierarki i Commerce, skal du følge disse trin.
        
1. Gå til **Organisationsadministration \> Organisationer \> Formål med organisationshierarkier**.
1. Vælg **Opkræv automatisk detailgebyr** i ruden til venstre.
1. Vælg **Tilføj** under **Tildelte hierarkier**.
1. Vælg et organisationshierarki f.eks. **Detailbutikker efter region** i dialogboksen **Organisationshierarkier**, og vælg derefter **OK**.
1. Vælg **Angiv som standard** under **Tildelte hierarkier**.
1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Find og vælg jobbet **1040** (**Produkter**) i venstre rude.
1. Vælg **Kør nu** i handlingsruden.
1. Gentag de forrige to trin for at køre jobbene **1070** (**Kanalkonfiguration**) og **1110** (**Global konfiguration**).

![Konfiguration af formålet med organisationshierarkiet til automatisk debitering af detailvarer.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>Definer automatiske gebyrer efter kanal

Når du har slået funktionen **Aktivér filtrering af automatiske gebyrer efter kanal** til og konfigureret formålet med organisationshierarkiet for **Detailbutikker efter region**, kan automatiske gebyrer defineres på ordrehovedniveau eller på ordrelinjeniveau.

Hvis du vil definere automatiske gebyrer efter kanal i Commerce, skal du følge disse trin.

1. Gå til **Debitor \> Konfiguration af gebyrer \> Automatiske gebyrer**.
1. Vælg **Overskrift** eller **Linje** i feltet **Niveau** i ruden til venstre, afhængigt af firmaets krav.
1. Vælg den relevante kanalkode (f.eks. **Tabel** eller **Gruppe**) i feltet **Detailkanalkode**. Hvis standardindstillingen **Alle** bruges, anvendes gebyrreglerne på alle kanaler.

    - Hvis du vælger **Gruppe**, skal du sikre dig, at der oprettes en gebyrgruppe for detailkanalen på **Retail og Commerce \> Opsætning af kanal \> Gebyrer \> Gebyrgrupper for detailkanal**.
    - Hvis du vælger **Tabel**, kan du vælge en bestemt kanal (f.eks. **San Francisco**) i feltet **Detailkanalrelation**.

1. Gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.
1. Find og vælg jobbet **1040** (**Produkter**) i venstre rude.
1. Vælg **Kør nu** i handlingsruden.
1. Gentag de forrige to trin for at køre jobbene **1070** (**Kanalkonfiguration**) og **1110** (**Global konfiguration**).
    
![Automatiske gebyrer defineret efter kanal.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>Eksempelscenario

I følgende eksempel beskrives de trin, der skal udføres for at konfigurere et produkt, så genbrugsgebyrer debiteres, når produktet sælges via en fysisk kanal i San Francisco. I eksemplet vises også, hvordan de automatiske gebyrer vises i kasseprogrammet (POS) i Commerce.

Organisationen definerer en gebyrkode, der kaldes **GENBRUG**, som vist i følgende illustration.

![GENBRUG-gebyrkode.](media/Auto-charges-charge-code.png)

Der oprettes et automatisk gebyr på linjeniveau. Den har følgende konfiguration:

- Feltet **Kontokode** er angivet til **Alle**.
- Feltet **Varekode** er angivet til **Tabel**.
- Feltet **Varerelation** er angivet til produkt-id **91001**.
- Feltet **Kode for leveringsmåde** er angivet til **Alle**.
- Feltet **Detailkanalkode** er angivet til **Tabel**.
- Feltet **Detailkanalrelation** er angivet til lageret i **San Francisco**.

Der oprettes en automatisk gebyrlinje. Den har følgende konfiguration:

- Feltet **Valuta** er angivet til **USD**.
- Feltet **Gebyrkode** er angivet til **GENBRUG**.
- Feltet **Kategori** er angivet til **Fast**.
- Feltet **Gebyrer** er angivet til **$6,25**.

![Konfiguration af automatisk gebyrer for linjeniveau og den automatiske gebyrlinje.](media/Auto-charges-recyclingfee-line-fee.png)

I kasseprogrammet oprettes der en salgsordre i lagerkanalen **San Francisco**. Linjen **Gebyrer** viser genbrugsgebyret på **$6,25**.

Når du vælger **Transaktionsindstillinger \> Gebyrer \> Administrer gebyrer** i kasseprogrammet, kan du få vist gebyrkoden og beskrivelsen for genbrugsgebyret.

![Genbrugsgebyr i kasseprogrammet.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Avancerede automatiske gebyrer for omni-kanal](omni-auto-charges.md)

[Beregne hovedgebyrer forholdsmæssigt på matchende salgslinjer](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]