---
title: Callcenter-kataloger
description: I dette emne beskrives callcenterspecifikke funktioner for kataloger i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 05/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e4f89d86b64e0c8c76c15d3c2c1c00af353e9ca
ms.openlocfilehash: e64ec1191d82b9f1418e86ce819736903c0137aa
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---

# <a name="call-center-catalogs"></a>Callcenter-kataloger

[!include [banner](includes/banner.md)]

I dette emne beskrives de callcenterspecifikke funktioner, der er knyttet til katalogfunktionerne i Microsoft Dynamics 365 for Retail.  

Katalogfunktionerne i Dynamics 365 for Retail kan bruges til flere formål. Oprindeligt blev katalogfunktionerne oprettet for at understøtte integration af e-handel med tredjepart. Under opsætning af kataloget kunne virksomheder oprette en gruppering af produkter og attributter, der kunne udgives eksternt med henblik på forbrug i en tredjeparts e-handelsløsning.  

Da understøttelse af en callcenterkanal blev tilføjet i Dynamics 365 for Retail, blev katalogkonceptet udvidet, så der kunne tilføjes yderligere funktioner til understøttelse og administration af funktioner, der er relateret til traditionelle marketingkataloger direkte til forbrugeren. Et firma, der sælger direkte til forbrugerne, udgiver ofte trykte kataloger, som derefter sendes til et eller flere kundesegmenter. Disse kataloger indeholder normalt bestemte kampagner eller tilbud, der kun anvendes, hvis kunden kan angive en katalogidentifikationskode på tidspunktet for oprettelse af ordren. 

Firmaer, der benytter marketing direkte til forbrugerne, er meget fokuserede på at spore responsen på disse kataloger, for at sikre sig, at omkostninger til at producere og sende dem bliver dækket ind. For at spore kundernes respons er der normalt trykt en kode på bagsiden af kataloget, og denne kode skal oplyses og anvendes, når modtageren af kataloget ringer for at afgive en ordre via telefon (eller oftere skal koden nu angives, når kunden afgiver en ordre online). Der bruges forskellige betegnelser i branchen til at identificere denne katalogsporingskode (herunder nøglekode, kampagnekode, katalogkode og kildekode), men i Dynamics 365 for Retail refererer vi til koden som **Kildekode-id**.

## <a name="basic-catalog-setup"></a>Grundlæggende katalogopsætning

Gå til **Retail** > **Kataloger og sortimenter** > **Alle kataloger** for at konfigurere dit katalog.

Når du opretter et nyt katalog, skal du først knytte kataloget til en eller flere detailkanaler. Dette gøres i oversigtspanelet **Detailkanaler** i formularen **Opsætning af katalog**. Klik på **Tilføj**, og vælg en eller flere detailkanaler. Kun varer, der er knyttet til den valgte kanals [udvalg](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/assortments) kan bruges, når du opretter kataloget.

Hvis du vil føje produkter til et katalog, skal du vælge et navigationshierarki. Navigationshierarkiet understøtter kategoristrukturen for kataloget. Du skal vælge et af de navigationshierarkier, der er knyttet til detailkanaler, der er valgt i oversigtspanelet **Detailkanaler** på siden **Katalog**. Hvis en navigationskanal ikke tidligere er blevet knyttet til en kanal, kan du gå til **Detail** > **Konfiguration af kanal** > **Kanalkategorier og produktattributter** for at knytte en navigationshierarkistandard til hver af dine detailkanaler.

På menufanen **Kataloger** skal du på siden **Opsætning af katalog** klikke på **Tilføj produkter** for at konfigurere produkterne, der skal føjes til kataloget, eller vælge en node i navigationshierarkiet (hvis du vælger en node, ændres skærmpræsentationen, så du kan føje produkter direkte til en kategori i kataloget).

Klik på topnoden i kataloghierarkiet for at vende tilbage til hovedkatalogets overskriftsvisning. Konfigurer ikrafttrædelses- og slutdatoer efter behov i oversigtspanelet **Generelt**.  

Før kataloget er tilgængeligt for brug, skal det udgives. Klik på **Valider katalog** i menuen **Kataloger** for at behandle en validering. Dette er en påkrævet handling, som validerer, at den nødvendige konfiguration er korrekt. Klik på **Vis resultater** for at få vist detaljerne om valideringen. Hvis der findes fejl, skal du rette dataene og køre valideringen igen, indtil valideringen er godkendt.  

Når valideringen er bekræftet, skal du klikke på **Arbejdsgang** i menuen for at starte arbejdsgangen for godkendelsen. Klik på **Send** i menuen **Arbejdsgang** for at udføre processen. Konfigurer trinnene og de godkendte brugere for arbejdsgangen fra **Detail** > **Konfiguration af hovedkontor** > **Detailarbejdsgange**. Arbejdsgangen definerer de trin, der er nødvendige for at få vist kataloget med status **Godkendt**. Når kataloget har status **Godkendt**, kan du klikke på indstillingen **Udgiv** i menuen **Kataloger** for at fuldføre processen. Når kataloget har status **Udgivet** status, kan det bruges i callcenterets ordreindtastning og katalogafsendelsesprocesser.

