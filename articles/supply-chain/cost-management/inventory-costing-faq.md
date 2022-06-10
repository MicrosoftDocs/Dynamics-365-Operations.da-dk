---
title: Ofte stillede spørgsmål om lagerefterkalkulation
description: Dette emne besvarer nogle ofte stillede spørgsmål om lagerefterkalkulation i Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 05/03/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-03
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45f65bd4a5cfb9bd0c4eb03ceb56eca452f6ec95
ms.sourcegitcommit: cbe9493d479f96f271d94599ec1b85131b26169f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809283"
---
# <a name="inventory-costing-faq"></a>Ofte stillede spørgsmål om lagerefterkalkulation

[!include [banner](../includes/banner.md)]

Dette emne besvarer nogle ofte stillede spørgsmål om lagerefterkalkulation i Microsoft Dynamics 365 Supply Chain Management.

## <a name="inventory-close-adjustments-and-recalculation"></a>Lagerlukning, reguleringer og genberegning

### <a name="is-the-inventory-close-required"></a>Er lagerlukningen påkrævet?

Hvis du planlægger at bruge lagerarkiveringsfunktionen, skal der bruges lagerlukning. Hvis du ikke planlægger at bruge lagerarkiveringsfunktionen, anbefales det på det kraftigste, at du stadig kører lagerlukningen, uanset hvilke efterkalkulationsmodeller du bruger.

### <a name="how-often-should-the-inventory-close-be-run"></a>Hvor ofte skal lagerlukningen køres?

Lagerlukningen skal køres mindst én gang pr. finansperiode. Hvis finansbogholderiet f.eks. er angivet til en kalendermånedsbaseret regnskabskalender, skal du køre lagerlukningen én gang om måneden.

### <a name="is-the-inventory-recalculation-required"></a>Er genberegning af lager påkrævet?

Nej, genberegning af lager er ikke påkrævet. Hvis du bruger en periodisk efterkalkulationsmodel, f.eks. FIFO (First In, First Out), LIFO (Last in, First out) eller vægtet gennemsnit, skal du nøje overveje, om du vil køre lagergenberegningen. Den kan give en mere præcis efterkalkulation i de heuristikmodeller, du har valgt.

### <a name="how-often-should-the-inventory-recalculation-be-run"></a>Hvor ofte skal genberegning af lager køres?

Hvis du planlægger at køre lagergenberegningen, anbefales det, at du overvejer at køre den hver dag som en batchproces. Hvis organisationen ikke kræver hyppige rapporter om lagerværdierne for periodiske efterkalkulationsmodeller, kan du overveje at køre lagerberegningen med længere mellemrum.

### <a name="when-should-i-use-the-on-hand-inventory-adjustment-on-the-closing-and-adjustments-page"></a>Hvornår skal jeg bruge reguleringen af den lagerbeholdning, der er på siden Lukning og Regulering?

Regulering af den disponible lagerbeholdning kan kun køres, når en lagerlukning er fuldført. Den køres typisk for datoen efter den sidste lukning. Reguleringen af beholdningen kan kun regulere den lagerbeholdning, der stadig er disponibel på den dato, hvor reguleringen køres.

### <a name="when-should-i-use-the-inventory-transaction-adjustment-on-the-closing-and-adjustments-page"></a>Hvornår skal jeg bruge reguleringen af lagertransaktion på siden Lukning og regulering?

Du skal bruge lagertransaktionsreguleringen, før du kører en lagerlukning. Den bruges typisk til at rette en forkert tilgang. Du kan ikke bogføre lagertransaktionsreguleringen, efter at der er kørt en lagerlukning, og transaktionen er udlignet.

### <a name="are-purchase-order-returns-treated-like-other-issues-during-the-inventory-close"></a>Behandles indkøbsordrereturneringer ligesom andre afgange i forbindelse med lagerlukningen?

Ja. En indkøbsordretilgang er en afgang, der udlignes med en tilgang i den heuristiske model, som du vælger for varen. Hvis du bruger en periodisk efterkalkulationsmodel, kan du bruge afmærkning til at tilsidesætte den heuristiske kostpris.

### <a name="what-happens-to-sales-order-returns-during-the-inventory-close"></a>Hvad sker der med salgsordrereturneringer under lagerlukningen?

Når du kører lagerlukningen, behandles en salgsordrereturnering som en tilgang til lageret. Afgange udlignes i forhold til lageret på basis af den heuristikmodel, du vælger for varen.

### <a name="what-cost-price-is-used-on-a-sales-order-return"></a>Hvilken kostpris bruges på en salgsordrereturnering?

Når du opretter en returnering, der er relateret til en salgsordre, kopieres værdien i feltet **Enhedspris** fra den oprindelige salgsordre, og feltet **Returkostpris** på returneringen angives til den regulerede kostpris fra den oprindelige lagertransaktion for den salgsordrelinje, der returneres. Hvis indstillingen **Værdi åben** for den relaterede lagertransaktion er angivet til *Ja*, kan lagerlukningen forårsage opdateringer af afgangsomkostningen på den oprindelige salgsordre. Feltet **Returkostpris** er ikke opdateret i dette scenario. Når du bogfører en følgeseddel til en returordre, kontrollerer systemet kostprisen og bruger den opdaterede kostpris på returlagertransaktionen.

Ved returnering af en standardkostvare, der er knyttet til en salgsordre, vil systemet bruge standardomkostningen fra tidspunktet for den oprindelige salgsordre, selvom der er en ny standardomkostning aktiv for varen.

Når du opretter en returnering, der ikke er knyttet til en salgsordre, angives feltet **Returkostpris** til den aktive varepris, som du har for varen på den lokation, du opretter returordren for. Hvis der ikke findes en aktiv kostpris i en efterkalkulationsversion for varen, er værdien 0 (nul). Hvis du lader værdien være 0 (nul), modtager du en advarsel, der viser, at retur parti-id'et eller returkostprisen ikke er angivet.

### <a name="what-is-the-expected-performance-of-the-inventory-close"></a>Hvad er den forventede ydeevne af lagerlukningen?

Mange faktorer kan påvirke lagerlukningens ydeevne. Disse faktorer omfatter det samlede antal varer, det samlede antal transaktioner i perioden, de lagermodeller, du bruger, og antallet af batchhjælpeenheder, du konfigurerer i parametrene for lager- og lokationsstyring. Du kan forvente, at lukningen kan tage så lidt som et par minutter eller så meget som flere timer. Der findes ingen specifik vejledning om, hvor lang tid det bør tage at køre lukningen. Du skal definere de ikke-funktionsmæssige forretningskrav for lagerlukningens ydeevne og arbejde tæt sammen med partneren for at definere planen for kørsel af lagerlukningsprocessen. Hvis du oplever en uventet lav ydeevne i lagerlukningsprocessen, skal du åbne en supportanmodning.

## <a name="costing-sheet-and-indirect-costs"></a>Kostprisark og indirekte omkostninger

### <a name="which-costing-models-support-the-costing-sheet"></a>Hvilke efterkalkulationsmodeller understøtter kostprisarket?

Selvom kostprisarket typisk bruges i organisationer, der bruger standardefterkalkulation, kan du bruge det med en hvilken som helst efterkalkulationsmodel, der findes i Supply Chain Management.

### <a name="can-i-have-multiple-costing-sheets-for-various-parts-of-my-organization"></a>Kan jeg have flere kostprisark til forskellige dele af organisationen?

Nej Der kan kun være ét kostprisark pr. juridiske enhed.

### <a name="can-i-have-different-costing-sheets-for-each-site"></a>Kan jeg have forskellige kostprisark for hver lokation?

Nej du kan ikke have særskilt kostprisark for hver lokation. Der kan kun oprette ét kostprisark pr. juridiske enhed. Du kan dog konfigurere totalnoder, omkostningsgrupper eller indirekte omkostningsnoder pr. lokation. Denne konfiguration er en manuel proces, og du skal vedligeholde hierarkiet og varetildelingerne i kostprisarket, når der sker organisatoriske eller driftsmæssige ændringer. Hvis en enkelt vare produceres eller købes på mere end én lokation, findes der ingen mekanisme, der giver dig mulighed for at behandle varen anderledes på kostprisarket for hver lokation. Bemærk desuden, at alle indirekte omkostningskoder har en sats eller en tillægsafgift, der er defineret i efterkalkulationsversionen. De omkostninger, du definerer, er altid lokationsspecifikke.

### <a name="can-i-deactivate-and-activate-versions-of-the-costing-sheet"></a>Kan jeg deaktivere og aktivere versioner af kostprisarket?

Selvom der ikke findes en detaljeret versionshistorik for kostprisarket, kan du foretage ændringer i kostprisarket og derefter gemme og validere det, når du er klar. Der findes ingen mekanisme, der giver dig mulighed for at gå tilbage til en ældre version af kostprisarket eller få vist de ændringer, der er foretaget i efterkalkulationsarket. Hvis du starter ændringerne og ikke ønsker, at de skal træder i kraft, kan du lukke siden uden at gemme og validere ændringerne. Du bliver bedt om at kassere ændringerne.

