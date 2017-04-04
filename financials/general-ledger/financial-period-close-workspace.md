---
title: "Arbejdsområde til afslutning på regnskabsperiode"
description: "Denne artikel indeholder en oversigt over arbejdsområdet Afslutning på regnskabsperiode og den tilknyttede konfiguration."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Arbejdsområde til afslutning på regnskabsperiode

Denne artikel indeholder en oversigt over arbejdsområdet Afslutning på regnskabsperiode og den tilknyttede konfiguration.

Arbejdsområde til afslutning på regnskabsperiode

Den **regnskabsperiode tæt** arbejdsområde kan du spore din afsluttende økonomiske processer på tværs af firmaer, områder og personer. Afhængigt af din visning af den **regnskabsperiode tæt** arbejdsområde, får du vist enten alle opgaverne og statusserne for en tidsplan for lukningen eller blot de opgaver, der er tildelt til dig. 

Du skal først vælge en afsluttende plan øverst i arbejdsområdet. Alle data, der vises i arbejdsområdet filtreres derefter af den valgte lukning tidsplan.

### <a name="summary-tiles"></a>Oversigt over felter

Feltet **Oversigt** giver et overblik over processen og indikatorer, der hjælper dig med at holde ultimoprocessen på sporet. Du kan se opgaver, der ligger efter forfaldsdato resterende opgaver i dag, opgaver, der forfalder i dag, men er blokeret på grund af afhængigheder og alle resterende opgaver for processen. Disse oplysninger er for alle selskaber, der er inkluderet i den valgte lukning tidsplan.

### <a name="tasks-and-status-section"></a>Opgaver og statussektion

I den **opgaver og status** afsnit, status for samlet tidsplan for lukningen er fordelt på forskellige måder: status ved virksomhedens status efter område og status af person, der er ansvarlig. Du kan få vist status for alle opgaver i afsluttende planlægger, blot de opgaver, der forfalder i dag, eller opgaver, der er forfaldne ved at ændre filteret i toppen af listen over kort. Du kan også vælge filteret virksomhed til at få vist status for en bestemt virksomhed. Hver medarbejder får en opdeling efter procent, som er afsluttet, og antallet af opgaver, der er tilbage. Klik på kortet eller **få vist oplysninger om** handling for at filtrere listen over detaljerede opgave ved det valgte kort. 

Den sidste fane er detaljeret opgaveliste. Denne liste viser hele opgavelisten og kan filtreres, så den kun viser de opgaver, du er interesseret i. Du kan filtrere listen over opgaver på flere måder. For eksempel kan du filtrere efter opgave forfaldsdato, tilknyttede firma og tilknyttede område. Du kan også vælge at vise eller skjule fuldførte opgaver på opgavelisten. 

To indikatorer bruges til opgaver:

-   Et udråbstegn ikon angiver, at opgaven er forfaldne. Opgaver, der er overskredet, er forfaldsdatoen også fremhævet med rødt.
-   Et hængelåsikon betyder, at opgaven afhænger af andre opgaver, der endnu ikke er fuldført. En opgave, der er blokeret af afhængigheder kan ikke markeres som fuldført. Du kan angive afhængigheder for en opgave ved hjælp af den **angive afhængighed** handling.

Opgavenavnet er et hyperlink til Microsoft Dynamics 365 for operationer side eller en anden webside, hvor brugeren skal gå til at afslutte arbejdet. Du kan angive dette hyperlink ved hjælp af den **opgavekæde** når du redigerer eller opretter en opgave. 

Du kan vedhæfte filer, noter, billeder og URL-adresser til en opgave ved hjælp af den **vedhæftede filer** handling. Du kan for eksempel angive kladdenumre, som bruges som en del af en opgave, tilføje kommentarer til en bestemt opgave eller vedhæfte en rapportfil, der blev udskrevet på en opgave. Der vises et ikon i den **vedhæftet** kolonne for opgaven, hvis en vedhæftet fil, der findes. 

Den **opgave fuldføres** indstilling skal være valgt manuelt, efter at opgaven er udført. Når en opgave er markeret som fuldført, den **afsluttet dato** opdateres automatisk til den aktuelle dato og klokkeslæt. Afhængighed indikatorer også opdateres efter behov.

## <a name="all-financial-period-close-tasks-list-page"></a>Listesiden Alle opgaver til afslutning på regnskabsperiode
Du kan få vist alle aktuelle og forrige periode Luk opgaver fra den **alle regnskabsperiode Luk opgaver** listeside. Denne listeside er bedst egnet til historisk analyse af den afsluttende proces, fordi den indeholder oplysninger om den planlagte forfaldsdato, den faktiske slutdato og den person, der har fuldført opgaven. Du kan let eksportere oplysningerne på denne listeside til Microsoft Excel til rapportering og overvågningsformål.

## <a name="financial-period-close-configuration-page"></a>Siden Konfiguration af afslutning på regnskabsperiode
Før du kan bruge den **regnskabsperiode tæt** arbejdsområde, skal du konfigurere processen i Microsoft Dynamics 365 for operationer ved hjælp af den **økonomiske periode Luk konfiguration** side. (Klik på **Finans**&gt;**periode lukke**&gt;**økonomiske periode Luk konfiguration**.)

### <a name="resources"></a>Ressourcer

På den **ressourcer** fane, du definerer de personer, der er involveret i de afsluttende processer. En medarbejder, der skal være ansvarlig for en afsluttende opgave skal først tildeles her. Du skal også angive medarbejderens visning af arbejdsområdet. Følgende valgmuligheder er tilgængelige:

