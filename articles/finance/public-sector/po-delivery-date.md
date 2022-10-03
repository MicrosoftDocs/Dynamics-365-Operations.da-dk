---
title: Beregne leveringsdatoen for en linje baseret på gennemløbstiden
description: Denne artikel indeholder en beskrivelse af, hvordan du kan beregne en leveringsdato for en linje på baggrund af leverandørens gennemløbstid og din organisations kalender med arbejdsdage.
author: velofog
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: velofog
ms.search.validFrom: 2019-09-03
ms.dyn365.ops.version: 10.0.7
ms.search.industry: public sector
ms.openlocfilehash: fbf96fd3056b2743b2adf62dddc92e5e1616a676
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573004"
---
# <a name="calculate-the-delivery-date-for-a-line-based-on-the-lead-time"></a>Beregne leveringsdatoen for en linje baseret på gennemløbstiden

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan beregne en leveringsdato for en linje på baggrund af leverandørens gennemløbstid og din organisations kalendere for arbejdsdage, som de er angivet på fanen **Tilbud** på siden **Svar på tilbudsanmodning**. Leverandører kan angive en leveringstid for hver linje. Når en indkøbsordre er bekræftet, beregnes en leveringsdato for en linje fra bekræftelsesdatoen, baseret på leveringstiden og kalenderen med arbejdsdage. Hvis der ikke er angivet en leveringstid, bruges bekræftelsesdatoen som leveringsdato, medmindre leveringsdatoen automatisk beregnes.

Leveringstiden for en linje er tilgængelig på følgende sider: **Svar på tilbudsanmodning**, **Indkøbsrekvisitioner**, **Købsaftaler** og **Indkøbsordre**.

Oplysningerne om gennemløbstiden overskrives ikke, når du beregner leveringsdatoer for alle linjer på siden vha. knappen **Leveringsdatoer** på fanen **Beregn** i handlingsruden. Du kan opdatere oplysningerne om leveringstiden for ikke-bekræftede eller ikke-godkendte poster. Når du bekræfter en ændringsrækkefølge, kan du genberegne en leveringsdato.

## <a name="set-up-a-lead-time-calendar"></a>Konfigurere en leveringstidskalender

Du skal konfigurere muligheden for at beregne leveringsdatoer og den kalender, der bruges i disse beregninger, på siden **Indkøbs- og forsyningsparametre**.

1. Gå til **Virksomhedsadministration \> Opsætning \> Kalendere**, og find ud af, om en eksisterende kalender angiver de dage, hvor kontoret er åbent. Hvis du finder en eksisterende kalender, der matcher din organisations arbejdsdage (dvs. dagene, når kontoret er åbent og kan modtage forsendelser), skal du gå videre til trin 2. Ellers skal du følge disse trin for at oprette en ny kalender til arbejdsdage. Du kan oprette en ny kalender, f.eks. hvis dit kontor modtager forsendelser fra mandag til og med torsdag, men din organisations arbejdsdage går fra mandag til fredag.

    1. Vælg **Ny** for at oprette en ny kalender. Du kan også vælge **Kopiér** for at oprette en kalender ud fra en eksisterende, tilsvarende kalender, som du hurtigt kan opdatere.
    2. Angiv et id for kategorigruppen i feltet **Kalender**.
    3. Angiv et beskrivende navn i feltet **Navn**.
    4. Vælg **Arbejdstider**.
    5. Vælg **Opbyg arbejdstider**.
    6. Fjern markeringen i afkrydsningsfeltet **Lukket for afhentning** for hver kalenderdag, der er en arbejdsdag.
    7. Vælg **Gem** for at gemme ændringerne.

    > [!IMPORTANT]
    > Vi anbefaler ikke, at du ændrer en eksisterende kalender, der allerede bruges af en anden del af organisationen.

2. Gå til **Indkøb og forsyning \> Opsætning \> Indkøbs- og forsyningsparametre**.
3. Under fanen **Generelt** skal du angive indstillingen for **Beregn en leveringsdato for indkøbsordre, baseret på leveringstiden og arbejdsdage** til **Ja**.
4. Vælg den kalender, der angiver dagene for, hvornår kontoret er åbent, i feltet **Vælg kalender, der skal bestemme arbejdsdage**.
5. Vælg **Gem** for at gemme ændringerne.

Afsnittet **Leveringstid** vises nu på siderne **Indkøbsrekvisitioner**, **Indkøbsordre** og **Købsaftaler**.

## <a name="edit-the-lead-time-for-a-line"></a>Redigere leveringstiden for en linje

