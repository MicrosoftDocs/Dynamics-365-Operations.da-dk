---
title: Modtagelsesoversigt
description: Dette emne indeholder oplysninger om funktionen Modtagelsesoversigt. Siden Modtagelsesoversigt er en del af denne funktion og indeholder en oversigt over alle varer, der forventes at ankomme som indgående varer.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 2bc0cfc3c4689953c867109da4e414d4291515f9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219407"
---
# <a name="arrival-overview"></a>Modtagelsesoversigt

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om funktionen Modtagelsesoversigt. Siden Modtagelsesoversigt er en del af denne funktion og indeholder en oversigt over alle varer, der forventes at ankomme som indgående varer.

Siden **Modtagelsesoversigt** indeholder en oversigt over alle forventede indgående varer. Den viser også modtagelser, der kan initialiseres baseret på oversigten. I dette emne beskrives tilgangsprocessen.

## <a name="business-scenario"></a>Forretningsscenario
Overvej følgende scenario i de indgående processer.

[![Forretningsscenario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Claus, en medarbejder i modtagelsen, vil gerne vide, hvad der skal modtages på den aktuelle dag. På siden **Modtagelsesoversigt** kan Claus få et overblik over aktuelle opgaver og et overslag over antal, omfang, vægt, forskellige ordretyper og osv. Senere ankommer en levering i et af modtagelsesområderne, og Claus modtager en liste over leveringen. Claus kan udføre følgende opgaver på siden **Modtagelsesoversigt**:

-   Identificer den tilsvarende tilgangsordre, og registrer tilgangen som **Igangværende**. De linjer, der kræves til en registrering, oprettes automatisk, og modtagelsen kan overvåges, selvom posteringerne endnu ikke er bogført som **Registreret**.
-   Åbn den relevante reference til modtagelseskladden (dvs. **Varemodtagelse**-kladden eller **Produktionsindlagring**-kladden), og identificere de kladder, der er klar til en opdatering af produktkvittering.

## <a name="arrival-overview-page"></a>Siden Modtagelsesoversigt
Åbn siden **Modtagelsesoversigt** ved at klikke på **Lagerstyring** &gt; **Indgående ordrer** &gt; **Modtagelsesoversigt**. Du kan få vist en liste over ordrer, der forventes at blive modtaget. Oversigten er opdelt i et sidehoved og linjer. Sidehovedoplysningerne er grupperet efter ordretype, forventet modtagelsesdato og leveringsdestination. Når der vælges en sidehovedlinje til modtagelse, vælges alle detaljelinjerne, der vedrører modtagelsesreferencen, på den del af siden, der indeholder linjedetaljer. Når alle relaterede kladdelinjer er bogført, vises disse oplysninger ikke.

### <a name="arrival-overview-profiles"></a>Profiler for oversigt over modtagelse

Siden **Modtagelsesoversigt** indeholder en oversigt over varer, der forventes at ankomme, og den dato, hvor de forventes at ankomme. Som en del af modtagelsesprocessen kan der bruges flere sæt personlige indstillinger. Individuelle brugere kan definere deres personlige indstillinger på siden **Profiler for oversigt over modtagelse**.

### <a name="set-up-item-arrival"></a>Konfigurere varemodtagelse

I eksemplet vil Claus konfigurere en ny computer på et sted, der skal bruges til at modtage færdigvarer, der stammer fra produktion på Sted 1. På siden **Profiler for oversigt over modtagelse** opretter Claus en ny konfiguration, der hedder **Sted 1 produktion** og angiver følgende indstillinger.

1.  I oversigtspanelet **Modtagelsesindstillinger** i feltgruppen **Afgrænsning** skal du angive oplysninger om et dagsinterval og de lagersteder, der skal medtages i oversigten.
2.  I oversigtspanelet **Modtagelsesindstillinger** i feltgruppen **Kladde** skal du angive et tilgangslagersted, et sted og et kladdenavn (varemodtagelse/produktionsindlagring).
3.  I oversigtspanelet **Oplysninger om modtagelsesforespørgsel** i feltgruppen **Sted** skal du i feltet **Begræns til sted** angive et sted for at begrænse visningen i oversigtsområdet.
4.  I oversigtspanelet **Oplysninger om modtagelsesforespørgsel** i feltgruppen **De viste posteringstyper** skal du vælge **Ja** for indstillingen **Produktionsordrer**.
5.  I oversigtspanelet **Oplysninger om modtagelsesforespørgsel** i gruppen **Diverse** skal du vælge **Ja** for indstillingen **Opdater ved opstart**, hvis visningen skal opdateres automatisk ved start. Vælg **Ja** for indstillingen **Opdater ved ændring af afgrænsning**, hvis visningen skal opdateres automatisk, når områdeværdier ændres.

I dette eksempel er feltet **Navn for profil for oversigt over modtagelse** i oversigtspanelet **Modtagelsesindstillinger** på siden **Modtagelsesoversigt** indstillet til **Sted 1 produktion**.

### <a name="prerequisites-for-arrival-journals"></a>Forudsætninger for modtagelseskladder

Hvis du automatisk vil oprette modtagelseskladder fra siden **Modtagelsesoversigt**, skal du definere relevante oplysninger i feltgruppen **Kladde** i oversigtspanelet **Modtagelsesindstillinger**.

-   Du skal angive et kladdenavn for at oprette en kladde.

[![Angivelse af et kladdenavn](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Hvis du angiver værdier i felterne **Lagersted** og **Placering**, anvendes disse værdier på kladdelinjerne. Hvis du ikke angiver værdier, bruges værdierne fra den dimension, der er angivet af lagertransaktionerne.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Varer, der modtages fra én forventet modtagelsesordre

I oversigtspanelet **Tilgange** vælger Claus en linje og klikker derefter på **Start modtagelse**. Alle tilknyttede linjer, der er i det angivne område, og som har et antal at registrere, vælges automatisk. Der genereres en varemodtagelseskladde, der har et match mellem den forventede modtagelsesordre og kladden. Antallet initialiseres automatisk på alle linjer, der oprettes.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Varer, der modtages fra mere end én forventet modtagelsesordre

I oversigtspanelet **Tilgange** vælger Claus flere linjer og klikker derefter på **Start modtagelse**. Der genereres en varemodtagelseskladde, der har et match mellem alle forventede modtagelsesordrer og kladden. Alle linjer oprettes i én overskrift til varemodtagelseskladden, og antallet initialiseres automatisk.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Modtage varer fra én eller flere forventede modtagelsesordrer

#### <a name="view-information"></a>Vis oplysninger

For at få et overblik over forventede tilgange i et datointerval angiver Claus følgende oplysninger i felterne i oversigtspanelet **Modtagelsesindstillinger** på siden **Modtagelsesoversigt** og klikker derefter på **Opdater** for at opdatere visningen:

-   Navn for profil for oversigt over modtagelse: **Forespørgsel**
-   Vis linjer: **Alle**
-   Dage tilbage: (Tom)
-   Dage frem: **0**
-   Lagersteder: **GL, HL**

Claus kan se følgende oplysninger:

-   Alle relaterede modtagelsesordrer for systemdatoen og et ubegrænset antal dage tilbage fra den (**InventTrans.StatusDate**-intervallet) og tilgange til lagersteder GL og HL uanset status.
-   Detaljerede linjeoplysninger for mere end én ordre. Claus kan vælge flere overskriftslinjer i oversigten og derefter klikke på **Vis alle valgte** for at få vist alle de tilsvarende linjedetaljer for alle valgte ordrer.
-   Oplysninger om en bestemt indkøbsordre. For kun at få vist oplysninger, der er knyttet til et bestemt referencenummer i oversigten, kan Claus angive et kontonummer i feltet **Kontonummer** og et ordrenummer i feltet **Referencenummer**.
-   Der er oprettet en oversigt over de registreringsopgaver, der forfalder for de ordrelinjer, der er har en varemodtagelseskladde, men den endnu ikke er blevet bogført. For at få vist disse oplysninger kan Claus vælge **Igangværende** i feltet **Vis linjer**.

### <a name="update-journals"></a>Opdatere kladder

For at registrere en eller flere ordrelinjer, der skal behandles, kan Claus vælge linjerne i oversigtsgitteret eller i linjegitteret og derefter klikke på **Kladder** &gt; **Vis modtagelser fra tilgange**. Varemodtagelsesoverskrifter, der svarer til linjerne, vises. For at opdatere indkøbsordrens produktkvittering med de registrerede varer kan Claus gå ind på varemodtagelseskladdens overskrifter, der er klar til opdatering. For at få adgang til disse varemodtagelseskladders overskrifter, klikker han på **Kladder** &gt; **Kladder, der er klar til produktkvittering**. Alle overskriftslinjer, der er klar til produktkvitteringsopdatering på det angivne lagerstedområde, vises. (De overskriftslinjer, der vises, er ikke relateret til dagsintervallet).

### <a name="start-an-arrival-registration"></a>Starte en modtagelsesregistrering

Ved at vælge flere linjer på siden **Modtagelsesoversigt** kan Claus starte en modtagelse af mere end én tilgangsreference. Når han vælger en linje fra oversigten over tilgange, vælges de tilsvarende linjedetaljer. Hvis der findes et antal til registrering, er knappen **Start modtagelse** tilgængelig. Claus kan bruge to metoder til at starte modtagelsesregistreringen:

-   Han kan filtrere siden, så den kun viser de poster, der opfylder bestemte kriterier, ved i feltet **Leverandørreference** at scanne et referencenummer fra en leverandør, f.eks. stregkoden for en følgeseddel.
-   I oversigtsdelen eller detaljedelen af siden **Modtagelsesoversigt** kan han manuelt vælge eller fravælge poster til modtagelsesregistrering. Derefter, når Claus klikker på **Start modtagelse**, oprettes de valgte poster automatisk i en varemodtagelseskladde. Posterne indeholder linjeoplysningerne, og alle entydige feltoplysninger tildeles.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Opdatere oplysninger om modtagelse og behandle en produktkvittering
Når alle varer er registreret, kan lagerchefen eller indkøbschefen opdaterer varetilgangen med en produktkvittering for at tilføje fysiske omkostninger. Følg disse trin for at opdatere oplysninger om modtagelse og bogføre en produktkvittering.

1.  Klik på **Lagerstyring** &gt; **Indgående ordrer** &gt; **Modtagelsesoversigt**.
2.  På siden **Modtagelsesoversigt** skal du klikke på **Kladder** &gt; **Kladder, der er klar til produktkvittering** for at få vist en liste over kladder, der er klar til produktkvitteringsopdatering.
3.  Vælg de kladder, der skal opdateres, og klik derefter på **Funktioner** &gt; **Produktkvittering**.
4.  På siden **Bogføring** skal du angive produktkvitteringsnummer, hvis det ikke allerede findes på kladden, og derefter klikke på **OK** for at behandle produktkvitteringen.

## <a name="summary"></a>Resume
Siden **Modtagelsesoversigt** kan hjælpe lagerchefen og lagermedarbejdere med at få et overblik over det forventede arbejde, der skal udføres som en del af en indgående proces. Siden kan også bruges til at starte varemodtagelsesprocessen for at sikre, at varerne spores ved den første registrering på lagerstedet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]