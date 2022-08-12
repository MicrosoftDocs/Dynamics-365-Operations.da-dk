---
title: Rette fejlen "Ikke tilstrækkelig kapacitet kunne findes" i planlægningsprogrammet og kapacitetsbegrænsning
description: Denne artikel indeholder oplysninger om årsagerne til og løsningerne for 'Produktionsordren %1 kunne ikke planlægges. Fejlen i planlægningsprogrammet "Ikke tilstrækkelig kapacitet kunne findes".
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135593"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Rette fejlen i planlægningsprogrammet "Ikke tilstrækkelig kapacitet kunne findes"

[!include [banner](../includes/banner.md)]

Du kan få vist følgende fejlmeddelelse, når du forsøger at kære planlægning:

> Produktionsordren %1 kan ikke planlægges. Der blev ikke fundet nok kapacitet.

Der er flere årsager til, at planlægningsprogrammet kan mislykkes og udstede denne fejlmeddelelse. Denne artikel indeholder retningslinjer, der kan hjælpe dig med at finde rodårsagen til fejlen og derefter reducere den.

## <a name="review-the-applicable-resources"></a>Gennemse de relevante ressourcer

Fejlen kan opstå, hvis ingen relevante ressourcer opfylder operationskravene på produktionsordrewebstedet.

Følg disse trin for at gennemse mulige ressourcer.

1. Gå til **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer**, og åbn eller vælg de produktionsordrer, der ikke kan planlægges.
1. I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Produktionsdetaljer** vælge **Rute**.
1. Vælg operationen på siden **Produktionsrute**, og vælg derefter **Relevante ressourcer** i handlingsruden.
1. I dialogboksen **Gældende ressourcer** skal du angive feltet **Brug krav til** til *grovplanlægning* eller *finplanlægning* afhængigt af, hvilken type planlægning du bruger.
1. Kontroller, at der er relevante ressourcer på produktionsordrewebstedet.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Gennemse de kalendere, der er knyttet til ressourcerne

Fejlen kan opstå, hvis der ikke er knyttet en kalender til ressourcen eller ressourcegruppen, eller hvis den tilknyttede kalender ikke er konfigureret korrekt (f.eks. hvis den ikke har nogen arbejdstider, eller hvis dens effektivitet som procentdel er 0 \[nul\]).

Hvis du vil kontrollere, at en kalender er knyttet til ressourcen eller ressourcegruppen, skal du følge disse trin.

1. Gå til **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer**, og åbn eller vælg de produktionsordrer, der ikke kan planlægges.
1. I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Produktionsdetaljer** vælge **Rute**.
1. Vælg operationen på siden **Produktionsrute**, og vælg derefter **Relevante ressourcer** i handlingsruden.
1. Vælg ressourcen i dialogboksen **Gældende ressourcer**, og vælg derefter **Vis ressource**. Du kan også vælge og holde (eller højreklikke) i feltet **Ressourcegruppe** og derefter vælge **Vis detaljer**.
1. På siden **Ressourcer** eller på siden **Ressourcegrupper** i oversigtspanelet **Kalendere** skal du kontrollere, at en kalender er knyttet til ressourcen eller ressourcegruppen.

> [!NOTE]
> Hvis der opstår fejl under grovplanlægning, skal du sikre dig, at der er knyttet en kalender til alle gældende ressourcegrupper.

Benyt følgende fremgangsmåde for at gennemse opsætningen af kalenderen.

1. Gå til **Virksomhedsadministration \> Opsætning \> Kalendere \> Kalendere**, og vælg den kalender, der er tilknyttet ressourcen eller ressourcegruppen.
1. Vælg **Arbejdsgang** i handlingsruden.
1. Sørg for, at siden ikke er tom, på siden **Arbejdstider**. Derudover skal du for de dage, du er interesseret i, kontrollere, at **kontrolfeltet** ikke er angivet til *Lukket*, arbejdstider findes, og at feltet **Effektivitet er procent** og ikke er angivet til *0* (nul).

Hvis kalenderen er knyttet til basiskalenderen, skal du også gennemse opsætningen af basiskalenderen.

> [!NOTE]
> Ved grovplanlægning bruges ressourcegruppens kalender til at bestemme start- og sluttidspunkter for hver operation. Det begrænser også den tid, systemet kan planlægge for en bestemt operation for en bestemt dag i en bestemt ressourcegruppe. Hvis arbejdstiderne for en ressourcegruppe på en bestemt dag f.eks. er fra kl. 8:00 til 16:00, kan den belastning, som en operation placerer på ressourcegruppen, ikke overstige den belastning, der kan være i otte timer, uanset mængden af tilgængelig kapacitet, som ressourcegruppen har på den pågældende dag. Den tilgængelige kapacitet kan dog begrænse belastningen yderligere.

## <a name="review-the-scheduling-parameters"></a>Gennemse planlægningsparametre

For at sikre god ydeevne søger planlægningsprogrammet kun efter en ressource i et bestemt tidsrum og i et bestemt antal planlægningskonflikter.

Benyt følgende trin for at gennemse planlægningsparametre.

1. Gå til **Virksomhedsadministration \> Opsætning \> Planlægningsparametre**.
1. Udfør ét af følgende trin:

    - Hvis indstillingen **Timeout for Planlægning aktiveret** er angivet til *Nej*, skal du gå til trin 3.
    - Hvis indstillingen **Timeout for planlægning aktiveret** er angivet til *Ja*, øges værdien af feltet **Maksimal planlægningstid pr. sekvens**, så behandlingen får mere tid, der skal fuldføres.

