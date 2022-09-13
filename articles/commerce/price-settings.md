---
title: Prissætningsindstillinger
description: I denne artikel beskrives de forskellige indstillinger for prissætning og rabatstyring i Microsoft Dynamics 365 Commerce headquarters.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 4bc8cb16e7960d26adbb9590b4ad83cf46b02838
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410761"
---
# <a name="pricing-settings"></a>Prissætningsindstillinger

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

I denne artikel beskrives de forskellige indstillinger for prissætning og rabatstyring i Microsoft Dynamics 365 Commerce headquarters. Disse indstillinger sætter organisationer i stand til at definere prissætningsfunktionsmåden i deres Commerce-løsning for at imødekomme bestemte forretningsbehov.

## <a name="company-level-pricing-settings"></a>Indstillinger for firmaprissætning

De fleste prissætningsindstillinger findes på firmaniveau og **Commerce-parametrene \> Priser og rabatter** i Commerce headquarters.

### <a name="best-price-and-compound-concurrency-control-model"></a>Model til bedste pris og samtidighedskontrol af sammensætning

Indstillingen **Model til bedste pris og samtidighedskontrol af sammensætning** bestemmer, hvordan prissætningsprogrammet behandler flere rabatter i **bedste pris** eller **sammensat** samtidighedstilstand. 

Hvis parameteren er angivet til **Bedste pris og sammensæt inden for prioritet, sammensæt aldrig på tværs af prioriteter**, bruges alle **sammensatte** rabatter, der har samme prissætningsprioritet, sammensat. Det sammensatte resultat konkurrerer derefter med de **bedste pris**-rabatter, der har samme prissætningsprioritet, den bedste pris anvendes, og alle rabatter, der har en lavere prissætningsprioritet, ignoreres.

Hvis parameteren kun er angivet til **Bedste pris inden for prioritet, altid sammensat på tværs af prioriteter**, behandles alle **sammensatte** rabatter som **bedste pris**-rabatter. I en prissætningsprioritet vinder kun en enkelt rabat. Hvis den enkelte rabat er en **bedste pris** eller **sammensat** rabat, er den sammensat med alle øvrige **bedste priser** eller **sammensatte** rabatter, der har en lavere prissætningsprioritet.

### <a name="discount-compound-behavior"></a>Sammensætningsfunktion for rabat

Indstillingen **Sammensætningsfunktion for rabat** bestemmer, hvordan prissætningsprogrammet beregner flere sammensatte rabatter.

Hvis parameteren er angivet til **Sammensat**, anvendes én rabat oven på en anden på en akkumulerende måde. Hvis den er angivet til **Sammensat til den oprindelige pris**, behandles alle rabatter uafhængigt af hinanden og anvendes på samme oprindelige pris.

Du kan f.eks. sammensætte rabatter på 10 % og 20 % for et produkt, der har en oprindelig pris på $100. Hvis du angiver parameteren **Sammensætningsfunktion for rabat** til **Sammensat**, vil den endelige pris blive $72 ($100 &times; 90 % &times; 80 %). Hvis du angiver den til **Sammensat til den oprindelige pris**, vil den endelige pris blive $70 ($100 – $10 – $20).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Aktivere konkurrence mellem eksklusiv grænse og andre periodiske rabatter

Hvis indstillingen **Aktivér konkurrence mellem eksklusive grænseværdier og andre periodiske rabatter** er angivet til **Ja**, sørger prissætningsprogrammet for, at eksklusive grænserabatter konkurrerer med eksklusive rabatter, som ikke er en grænseværdi. Prissætningsprioriteten gælder stadig. Den **bedste pris** og den **sammensatte** grænserabat forbliver uændret. Det vil sige, at de ikke konkurrerer med ikke-grænserabatter.

### <a name="manual-line-discount-and-system-discount"></a>Manuel linjerabatprocent og systemrabat

