---
title: Arbejdsområde til afslutning på regnskabsperiode
description: Denne artikel indeholder en oversigt over arbejdsområdet Afslutning på regnskabsperiode og den tilknyttede konfiguration.
author: ShylaThompson
manager: AnnBe
ms.date: 11/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab00a5dba10b4318b66734329c097d239dcc868c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839177"
---
# <a name="financial-period-close-workspace"></a>Arbejdsområde til afslutning på regnskabsperiode

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over arbejdsområdet Afslutning på regnskabsperiode og den tilknyttede konfiguration.

Arbejdsområde til afslutning på regnskabsperiode

I arbejdsområdet **Afslutning på regnskabsperiode** kan du spore dine afsluttende regnskabsprocesser på tværs af firmaer, områder og personer. Afhængigt af din visning af arbejdsområdet **Afslutning på regnskabsperiode** kan du se enten alle opgaver og statusser for en ultimotidsplan eller blot de opgaver, der er tildelt til dig. 

Du skal først vælge en ultimotidsplan øverst i arbejdsområdet. Alle data, der vises i arbejdsområdet, filtreres derefter af den valgte ultimotidsplan.

### <a name="summary-tiles"></a>Oversigt over felter

Felterne **Oversigt** giver et overblik over processen, og indikatorer hjælper dig med at holde lukningsprocessen på sporet. Du kan se de opgaver, der er forfaldne, resterende opgaver for dags dato, opgaver, der forfalder i dag, men er blokeret på grund af afhængigheder, og alle de resterende opgaver for processen. Disse oplysninger er for alle firmaer, der er inkluderet i den valgte ultimotidsplan.

### <a name="tasks-and-status-section"></a>Opgaver og statussektion

I afsnittet **Opgaver og status** er status for den samlede ultimotidsplan opdelt på forskellige måder: status efter virksomhed, status efter område og status efter ansvarlig person. Du kan få vist status for alle opgaver i ultimotidsplanen, blot de opgaver, der forfalder i dag, eller opgaver, der er forfaldne, ved at ændre filteret i toppen af listen over kort. Du kan også vælge virksomhedsfilteret for at få vist status for en bestemt virksomhed. Hver statusfane viser en opdeling efter den procentdel, som er afsluttet, og antallet af opgaver, der er tilbage. Klik på kortet eller handlingen **Vis detaljer** for at filtrere den detaljerede opgaveliste efter det valgte kort. 

Den sidste fane er for den detaljerede opgaveliste. Denne liste viser hele opgavelisten og kan filtreres, så den kun viser de opgaver, du er interesseret i. Du kan filtrere opgavelisten på flere måder. For eksempel kan du filtrere efter opgavens forfaldsdato, det tilknyttede firma og det tilknyttede område. Du kan også vælge at vise eller skjule fuldførte opgaver på opgavelisten. 

To indikatorer bruges til opgaver:

-   Et ikon med et udråbstegn angiver, at opgaven er forfalden. For opgaver, der er forfaldne, er forfaldsdatoen også fremhævet med rødt.
-   Et hængelåsikon betyder, at opgaven afhænger af andre opgaver, der endnu ikke er fuldført. En opgave, der er blokeret af afhængigheder, kan ikke markeres som fuldført. Du kan angive afhængigheder for en opgave ved hjælp af handlingen **Indstil afhængighed**.

Opgavenavnet er et hyperlink til siden Microsoft Dynamics 365 for Operations eller en anden webside, som brugeren skal gå til for at fuldføre arbejdet. Du kan angive dette hyperlink ved hjælp af feltet **Opgavelink**, når du redigerer eller opretter en opgave. 

Du kan vedhæfte filer, noter, billeder og URL-adresser til en opgave ved hjælp af handlingen **Vedhæftede filer**. Du kan for eksempel angive kladdenumre, som bruges som en del af en opgave, tilføje kommentarer til en bestemt opgave eller vedhæfte en rapportfil, der er blevet udskrevet for en opgave. Der vises et ikon i kolonnen **Vedhæftet fil** for opgaven, hvis der findes en vedhæftet fil. 

