---
title: Frigiv til lagerregel
description: Dette emne indeholder oplysninger om funktionen Frigiv til lagerregel, der giver fleksibilitet under frigivelse til lagerstedet. Den tilføjer en konfigurationsindstilling, der bestemmer, om systemet tillader, at delvist reserverede ordrelinjer frigives.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 2fbc292ccf8e1f459bef4d70b8c37b2da8c3dd17
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580018"
---
# <a name="release-to-warehouse-rule"></a>Frigiv til lagerregel

[!include [banner](../includes/banner.md)]

Funktionen *Frigiv til lagerregel* giver fleksibilitet under frigivelse til lagerstedet. Den tilføjer en konfigurationsindstilling for hvert lagersted. Du kan bruge denne indstilling til at angive, om delvist reserverede ordrelinjer kan frigives for det pågældende lagersted. Funktionen arbejder sammen med den avancerede funktionalitet til cross-docking i situationer, hvor en del af et ordrelinjeantal er markeret i forhold til en forsyningskilde, men den resterende del kan behandles på lagerstedet. Derfor kan linjen frigives, så lagerbehandling af det tilgængelige lagerantal kan fortsættes.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Aktivér og initialiser funktionen Frigiv til lagerregel

### <a name="turn-on-the-feature"></a>Slå funktionen til

Før du kan bruge funktionen *Frigiv til lagerregel*, skal den være aktiveret i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Frigiv til lagerregel*

### <a name="initialize-the-feature"></a>Initialisere funktionen

Når funktionen er aktiveret i systemet, skal du initialisere den for at angive reglen til den korrekte starttilstand for alle lagersteder.

- Når det gælder lagersteder, der ikke er aktiveret til lokationsstyring, er reglen som udgangspunkt angivet til **Ikke tilgængelig**.
- Når det gælder lagersteder, der er aktiveret til lokationsstyring, er reglen som udgangspunkt angivet til **Tillad delvis reservation**

Hvis du vil initialisere funktionen og angive frigiv til lagerregel for alle lagersteder, skal du følge disse trin.

1. Gå til **Lagerstedsstyring \> Opsætning \> Parametre til lagerstedsstyring**.
1. Gå til siden **Parametre til lokationsstyring**, og vælg linket for reglen **Initialiser frigivelse til lager** under fanen **Generelt** i sektionen **Firmaoplysninger**. (Hvis dette link ikke vises, er funktionen enten ikke slået til eller er allerede blevet initialiseret)
1. Når du bliver bedt om at bekræfte handlingen, skal du vælge **Ja** for at initialisere funktionen.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Angiv Frigiv til lagerregel for hvert lagersted

Når funktionen er aktiveret og initialiseret, vil alle lagersteder have en oprindelig indstilling som beskrevet i det forrige afsnit. Du kan ændre denne indstilling for individuelle lagersteder ved at følge disse trin.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
1. Vælg det lagersted, der skal konfigureres.
1. Vælg **Rediger** for at sætte siden i redigeringstilstand.
1. I oversigtspanelet **Lager** under sektionen **Reservationer** styrer feltet **Krav til lagerreservation**, om delvis frigivelse af ordrer er tilladt. Vælg en af følgende værdier:

    - **Ikke tilgængelig** – når funktionen først er aktiveret og initialiseret, tildeles denne værdi automatisk til alle lagersteder, der ikke er aktiveret til lokationsstyring. Den kan ikke ændres. Denne værdi er ikke tilgængelig for lagersteder, der er aktiveret til lokationsstyring.
    - **Tillad delvis reservation** – ordrer kan frigives, når et antal er reserveret. Systemet evaluerer, om det ikke-reserverede antal skal markeres til avanceret direkte levering, og markerer det antal, der er nødvendigt. Hvis der ikke er nogen markeringer, opretter systemet kun arbejde for det reserverede antal. Når funktionen først er aktiveret og initialiseret, tildeles denne værdi automatisk til alle lagersteder, der er aktiveret til lokationsstyring. Denne værdi er ikke tilgængelig for lagersteder, der ikke er aktiveret til lokationsstyring.
    - **Kræv fuld reservation** – ordrer kan kun frigives, hvis hele antallet er reserveret. De kan ikke frigives, hvis det samlede antal ikke enten er fysisk reserveret eller planlagt til cross-docking. Denne værdi er ikke tilgængelig for lagersteder, der ikke er aktiveret til lokationsstyring.

1. Vælg **Gem**.

## <a name="scenarios"></a>Scenarier

Dette afsnit indeholder to scenarier, som du kan arbejde med for at finde ud af, hvad funktionen gør, og hvordan du bruger den.

### <a name="make-sample-data-available"></a>Gøre eksempeldata tilgængelige

Hvis du vil arbejde gennem disse scenarier ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret. Derudover skal du vælge den juridiske enhed **USMF**, før du starter.