### <a name="purchase-requisition"></a>Indkøbsrekvisition

De leveringstidsoplysninger, som en kreditor angiver for en linje på siden **Svar på tilbudsanmodning**, vises i afsnittet **Leveringstid** for en indkøbsrekvisition. Du kan angive eller redigere oplysningerne om leveringstiden for en indkøbsrekvisitionslinje. Leveringstidsværdierne for indkøbsrekvisitionslinjerne overføres, når en indkøbsordre oprettes.

1. Gå til **Indkøb og forsyning \> Indkøbsrekvisitioner \> Alle indkøbsrekvisitioner** for at åbne listesiden **Alle indkøbsrekvisitioner**. (Du kan også åbne en anden listeside.)
2. Vælg en indkøbsrekvisition på listen. Du kan også vælge **Ny**.
3. Vælg en linje i oversigtspanelet **Indkøbsrekvisitionslinjer**, og vælg derefter **Detaljer**.
4. Angiv oplysninger om leveringsdato i afsnittet **Leveringstid** på oversigtspanelet **Detaljer** på siden **Oplysninger om linje i indkøbsrekvisition**.

    - Angiv det antal dage, der kræves til leveringstiden, i feltet **Leveringstid**.
    - Hvis du kun vil bruge arbejdsdage, ikke alle kalenderdage for at beregne leveringstiden, skal du angive indstillingen **Arbejdsdage** til **Ja**.

7. Vælg **Gem** for at gemme ændringerne.

### <a name="purchase-agreement"></a>Købsaftale

De leveringstidsoplysninger, som du angiver for en linje på siden **Indkøbsrekvisition**, vises i afsnittet **Leveringstid** for en købsaftale. Du kan redigere en eksisterende ikke-godkendt købsaftale eller medtage oplysningerne om leveringstiden i en ny købsaftale. Leveringstidsværdierne for købsaftalelinjerne overføres, når en indkøbsordre oprettes.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Købsaftaler**.
2. Vælg en købsaftale i listen på listesiden **Købsaftaler**. Du kan også vælge **Ny**.' (som i trin 2 i proceduren "Indkøbsrekvisition" ovenfor).
3. Vælg **Rediger** på fanen **Vedligehold** på Handlingsruden på siden **Detaljer om købsaftale**.
4. Vælg en købsaftale i listen på oversigtspanelet **Købsaftaler**.
5. Opdater den beregnede leveringsdato i sektionen **Leveringstid** på fanen **Generelt** i oversigtspanelet **Linjedetaljer**.

    - Angiv det antal dage, der kræves til leveringstiden, i feltet **Leveringstid**.
    - Hvis du kun vil bruge arbejdsdage, ikke alle kalenderdage for at beregne leveringstiden, skal du angive indstillingen **Arbejdsdage** til **Ja**.

8. Vælg **Gem** for at gemme ændringerne.

### <a name="purchase-order"></a>Indkøbsordre

De leveringstidsoplysninger, som du angiver for en linje på siden **Købsaftale** og **Indkøbsrekvisition** vises i afsnittet **Leveringstid** for en indkøbsordre. Du kan redigere oplysninger om leveringstiden for en ikke-bekræftet indkøbsordre.

1. Gå til **Indkøb og forsyning \> Indkøbsordrer \> Alle indkøbsordrer**.
2. Vælg en indkøbsordre i listen på listesiden **Alle indkøbsordrer**. Du kan også vælge **Ny**.' (som i trin 2 i proceduren "Indkøbsrekvisition" ovenfor).
2. Vælg **Rediger** på fanen **Vedligehold** på Handlingsruden på siden **Indkøbsordre**.
3. Opdater den beregnede leveringsdato i feltet **Leveringsdato**, i afsnittet **Leveringstid**, på fanen **Levering**, i oversigtspanelet **Linjedetaljer**.
4. Rediger det antal dage, der kræves til leveringstiden, i feltet **Leveringstid**.
5. Hvis du kun vil bruge arbejdsdage, ikke alle kalenderdage for at beregne leveringsdatoen, skal du angive indstillingen **Arbejdsdage** til **Ja**. Leveringsdatoen opdateres, når indkøbsordren godkendes og bekræftes baseret på den angivne leveringstid.
6. Vælg **Gem** for at gemme ændringerne.

> [!NOTE]
> I forbindelse med frigivne varer kan du vælge en leveringstid for købet. Købets leveringstiden beregner automatisk leveringsdatoen, når der oprettes en indkøbsordre. Leveringsdatoen genberegnes ikke, hvis leveringstiden på indkøbsordrelinjen er 0 (nul).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