### <a name="can-i-create-indirect-costs-for-each-item"></a>Kan jeg oprette indirekte omkostninger for hver vare?

I kostprisarket kan du oprette indirekte omkostningskoder, hvor feltet **Nodetype** er angivet til *Tillæg*, *Sats* eller *Baseret på outputenhed*. Du kan derefter definere satsen eller tillægget, så det er specifikt for et varenummer. Føj en række til gitteret i oversigtspanelet **Sats** eller **Tillæg**. Angiv feltet **Gyldig for** til *Tabel* og **Relation**-feltet til det specifikke varenummer.

### <a name="can-i-create-an-indirect-cost-that-isnt-related-to-a-specific-item"></a>Kan jeg oprette en indirekte omkostning, der ikke er relateret til en bestemt vare?

Ja. Du kan oprette en kode for indirekte omkostninger, hvor feltet **Nodetype** er angivet til *Baseret på outputenhed*. Du kan derefter indstille feltet **Undertype** til *Antal*, *Vægt* eller *Mængde* for at angive antallet, vægten eller volumen af den vare, du producerer. Den sats, du angiver i oversigtspanelet **Sats**, anvendes på den valgte undertype. Du angiver f.eks. feltet **Undertype** til *Antal* og **Sats**-feltet til *1,00 USD* og opretter derefter en produktions- eller batchordre for et antal på 10. I dette tilfælde vil den indirekte omkostning, der føjes til færdigvaren, blive 10,00 USD.

### <a name="can-i-use-the-costing-sheet-to-split-my-production-costs-by-hours-and-materials"></a>Kan jeg bruge kostprisarket til at opdele produktionsomkostningerne efter timer og materialer?

Ja. Du kan oprette **Total**-noder på kostprisarket for at adskille omkostningerne efter enhver gruppering, du vælger. Du kan f.eks. oprette en **Total**-node, der hedder *Timer*, og en anden med navnet *Materialer*. Under noden **Timer** skal du tilføje hver kodegruppe, der er relateret til dine timer. Under noden **Materialer** skal du tilføje hver kostgruppe, der er relateret til dine materialer.

## <a name="dimension-groups"></a>Dimensionsgrupper

### <a name="can-i-manage-cost-at-the-batch-or-serial-number-level"></a>Kan jeg administrere omkostninger på batch- eller serienummerniveau?

Ja, hvis du bruger en periodisk efterkalkulationsmodel, f.eks. FIFO, LIFO, LIFO-dato, vægtet gennemsnit eller vægtet gennemsnitsdato, kan du aktivere **Økonomisk lager**-indstilling for dimensionen **Batch** eller **Serienummer** i sporingsdimensionsgruppen for at spore omkostninger på et detaljeret niveau.

### <a name="can-i-manage-costs-at-the-location-level"></a>Kan jeg administrere omkostninger på lokationsniveau?

Nej, du kan ikke aktivere indstillingen **Økonomisk lager** for dimensionen **Lokation** i lagringsdimensionsgruppen. Hvis organisationen skal spore omkostninger på et mere detaljeret niveau, skal du overveje, om du kan oprette virtuelle lagersteder, og derefter vælge indstillingen **Økonomisk lager** dimensionen **Lagersted** i lagringsdimensionsgruppen.

### <a name="should-i-enable-the-use-warehouse-management-processes-option-for-the-storage-dimension-group"></a>Bør jeg aktivere indstillingen Brug lokationsstyringsprocesser for lagringsdimensionsgruppen?

Hvis du mener, at du vil bruge funktionerne til avanceret lokationsstyring i fremtiden, skal du aktivere indstillingen **Brug lokationsstyringsprocesser**. Når du har gemt en lagringsdimensionsgruppe, kan du ikke længere ændre indstillingen af **Brug lokationsstyringsprocesser** for den. Hvis du beslutter dig for at bruge lokationsstyringsprocesser senere, skal du oprette et nyt lagersted, hvor indstillingen er aktiveret. Der findes ingen automatiske processer, som du kan bruge til at flytte hele lageret fra et lagersted til et andet eller til at kopiere relaterede konfigurationer til et nyt lagersted.

### <a name="can-i-enable-the-use-warehouse-management-processes-for-the-storage-dimension-group-even-if-im-not-planning-to-use-advanced-warehousing"></a>Kan jeg aktivere Brug lokationsstyringsprocesser for lagringsdimensionsgruppen, selvom jeg ikke planlægger at bruge avancerede lagersteder?

Ja, selvom du ikke har planer om at bruge funktionerne til avanceret lokationsstyring, kan du aktivere indstillingen **Brug lokationsstyringsprocesser** for lagringsdimensionsgruppen. Hvis du vil oprette og behandle transaktioner, skal du udføre minimumkonfigurationen som f.eks. reservationshierarkier og enhedsseriegrupper. Indstillingerne for avanceret lagersted ignoreres dog generelt, når du behandler pluklister, følgesedler og produktkvittering manuelt (f.eks. på salgsordre- og indkøbsordresider).

### <a name="when-should-i-enable-the-physical-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Hvornår skal jeg aktivere indstillingen Fysisk lager for en lager- eller sporingsdimensionsgruppe?

Du skal aktivere indstillingen **Fysisk lager** for lagrings- og sporingsdimensionsgrupper, når du skal beholde detaljerede lagerposter på baggrund af denne dimension. Normalt spores alle aktive dimensioner også fysisk. Derfor spores eventuelle tilgange, afgange eller bevægelser i lageret af den valgte dimension. Hvis en dimension ikke er obligatorisk (f.eks. nummerplade), kan du aktivere indstillingen **Blank tilgang tilladt**, og **Blank afgang tilladt** for at give brugerne mulighed for at modtage, afsende eller flytte lager, også selvom dimensionen ikke er angivet.

### <a name="when-should-i-enable-the-financial-inventory-option-for-a-storage-or-tracking-dimension-group"></a>Hvornår skal jeg aktivere indstillingen Økonomisk lager for en lager- eller sporingsdimensionsgruppe?

Du skal aktivere indstillingen **Økonomisk lager** for lagrings- og sporingsdimensionsgrupper, når du skal beholde detaljerede økonomiske poster på baggrund af denne dimension. **Lokation**-dimensionerne spores altid økonomisk, mens andre dimensioner er valgfrie ved økonomisk sporing. Hvis du bruger en periodisk efterkalkulationsmodel, f.eks. FIFO, LIFO eller vægtet gennemsnit, angiver aktivering af indstillingen **Økonomisk lager** for en dimension, at du kun foretager udligninger i tilfælde, hvor tilgangen og afgangen har de samme dimensionsværdier. Hvis du f.eks. aktiverer indstillingen **Økonomisk lager** for dimensionen **Lagersted**, vil du have forskellige omkostninger på hvert lagersted, og tilgange og tilgange fra forskellige lagersteder kan ikke udlignes.

### <a name="can-i-make-changes-to-a-product-storage-or-tracking-dimension-group-after-transactions-exist"></a>Kan jeg foretage ændringer i en produkt-, lagrings- eller sporingsdimensionsgruppe, når der findes transaktioner?

Når du har oprettet en varemodelgruppe, kan du ændre indstillingen af **Disponer pr. dimension**, **For indkøbspriser** og **For salgsprisfelter**, hvis afkrydsningsfeltet **Aktiv** er markeret for en dimension i varemodelgruppen. Ingen andre ændringer er tilladt. Du kan f.eks. ikke aktivere eller deaktivere indstillingerne **Aktiv**, **Blank afgang tilladt**, **Blank tilgang tilladt**, **Fysisk lager** og **Økonomisk lager**.

### <a name="can-i-change-the-product-storage-or-tracking-dimension-group-for-a-released-product"></a>Kan jeg ændre produkt-, lagrings- eller sporingsdimensionsgruppen for et frigivet produkt?

Hvis den disponible lagerbeholdning for et produkt er 0 (nul), og indstillingen **Åben værdi** er angivet til *Nej* for alle lagertransaktioner, kan du ændre lager- og sporingsdimensionsgrupperne på den frigivne produktionsside. Du kan ikke ændre produktdimensionsgruppen, når posten er oprettet.

## <a name="item-model-groups"></a>Varemodelgrupper

### <a name="when-should-i-enable-the-stocked-product-option"></a>Hvornår skal jeg aktivere indstillingen Lagerført produkt?

