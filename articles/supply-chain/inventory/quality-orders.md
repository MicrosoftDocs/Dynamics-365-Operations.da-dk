---
title: Kvalitetsordrer
description: Dette emne beskriver, hvordan du opretter kvalitetsordrer manuelt eller automatisk, og hvordan du kan arbejde med dem for at udføre inspektioner og registrere testresultater i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c951716a456101ba753e5c567c80deb4ee7e764f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956601"
---
# <a name="quality-orders"></a>Kvalitetsordrer

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du opretter kvalitetsordrer manuelt eller automatisk, og hvordan du kan arbejde med dem for at udføre inspektioner og registrere testresultater i Microsoft Dynamics 365 Supply Chain Management.

## <a name="automatically-created-quality-orders"></a>Automatisk oprettede kvalitetsordrer

Du kan konfigurere systemet, så der automatisk oprettes kvalitetsordrer på baggrund af varestikprøvereglerne. Du kan finde flere oplysninger under [Varestikprøver for kvalitetsstyring](quality-item-sampling.md).

## <a name="manually-create-quality-orders"></a><a name="manual-quality-orders"></a>Oprette kvalitetsordrer manuelt

Benyt denne fremgangsmåde for at oprette en kvalitetsordre manuelt.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Vælg **Ny**.
1. Vælg den lagerreference, som kvalitetsordren skal relateres til, i feltet **Referencetype** i dialogboksen **Kvalitetsordrer**. Du kan finde en beskrivelse af de referencetyper, der kan vælges, i afsnittet [Referencetyper for kvalitetsordre](#ref-types) senere i dette emne.

    > [!NOTE]
    > Det lager, der er knyttet til den valgte reference, skal være tilgængeligt. Hvis der ikke er nogen tilgængelig lagerbeholdning for kombinationen af referencetype, antal og lagerdimensioner, som du vælger, vises en fejlmeddelelse.

1. Benyt en af følgende fremgangsmåder, afhængigt af den værdi du valgte i feltet **Refernecetype**:

    - Hvis du har valgt **Lagerbeholdning**, kræves der ingen yderligere referenceoplysninger.
    - Hvis du har valgt **Salg** eller **Indkøb**, skal du angive følgende oplysninger:

        - **Kontovalg** – Anfør reference til debitor- eller kreditorkontonummeret.
        - **Referencenummer** – Anfør reference til salgsordre- eller indkøbsordrenummeret.
        - **Referenceparti** – Anfør reference til den specifikke salgsordrelinje eller indkøbsordrelinje.

    - Hvis du har valgt **Produktion**, **Karantæne** eller **Ko-produktproduktion**, skal du referere til produktionsordren, batchordren eller karantæneordrenummeret i feltet **Referencenummer**.
    - Hvis du har valgt **Ruteoperation**, skal du angive følgende oplysninger:

        - **Referencenummer** – Anfør reference til produktionsordre- eller batchordrenummeret.
        - **Oper.nr.** – Anfør reference til det specifikke ruteoperationsnummer.
        - **Operation** – Anfør reference til den specifikke ruteoperation.
        - **Ressource** – Anfør reference til den specifikke ressource, der skal bruges sammen med ruteoperationen.

1. Vælg den testgruppe, som skal udføres, i feltet **Testgruppe**.
1. Angiv det antal varer, der skal testes, i feltet **Antal**.
1. I sektionen **Lagerdimensioner** skal du angive eventuelle yderligere lagerdimensioner, der kræves for den valgte vare.
1. Vælg **OK**.

Når der er oprettet en kvalitetsordre, kan du begynde at inspicere lageret og registrere testresultaterne. Du kan finde flere oplysninger om registrering og validering af testresultater i [Inspicere varernes kvalitet](tasks/inspect-quality-goods.md).

## <a name="quality-order-reference-types"></a><a name="ref-types"></a>Referencetyper for kvalitetsordre

Kvalitetsordrer bruges til at spore detaljer om inspektioner og testresultater for specifikt lager på lagerstedet. En kvalitetsordre skal indeholde en reference, der repræsenterer kilden til det lager, der testes. Kvalitetsordrer kan være relateret til følgende referencetyper:

- **Lagerbeholdning** – Denne referencetype angiver, at du inspicerer den disponible lagerbeholdning. Inspektioner af denne type er typisk tilfældige eller ikke planlagte, og gennemføres, når en lagerarbejder identificerer et problem.
- **Salg** – Denne referencetype angiver, at du inspicerer den lagerbeholdning, der er relateret til en bestemt salgsordre. Inspektioner af denne type har typisk relation til kundespecifikationer eller generering af et analysecertifikat (CoA), som skal leveres til en kunde som en del af en forsendelse. (Et CoA kaldes nogle gange også et overensstemmelsescertifikat \[CoC\].)
- **Indkøb** – Denne referencetype angiver, at du inspicerer den lagerbeholdning, der er relateret til en indkøbsordre. Inspektioner af denne type bruges ofte til at inspicere indgående varer, før de sættes på lager eller forbruges i produktionsprocesser.
- **Produktion** – Denne referencetype angiver, at du inspicerer den lagerbeholdning, der er relateret til en produktionsordre. Inspektioner af denne type bruges ofte til at kontrollere færdige varer, før de sættes på lager.
- **Karantæne** – Denne referencetype angiver, at du inspicerer den lagerbeholdning, der er relateret til en karantæneordre. Karantæneordrer er en særlig ordretype, der sporer lageret på et opdelt lagersted eller et opdelt område på lagerstedet. Inspektioner af denne type bruges ofte til at undersøge de varer, en kunde har returneret, eller som er sat i karantæne for at blive analyseret yderligere. Karantæneordrer kan genereres ud fra kvalitetsordrer. Alternativt kan de genereres fra andre kilder, og kvalitetsordrerne kan derefter relateres til karantæneordrerne.
- **Ruteoperation** – Denne referencetype angiver, at du inspicerer den lagerbeholdning, der er relateret til et bestemt trin på ruten for en produktionsordre. Inspektioner af denne type bruges typisk til at analysere IGVA for et produkt, før det går videre til næste trin i produktionsprocessen.
- **Produktion af samprodukter** – Denne referencetype angiver, at du inspicerer den lagerbeholdning, der er relateret til et samprodukt for en produktionsordre. Inspektioner af denne type bruges typisk til at inspicere samproduktet i en batchordre, før samproduktet føjes til lageret.

## <a name="view-and-create-quality-orders-from-various-parts-of-the-system"></a>Få vist og oprette kvalitetsordrer fra forskellige dele af systemet

Kvalitetsordrer kan oprettes manuelt. Alternativt kan de oprettes automatisk ud fra de kvalitetskrav, du definerer. Yderligere oplysninger om, hvordan du opretter og administrerer automatisk oprettelse af kvalitetsordrer, finder du i [Kvalitetstilknytninger](quality-associations.md).

Du kan bruge kvalitetsordresiden til manuelt at oprette en ny kvalitetsordre eller få vist status for en kvalitetsordre, der er relateret til en anden post. Du kan få adgang til kvalitetsordresiden på flere forskellige måder.

### <a name="from-the-quality-orders-page"></a>Fra siden Kvalitetsordrer

Hvis du vil oprette kvalitetsordrer manuelt og have vist alle eksisterende kvalitetsordrer, skal du gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**. De resterende afsnit i dette emne indeholder flere oplysninger om, hvordan du kan arbejde med siden **Kvalitetsordrer**.

### <a name="from-sales-orders"></a>Fras salgsordrer

Hvis du vil arbejde med kvalitetsordrer, der er relateret til salgsordrerne, skal du gå til **Salgs- og marketing \> Salgsordrer \> Alle salgsordrer** og derefter følge et af disse trin:

- Åbn en salgsordre, eller vælg den i gitteret. I handlingsruden under fanen **Pluk og pak** skal du derefter vælge **Kvalitetsordrer** i gruppen **Kvalitetsstyring** for at åbne siden **Kvalitetsordrer**. Her kan du få vist, oprette eller opdatere kvalitetsordrer, der er relateret til salgsordren.
- Åbn en salgsordre, og vælg derefter oversigtspanelet **Generelt** under fanen **Sidehoved**. Feltet **Kvalitetsordrestatus** viser den overordnede status for alle de kvalitetsordrer, der er relateret til salgsordren.
- Åbn en salgsordre, og vælg derefter oversigtspanelet **Salgsordrelinjer** under fanen **Linjer**. Kolonnen **Kvalitetsordrestatus** viser status for hver linje i salgsordren.

### <a name="from-purchase-orders"></a>Fra indkøbsordrer

Hvis du vil arbejde med kvalitetsordrer, der er relateret til indkøbsordrerne, skal du gå til **Indkøb og kilder \> Indkøbsordrer \> Alle indkøbsordrer** og derefter følge et af disse trin:

- Åbn en indkøbsordre, eller vælg den i gitteret. I handlingsruden under fanen **Modtag** skal du derefter vælge **Kvalitetsordrer** i gruppen **Kvalitetsstyring** for at åbne siden **Kvalitetsordrer**. Her kan du få vist, oprette eller opdatere kvalitetsordrer, der er relateret til indkøbsordren.
- Åbn en indkøbsordre, og vælg derefter oversigtspanelet **Generelt** under fanen **Sidehoved**. Feltet **Kvalitetsordrestatus** viser den overordnede status for alle de kvalitetsordrer, der er relateret til indkøbsordren.
- Åbn en indkøbsordre, og vælg derefter oversigtspanelet **Indkøbsordrelinjer** under fanen **Linjer**. Kolonnen **Kvalitetsordrestatus** viser status for hver linje i indkøbsordren.

### <a name="from-production-orders"></a>Fra produktionsordrer

Hvis du vil arbejde med kvalitetsordrer, der er relateret til produktionsordrerne, skal du gå til **Produktionskontrol \> Produktionsordrer \> Alle produktionsordrer** og derefter følge et af disse trin:

- Åbn en produktionsordre, eller vælg den i gitteret. I handlingsruden under fanen **Vis** skal du derefter vælge **Kvalitetsordrer** i gruppen **Kvalitetsstyring** for at åbne siden **Kvalitetsordrer**. Her kan du få vist, oprette eller opdatere kvalitetsordrer, der er relateret til produktionsordren.
- Åbn en produktionsordre, eller vælg den i gitteret. I handlingsruden under fanen **Produktionsordre** skal du derefter vælge **Rute** i gruppen **Produktionsdetaljer** for at åbne siden **Produktionsrute**. Hvis du vil have vist de kvalitetsordrer, der er relateret til en ruteoperation, skal du følge et af disse trin:

    - Vælg målruteoperationen i gitteret. Vælg derefter **Forespørgsler \> Kvalitetsordrer** i handlingsruden.
    - Vælg værdien i feltet **Oper.nr.** for målruteoperationen for at åbne siden med oplysninger om **Produktionsrute**. I oversigtspanelet **Generelt** viser feltet **Kvalitetsordrestatus** status for de kvalitetsordrer, der er relateret til ruteoperationen.

- Åbn en produktionsordre, og vælg oversigtspanelet **Generelt**. Feltet **Kvalitetsordrestatus** viser den overordnede status for alle de kvalitetsordrer, der er relateret til produktionsordren.

### <a name="from-quarantine-orders"></a>Fra karantæneordrer

Hvis du vil arbejde med kvalitetsordrer, der er relateret til karantæneordrerne, skal du gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Karantæneordrer** og derefter følge et af disse trin:

- Gennemse værdierne i kolonnen **Kvalitetsordrestatus**. På denne måde kan du få vist den overordnede status for alle de kvalitetsordrer, der er relateret til hver karantæneordre i gitteret.
- Vælg en karantæneordre i gitteret, og vælg derefter **Kvalitetsordrer** for at vise, oprette eller opdatere kvalitetsordrer, der er relateret til karantæneordren, i handlingsruden.

## <a name="advanced-actions-for-quality-orders"></a>Avancerede handlinger for kvalitetsordrer

Du kan udføre flere handlinger vedrørende kvalitetsordrer for at administrere status, oprette dokumenter og forespørge på flere detaljer.

### <a name="reopen-a-quality-order"></a>Genåbne en kvalitetsordre

Som standard kan du ikke længere redigere eller opdatere en kvalitetsordre, efter at den er valideret, og testene er bestået. I nogle tilfælde kan du dog være nødt til at genåbne en kvalitetsordre, når den er fuldført.

Benyt denne fremgangsmåde for at genåbne en kvalitetsordre.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Åbn den validerede kvalitetsordre, eller vælg den i gitteret.
1. Vælg **Genåbn kvalitetsordre** i handlingsruden.

### <a name="create-a-certificate-of-analysis-for-a-quality-order"></a>Oprette et analysecertifikat for en kvalitetsordre

Et CoA er en rapport, der genereres af en organisations kvalitetssikringsteam. Det validerer, om et produkt opfylder specifikke bestemmelser eller krav. Det kan være, at dine kunder eller lovmyndigheder i dit geopolitiske område, der kræver CoA'er. De kan også være påkrævede i din branche og for den type produkter, du håndterer, køber, producerer eller sælger.

Supply Chain Management giver dig mulighed for at generere et coA fra en kvalitetsordre. Rapporten vil indeholde resultaterne af eventuelle test af kvalitetsordren, hvor indstillingen **Analysecertifikatrapport** er angivet til *Ja*. Denne indstilling kan angives som standard baseret på den test, du definerer på siden **Test**. Du kan dog tilsidesætte indstillingen for specifikke test for en specifik kvalitetsordre.

Benyt denne fremgangsmåde for at generere et CoA for en kvalitetsordre.

1. Gå til **Lagerstyring \> Periodiske opgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Vælg den kvalitetsordre, du vil oprette et CoA for.
1. Vælg **Forespørgsler \> Analysecertifikat** i handlingsruden.
1. Vælg **Ny** på siden **Analysecertifikat** i handlingsruden.
1. Valgfrit: Vælg den kontakt, som certifikatet skal sendes til, i feltet **Kontakt**.
1. Vælg **Udskriv** i handlingsruden.
1. Definer, hvordan rapporten skal udskrives, i dialogboksen **Analysecertifikat**. Vælg derefter **OK**, hvis du vil udskrive rapporten til en printer, skærmen, en fil eller en e-mail.
1. Luk siderne.

### <a name="block-or-unblock-inventory-for-a-quality-order"></a>Blokere eller fjerne blokering af lagerbeholdning for en kvalitetsordre

Når der automatisk genereres en kvalitetsordre fra en kvalitetstilknytning, kan den varestikprøve, der er tildelt kvalitetstilknytningen, konfigureres til at blokere hele lagerbeholdningens antal for den reference, der skal testes. Yderligere oplysninger om varestikprøver finder du i [Varestikprøve for kvalitetsstyring](quality-item-sampling.md).

Hvis du ikke bruger fuld blokering, eller hvis du opretter en kvalitetsordre manuelt, opretter systemet automatisk en lagerblokeringspost for antallet af den vare, der testes på kvalitetsordren. I den post, der oprettes på siden **Lagerblokering**, er feltet **Lagerblokeringstype** angivet til *Kvalitetsordre*.

Hvis du vil have vist og redigere lagerblokering for en kvalitetsordre, der er valgt på siden **Lagerblokering**, skal du vælge **Forespørgsler \> Lagerblokering** i handlingsruden. Du finder flere oplysninger under [Lagerblokering](inventory-blocking.md).

### <a name="inquire-about-the-details-of-a-quality-order"></a>Forespørge om detaljer om en kvalitetsordre

Brug følgende knapper i handlingsruden på siden **Kvalitetsordrer** til at få vist flere oplysninger om eller relateret til en kvalitetsordre:

- **Forespørgsler \> Arbejdsdetaljer** – Åbn en side, hvor du kan få vist lagerstedsarbejde, der er relateret til kvalitetsordren.
- **Forespørgsler \> Uoverensstemmelser** – Åbn en side, hvor du kan få vist eventuelle uoverensstemmelser, der er relateret til kvalitetsordren.
- **Lagerbeholdning** – Kommandoerne i denne menu er fælles på tværs af alle lagertransaktioner. Du kan bruge dem til at få vist eller opdatere detaljer som f.eks. transaktioner, disponibel lagerbeholdning, reservationer og afmærkning.

### <a name="create-cases-related-to-quality-orders"></a>Oprette sager, der er relateret til kvalitetsordrer

Du kan oprette sager, der er relateret til kvalitetsordrer. På denne måde kan du spore detaljer om problemer og arbejde frem mod en løsning. Du kan derefter bruge arbejdsgangsfunktionerne i sagsstyring til at dirigere en sag gennem en foruddefineret virksomhedssproces for at få flere godkendelser eller flere oplysninger om et bestemt problem. Du kan også bruge funktionen til videnartikler til at oprette et vidensbase for løsninger på almindelige problemer.

## <a name="case-management-examples-for-quality-management"></a>Eksempler på sagsstyring for kvalitetsstyring

### <a name="example-1"></a>Eksempel 1

Du arbejder for en produktionsvirksomhed, der skal følge strenge bestemmelser for produktionen af lovregulerede produkter, f.eks. fødevarer. Kvalitetsordrer bruges til at registrere og spore detaljer om varernes kvalitet gennem hele produktionsprocessen. Hvis en kvalitetsordre ikke består bestemte test, kan der være problemer med udstyret. Sager bruges til at følge en virksomhedsproces og eskalere problemet til de rette teknikere, så rodårsagen kan bestemmes. For at gøre det nemmere at følge virksomhedsprocesserne har virksomheden vidensbase om almindelige problemer, der er relateret til kvalitetsordrer og udstyr.

### <a name="example-2"></a>Eksempel 2

Du arbejder for et distributionsvirksomhed, der leverer produkter, der kan tilpasses til forskellige lande og områder. Nogle kunder har strenge specifikationer, der skal opfyldes. Ellers kan det medføre gebyrer, returneringer eller tilbageførsler. Du kan bruge kvalitetsordrer til at spore detaljerne om hver test og resultater, der svarer til kundens behov. Sager bruges til at gennemgå og godkende oplysningerne om CoA'et, før dokumentet genereres og vedhæftes sammen med andre forsendelsespapirer.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Processer for kvalitetsstyring](quality-management-processes.md)
- [Kvalitetstest](quality-tests.md)
- [Kvalitetstestgrupper](quality-test-groups.md)
- [Kvalitetstilknytninger](quality-associations.md)
- [Processer for kvalitetsstyring](quality-management-processes.md)
- [Aktivere styring af kvalitet og uoverensstemmelse](enable-quality-management.md)
- [Kvalitetsstyring for lagerstedsprocesser.](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