1. Udfør ét af følgende trin:

    - Hvis indstillingen **Timeout for Planlægning optimeret aktiveret** er angivet til *Nej*, skal du gå til trin 4.
    - Hvis indstillingen **Timeout for planlægning optimeret aktiveret** er angivet til *Ja*, øges værdien af feltet **Timeout for optimeringsforsøg**, så behandlingen får mere tid, der skal fuldføres.

1. Hvis du har ændret nogen af indstillingerne på siden, skal du omplanlægge ordren for at prøve igen.

## <a name="review-capacity"></a>Gennemse kapacitet

Fejlen kan opstå, når du udfører planlægningsbegrænsning, men der ikke er ledig kapacitet.

Udfør følgende trin for at udføre planlægning af ubegrænset kapacitet.

1. Gå til **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer**, og åbn eller vælg de produktionsordrer, der ikke kan planlægges.
1. I handlingsruden under fanen **Planlæg** i **Produktionsordregruppen** skal du vælge **Planlæg operationer** eller **Planlæg job**.
1. Angiv indstillingen **Kapacitetsbegrænsning** til **Nej** i dialogboksen **Grovplanlægning** eller *Finplanlægning*.
1. Vælg **OK** for at planlægge ordren.

Hvis du vil se den tilgængelige kapacitet på ressourcen, skal du følge disse trin.

1. Gå til **Virksomhedsadministration \> Ressourcer \> Ressourcer**, og vælg en ressource, der gælder for den ordre, der ikke kan planlægges.
1. Vælg **kapacitetsbelastning** eller **kapacitetsbelastning grafisk** i gruppen **Visning** under fanen **Ressource** i handlingsruden, og kontroller, at der er tilgængelig kapacitet.

Hvis du vil se den tilgængelige kapacitet på ressourcegruppen, skal du følge disse trin.

1. Gå til **Virksomhedsadministration \> Ressourcer \> Ressourcegrupper**, og vælg en ressourcegruppe, der gælder for den ordre, der ikke kan planlægges.
1. Vælg **kapacitetsbelastning** eller **kapacitetsbelastning grafisk** i gruppen **Visning** under fanen **Ressourcegruppe** i handlingsruden, og kontroller, at der er tilgængelig kapacitet.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Varedisponering reserverer en ressource, når ressourcekalenderen lukkes

Når der anvendes grovplanlægning, planlægger varedisponering kapacitet i overensstemmelse med kalenderen for den primære ressourcegruppe. Den reserverer den sekundære operation samtidig med den primære operation og tager ikke højde for kalenderne eller kapaciteten af den sekundære operation. Det kan resultere i, at produktionsordren planlægges i en lukket kalender eller på et tidspunkt, hvor den sekundære operation ikke er tilgængelig (kalender lukket, ingen kapacitet).

Når der anvendes finplanlægning, tages der i varedisponering højde for både den primære og den sekundære operations kapacitet og kalender ved planlægning af ordren. Hvis ordren skal planlægges, skal kalenderne for ressourcerne i begge operationer være åbne og have ledig kapacitet.

## <a name="maximum-job-lead-time-is-too-short"></a>Maksimale jobgennemløbstid er for kort

Planlægningsprogrammet kan ikke planlægge en ordre, hvis den **maksimale jobgennemløbstid**, der er angivet for lokationen, er mindre end den gennemløbstid, der er angivet for en vare i varens standardordreindstillinger eller disponeringsindstillinger.

Hvis du vil have vist eller redigere indstillingen for **maksimal jobgennemløbstid** for lokationen, skal du gå til **Produktionskontrol \> Konfiguration \> Produktionskontrolparametre** og åbne fanen **Generelt**.

Benyt følgende fremgangsmåde for at vise eller redigere standardindstillingerne for et element.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Find og vælg det relevante produkt på listen.
1. I handlingsruden skal du åbne fanen **Administrer lager** og vælge **Standardordreindstillinger**.
1. Udvid oversigtspanelet **Lager**, og få vist eller rediger indstillingen for **Leveringstid for lager** efter behov.

Benyt følgende fremgangsmåde for at vise eller redigere indstillinger for varedisponering for et element.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Find og vælg det relevante produkt på listen.
1. Åbn fanen **Plan** i handlingsruden, og vælg **Varedisponering**.
1. Åbn fanen **Gennemløbstid**, og få vist eller rediger værdien for **produktionstid** efter behov.

## <a name="excessive-quantity-of-required-resources"></a>For mange påkrævede ressourcer

Under planlægning forsøger programmet at matche den krævede ressourcemængde, der er angivet for en ruteoperation, med de relevante ressourcer i henhold til kravene til operationsressourcen. Hvis ressourceantallet angives for højt, kan det medføre, at en rute ikke kan tildeles, hvilket medfører planlægningsfejl.

Benyt følgende fremgangsmåde for at kontrollere både det angivne antal og de relevante ressourcer for et valgt produkt, en rute og en ruteoperation:

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Find og vælg det relevante produkt på gitteret.
1. Åbn fanen **Opret** i handlingsruden, og vælg **Rute**.
1. Find og vælg det relevante rute i gitteret.
1. Åbn fanen **Oversigt** nederst på siden.
1. Vælg en operation på listen over de valgte ruteoperationer.
1. Vælg **Tilgængelige ressourcer** for at åbne en dialogboks, hvor du kan få vist de relevante ressourcer for den valgte ruteoperation.
1. Åbn fanen **Ressourcebelastning**. I feltet **Antal** vises det ressourceantal, der kræves til den valgte ruteoperation. Få vist og/eller rediger den efter behov.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