Du skal aktivere indstillingen **Lagerført produkt** for enhver vare, der skal spores på lageret. Når denne indstilling er aktiveret, bevares de detaljerede lagertransaktioner, der sporer varens tilgang og afgang. Denne indstilling er typisk aktiveret for alle materielle varer, du f.eks. opbevarer på lagerstedet. Du skal også aktivere denne indstilling, hvis du planlægger at føje en ikke-materiel vare, f.eks. en servicevare, til styklister eller formler. Hvis du ikke aktiverer indstillingen **Lagerført vare**, spores der ingen lagertransaktioner i lagerreskontroen, og varernes kostpris udgiftsføres typisk i finansmodulet. Denne indstilling bruges ofte, f.eks. til butiksartikler eller ydelser, der ikke findes på dine styklister eller formler.

### <a name="when-should-i-enable-the-post-physical-inventory-option"></a>Hvornår skal jeg aktivere indstillingen Bogfør fysisk lager?

Indstillingen **Bogfør fysisk lager** er typisk aktiveret, når indstillingen **Lagerført produkt** er aktiveret. Når du aktiverer denne indstilling, sporer systemet den fysiske opdatering af varen i lagertransaktionen. Denne indstilling bruges sammen med parametre i Kreditor, Debitor og Produktionsstyring, der angiver, at den fysiske opdatering skal oprette et bilag. Du vil normalt aktivere denne indstilling, når du ønsker, at finansbogholderiet skal opdateres, når du fysisk opdaterer lageret. Hvis Supply Chain Management ikke er dit system til finansposter, kan du vælge at deaktivere denne indstilling.

### <a name="when-should-i-enable-the-post-financial-inventory-option"></a>Hvornår skal jeg aktivere indstillingen Økonomisk lager?

Indstillingen **Bogfør økonomisk lager** er typisk aktiveret, når indstillingen **Lagerført produkt** er aktiveret. Denne indstilling bruges sammen med parametre i Kreditor, Debitor og Produktionsstyring, der angiver, at den økonomiske opdatering skal oprette et bilag. Du vil typisk aktivere denne indstilling, når du vil opdatere Finans, hver gang du opdaterer lageret økonomisk (f.eks. ved at fakturere salgsordrer og indkøbsordrer eller afslutte en produktionsordre). Hvis Supply Chain Management ikke er dit system til finansposter, kan du vælge at deaktivere denne indstilling.

### <a name="when-should-i-enable-the-post-to-deferred-revenue-account-on-sales-delivery-option"></a>Hvornår skal jeg aktivere indstillingen Bogfør på konto til udskudt indtægt ved salgslevering?

Du kan bruge indstillingen **Bogfør på konto til udskudt indtægt ved salgslevering** til at angive, om du vil anerkende omsætningen i Finans, når du bogfører en følgeseddel for en salgsordre. Denne indstilling bruges som regel, når der er lang forsinkelse mellem følgesedlen og fakturaen på en salgsordre, eller når det ikke er muligt at fakturere alle salgsordrer i perioden. Du vil typisk deaktivere denne indstilling, hvis du bogfører salgsordrefakturaerne, umiddelbart efter at du har bogført følgesedlen. På denne måde undgår du at generere ekstra finansposteringer, der straks tilbageføres, når du fakturerer en salgsordre.

### <a name="when-should-i-enable-the-accrue-liability-on-product-receipt-option"></a>Hvornår skal jeg aktivere indstillingen Periodiser passiver ved produktmodtagelse?

I de fleste organisationer vil du aktivere indstillingen **Periodiser passiver ved produktmodtagelse** for alle varemodelgrupper, uanset om du har et lagerført produkt eller et produkt, der ikke er lagerført. Denne indstilling bruges til at bogføre en periodisering i finansmodulet baseret på produkttilgangsprisen. Da der typisk opstår en forsinkelse mellem bogføringen af produktkvitteringen for en indkøbsordre og bogføringen af fakturaen, skal de fleste organisationer anerkende passivet på balancen for at overholde de lokale regler, f.eks. almindeligt accepteret regnskabspraksis (GAAP). Hvis Supply Chain Management ikke er dit system til finansposter, kan du vælge at deaktivere denne indstilling. Hvis der bruges indkøbskategorier på indkøbsordrer i din organisation, kan du styre periodiseringskravet ved at aktivere indstillingen **Periodiser købsudgift ved tilgang** for kategoripolitikreglen på siden **Indkøbspolitikker**.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-product-receipt-if-a-receipt-registration-isnt-yet-posted"></a>Hvordan kan jeg forhindre en bruger i at bogføre en produkttilgang for en indkøbsordre, hvis der endnu ikke er bogført en tilgangsregistrering?

Du kan forhindre en bruger i at bogføre en produkttilgang for en indkøbsordre, hvis der endnu ikke er foretaget en registrering af en indkøbsordre, ved at aktivere indstillingen **Registreringskrav** for varemodelgruppen. Denne indstilling bruges typisk i organisationer, der bruger en tilgangsproces i to trin, eller i scenarier, hvor du skal registrere et batch- eller serienummer, f.eks. på de varer, du modtager. Indstillingen **Registreringskrav** gælder for *alle* lagertilgange for en vare, ikke kun for indkøbsordrer. Den gælder f.eks. for en lagerkladde, der har et positivt antal, og en færdigmeldingskladde for en produktionsordre.

### <a name="how-can-i-prevent-a-user-from-posting-a-purchase-order-invoice-if-a-product-receipt-isnt-yet-posted"></a>Hvordan kan jeg forhindre en bruger i at bogføre en faktura for en indkøbsordre, hvis der endnu ikke er bogført en produkttilgang?

Du kan forhindre en bruger i at bogføre en produktfaktura for en indkøbsordre, hvis der endnu ikke er sket en produkttilgang for en indkøbsordre, ved at aktivere indstillingen **Tilgangskrav** for varemodelgruppen. Denne indstilling bruges typisk i organisationer, hvor det kræves, at tilgange registreres fysisk i finansmodulet for periodiseringer. Indstillingen **Tilgangskrav** gælder for *alle* lagertilgange for en vare, ikke kun for indkøbsordrer. Den gælder f.eks. for en lagerkladde, der har et positivt antal, og en færdigmeldingskladde for en produktionsordre. Hvis din organisation bruger indkøbskategorier på indkøbsordrer, kan du styre tilgangskravet ved at aktivere indstillingen **Tilgangskrav** for kategoripolitikreglen på siden **Indkøbspolitikker**.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-packing-slip-if-a-sales-order-picking-list-isnt-yet-posted"></a>Hvordan kan jeg forhindre en bruger i at bogføre en salgsordres følgeseddel, hvis der endnu ikke er bogført en plukliste for en salgsordre?

Du kan forhindre en bruger i at bogføre en salgsordrefølgeseddel eller faktura, hvis der endnu ikke er en salgsordreplukliste, ved at aktivere indstillingen **Plukkrav** for varemodelgruppen. Denne indstilling bruges typisk i organisationer, der udfører en fysisk plukproces på lagerstedet (f.eks. ved hjælp af den mobile lagerstedsenhed til plukning). Indstillingen **Plukkrav** gælder for *alle* lagerafgange for en vare, ikke kun for salgsordrer. Den gælder f.eks. for en lagerkladde, der har et negativt antal, og en pluklistekladde for en produktionsordre.

### <a name="how-can-i-prevent-a-user-from-posting-a-sales-order-invoice-if-the-sales-order-packing-slip-isnt-yet-posted"></a>Hvordan kan jeg forhindre en bruger i at bogføre en salgsordres faktura, hvis der endnu ikke er bogført en følgeseddel for salgsordren?

Du kan forhindre en bruger i at bogføre en salgsordrefaktura, hvis der endnu ikke er en salgsordrefølgeseddel, ved at aktivere indstillingen **Fradragskrav** for varemodelgruppen. Denne indstilling bruges typisk i organisationer, der udfører en fysisk emballeringsproces på lagerstedet (f.eks. ved hjælp af mobilappen Warehouse Management til at pakke eller ved at generere et dokument, der skal inkluderes i de varer, der afsendes). Indstillingen **Fradragskrav** gælder for *alle* lagerafgange for en vare, ikke kun for salgsordrer. Den gælder f.eks. for en lagerkladde, der har et negativt antal, og en pluklistekladde for en produktionsordre.

### <a name="can-i-prevent-items-that-are-registered-from-being-sold"></a>Kan jeg forhindre, at varer, der er registreret, bliver solgt?

Når en vare registreres på lageret i Supply Chain Management, er antallet fysisk tilgængeligt til at blive afgivet i systemet. Hvis varer, der er registreret, men endnu ikke modtaget, *ikke* bør være tilgængelige for udstedelse til salgsordrer eller produktionsordrer, bør du f.eks. overveje at bruge lagerstatus, lagerblokering, kvalitetsordrer, karantæneordrer eller reservationsfunktioner til at administrere forretningsprocessen.

## <a name="production-costing"></a>Efterkalkulation af produktion

### <a name="can-i-use-one-costing-model-for-raw-materials-and-a-different-costing-model-for-finished-goods"></a>Kan jeg bruge én efterkalkulationsmodel til råmaterialer og en anden efterkalkulationsmodel for færdigvarer?