## <a name="use-catalogs-to-drive-sales-order-pricing-and-promotions"></a>Bruge kataloger til salgsordrepriser og -kampagner

En grundlæggende årsag til at definere et katalog til brug i et callcenter er, at man på denne måde kan konfigurere bestemte priser og kampagner for kataloget. Kunder, der bestiller fra dette katalog, modtager disse priser og kampagner i ordreindtastningen i callcenteret, hvis katalogets **Kildekode-id** anvendes på ordrehovedet eller -linjerne.

Du kan konfigurere specifikke priser for kataloget ved at vælge indstillingen **Prisgrupper** under fanen **Kataloger** for at knytte en eller flere prisgrupper til kataloget. Alle handelsaftaler, prisjusteringskladder og særlige detailrabatter (tærskel, antal, mix og match), der er blevet knyttet til den samme prisgruppe, anvendes, når kunder bestiller fra dette katalog.

I oversigtspanelet **Kildekoder** skal du klikke på **Tilføj** for at føje en eller flere **Kildekode-id**-identifikatorer til dette katalog. Dette er den kode, der skal anvendes på salgsordrehovedet (og -linjerne) under ordreindtastningen i callcenteret. Denne kode bruges til at knytte salgsordrerne til kataloget og i sidste ende til prisgrupperne og eventuelle særlige priser og kampagner, der er konfigureret.  

## <a name="use-the-source-id-to-track-costs-and-response-rates"></a>Bruge kilde-id'et til at spore omkostninger og svarrater

Når du definerer **Kildekode-id**, kan du vælge at kæde dette id til et **Målmarkeds-id**. Dette **Målmarkeds-id** kan defineres i **Detail** > **Kunder** > **Målmarked**. Målmarkedet er en liste over kunder og/eller kundeemner, der hører til et brugerdefineret segment. Hvis du knytter kunde- eller kundeemnedataene til kildekode-id'et, giver det mulighed for at få bedre indsigt i modtagerne af kataloget. Hvis en kunde er knyttet til en målgruppe, og denne målgruppe er knyttet til et aktivt kildekode-id/-katalog, kan callcenterbrugere se, hvilke kataloger en kunde har modtaget, ved at vælge menupunktet **Kildekoder** under menufanen **Kunder** på siden **Kundeservice**. Under ordreindtastningen kan callcenterbrugerne også se de bestemte kataloger, der er sendt til en kunde på rullelisten **Kilde** i salgsordrehovedet. Hvis du ændrer filteret fra **Alle** til **Målrettede** kan brugeren få vist de specifikke aktive kataloger, som kun fik tilsendt. Dette er nyttigt i situationer, hvor kunden kan have glemt sit katalog eller ikke kan finde eller læse katalogkoden, når de ringer for at oprette en salgsordre.

Det er muligt at knytte flere kildekode-id'er til et katalog. Det er ofte nødvendigt, når en virksomhed ønsker at spore svarhyppigheden ud fra forskellige segmenter. Firmaet oplyser en entydig katalogkode til forskellige kundesegmenter, hvilket giver mulighed for at spore svarhyppigheden helt ned på segmentniveau inden for en bestemt kataloghændelse.

Hvis du vælger en bestemt **Kildekode-id**-post og klikker på indstillingen **Oplysninger** i oversigtspanelet **Kildekoder**, vises yderligere felter, hvor salgsprognoser, forsendelsesomkostninger og afsendelsesdatoer kan hentes. Disse data er nyttige, når du vil udføre detaljeret analyse af effektiviteten af kataloget. Brugere kan vende tilbage til denne side over tid og bruge knapperne **Analyse af kildekode** og **Sammenlign kampagner** til at udløse analyserapporter, der er baseret på aktuelle salgsdata og sammenligne omkostninger og budgettet med faktiske oplysninger.

## <a name="configure-catalog-specific-order-and-item-scripts"></a>Konfiguration af katalogspecifikke ordre- og varescripts 

Når callcenterbrugere opretter salgsordrer, de kan bruge scripts på skærmen. Disse tekstbaserede scripts kan give yderligere oplysninger, som brugeren skal meddele kunden, eller det kan være interne noter eller påmindelser, som callcenterbrugerne skal gennemse og reagere på, når de opretter salgsordren.  