Indstillingen **Manuel linjerabat og systemrabat** bestemmer, hvordan prissætningsprogrammet anvender en manuel linjerabat og en systemrabat på samme linje. Den manuelle linjerabat kan være sammensat oven på systemrabatten, eller den kan erstatte systemrabatten. Når den manuelle linjerabat og systemrabat er sammensat, overholder beregningslogikken indstillingen for **Sammensætningsfunktion for rabat**. En manuel samlet rabat, som gælder for hele ordren, overholder ikke denne indstilling.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Hold varer på den samme salgslinje til afrunding af rabatpris

Sommetider kan beløbet for et antalsrabatbeløb ikke divideres ligeligt med det kvalificerende antal (f.eks. hvis rabatbeløbet $10 for tre købte enheder). I disse tilfælde bestemmer indstillingen **Hold varer på den samme salgslinje til afrunding af rabatpris**, hvordan prissætningsprogrammet anvendes, og fordeler rabatbeløbet. Hvis parameteren er angivet til **Ja**, anvendes rabatbeløbet som et hele og fordeles ikke. Hvis det er angivet til **Nej** , fordeles rabatbeløbet på tværs af kvalificerende antal og afrundes. Et rabatbeløb på $10 for tre enheder opdeles f.eks. i $3,33 for én enhed, $3,33 for den anden enhed og $3,34 for den tredje enhed.

### <a name="apply-discounts-to-key-in-price-products"></a>Anvende rabatter på Indtast pris-produkter

Indstillingen **Anvende rabatter på Indtast pris-produkter** bestemmer, om rabatter kan anvendes sammen med "indtastede priser", der angives i POS. Indstillingen **Indtast pris** i produktkonfigurationen bestemmer, om og hvordan et produkt understøtter den indtastede pris.

### <a name="apply-discounts-to-price-overrides"></a>Anvend rabatter på prisændringer

Indstillingen **Anvend rabatter på prisændringer** bestemmer, om rabatter kan anvendes sammen med prisændringer.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Fordele rabat for billigste rabatter

Ved mix- og match-rabatter, der bruger den "billigste" beregningstype, bestemmer indstillingen **Fordeler rabat for billigste rabatter**, om prissætningsprogrammet fordeler rabatten på tværs af linjer.

Hvis parameteren er angivet til **Nej**, anvendes rabatten kun på de billigste linjer. For en "køb 2 få 1 gratis" mix og match-rabat vil den billigste vare f.eks. være gratis, og de øvrige to varer vil fortsat være til fuld pris. I dette tilfælde får en kunde, der returnerer begge varer til fuld pris, stadig den tredje vare gratis. Dette scenario kan medføre tab for forhandleren.

Hvis parameteren er angivet til **Ja**, fordeler prissætningsprogrammet rabatten på alle relevante linjer. Denne indstilling kan være med til at reducere tabet ved returneringer.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Beregn priser og rabatter på flere linjer manuelt.

Indstillingen **Beregn priser og rabatter på flere linjer manuelt** bestemmer, om prissætningsprogrammet bruger forsinkede pris- og rabatberegninger til POS-programmet og call center-kanalen. Hvis parameteren er angivet til **Ja**, beregner prissætningsprogrammet ikke omgående flerlinjerabatter (f.eks. antalsrabatter, grænserabatter og mix og match-rabatter), når en salgsordre oprettes eller redigeres i POS-programmet eller call center-kanalen.

> [!NOTE]
> I Commerce version 10.0.30 og tidligere styrer indstillingen **Beregn priser og rabatter på flere linjer manuelt** kun call center-kanalen. Den separate indstilling **Beregn rabatter for flere varer manuelt** i funktionalitetsprofilen styrer funktionaliteten for prisberegning i POS-programmet. I Commerce version 10.0.31 konsolideres de to indstillinger til én indstilling på firmaniveau.

### <a name="retention-period-in-days"></a>Tilbageholdelsesperiode i dage