Ja, du kan bruge forskellige efterkalkulationsmodeller til hver vare. Det er ikke ualmindeligt, at producenter bruger en periodisk kostprismodel til råmaterialer og standardomkostninger for halvfabrikata og færdigvarer.

### <a name="how-can-i-drive-overhead-off-machine-costs"></a>Hvordan kan jeg køre faste omkostninger fra maskinomkostninger?

Hvis du vil køre faste omkostninger fra maskinomkostningerne, skal du oprette ressourcer og ressourcegrupper for de enkelte maskiner i overensstemmelse med virksomhedsbehovet. Hver ressource eller ressourcegruppe kan tildeles til omkostningskategorier for at styre omkostningerne for maskinen. Hver omkostningsart kan knyttes til en kostprisgruppe, og de enkelte omkostningsgrupper kan bruges som grundlag for beregning af indirekte omkostninger i kostprisarket.

### <a name="how-do-i-recognize-cost-that-is-related-to-energy-consumption-for-example-water-energy-or-gas-consumption-on-the-costing-sheet"></a>Hvordan kan jeg registrere omkostninger, der er relateret til forbrug af energi (f.eks. vand- eller gasforbrug) på kostprisarket?

Du kan generelt registrere omkostninger, der er relateret til forbrug af energi, på en af to måder:

- Opret en linje i styklisten eller formlen. Normalt oprettes denne linje som en servicevare, og du kan angive den måleenhed, du forbruger, i forhold til det antal, du producerer. På denne måde kan brugeren forbruge en anden mængde under produktionsprocessen. Du kan automatisk forbruge varerne ud fra den værdi, du vælger i feltet **Varetrækprincip**.
- Opret en indirekte omkostning på kostprisarket. Denne metode bruges typisk til at fordele de samlede omkostninger for dit forbrug af energi på tværs af produktionsprocessen. Du kan f.eks. bruge kostprisgruppen og overtagelsesgrundlaget til at skalere forbruget baseret på materialer eller arbejdskraft i ruten.

Du skal vælge den bedste mulighed baseret på rapportering, afstemning og driftsmæssige behov.

### <a name="can-i-capture-resource-details-in-the-bom-or-formula"></a>Kan jeg indlæse ressourceoplysninger i styklisten eller formlen?

Ressourcedetaljer kan kun registreres i en ruteoperation. Selvom du kan oprette en servicevare, der repræsenterer en ressource, og tildele en omkostning for at øge omkostningsberegningen for en færdigvare, anbefales det normalt ikke at bruge denne fremgangsmåde. I stedet anbefales det, at du opretter en simpel rute med én linje til sporing af ressourceomkostningerne og konfiguration af operationen, så den forbruges automatisk i starten eller slutningen af produktionsordren.

### <a name="can-i-view-the-calculation-details-if-the-cost-is-manually-entered"></a>Kan jeg se kalkulationsdetaljerne, hvis omkostningen angives manuelt?

Nej Hvis du angiver prisen manuelt på **Varepris**-siden, er knapperne **Vis beregningsoplysninger** og **Oplysninger om rapportberegning** ikke tilgængelige. Hvis du vælger knappen **Omkostningstotaler pr. kostgruppe** for en kostpris, der angives manuelt, vises en opsummeret linje, og alle omkostninger opsummeres for færdigvaren.

### <a name="does-the-system-calculate-variances-on-a-production-order-when-i-manually-enter-the-cost"></a>Beregner systemet afvigelser i en produktionsordre, når jeg angiver omkostningen manuelt?

Ja, systemet beregner afvigelser, når du manuelt angiver en standardomkostning. Men når du angiver en standardomkostning manuelt i stedet for at beregne den, betragtes alle materialer, ruter og indirekte omkostningsforbrug i produktionsordren som en produktionserstatning. Hvis der er flere afvigelser, f.eks. forbrug af ekstra materialer eller arbejdskraft, vil de også blive registreret som afvigelser fra produktionsstyklisten. Det anbefales derfor, at du altid kører en beregning for varer med en stykliste, en rute eller indirekte omkostninger.

### <a name="how-can-i-carry-the-variances-from-a-subproduction-order-to-the-parent-production-order"></a>Hvordan kan jeg føre afvigelserne fra en underproduktionsordre til den overordnede produktionsordre?

Når du bruger en periodisk efterkalkulationsmodel som f.eks. FIFO, LIFO eller vægtet gennemsnit, genkendes omkostningerne fra en underproduktion i den heuristiske model, du har valgt for varerne. Hvis du kræver faktisk efterkalkulation, skal du overveje at bruge afmærkningsprincippet til at angive, hvilken underproduktion der udstedes til en overordnet produktionsordre. Du kan også overveje at bruge indstillingen **Økonomisk lager** for **Batch**- eller **Serienummer**-dimensionen i sporingsdimensionsgruppen, f.eks.

### <a name="how-does-the-flushing-principle-affect-consumption"></a>Hvordan påvirker varetrækprincippet forbruget?

Varetrækprincippet på en stykliste, formel eller rutelinje styrer timingen og teknikken, der bruges til at forbruge varen eller arbejdet. Hvis du vælger *Start*, forbruges varen eller arbejdet automatisk, når du starter produktionsordren. Hvis du vælger *Afslut*, forbruges varen eller arbejdet automatisk, når du færdigmelder produktionsordren. Hvis du vælger *Manuel*, skal en bruger plukke materialer manuelt eller registrere tiden i en job- eller rutekortkladde. Styklister og formler har også indstillingen *Disponibel på lokation*. Hvis du vælger denne indstilling, forbruges varerne automatisk, når de overføres til produktionslokationen.

### <a name="how-should-i-run-cost-calculations-if-i-have-multi-level-boms-or-formulas"></a>Hvordan skal jeg køre omkostningsberegninger, hvis jeg har styklister eller formler på flere niveauer?

Generelt anbefales det, at du starter på det laveste niveau for dine styklister eller formler til beregningen. Du kan gøre filtrering nemmere, når du udfører massekørslen af omkostningsberegninger, ved at bruge beregningsgrupper som en hjælp til opdeling af produkter. Det anbefales også, at du kører det periodiske job *Genberegn styklisteniveauer*, før du går i gang med massekørsel af omkostningsberegninger. Hver organisation skal overveje produktmiksen og definere en strategi, der opfylder de specifikke for dine produkt- og stykliste- eller formelstrukturer.

## <a name="transfer-order-costing"></a>Efterkalkulation af flytteordre

### <a name="is-there-a-way-to-allocate-freight-to-a-transfer-order-cost"></a>Er det muligt at fordele fragt på en omkostning i forbindelse med en flytteordre?

Du kan føje gebyrer til en flytteordre for at tilføje omkostninger. Gebyrkoden definerer debet og kredit for det gebyr, du tilføjer. Du skal først oprette gebyrkoder i modulet **Lagerstyring**. Hvis du vil føje et gebyr til en flytteordre, skal du vælge **Gebyrer** på flytteordrelinjen, hvor du vil føje et gebyr til.

## <a name="variances"></a>Afvigelser

### <a name="can-i-treat-variances-differently-based-on-the-site-or-warehouse"></a>Kan jeg behandle afvigelser forskelligt, afhængigt af lokationen eller lagerstedet?

Der er ingen mulighed for at konfigurere afvigelseskonti efter lokation. Når du bruger standardefterkalkulation for et frigivet produkt, kan du vælge den hovedkonto, der bruges til bogføring af standardomkostningsafvigelser på **Bogføring**-siden. Du kan vælge at konfigurere kontiene for én vare, en gruppe varer eller alle varer. Du kan også konfigurere én omkostningsgruppe, en gruppe af omkostningsgrupper eller alle omkostningsgrupper.

### <a name="can-i-separate-variances-that-are-the-result-of-currency-exchange-rates-from-other-types-of-variances"></a>Kan jeg adskille afvigelser, der er resultatet af valutakurser fra andre typer afvigelser?

Hvis en afvigelse er resultatet af en valutakursdifference mellem indkøbsordreprisen og standardkostprisen for en vare, kan kursdifferencen på ingen måde adskilles fra andre afvigelser.

## <a name="reporting"></a>Rapportering

### <a name="how-many-inventory-value-report-configurations-can-i-create-and-use"></a>Hvor mange lagerværdirapportkonfigurationer kan jeg oprette og bruge?

Der er ingen grænser for, hvor mange lagerværdirapportkonfigurationer du kan oprette. Du skal evaluere dine specifikke rapporteringskrav og oprette det antal konfigurationer, du skal bruge for at opfylde disse krav. Du skal bruge mindst én konfiguration af lagerværdirapporten for at køre rapporten eller indstillingen for rapportlagring.

### <a name="can-i-use-the-inventory-value-report-to-analyze-the-cost-of-an-item-in-each-warehouse"></a>Kan jeg bruge rapporten lagerværdi til at analysere kostprisen for en vare på hvert lagersted?