Det er ofte nyttigt at have forskellige sæt af scripts til forskellige kataloger. I oversigtspanelet **Scripts** kan foruddefinerede scripts knyttes til et katalog. Brug feltet **Timing** til at bestemme, om scriptet skal vises i begyndelsen af ordren (så snart kildekode-id'et angives i ordrehovedet) eller i slutningen af ordren (i formularen med salgsordreoversigten).

Når du vælger en node i katalogets hierarki og arbejder med dataene i oversigtspanelet **Produkter** kan brugere også tilknytte scripts, der er specifikke for kataloger eller varer, ved hjælp af handlingen **Scripts**.  

## <a name="configure-catalog-specific-up-sell-and-cross-sell-items"></a>Konfigurere katalogspecifikt mersalg og tillægssalg

Tilknytning af forslag til mersalg eller tillægssalg for en vare kan gøres fra produktopsætningen, men i nogle tilfælde vil en virksomhed måske fremme særlige mersalg eller tillægssalg af en vare til kunder, der bestiller et bestemt produkt fra et bestemt katalog. I oversigtspanelet **Produkter** skal du vælge en vare og klikke på **Mersalg/tillægssalg af varer** for at konfigurere mersalg eller tillægssalg af produkter direkte til kunder, der køber den valgte vare fra kataloget. Under ordreindtastning i callcenteret vises katalogspecifikke varer til mersalg eller tillægssalg på skærmen i stedet for standardmersalgs- eller -tillægssalgsprodukter, der kan være konfigureret for den pågældende vare via den normale produktkonfiguration.

Mersalgs- eller tillægssalgsvarer kan også bruge scriptfunktionerne til at vise bestemte meddelelser, som en bruger får vist, når mersalgs-eller tillægssalgsvaren vises under ordreindtastningen. Scripts, der er knyttet til mersalgs-eller tillægssalgsprodukter, der er konfigureret specielt til et katalogprodukt, vises kun, når dette katalogs kildekode anvendes i ordreindtastningen i callcenteret.

## <a name="catalog-page-analysis"></a>Analyse af katalogside

Under fanen **Kataloger** findes indstillinger til at konfigurere **Katalogsider** med. Denne funktion gør det muligt at definere bestemte sider og sidetyper til udskrevne katalog og deres tilknyttede omkostninger.  

Når du konfigurerer produkterne i kataloget, kan du bruge handlingen **Layout for produktside** til at definere bestemte sider, procentdele af siden og placeringen af sidedetaljer for varen. Ved at konfigurere disse data kan brugerne udnytte **Rapport om analyse af katalogområde**. Du kan finde denne rapport ved at gå til **Detail** > **Call center-rapporter** > **Analyse af katalogområde**-rapporten. Rapporten analyserer salg via kataloget (salgsordrer, hvor kilde-id'et for kataloget er knyttet til fakturahovedet eller fakturalinjen) og den tilknyttede procentdel af side og omkostninger for at oprette en traditionel direkte markedsføringsrapport af typen **Square inches-analyse**.

## <a name="catalog-requests"></a>Kataloganmodninger

Når kataloger konfigureres og udgives i Dynamics 365 for Retail, kan funktionen **Send katalog** kan anvendes. Denne funktion er tilgængelig på siderne **Kundesøgning** og **Kundeservice**. Når du har valgt en kundepost via **Kundesøgning**, eller mens du fik vist en bestemt kundekonto fra **Kundeservice**, kan brugerne vælge indstillingen **Send katalog**, der åbner en dialogboks, hvor brugeren kan vælge på en liste over alle udgivne og aktive kataloger. Brugeren kan vælge et katalog og et antal og et bestemt kilde kode-id, der skal sendes. Når de klikker på knappen **Send**, gemmes en anmodning, der kan administreres ved at udskrive rapporten **Kataloganmodninger**. Du kan finde denne rapport ved at gå til **Detail** > **Call center-rapporter** > **Kataloganmodningsrapport**. Rapporten viser alle kataloganmodninger, herunder kundeoplysningerne som navn og adresse på den kunde, der har anmodet om kataloget. Denne rapport kan bruges internt, eller dataene kan overføres til tredjepart, som understøtter eksterne processer, som kræves for fysisk at sende kataloget til kunden.

## <a name="additional-features"></a>Yderligere funktioner

Under fanen **Kataloger** findes også indstillinger til konfiguration af en **Betalingsplan** og **Gratis produkter**. Hvis det kildekode-id, der er knyttet til kataloget, anvendes under ordreindtastningen i callcenteret, er kunden berettiget til de gratis produkter eller anvendelse af de specifikke betalingsplaner i et katalog som defineret. Hvis det er nødvendigt at angive begrænsninger, så kunden kun kan vælge mellem betalingsplaner, der er knyttet til kundens katalog, og ikke alle aktive betalingsplaner i systemet, kan afkrydsningsfeltet **Tillad kun katalogplaner** markeres for en eller flere af de kildekode-id'er, der er defineret for at gennemtvinge denne begrænsning.

## <a name="additional-notes"></a>Yderligere bemærkninger

Når et kildekode-id i øjeblikket anvendes på en salgsordre i callcenteret, bruges det til at vise priser, kampagner, scripts og mersalg eller tillægssalg, der gælder for et bestemt katalog. Systemet kan ikke forbyde eller forhindre, at et produkt, ikke der findes i kataloget, kan bestilles på salgsordren. Hvis en vare, der ikke indgår i kataloget, bestilles, bruger systemet først den **Prisgruppe**, der er defineret i callcenterkanalen (**Detail** > **Kanaler** > **Call centers** > **Alle call centers**) til varepris eller kampagner.  Hvis der ikke findes en bestemt kanalpris, bruges basissalgsprisen for varen.