Indstillingen **Tilbageholdelsesperiode i dage** angiver, hvor mange dage efter udløbsdatoen (hvis udløbsdatoen er angivet) eller den deaktiverede dato (hvis en udløbsdato ikke er angivet) en rabat skal systematisk slettes. Hvis parameteren er angivet til **0** (nul), foretages der ingen automatisk sletning.

> [!NOTE]
> I Commerce version 10.0.30 og tidligere kaldes denne indstilling **Antal dage, hvorefter de udløbne rabatter skal slettes**.

### <a name="coupon-bar-code"></a>Kuponstregkode

Indstillingen **Kuponstregkode** bestemmer, hvilken bestemt stregkode der bruges til at generere kuponstregkoder. Brugere kan vælge en af de foruddefinerede stregkoder, der er konfigureret på siden **Stregkodeopsætning**. Yderligere oplysninger om stregkoder og stregkodemasker finder du i [Konfigurere stregkoder](set-up-bar-codes.md) og [Konfigurere stregkodemasker](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Kuponkoden skal anvendes manuelt for at returnere transaktioner

Indstillingen for **Kuponkoden skal anvendes manuelt for at returnere transaktioner** gælder kun for returtransaktioner, der ikke er angivet en salgskvittering for. Angiv parameteren til **Nej**, hvis der automatisk skal anvendes kuponkoder på transaktionen. Angiv den til **Ja**, hvis kuponkoder skal føjes til transaktionen manuelt.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Brug opsætning af salgsaftaler for organisationen

I forbindelse med business-to-business-ordrer (B2B) bruges de salgsaftaler, der er angivet for organisationen i brugerens kundehierarki, til at bestemme den kontraktbaserede pris, hvis parameteren **Brug opsætning af salgsaftaler for organisationen** er angivet til **Ja**. Hvis parameteren er angivet til **Nej**, eller hvis kundehierarkiet ikke er defineret, søger prissætningsprogrammet efter salgsaftaler, der er defineret for brugeren, for at bestemme den kontraktbaserede pris. Du kan finde flere oplysninger om kundehierarkier for B2B-e-handel i [Administrere B2B-forretningspartnere ved hjælp af kundehierarkier](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Indstillinger for kanalprissætning

Følgende indstillinger sætter organisationer i stand til at styre prissætningsmåden for bestemte salgskanaler.

### <a name="enable-order-price-control"></a>Aktivér ordrepriskontrol

Parameteren **Aktivér ordrepriskontrol** findes i oversigtspanelet **Generelt** på siden **Call Center-konfiguration**. Indstillingen bestemmer, om prissætningsprogrammet gennemtvinger en begrænsning af prisændringsoperationen i call center-kanalen. Det fungerer sammen med indstillingen **Tillad prisjustering** på produktniveau.

Hvis ordreprisstyring er deaktiveret, kan alle call center-brugere foretage prisændringer på salgslinjer i call center-kanalen, uanset om de tilsvarende produkter tillader prisjustering.

Hvis ordreprisstyring er slået til, er det kun produkter, hvor parameteren **Tillad prisjustering** er angivet til **Ja**, der tillader prisændring af salgsordrer i callcenter-kanaler, og der skal angives en årsagskode på tilsvarende salgslinjer. En call center-bruger kan kun ændre salgsprisen med den værdi af **Omkostningsavance i procent**, der er defineret i **Retail og Commerce \> Konfiguration af kanal \> Call center-konfiguration \> Tilsidesæt tilladelser**. Hvis en prisændring overstiger denne procent, skal brugeren sende en anmodning, som derefter behandles via en foruddefineret Commerce-arbejdsproces til gennemsyn og godkendelse. Yderligere oplysninger om Commerce-arbejdsprocesser finder du i [Oversigt over arbejdsprocessystem](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Indstillinger for produktprissætning

Følgende indstillinger gennemtvinger prissætningsregler på produktniveau og findes på en organisations **Produktkonfiguration**-side.

### <a name="allow-price-adjust"></a>Tillad prisjustering

Hvis parameteren **Tillad prisjustering** er angivet til **Ja**, kan der anvendes en prisændring på produktet i call center-kanalens salgsordrer.

### <a name="key-in-price"></a>Indtast pris

Indstillingen **Indtast pris** bestemmer, om der skal angives en pris, når et produkt føjes til en salgstransaktion i POS. Den definerer også tilsvarende prisværdibegrænsninger.

### <a name="zero-price-valid"></a>Nulpris gyldig

Indstillingen **Nulpris gyldig** bestemmer, om de foruddefinerede, systemberegnede eller manuelt regulerede salgspriser for et produkt kan være 0 (nul). Angiv parameteren til **Ja**, hvis det er tilladt at angive en pris på nul. Indstillingen kan også angives på kategoriniveau fra Commerce-produkthierarkiet.

### <a name="prevent-all-discounts"></a>Undgå alle rabatter

Hvis du angiver parameteren **Undgå alle rabatter** til **Ja**, forhindrer du, at alle rabattyper (herunder manuelle rabatter) anvendes på et produkt. Indstillingen kan også angives på kategoriniveau fra Commerce-produkthierarkiet.

> [!NOTE]
> Denne indstilling begrænser ikke pristilsidesættelsen, fordi dette indstiller prisen og bliver ikke behandlet som en rabat.

### <a name="prevent-manual-discounts"></a>Undgå manuelle rabatter

Hvis du angiver parameteren **Undgå manuelle rabatter** til **Ja**, forhindrer du, at manuelle linjerabatter eller transaktionsrabatter anvendes på et produkt. Alle andre rabatter kan stadig anvendes. Indstillingen kan også angives på kategoriniveau fra Commerce-produkthierarkiet.

> [!NOTE]
> Denne indstilling begrænser ikke pristilsidesættelsen, fordi dette indstiller prisen og bliver ikke behandlet som en rabat.

### <a name="prevent-retail-discounts"></a>Forebyg detailrabatter

Hvis parameteren **Forebyg detailrabatter** er angivet til **Ja**, kan **simple**, **antal**-, **grænseværdi**-, **mix og match**- og **levering**-rabatter ikke anvendes på et produkt. Alle andre rabatter (herunder manuelle) kan stadig anvendes.

### <a name="prevent-tender-based-discounts"></a>Undgå tilbudsbaserede rabatter

Hvis parameteren **Undgå tilbudsbaserede rabatter** er angivet til **Ja**, kan der ikke anvendes en **tilbudsbaseret** rabat på et produkt. Alle andre rabatter (herunder manuelle) kan stadig anvendes.

Detailhandlere vælger ofte at udelukke nogle produkter, f.eks. nye varer eller eftertragtede varer, fra varebaserede rabatter (f.eks. simple rabatter og antalsrabatter). Men hvis kunden betaler ved hjælp af det foretrukne betalingsmiddel, kan de dog stadig anvende den tilbudsbaserede rabat. For at opnå dette resultat kan detailhandlere angive **Undgå alle rabatter** og **Undgå tilbudsbaserede rabatter** til **Nej** og **Forebyg detailrabatter** og **Undgå manuelle rabatter** til **Ja**.

## <a name="deprecated-or-removed-settings"></a>Udfasede eller fjernede indstillinger

Følgende prissætningsindstillinger er fjernet eller er planlagt til fjernelse fra Dynamics 365 Commerce.

| Indstilling | Årsag til udfasning eller fjernelse | Udfasnings- eller fjernelsesstatus |
|---------|-----------------------------------|-------------------------------|
| Håndtering af overlappende rabatter | Vi leverede denne indstilling i Commerce-parametre for at styre, hvordan prissætningsprogrammet søger efter og bestemmer den bedste rabatkombination, der skal anvendes. Indstillingen **Bedste rabat** gennemtvinger alle mulige rabatkombinationer ved prisberegning. **Bedste performance** er en optimeret indstilling, der bruger en heuristisk algoritme og en metode til rangering af beregningsværdi for at prioritere, evaluere og fastlægge den bedste rabatkombination i rette tid. **Afbalanceret beregning** i kodegrundlag fungerer på samme måde som indstillingen **Bedste performance**. Derfor er det egentlig en dubletindstilling. For at forbedre performance er prissætningsprogrammet opdateret, så det kun bruger **Bedste performance** som standardindstilling. Derfor er denne indstilling ikke længere gældende. | Udfases i version 10.0.21 og vil blive fjernet i oktober 2022. |
| Tillad prisjusteringer at øge produktprisen | Vi havde denne indstilling til at kontrollere, om prisjusteringsfunktionen kan øge produktpriser. Når denne parameter deaktiveres, kan organisationer kun bruge funktionen til prisjustering for at angive et produkts enhedspris, så den er lavere end basisprisen og samhandelsaftalens salgspris. Denne indstilling blev udfaset, fordi funktionen til prisjustering er opdateret, så den understøtter tovejs-justeringer (forhøjelse eller reduktion) som standard. | Udfases i version 10.0.30 og vil blive fjernet i oktober 2023. |
| Aktivér prisrapport for detailbutik | Vi leverede denne indstilling for at styre, om **Prisrapport**-funktionen er tilgængelig og kan bruges på siden til butikskonfiguration. Denne indstilling udfases, fordi formularen siden til butikskonfiguration er opdateret, så **Prisrapport** altid vises som standardfunktion. | Udfases i version 10.0.31 og vil blive fjernet i oktober 2023. |
| Brug dags dato til at beregne priser | Prissætningsprogrammet Dynamics 365 Supply Chain Management understøtter prisberegningen baseret på ønsket afsendelsesdato og ønsket modtagelsesdato sammen med dags dato. Programmet for Commerce-prissætning understøtter kun prisberegning baseret på dags dato. Til kunder, der bruger både Supply Chain Management- og Commerce-egenskaber, har vi angivet denne indstilling og anbefaler, at kunder altid angiver den til **Ja**, så de to prissætningsfunktioner kan arbejde sammen. Denne indstilling er udfaset, fordi den reelt ikke ændrer beregningsmåden og derfor er overflødig. | Udfases i version 10.0.31 og vil blive fjernet i oktober 2023. |
| Maksimumpris | Vi har leveret denne indstilling i funktionalitetsprofilen for at styre, om det kun er produkter, der har en salgspris, som ligger under den angivne maksimumpris, som kan sælges via POS i bestemte butikker. Denne indstilling er udfaset på grund af lav funktionsbrug. | Udfases i version 10.0.31 og vil blive fjernet i oktober 2023. |
| Anvend rabatter på enhedspris | Denne indstilling var beregnet til at styre, om priser og rabatter afrundes til enhedsprisniveauet eller på salgslinjeniveau under prisberegningen. Den er udfaset, fordi den ikke forbruges nogen steder i den aktuelle kodebasis. | Udfases i version 10.0.31 og vil blive fjernet i oktober 2023. |
| Beregn rabatter for flere varer manuelt. | Vi har leveret denne indstilling for at styre, om prissætningsprogrammet bruger forsinkede prisberegninger til detailbutikskanalen. Hvis parameteren er angivet til **Ja**, beregner prissætningsprogrammet ikke omgående flerlinjerabatter (f.eks. antalsrabatter, grænserabatter og mix og match-rabatter), når en salgsordre oprettes eller redigeres i POS-programmet. Vi har besluttet at konsolidere denne indstilling med en lignende indstilling i Handelsparametre for at oprette et omnichannel-kontrolelement. | Udfases i version 10.0.31 og vil blive fjernet i oktober 2023. |

Du kan få en komplet liste over fjernede eller udfasede funktioner i Dynamics 365 Commerce under [Fjernede eller udfasede funktioner i Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