Ja. Du kan aktivere indstillingen **Vis** eller **Total** for hver **Lagersted**-dimension i konfigurationen af rapporten Lagerværdi. Men rapporten vil kun vise værdier for dimensioner, hvor indstillingen **Økonomisk lager** er aktiveret for lagringsdimensionsgruppen. For andre dimensioner vises kun tomme kolonner. Yderligere oplysninger finder du i [Eksempler og logik til rapport over lagerværdi](inventory-value-report-examples.md).

### <a name="how-can-i-view-the-inventory-quantity-as-of-a-specific-date-with-the-weighted-average"></a>Hvordan kan jeg få vist lagerantallet pr. en bestemt dato med det vægtede gennemsnit?

Du kan bruge rapporten **Aldersfordelt lager**, som indeholder kolonnen **Gennemsnitlig enhedskostpris**, der viser lagerværdien pr. en bestemt dato. Yderligere oplysninger finder du i [Eksempler på og logik om rapport om aldersfordelt lager](inventory-aging-report.md).

### <a name="how-can-i-view-which-receipt-transactions-are-settled-against-an-issue-transaction"></a>Hvordan kan jeg få vist, hvilke tilgangstransaktioner der udlignes mod en afgangstransaktion?

Du kan få vist udligningerne for en lagertransaktion ved at vælge **Udligninger** eller **Kostprissporing** under fanen **Lager** i handlingsruden for siden **Lagertransaktion** eller **Lagertransaktionsdetaljer**. Hvis du vælger en tilgang for at få vist de afgange, der er relateret til transaktionen, viser kostprissporingen ikke oplysningerne. Der vises kun detaljer, hvis du vælger en afgangstransaktion.

### <a name="how-does-the-inventory-value-report-show-items-that-have-a-positive-physical-quantity-and-a-negative-financial-value"></a>Hvordan viser rapporten over lagerværdi varer, der har et positivt fysisk antal og en negativ økonomisk værdi?

I rapporten over lagerværdier adskilles de fysiske og økonomiske beløb og antal i deres egne kolonner. De værdier, der vises i rapporten, er fra det datointerval, du valgte, da du kørte rapporten. Det oversigtsniveau, der vises, afhænger af de valgte indstillinger. Hvis en vare har transaktioner med fysisk tilgang og økonomisk afgang, opsummeres antal og værdier uafhængigt af hinanden. Hvis du har valgt at få vist detaljeringsniveauet som transaktioner, vises rækker for hver tilgang og afgang separat, og det fysiske og økonomiske antal og beløb vises. Yderligere oplysninger finder du i [Eksempler og logik til rapport over lagerværdi](inventory-value-report-examples.md).

### <a name="what-is-the-impact-of-storage-and-tracking-dimension-groups-on-the-inventory-value-report"></a>Hvad er virkningen af lagrings- og sporingsdimensionsgrupper på lagerværdirapporten?

Hvis du aktiverer indstillingen **Økonomisk værdi** for en dimension i en lager- eller sporingsdimensionsgruppe, kan du vælge indstillingen **Vis** eller **Total** for dimensionen i rapportkonfigurationen for lagerværdi. Hvis du vælger indstillingen **Vis** eller **Total** for en dimension, hvor indstillingen **Økonomisk værdi** ikke er valgt, vil kolonnen være tom i rapportoutputtet. Hvis du har aktiveret indstillingen **Økonomisk værdi** for en dimension i en lager- eller sporingsdimensionsgruppe, og du ikke vælger indstillingen **Vis** eller **Total** i rapportkonfigurationen for lagerværdi, opsummerer systemet værdierne for de valgte dimensioner, når de spores økonomisk.

### <a name="can-i-customize-the-power-bi-embedded-reports-for-costing"></a>Kan jeg tilpasse de integrerede Power BI Embedded-rapporter til efterkalkulation?

Ja, brugere med de korrekte sikkerhedstilladelser kan opdatere lærredet for rapportdesignet til enhver Power BI Embedded-rapport i Supply Chain Management. Du kan finde flere oplysninger i [Tilpasse integrerede rapporter i analytiske arbejdsområder](../../fin-ops-core/dev-itpro/analytics/customize-analytical-workspace.md).

### <a name="where-can-i-view-the-variance-analysis-statement"></a>Hvor kan jeg få vist opgørelsen over afvigelsesanalysen?

Du kan få adgang til opgørelsen af afvigelsesanalyser ved at gå til **Omkostningsstyring \> Forespørgsler og rapporter \> Lagerregnskab – analyserapporter** eller **Omkostningsstyring \> Forespørgsler og rapporter \> Produktionsregnskab – analyserapporter**. Begge indstillinger åbner den samme rapport, og rapporten har samme funktionalitet.

## <a name="item-prices-and-default-costs"></a>Varepriser og standardomkostninger

### <a name="can-i-maintain-the-cost-for-each-product-variant"></a>Kan jeg vedligeholde omkostningerne for hver produktvariant?

Ja. Du kan aktivere indstillingen **Brug kostpris efter variant** i oversigtspanelet **Administrer omkostninger** på siden **Frigivne produkter** for at aktivere prissætning efter produktvariant. (Denne indstilling er kun tilgængelig for produktmastere). Derefter kan du på siden **Varepris** (som du kan åbne fra siden **Efterkalkulationsversion** eller siden **Frigivne produkter**) vælge **Dimensionsvisning** for at angive, om du vil have vist dimensionen **Konfiguration**, **Størrelse**, **Farve** eller **Typografi**. Hvis du vil gemme opsætningen og bruge de valgte dimensioner, hver gang du åbner siden, skal du aktivere indstillingen **Gem opsætning** og derefter vælge **OK**. Du kan kun angive dimensionerne for varer, hvor dimensionerne er aktive i produktdimensionsgruppen.

### <a name="can-i-maintain-the-cost-for-each-warehouse"></a>Kan jeg vedligeholde omkostningerne for hvert lagersted?

Nej, du kan ikke vedligeholde varens pris efter lagersted. Du kan dog vedligeholde samhandelsaftaler for indkøbs- eller salgspriser efter lagersted. Vælg først indstillingen **For indkøbspriser** eller **For salgspriser** for dimensionen på siden **Lagringsdimensionsgruppe**. Når du derefter opretter samhandelskladden og åbner linjerne for dimensionerne, skal du vælge **Lager \> Vis dimensioner** for at vælge, hvilken dimension der skal vises i gitteret. Hvis du vil gemme opsætningen og bruge de valgte dimensioner, hver gang du åbner siden, skal du aktivere indstillingen **Gem opsætning** og derefter vælge **OK**. Du kan kun angive dimensionerne for varer, hvor dimensionerne er aktive i produktdimensionsgruppen.

### <a name="what-are-price-charges"></a>Hvad er prisgebyrer?

Prisgebyrer gør det muligt at føje et fast beløb til enhedsprisen på vareprisen eller samhandelsaftalen. Når du angiver et beløb i feltet **Prisgebyrer**, kan du også angive en værdi i feltet **Gebyrmængde**. Prisgebyrerne amortiseres i forhold til din angivne gebyrmængde. Aktivér indstillingen **Inkl. i enhedspris**, hvis du vil medtage prisgebyrer i varens enhedspris. Denne indstilling er altid aktiveret for en standardomkostning.

### <a name="how-should-i-configure-prices-for-items-that-are-procured-in-multiple-currencies"></a>Hvordan skal jeg konfigurere priser for varer, der fremskaffes i flere valutaer?

Hvis du angiver en standardpris i feltet **Indkøbspris** på siden **Frigivet produkt**, antages det, at den findes i regnskabsvalutaen i finansmodulet for den juridiske enhed, du arbejder i. Hvis du på samme måde angiver en indkøbspris i en efterkalkulationsversion, hvor feltet **Pristype** er angivet til *Indkøb*, antages prisen at være i regnskabsvalutaen for din juridiske enhed. Når du opretter en indkøbsordre for en kreditor, der har en anden valuta, omregnes valutaen automatisk fra regnskabsvalutabeløbet til transaktionsvalutaen ved hjælp af den valutakurs, du angiver i feltet **Regnskabsvalutakurstype** i Finans.

Når du opretter en samhandelskladde, kan du angive den valuta, som prisen skal udtrykkes i, på hver linje. Du kan oprette samhandelsaftaler for flere valutaer, bestemte kreditorer og mange andre kombinationer af faktorer. Hvis du opretter en indkøbsordre, hvor der findes en samhandelsaftale for den valuta, du har valgt, bruges den samhandelsaftale, der har den tilsvarende valuta. Når du bogfører transaktioner som f.eks. produkttilgange eller fakturaer, omregnes beløbet til finansregnskabsvalutaen ved hjælp af den regnskabsvalutakurs, du angiver i Finans.