Indstillingen **Opgave fuldført** skal vælges manuelt, efter at opgaven er fuldført. Når en opgave er markeret som fuldført, opdateres feltet **Fuldførelsesdato** automatisk med den aktuelle dato og klokkeslæt. Afhængighedsindikatorer opdateres også efter behov.

## <a name="all-financial-period-close-tasks-list-page"></a>Listesiden Alle opgaver til afslutning på regnskabsperiode
Du kan få vist alle aktuelle og forrige periode afslutningsopgaver fra listesiden **Alle opgaver til afslutning på regnskabsperiode**. Denne listeside er bedst egnet til historisk analyse af afslutningsprocessen, fordi den indeholder oplysninger om den planlagte forfaldsdato, den faktiske slutdato og den person, der har fuldført opgaven. Du kan let eksportere oplysningerne på denne listeside til Microsoft Excel til rapporterings- og overvågningsformål.

## <a name="financial-period-close-configuration-page"></a>Siden Konfiguration af afslutning på regnskabsperiode
Før du kan bruge arbejdsområdet **Afslutning på regnskabsperiode**, skal du konfigurere processen i Microsoft Dynamics 365 for Finance and Operations ved hjælp af siden **Konfiguration af afslutning på regnskabsperiode**. (Klik på **Finans** &gt; **Luk periode** &gt; **Konfiguration af afslutning på regnskabsperiode**).

### <a name="resources"></a>Ressourcer

Under fanen **Ressourcer** kan du definere de personer, der er involveret i de afsluttende processer. En medarbejder, der skal være ansvarlig for en afsluttende opgave, skal først tildeles her. Du skal også angive medarbejderens visning af arbejdsområdet. Følgende valgmuligheder er tilgængelige:

-   **Kun tildelte opgaver** – Brugeren ser kun de opgaver, der er tildelt ham eller hende.
-   **Alle opgaver og statusser** – Brugeren får vist alle ultimoopgaver og status for den overordnede proces.

Brugere, der kun har tilladelse til at få vist de tildelte opgaver, kan ikke føje opgaver til opgavelisten, redigere opgaver eller fjerne opgaver fra opgavelisten.

### <a name="task-areas"></a>Opgaveområder

Opgaveområder bruges til at gruppere ultimoopgaver i logiske områder af ejerskab i organisationen. Kreditor, Debitor eller Finans kan eksempelvis bruges som opgaveområder.

### <a name="calendars"></a>Kalendere

Oprette og redigere kalendere for ultimoposteringer ved hjælp af fanen Kalendere. Det er her, du definerer arbejdsdagene til ultimoprocesser, og du bruger dem til planlægning af ultimoopgaver.  Opret en ny kalender, og angiv de arbejdsdage, der skal bruges til opgaveplanlægningen.  Det er bedst at oprette en kalender til en længere periode som f.eks. et år eller flere år, da den kan redigeres efter oprettelsen.  Efter oprettelsen af kalenderen skal du klikke på knappen Rediger for at opdatere kalenderen for bestemte dage f.eks. helligdage.  Afsluttende opgaver planlægges på dage, hvor værdien i kontrolelementet er indstillet til Åben.  Hvis afsluttende opgaver ikke skal planlægges på en bestemt dag, skal denne dag i kontrolelementet have værdien Lukket.

### <a name="templates"></a>Skabeloner

Du kan bruge en skabelon for afslutning af finans til at definere alle opgaver, der er en del af en afsluttende proces. En afsluttende opgave er en tilbagevendende arbejdsindsats, der er tildelt en person som del af hver afsluttende proces. I skabelonen skal der være defineret en relativ forfaldsdato for hver enkelt afsluttende opgave. Den relative forfaldsdato er antal dage før eller efter den definerede periodeafslutningsdato, hvor opgaven forfalder. Et forfaldstidspunkt knyttes også til hver opgave. Forfaldstidspunktet er angivet med brug af din tidszone og vil blive konverteret til tidszonen for hver bruger. 