-   **Kun tildelte opgaver** – Brugeren ser kun de opgaver, der er tildelt ham eller hende.
-   **Alle opgaver og statusser** – Brugeren får vist alle ultimoopgaver og status for den overordnede proces.

Brugere, der kun har tilladelse til at få vist de tildelte opgaver, kan ikke føje opgaver til opgavelisten, redigere opgaver eller fjerne opgaver fra opgavelisten.

### <a name="task-areas"></a>Opgaveområder

Opgaveområder bruges til at gruppere ultimoopgaver i logiske områder af ejerskab i organisationen. Kreditor, Debitor eller Finans kan eksempelvis bruges som opgaveområder.

### <a name="calendars"></a>Kalendere

Opret og rediger økonomiske afsluttende kalenderne under fanen kalendere.  Dette er, hvor du vil definere arbejdsdage til lukning af processer, og der skal bruges til planlægning af lukningsopgaver.  Oprette en ny kalender, og angiver arbejdsdagene, der skal bruges til opgaveplanlægningen.  Det er bedst at oprette en kalender i lang tid som et år eller flere år, da det kan redigeres efter oprettelsen.  Efter oprettelsen af kalenderen, skal du klikke på knappen Rediger for at opdatere kalenderen for bestemte dage f.eks.  Afsluttende opgaver planlægges på dage, hvor værdien i kontrolelementet er angivet til åben.  Hvis afsluttende opgaver ikke bør planlægge på en bestemt dag, skal på dagen have værdien i kontrolelementet, angive til afsluttet.

### <a name="templates"></a>Skabeloner

Du kan bruge en økonomisk Luk skabelon til at definere alle opgaver, der er en del af en afsluttende proces. En afsluttende opgave er en tilbagevendende indsats for arbejde, der er tildelt en person til at udføre som en del af hver lukningsprocessen. I skabelonen, en relativ forfaldsdato dato skal være defineret for hver enkelt afsluttende opgave. Den relative forfaldsdato dato er antallet dage før eller efter den definerede Periodeslutning dato, opgaven er forfaldne hver periode. En Forfaldstiden knyttes også til hver opgave. Forfaldstiden er angivet ved hjælp af som led i din tidszone og vil blive konverteret til tidszonen for hver bruger. 

Du kan tildele en opgave i skabelonen til en eller flere virksomheder, hvor opgaven gælder. Hvis en anden person er tildelt til at udføre dette arbejde indsats i hvert enkelt regnskab, kan det være nyttigt at oprette flere opgaver til den samme satsning på arbejde. Oprette én opgave for hver virksomhed 

Den **opgavekæde** menupunkt er knyttet til den opgave arbejde indsats og kan bruges til at gå direkte til den tilknyttede side fra opgavekæde i arbejdsområdet. For eksempel en afsluttende opgave at køre processen til værdiregulering af valuta for kreditor kan knyttes til de tilknyttede **værdiregulering af udenlandsk valuta** side i Microsoft Dynamics 365 for operationer. Du kan også foretage sammenkædning til en ekstern URL-adresse. 

> [! Tip] Hvis du vil sammenkæde en bestemt Management Reporter-rapport til en økonomisk periode Luk opgave, kan du bruge Webadressen til report. For at få adgang til Webadressen til report, åbne rapporten i report designer og derefter klikke på **fil**&gt;**se rapport** til at åbne rapporten i en webbrowser. Du kan derefter kopiere URL-adressen på browserens adresselinje og indsætte den i **URL-adressen** til feltet **Opgavelink**. 

Du kan definere opgaveafhængigheder i skabelonen. Hvis en opgave er angivet til at afhænge af en eller flere opgaver, kan opgaven ikke markeres som fuldført, indtil alle afhængigheder er opfyldt. 

Du kan oprette flere finansielle Luk skabeloner. Du kan derefter bruge de forskellige skabeloner til at registrere de afsluttende processer for forskellige perioder, f.eks. månedsafslutning eller årets slutning, eller til at registrere virksomheder, der bruger forskellige lukning. Når der oprettes en skabelon, kan du kopiere den til en ny skabelon og foretage de nødvendige ændringer. Du kan tildele kun én skabelon til hver afsluttende tidsplan.

### <a name="closing-schedules"></a>Ultimo tidsplaner

Du kan bruge en afsluttende tidsplan til at tildele finansielle Luk skabelon til en bestemt regnskabsperiode, der skal lukkes. Opgaver fra skabelonen oprettes derefter automatisk i den angivne periode, og den nye tidsplan for lukningen er føjet til arbejdsområdet. Når du opretter en ny plan i lukning den **slutdato for** felt bruges til at bestemme forfaldsdatoen datoer for de afsluttende opgaver, baseret på den relative forfaldsdato dato, der er tildelt i økonomiske Luk skabelonen. 

Tildel den kalender, der er relevante for den afsluttende tidsplan til at angive arbejdsdagene, der skal bruges i opgaveplanlægningen. Hvis du ikke definerer en bestemt kalender, opgaven forfalder datoer vil bruge alle ugens dage. 

Du skal også definere de virksomheder, der er knyttet til den afsluttende tidsplan. Hvis skabelonen opgaver tildeles til flere firmaer, oprettes separate opgaver for hvert regnskab, der er i den afsluttende plan og tildeles opgaven skabelon. 

Efter en tidsplan for lukningen er fuldført, kan du vælge den **lukket** indstilling for den. Tidligere opgaver vil fortsat være tilgængelig fra den **alle regnskabsperiode Luk opgaver** listeside, men afsluttende planen vil blive fjernet fra arbejdsområdet. Efter en tidsplan for lukningen er markeret som **lukket**, du vil ikke kunne tilføje opgaver, redigere opgaver eller fjerne opgaver fra den.