### <a name="how-should-i-configure-costs-for-items-that-are-procured-in-multiple-currencies"></a>Hvordan skal jeg konfigurere omkostninger for varer, der fremskaffes i flere valutaer?

Omkostninger kan ikke konfigureres i mere end én valuta. Den omkostning, du angiver for vareprisen eller standardomkostningerne, som du angiver i feltet **Pris** i oversigtspanelet **Administrer kostpris** på siden **Frigivne produkter**, udtrykkes altid i regnskabsvalutaen i Finans for den juridiske enhed, du har valgt.

Hvis organisationen bruger standardefterkalkulation, skal du definere en strategi for definition af omkostningerne, når der er flere valutaer. Du skal også definere en proces for regelmæssig opdatering af omkostningen for at reducere antallet af afvigelser, der bogføres.

### <a name="can-i-use-the-profit-setting-on-the-cost-group-page-to-calculate-sales-prices"></a>Kan jeg bruge indstillingen Avance på siden Kostprisgruppe til at beregne salgspriser?

Ja, du kan bruge indstillingen **Avance** på siden **Kostprisgruppe** til at tilføje en procentdel, når salgspriser beregnes ved hjælp af en omkostningsberegning. Du kan finde flere oplysninger under [Styklistekalkulationer](bom-calculations.md).

## <a name="marking"></a>Afmærkning

### <a name="how-does-marking-affect-periodic-costing-models"></a>Hvordan påvirker afmærkningen periodiske efterkalkulationsmodeller?

Hvis du bruger en periodisk efterkalkulationsmodel som f.eks. FIFO, LIFO eller vægtet gennemsnit, og du har markeret en tilgangstransaktion i forhold til en afgangstransaktion, ignoreres varens heuristiske model under lagerlukningen. I stedet vil systemet bruge de faktiske tilgangsomkostninger på omkostningen for afgang.

### <a name="what-happens-during-the-inventory-close-when-i-use-marking"></a>Hvad sker der under lagerlukningen, når jeg bruger afmærkning?

Når du markerer tilgange og afgange, udlignes de transaktioner, der er markeret sammen, ved lagerlukningen. Når afmærkning bruges til at oprette udligningen, angives feltet **Princip** på siden **Udligning** til *Afmærkning*. Hvis en transaktion er afmærket, før den fysisk eller økonomisk opdateres, bruger afgangen den afmærkede tilgangs kostpris i stedet for den løbende gennemsnitskostpris. Hvis transaktionerne er afmærket efter den økonomiske opdatering, vil processen lagerlukning og -regulering rette afgangsomkostning, så den matcher tilgangsomkostningen.

### <a name="can-i-manually-mark-transactions-when-i-use-standard-costing-or-moving-average"></a>Kan jeg afmærke transaktioner manuelt, når jeg bruger standardefterkalkulation eller glidende gennemsnit?

Nej, du kan ikke afmærke tilgange eller afgange manuelt, når du bruger standardefterkalkulation eller glidende gennemsnit. Hvis der automatisk afmærkes transaktioner (f.eks. direkte levering eller interne ordrer), bevares afmærkningsposten som tidsbestemt reservation. Men når du bruger standardefterkalkulation eller glidende gennemsnit, har afmærkningen af poster ingen indflydelse på varens kostpris.

### <a name="how-does-marking-affect-the-profit-and-loss-statement"></a>Hvordan påvirker afmærkningen driftsopgørelsen?

Når du afmærker en afgangstransaktion i forhold til en tilgang, vil omkostningerne for afgang svare til den valgte tilgang. Når du bogfører afregningen fysisk og økonomisk, påvirker bogføringen de konti for **Vareforbrug for leverede varer** og **Vareforbrug for fakturerede varer**, som du angiver i lagerposteringsprofilen. Hvis en transaktion er markeret efter den fysiske eller økonomiske opdatering, opretter processen *Lagerlukning og -regulering* en regulering, der har et tilsvarende bilag, der justerer kontoen **Vareforbrug for fakturerede varer** og modposterer til den konto, du angiver for **Omkostninger ved fakturerede enheder** (lager).

### <a name="how-does-marking-affect-master-planning"></a>Hvordan påvirker afmærkningen varedisponering?

Fanen **Standardopdatering** på siden **Varedisponeringsparametre** indeholder et felt med navnet **Opdater afmærkning**. Den indstilling, du vælger, bruges, når du fastlægger et ordreforslag, der genereres ved varedisponering. Der findes følgende indstillinger:

- *Nej* – Systemet udfører ikke nogen afmærkning.
- *Standard* – Systemet afmærker tilgange mod afgange i henhold til udligningen. En behovsordre afmærkes i forhold til en opfyldelsesordre. Hvis der er en rest i opfyldelsen, afmærkes opfyldelsesordren ikke.
- *Udvidet* – Både behovsordrer og opfyldelsesordrer afmærkes, uafhængigt af om der er et restantal åbent i opfyldelsesordren.

## <a name="negative-inventory"></a><a name="negative-inventory"></a>Negativt lager

### <a name="when-should-i-allow-physical-negative-inventory"></a>Hvornår skal jeg tillade fysisk negativt lager?

Generelt anbefales det ikke, at du tillader fysisk negativt lager, da det ikke er muligt at have mindre end 0 (nul) af en materiel vare på lagerstedet. Forretningsprocesserne i nogle brancher og forretningsscenarier kan dog begrænse operationer, der kræver, at lageret må blive fysisk negativt. Det kan f.eks. være, at detailhandlere ikke ønsker at forhindre salget af en vare, der medtages til kasseapparatet, heller ikke når systemet angiver, at der ikke er nogen tilgængelige varer. Procesproducenter er et andet eksempel. For disse producenter kan den mængde, der forbruges, overstige det, der anbefales i formlen. Alternativt kan forbruget forkalkuleres i stedet for præcist, så forbruget overstiger mængden på en bestemt lokation, f.eks. en tank.

Når det er muligt, bør du evaluere forretningsprocessen og forsøge at forbedre den for at sikre, at lageret ikke kan være negativt. Hvis du skal tillade negativt lager, skal du have en klar forretningsproces til korrigering af negativt lager, da det kan påvirke efterkalkulation negativt.

### <a name="when-should-i-allow-financial-negative-inventory"></a>Hvornår skal jeg tillade økonomisk negativt lager?

Generelt anbefales det, at de fleste organisationer tillader økonomisk negativt lager. (I de fleste tilfælde behandles indkøbsordrefakturaer ikke, før du kan afsende varerne). Du skal aktivere denne indstilling, når du har specifikke forretningsprocesser, der kræver, at salgsprisen afspejler den endelige kostpris for en indkøbsordre. Dette krav kan f.eks. gælde i en branche med fremstilling efter ordre eller i bestemte områder, hvor det er et lovkrav.

### <a name="what-happens-to-the-cost-of-my-issues-when-the-inventory-is-negative"></a>Hvad sker der med omkostningerne for mine afgange, når lageret er negativt?

Når lageret for varen er negativt, og du afstår flere varer, end du fysisk har, vil systemet bruge standardvareprisen til at beregne det løbende gennemsnit, hvis du bruger en periodisk efterkalkulationsmodel som f.eks. FIFO, LIFO eller vægtet gennemsnit. Hvis der ikke er angivet en standardpris for varen, vil systemet udstede lageret med en værdi på 0 (nul). Denne funktionsmåde kan bevirke, at fremtidige beregninger af det løbende gennemsnit eller glidende gennemsnit er forkerte.

### <a name="can-i-prevent-items-from-being-picked-packed-or-sold-on-sales-orders-and-production-orders-if-there-isnt-enough-on-hand-inventory"></a>Kan jeg forhindre varer i at blive plukket, pakket eller solgt på salgsordrer og produktionsordrer, hvis der ikke er tilstrækkelig lagerbeholdning?

Ja. Det anbefales, at du deaktiverer indstillingen **Fysisk negativt lager** for varemodelgruppen for at forhindre, at varer plukkes, pakkes eller sælges på salgsordrer og produktionsordrer.

### <a name="can-i-prevent-items-from-being-invoiced-on-a-sales-order-if-no-purchase-orders-have-been-invoiced-for-the-same-item"></a>Kan jeg forhindre varer i at blive faktureret på en salgsordre, hvis der ikke er faktureret indkøbsordrer for samme vare?

Ja. Det anbefales, at du deaktiverer indstillingen **Økonomisk negativt lager** for varemodelgruppen for at forhindre, at varer faktureres på en salgsordre, hvis der ikke er faktureret indkøbsordrer for samme vare.

### <a name="how-does-negative-inventory-affect-financial-ratios-such-as-gross-profit-margin"></a>Hvordan påvirker negativt lager de økonomiske forhold som f.eks. bruttoavance?