Du kan tildele en opgave i skabelonen til en eller flere virksomheder, hvor opgaven gælder. Hvis en anden person er tildelt til at udføre dette arbejde i hvert enkelt virksomhed, kan det være nyttigt at oprette flere opgaver til den samme arbejdsindsats. Oprette én opgave for hver virksomhed 

Menupunktet **Opgavelink** er knyttet til arbejdsindsatsen for opgaven og kan bruges til at gå direkte til den tilknyttede side fra opgavelinket i arbejdsområdet. En afsluttende opgave, der kører processen til valutaregulering for Kreditor, kan f.eks. knyttes til den tilhørende side med **Kursregulering** i Microsoft Dynamics 365 for Finance and Operations. Du kan også foretage sammenkædning til en ekstern URL-adresse. 

> [!TIP]
> Hvis du vil sammenkæde en bestemt Management Reporter-rapport med en opgave til afslutning på regnskabsperiode, kan du bruge URL-adressen til rapporten. For at få adgang til URL-adressen til rapporten skal du åbne rapporten i rapportdesigneren og derefter klikke på **Filer** &gt; **Vis rapport** for at åbne rapporten i en webbrowser. Du kan derefter kopiere URL-adressen på browserens adresselinje og indsætte den i **URL-adressen** til feltet **Opgavelink**. 

Du kan definere opgaveafhængigheder i skabelonen. Hvis en opgave er indstillet til at afhænge af en eller flere opgaver, kan opgaven ikke markeres som fuldført, før alle afhængigheder er opfyldt. 

Du kan oprette flere skabeloner for afslutning af finans. Du kan derefter bruge de forskellige skabeloner til at registrere ultimoprocesserne for forskellige periodetyper, f.eks. månedsafslutning eller årets slutning, eller til at spore virksomheder, der bruger forskellige ultimoprocesser. Når der er oprettet en skabelon, kan du kopiere den til en ny skabelon og foretage de nødvendige ændringer. Du kan tildele kun én skabelon til hver ultimotidsplan.

### <a name="closing-schedules"></a>Ultimo tidsplaner

Du kan bruge en ultimotidsplan til at tildele en skabelon for afslutning på finans til en bestemt regnskabsperiode, der skal lukkes. Opgaverne fra skabelonen oprettes derefter automatisk for den angivne periode, og den nye ultimotidsplan føjes til arbejdsområdet. Når du opretter en ny ultimotidsplan, bruges feltet **Periodens slutdato** til at bestemme de faktiske forfaldsdatoer for ultimoopgaverne baseret på den relative forfaldsdato, der er tildelt skabelonen for afslutning på finans. 

Tildel den kalender, der er relevant for ultimotidsplanen, for at angive de arbejdsdage, der skal bruges i opgaveplanlægningen. Hvis du ikke definerer en bestemt kalender, vil alle ugens dage blive anvendt som forfaldsdatoer for opgaven. 

Du skal også definere de virksomheder, der skal knyttes til ultimotidsplanen. Hvis skabelonopgaver tildeles flere virksomheder, oprettes der separate opgaver for hver virksomhed, der er i ultimotidsplanen, og de tildeles skabelonopgaven. 

Når en ultimotidsplan er fuldført, skal du vælge indstillingen **Lukket** for den. Opgavehistorikken vil fortsat være tilgængelig fra listesiden **Alle opgaver til afslutning på regnskabsperiode**, men ultimotidsplanen fjernes fra arbejdsområdet. Når en ultimotidsplan er fuldført, skal du vælge indstillingen **Lukket**, kan du ikke føje opgaver til den, redigere opgaver eller fjerne opgaver fra den.