Du kan også bruge disse scenarier som vejledning til funktionen, når du arbejder i et produktionssystem. Du skal dog i det tilfælde erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Scenarie 1: Kræve fuld frigivelse (ingen planlagt cross-docking)

Dette scenarie viser, hvordan funktionen fungerer for lagersteder, der er angivet til **Kræv fuld reservation**.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
1. I forbindelse med lagersted _62_ skal du angive feltet **Krav til lagerreservation** til **Kræv fuld reservation** som beskrevet i afsnittet [Angiv Frigiv til lagerregel for hvert lagersted](#set-option-warehouse) tidligere i dette emne.
1. Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.
1. Vælg **Ny** for at oprette en ny salgsordre.
1. Angiv følgende værdier i dialogboksen **Opret salgsordre**:

    - Gå til oversigtspanelet **Kunde**, indstil feltet **Kundekonto** til _US-004_.
    - I oversigtspanelet **Generelt** skal du indstille **Lagersted** til _62_.

1. Vælg **OK** for at oprette de nye salgsordrer og lukke dialogboksen.
1. Din nye indkøbsordre åbnes. Den indeholder en tom linje i gitteret i afsnittet **Salgsordrelinjer**. Angiv følgende værdier på denne linje:

    - **Varenummer:** *A0001*
    - **Antal:** *2*

1. Vælg **Tilføj linje** for at tilføje en ny linje, og angiv følgende værdier:

    - **Varenummer:** *A0002*
    - **Antal:** *2*

1. Vælg den første ordrelinje, og vælg derefter **Reservation** i menuen **Lager** over gitteret.
1. På siden **Reservation** skal du vælge **Reserver parti** for at reservere det fulde antal på valgte linje på lagerstedet.
1. Luk siden **Reservation** for at vende tilbage til salgsordren.
1. Undlad at reservere den anden ordrelinje.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.
1. Bemærk, at du får vist følgende fejlmeddelelse: "det fulde antal skal reserveres fysisk." Derfor vil systemet ikke oprette noget arbejde, en forsendelse eller en last for ordren.

    > [!NOTE]
    > Du modtager samme fejlmeddelelse, hvis du reserver den anden linje delvist.

### <a name="scenario-2-allow-partial-release"></a>Scenarie 2: Tillad delvis frigivelse

Dette scenarie viser, hvordan funktionen fungerer for lagersteder, der er angivet til **Tillad delvis frigivelse**.

1. Gå til **Lokationsstyring \> Konfiguration \> Lagersted \> Lagersteder**.
1. I forbindelse med lagersted _62_ skal du angive feltet **Krav til lagerreservation** til **Tillad delvis reservation** som beskrevet i afsnittet [Angiv Frigiv til lagerregel for hvert lagersted](#set-option-warehouse) tidligere i dette emne.
1. Som det var tilfældet i det [forrige scenarie](#scenario1), skal du gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer** og oprette en salgsordre for kundekontoen _US-004_ fra lagerstedet _62_. Tilføj følgende to ordrelinjer:

    - **Linje 1:** Indstil feltet **Varenummer** til _A0001_, feltet **Antal** til _2_ og feltet **Enhed** til _Styk_.
    - **Linje 2:** Indstil feltet **Varenummer** til _A0002_, feltet **Antal** til _2_ og feltet **Enhed** til _Styk_.

1. På samme måde som i det [foregående scenarie](#scenario1) reserveres det fulde antal for ordrelinje 1, men ordrelinje 2 reserveres ikke.
1. Vælg **Frigør til lagersted** under fanen **Lagersted** i handlingsruden.
1. Bemærk, at du ikke får vist en fejlmeddelelse på dette tidspunkt. I stedet for opretter systemet arbejde, forsendelser og laster efter behov og viser resultaterne.
1. Hvis du vil have vist forsendelses-, last- og arbejdsoplysningerne, skal du bruge indstillingerne i menuen **Lager** over gitteret:

    - **Linje 1:** Der findes tre indstillinger: **Forsendelsesoplysninger**, **Lastdetaljer** og **Arbejdsdetaljer**. Vælg hver indstilling for at få vist detaljer om forsendelsen, lasten og arbejdet, der blev oprettet, da ordren blev frigivet til lagerstedet.
    - **Linje 2:** Kun indstillingen **Arbejdsdetaljer** er tilgængelig. Markér den, og bemærk, at der ikke er oprettet noget arbejde, da der ikke er reserveret en lagerbeholdning. Derfor blev der ikke oprettet en forsendelse eller en last.

> [!NOTE]
> Det samme resultat forventes, når den anden linje er delvist reserveret. I dette tilfælde oprettes der arbejde for det reserverede linjeantal, men ikke for det ikke-reserverede antal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]