Når du tillader, at lageret bliver negativt, kan lagerværdien i balancen og kostprisen for solgte varer i driftskontoen undervurderes, især hvis der ikke er konfigureret en standardpris for varerne. Derfor kan økonomirapportering og nøgletal som f.eks. bruttoavancemargener overvurderes, fordi omkostningen ikke er korrekt. Hvis du bruger en periodisk efterkalkulationsmodel som f.eks. FIFO, LIFO eller vægtet gennemsnit, kan værdien af afgange reguleres, når du kører lagerluknings- og reguleringsprocessen, når de negative lagerantal er blevet rettet. Men hvis du bruger glidende gennemsnit, kan de enkelte transaktioner ikke værdireguleres.

### <a name="how-should-i-correct-negative-inventory"></a>Hvordan skal jeg rette negativt lager?

Det anbefales, at du ofte overvåger og korrigerer negativt lager, når organisationens eller forretningsbehovet kræver, at lageret må blive negativt. Du kan rette lagerværdierne ved at udføre en cyklusoptælling, bogføre en regulering eller bogføre en bevægelseskladde. Hvis du skal kunne registrere den uventede fortjeneste på lageret på en specifik finanskonto, skal du planlægge at bruge en bevægelseskladde. Ellers bogføres lagerreguleringen på kontoen **Lagertilgang** og modposteres på konti **Lagerudgifter, overskud**, du angiver i lagerposteringsprofilen, når du bruger cyklusoptælling eller lagerreguleringsprocessen.

### <a name="do-i-have-to-create-a-new-item-if-my-inventory-has-gone-negative-and-i-use-moving-average"></a>Skal jeg oprette en ny vare, hvis mit lager er blevet negativt, og jeg bruger glidende gennemsnit?

Nej Hvis din organisation tillader, at lageret bliver fysisk negativt, og du bruger det glidende gennemsnit som lagermodel, bruger systemet den reserveomkostningsrækkefølge, der er tildelt på siden **Parametre for lager- og lokationsstyring**, til at bestemme, hvordan omkostningerne skal tildeles til dine afgange. Generelt anbefales det, at du undgår at lade lageret blive fysisk negativ. Du kan finde flere oplysninger under de andre spørgsmål i afsnittet [Negativt lager](#negative-inventory) i dette emne.

## <a name="not-stocked-products"></a>Ikke-lagerførte produkter

### <a name="can-i-post-sales-order-picking-lists-for-not-stocked-products"></a>Kan jeg bogføre pluklister til salgsordrer for ikke-lagerførte produkter?

Når du genererer en plukliste til en salgsordre, der indeholder varer i en varemodelgruppe, som ikke er lagerført, kan du ikke se nogen linjer for de varer, der ikke er lagerført. Du kan ikke bruge mobilappen Warehouse Management til at behandle ikke-lagerførte varer.

Når du genererer en følgeseddel til en salgsordre, der indeholder varer i en varemodelgruppe, som ikke er lagerført, skal du angive feltet **Antal** til *Plukket mængde og ikke lagerførte produkter*, så de varer, der ikke er lagerført, medtages i dokumentgenereringen. Hvis du vælger *Alle*, medtages kun lagerførte varer på følgesedlen.

### <a name="should-i-use-a-not-stocked-product-or-a-category-sales-category-or-procurement-category"></a>Skal jeg bruge et produkt, der ikke er lagerført, eller en kategori (salgskategori eller indkøbskategori)?

Valget mellem et ikke lagerført produkt og en kategori afhænger af dine specifikke forretningsbehov. Ikke lagerførte produkter giver generelt mere kontrol over standardværdier, f.eks. antal og priser på indkøbsordrer og salgsordrer. Produkter, der ikke er lagerført, foretrækkes derfor i tilfælde af, at samme produkt eller tjeneste købes eller sælges mere end én gang. Kategorier er nyttige i scenarier, hvor prisen, varerne, beskrivelserne osv. ikke er ens fra transaktion til transaktion. Kategorier kan også bruges på alle produkter til at klassificere den type produkt, der sælges eller købes.

## <a name="service-items"></a>Servicevarer

### <a name="what-is-the-difference-between-a-service-item-and-a-not-stocked-product"></a>Er der en forskel mellem en servicevare og et produkt, der ikke er lagerført?

En servicevare er en produkttype. Når du opretter et nyligt frigivet produkt, kan du angive feltet **Produkttype** til enten *Vare* eller *Service*. *Vare* vælges typisk for at angive, at varen er materiel, hvorimod *Service* typisk vælges for at angive, at varen er immateriel.

Alle frigivne produkter, uanset om det er en vare eller et serviceprodukt, kan være lagerført eller ikke lagerført. Indstillingen for lagerført eller ikke lagerført styres af den varemodelgruppe, du vælger for det frigivne produkt. Når du vælger en varegruppe, der ikke er lagerført, oprettes der ikke lagertransaktioner til f.eks. den relaterede salgsordre eller indkøbsordre.

### <a name="can-i-include-not-stocked-items-in-a-bom"></a>Kan jeg medtage varer, der ikke er lagerført, på en stykliste?

Nej, du kan ikke medtage et frigivet produkt, der er knyttet til en varemodelgruppe, hvor indstillingen **Lagerført** er deaktiveret i en stykliste eller formel. Det er ligegyldigt, om feltet **Produkttype** er angivet til *Vare* eller *Service*. Det er kun varer, der lagerføres, som kan medtages på stykliste- eller formellinjer.

## <a name="costing-modelspecific-questions"></a>Efterkalkulationsmodel – specifikke spørgsmål

### <a name="which-costing-model-should-i-use"></a>Hvilken efterkalkulationsmodel skal jeg bruge?

De efterkalkulationsmodeller, du skal vælge, afhænger af virksomhedens forretningsbehov. Før du vælger en efterkalkulationsmodel, der skal bruges i Supply Chain Management, skal du kontrollere, at modellen er tilladt i de lokale regler. Det anbefales, at du validerer dit valg med en certificeret bogholder i dit område.

### <a name="can-i-use-more-than-one-costing-model-in-my-organization"></a>Kan jeg bruge mere end én efterkalkulationsmodel i min organisation?

Ja. Der er ingen grænser for antallet af varemodelgrupper eller efterkalkulationsmodeller, du kan vælge i Supply Chain Management.

### <a name="can-i-use-more-than-one-costing-model-for-each-item"></a>Kan jeg bruge mere end én efterkalkulationsmodel til hver vare?

Nej Du kan kun vælge én efterkalkulationsmodel for hvert frigivet produkt. Denne funktionsmåde styres af varemodelgruppen. Hvis du skal bruge mere end én efterkalkulationsmodel til at rapportere om lagerværdier, bør du overveje at bruge tilføjelsesprogrammet Globalt lagerregnskab.

### <a name="when-i-use-manufacturing-execution-which-costing-methodology-should-i-use"></a>Når jeg bruger produktionsudførelse, hvilken efterkalkulationsmetode skal jeg så bruge?

De efterkalkulationsmodeller, du skal vælge, afhænger af virksomhedens forretningsbehov. Der er ingen bestemt fordel eller ulempe ved at bruge en efterkalkulationsmodel, når din organisation også bruger produktionsudførelse.

### <a name="when-is-fefo-used"></a>Hvornår anvendes FEFO?

FEFO-metoden (First expired, First out) er ikke en efterkalkulationsmetode. Det er i stedet en reservationsteknik, der ofte bruges i produktionsorganisationer. Du kan aktivere FEFO-reservationer for en varemodelgruppe ved at aktivere indstillingen **FEFO-datokontrolleret** og derefter vælge en værdi i feltet **Kriterier for plukning**.

### <a name="are-there-performance-benefits-to-selecting-one-costing-model-over-another"></a>Er der ydeevnefordele ved at vælge én efterkalkulationsmodel frem for en anden?

Generelt har den efterkalkulationsmodel, du vælger for en vare, minimal indflydelse på systemets overordnede ydeevne. Den tid, det tager at køre lagerluknings- eller genberegningsprocessen, af kan blive påvirket af den lagerefterkalkulationsmodel, du vælger. Hvis du f.eks. bruger standardkostpris eller glidende gennemsnit, har lagerlukningsprocessen minimal indflydelse på systemet, da den ikke opdaterer hver enkelt lagertransaktion og opretter udligninger. Men en periodisk efterkalkulationsmodel, f.eks. FIFO, LIFO eller vægtet gennemsnit, kan øge den tid, der kræves for at fuldføre lagerlukningsprocessen. Specifikt kan lukkeprocessen være længere, når du angiver et højt antal i feltet **Det maksimale antal gentagelser tilladt pr. element**, eller et lavt tal i feltet **Minimumbeløb tilladt** for processen *Luk lager*.

### <a name="when-should-i-use-the-fixed-receipt-price-option"></a>Hvornår skal jeg bruge indstillingen Fast tilgangspris?

Når du markerer afkrydsningsfeltet **Fast tilgangspris** på siden **Varemodelgruppe** for en vare, bruger systemet tilgangsprisen som en standardomkostning for lagertilgangen. Hvis købsprisen og standardkostprisen, der er konfigureret for et produkt, er forskellige, bogføres differencen på kontoen **Vind ved fast tilgangspris** eller **Tab ved fast tilgangspris** og modposteres på kontoen **Modposteret fast tilgangspris**. (Alle disse konti er angivet på siden **Postering**).

Du skal markere afkrydsningsfeltet **Fast tilgangspris**, når du bruger en periodisk efterkalkulationsmodel som f.eks. FIFO, LIFO eller vægtet gennemsnit, og du kræver, at en afvigelse i købspris spores i finansmodulet, hvis prisen på en tilgang afviger fra standardvareomkostningen.

### <a name="moving-average"></a>Glidende gennemsnit

### <a name="is-moving-average-the-same-as-a-floating-average"></a>Er glidende gennemsnit det samme som et flydende gennemsnit?

Begreberne flydende gennemsnit, glidende gennemsnit og løbende gennemsnit bruges ofte synonymt. Af disse begreber er glidende gennemsnit den eneste officielle efterkalkulationsmodel, der er tilgængelig i Supply Chain Management. Selvom løbende gennemsnit ikke er en officiel efterkalkulationsmodel, er det den metode, der bruges, når du bruger en periodisk efterkalkulationsmodel som f.eks. FIFO, LIFO eller vægtet gennemsnit. Betegnelsen flydende gennemsnit bruges ikke i Supply Chain Management og kan have forskellige konnotationer i andre systemer.

### <a name="how-can-i-accommodate-the-difference-between-the-product-receipt-price-and-invoice-price-when-i-use-moving-average"></a>Hvordan kan jeg tage hensyn til forskellen mellem produkttilgangsprisen og fakturaprisen, når jeg bruger glidende gennemsnit?

Når du bruger glidende gennemsnit, bruges den fysiske kostpris (tilgangspris) til at beregne det glidende gennemsnit for alle afgangstransaktioner. Hvis der er forskel mellem den fysiske kostpris (tilgangsprisen) og den økonomiske kostpris (fakturaprisen), bogføres differencen automatisk på den hovedkonto, der er angivet for bogføringstypen **Prisdifference for glidende gennemsnit** under fanen **Lager** på siden **Lagerkonteringsprofil**.

### <a name="where-is-the-price-difference-for-moving-average-presented-in-the-general-ledger"></a>Hvor vises prisdifferencen for glidende gennemsnit i Finans?

Hvis der er prisforskel mellem bogføringen af en fysisk opdatering og en økonomisk opdatering for en tilgang, bogføres differencen på den hovedkonto, der er angivet for bogføringstypen **Prisdifference for glidende gennemsnit** under fanen **Lager** på siden **Lagerkonteringsprofil**. Du kan finde flere oplysninger under [Glidende gennemsnit](moving-average.md).

### <a name="when-i-use-moving-average-what-happens-if-there-is-an-issue-before-the-receipt"></a>Hvad sker der, når jeg bruger glidende gennemsnit, hvis der er en afgang før tilgangen?

Der kan typisk være en afgang før tilgangen, enten fordi du tillader fysisk negativt lager for varemodelgruppen, eller fordi afgangen er dateret bagud. Du kan finde flere oplysninger i afsnittet [Negativt lager](#negative-inventory) i dette emne.

Hvis du daterer transaktioner bagud, anbefales det, at du nøje overvejer forretningsprocesserne og -handlingerne for at finde ud af, om dette scenario kan undgås. Hvis du tilbagedaterer en transaktion for en vare, der bruger glidende gennemsnit, vil systemet tildele det aktuelle glidende gennemsnit til transaktionen. Senere afgange justeres ikke. Yderligere oplysninger om glidende gennemsnit med tilbagedaterede transaktioner finder du i [Glidende gennemsnit](moving-average.md).

### <a name="standard-costing"></a>Standardefterkalkulation

### <a name="what-is-the-difference-between-standard-costing-and-fixed-receipt-price"></a>Hvad er forskellen mellem standardefterkalkulation og fast tilgangspris?

Standardefterkalkulation kræver, at du definerer en varepris og aktiverer kostprisen i en efterkalkulationsversion. Denne omkostning bruges til alle tilgange og afgange. Afvigelser for lagertilgange registreres i finansmodulet ved hjælp af de standardkonti til omkostningsafvigelse, som du angiver under fanen **Standardomkostning** på siden **Lagerposteringsprofil**.

Men når du bruger en fast tilgangspris, er det kun omkostningerne for tilgange, der er faste, og systemet bruger den omkostning, du angiver i oversigtspanelet **Administrer omkostninger** på siden **Frigivne produkter**. Forskelle mellem standardkostprisen og prisen på indkøbsordren medfører, at afvigelsen i indkøbsprisen bogføres på driftskontiene for den faste tilgangspris. Afgange bruger ikke fast tilgangspris. I stedet værdireguleres økonomisk gennemsnit ved bogføring (medmindre du bruger afmærkning), og de værdireguleres til den heuristiske model, som du vælger, når du kører lagerlukningen.

### <a name="can-i-use-fefo-reservations-with-standard-costing"></a>Kan jeg bruge FEFO-reservationer sammen med standardefterkalkulation?

Ja, du kan bruge FEFO-reservationer i en varemodelgruppe, når du vælger standardefterkalkulation. FEFO-reservationer styrer den reservationslogik, der bruges til fysisk håndtering af varer, mens standardefterkalkulation styrer de fysiske og økonomiske omkostninger for en vare.

### <a name="can-i-upload-pending-prices"></a>Kan jeg uploade ventende priser?

Ja, du kan bruge tilføjelsesprogrammet Excel eller Data Management Framework til at uploade en ventende pris. Det anbefales, at du bruger følgende enheder:

- Afventende varepriser (V2)
- Ventende enhedsomkostninger for ruteomkostningskategori
- Beregningsfaktorer for efterkalkulationsarknode (V2)

### <a name="how-often-can-i-update-the-standard-cost-for-an-item"></a>Hvor ofte kan jeg opdatere standardomkostningen for en vare?

Der er ingen begrænsning på den frekvens, som du kan aktivere en ny standardomkostning til. Hvis du aktiverer en ny omkostning for en vare samme dag, som den sidste omkostning blev aktiveret, vil systemet bruge den nyeste aktiverede omkostning på nye transaktioner eller opdateringer (f.eks. opdateringer til eksisterende transaktioner).

### <a name="can-i-deactivate-or-delete-an-activated-cost"></a>Kan jeg deaktivere eller slette en aktiveret omkostning?

Nej, du kan ikke deaktivere eller slette en aktiveret omkostning. Hvis du har aktiveret en omkostning forkert, kan du aktivere en ny omkostning med den korrekte omkostning.

### <a name="are-calculation-groups-used-with-standard-costing"></a>Bruges beregningsgrupper i forbindelse med standardefterkalkulation?

Beregningsgrupper kan bruges med alle varer uanset, hvilken varemodelgruppe du vælger. Beregningsgrupperne bruges under processen til omkostningstotaler eller omkostningsberegninger til at bestemme de indstillinger, der skal bruges til de varer, du kører beregningen for. Du kan finde flere oplysninger om beregningsgrupper i [Styklisteberegningsgrupper](bom-calculation-groups.md).

### <a name="when-should-i-use-a-planned-costing-version"></a>Hvornår skal jeg bruge en planlagt efterkalkulationsversion?

Efterkalkulationsversioner kan have typen *Standardomkostning* eller *Planlagte omkostning*. Typen *Standardomkostning* bruges til de omkostninger, der er aktive i systemet, og som bogføres i transaktioner. Typen *Planlagt omkostning* bruges til kørsel af simuleringer af omkostninger og har ingen indflydelse på transaktionsomkostningen.

### <a name="can-the-total-cost-from-one-entity-be-transferred-to-another-entity-as-the-selling-cost"></a>Kan de samlede omkostninger fra én enhed overføres til en anden enhed som salgsomkostningen?

Du kan ikke kopiere omkostninger fra ét firma til et andet på en automatisk måde. Det er desuden ikke muligt automatisk at kopiere omkostninger fra en købspris til en salgspris. Hvis din organisation skal udføre en af disse opgaver, skal du overveje, om du kan bruge Data Management Framework til at eksportere dataene fra din efterkalkulationsversion og uploade til et andet firma som enten en salgspris i efterkalkulationsversionen eller som en samhandelsaftale. Manuel ændring af filerne kan være påkrævet.

### <a name="what-is-the-best-way-to-copy-planned-costs-to-a-standard-costing-version"></a>Hvordan kan jeg bedst kopiere planlagte omkostninger til en standardefterkalkulationsversion?

Du kan bruge knappen **Kopiér** på siden **Efterkalkulationsversioner** til at kopiere varepriser, omkostningsartpriser eller indirekte omkostninger fra én efterkalkulationsversion til en anden.
