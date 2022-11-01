---
title: Automatisere finansudligninger
description: Denne artikel indeholder oplysninger om at automatisere finansudligningsprocessen.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708326"
---
# <a name="automate-ledger-settlements"></a>Automatisere finansudligninger

[!include [banner](../includes/banner.md)]

I Microsoft Dynamics 365 Finance version 10.0.31 er funktionen  **Automatiser finansudligningsproces** tilgængelig i arbejdsområdet  **Funktionsstyring** . Du kan kun aktivere funktionen **Automatiser finansudligningsproces**, hvis funktionen **Opmærksomhed mellem finansudligning og årsafslutning** er aktiveret.

Med Finansudligning kan du sammenholde debet- og kreditposteringer i finansmodulet. Organisationer, der udfører finansudligningsaktiviteter på en tilbagevendende tidsplan, kan nu automatisere processen. Under den automatiske finansudligningsproces kan en debetpostering og en kreditpostering kun afstemmes automatisk, hvis beløbene i regnskabsvalutaen er ens. Et debetbeløb på $1,00 kan f.eks. automatisk sammenholdes med et kreditbeløb på $1,00. Men en debetværdi på $1,00 kan ikke automatisk afstemmes med to krediteringer, som hver især har værdien $0,50. Delvis sammenholdelse af finansposteringsbeløb understøttes ikke.

Automatisering af finansudligning definerer følgende detaljer:

- Når der køres finansudligninger
- Hvilke kriterier der bruges til at afstemme de debiteringer og krediteringer, der kan udlignes automatisk
- Hvilken rækkefølge finansudligningsoplysningerne behandles i

## <a name="define-the-occurrence-of-ledger-settlements"></a>Definere forekomsten af finansudligninger

Automatisering af finansudligning bruger struktur for procesautomatisering. Forskellige forretningsprocesser bruger denne struktur til at definere gentagelsen af en valgt proces. I forbindelse med finansudligninger skal du gå til  **Systemadministration \> Opsætning \> Procesautomatiseringer** eller **Finans \> Opsætning Finans \> Procesautomatiseringer**.

Vælg først indstillingen  **Opret ny procesautomatisering**, og vælg  **Finansudligninger**. En guide fører dig derefter igennem processen for opsætning af automatiseringen.

## <a name="general-page"></a>Siden Generelt

På siden  **Generelt**  i guiden skal du angive navnet på forekomsten af finansudligning, som du opretter. Hvis dine matchende debiteringer og krediteringer f.eks. udlignes på finanskontoen om mandagen, skal du angive et sigende navn, f.eks. **. Finansudligning\_Man**. Det navn, du angiver, vises i kolonnen **Automatisk regel** på siden **Finansudligninger** .

De resterende indstillinger på siden er generiske og definerer forekomstmønsteret for denne version af finansudligningerne. Hvis en forekomst f.eks. er til mandag, kan du definere den, så den kører en gang om ugen, og du kan vælge mandag som dag i ugen, hvor den skal køres. Du kan også angive et tidspunkt for tidlig planlægning, f.eks. kl. 2, så procesautomatiseringen er fuldført før starten på næste arbejdsdag. Det anbefales, at du planlægger procesautomatiseringen, så den udføres uden for normal arbejdstid. På den måde kan du reducere indflydelsen på regnskabsmedarbejderne i løbet af arbejdsdagen.

Yderligere oplysninger om de andre felter på siden  **Generelt**  finder du i dokumentationen til procesautomatisering.

## <a name="ledger-settlements-match-criteria-page"></a>Siden Matchkriterier for finansudligninger

Den næste side i guiden er  **Matchkriterier for finansudligninger** . Den bruges til at definere de hovedkonti, der er medtaget i forekomsten af procesautomatisering, og de kriterier, der bruges til at bestemme sammenholdelse af debiteringer og krediteringer.

### <a name="account-selection"></a>Kontovalg

De hovedkonti, du tidligere har defineret som finansudligningskonti for den juridiske enhed, vises. (Du definerer hovedkonti som finansudligningskonti i **Finans \> Opsætning Finans \> Finansparametre \> Finansudligninger**.)

### <a name="main-account-and-posting-layer"></a>Hovedkonto og posteringslag

Værdierne  **Hovedkonto** og **Posteringslag** er påkrævede matchkriterier. Værdierne **Hovedkonto** og **Posteringslag** for finansdebet- og kredittransaktionerne skal have være ens for at blive afstemt under den automatiske finansudligningsproces.

### <a name="posting-type"></a>Bogføringstype

Vælg indstillingen **Bogføringstype**, hvis finansdebet- og kredittransaktionerne skal have samme bogføringstype for at blive afstemt under den automatiske finansudligningsproces.

### <a name="financial-dimensions"></a>Økonomiske dimensioner

Vælg indstillingen **Økonomiske dimensioner**, hvis finansdebet- og kredittransaktionerne skal have samme økonomiske dimensioner for at blive afstemt under den automatiske finansudligningsproces. Når denne indstilling er valgt, skal kriterierne for økonomiske dimensionsværdier være valgt på listen **Tilgængelige økonomiske dimensioner**. Listen **Tilgængelige økonomiske dimensioner** indeholder ikke hovedkontodimensionen, da den automatisk kræves som del af matchkriterierne.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Vise resultaterne af finansudligningsautomatiseringen

Når automatiseringsserien for finansudligning er oprettet, vises hændelserne for hver finansudligning i en ugentlig visning af automatiseringsprocesserne. Desuden vises status for hver forekomst. Følgende statusangivelser bruges:

- **Planlagt**  – Automatiseringen er planlagt, men er endnu ikke kørt.
- **Afvikling** – Automatiseringen kører i øjeblikket.
- **Fejl**  – Automatiseringen er kørt, men der opstod en fejl. Du kan få vist fejlene ved at vælge knappen  **Vis resultater** .
- **Fuldført** – Automatiseringen er blevet kørt. Du kan få vist udligningsresultaterne på siden **Finansudligninger**.

Du kan se afstemningsresultaterne ved at gå til **Finans \> Periodiske opgaver \> Finansudligninger**. Feltet **Automatiseringsregel** på siden **Finansudligninger** viser navnet på den automatiserede finansudlignings planlagte opgave, der blev brugt til at udligne transaktionen. Mislykkede udligningsforsøg opdaterer ikke værdien af **Automatiseringsregel**. Hvis du manuelt tilbagefører en transaktion, der tidligere er blevet udlignet med automatiseringsprocessen, fjernes værdien for **Automatiseringsregel**.

I feltet **Dato for udligning** for de matchede poster vises den dato, hvor automatiseringsprocessen blev udført.

## <a name="editing-a-ledger-settlement-automation"></a>Redigering af en automatisering af finansudligning

Via automatiseringsstrukturen kan du redigere serien og de forekomster, der er oprettet for finansudligningen. Serien kan redigeres enten fra siden **Procesautomatisering** eller i den ugentlige visning af procesautomatiseringer. Hvis chefen f.eks. beslutter at udføre finansudligning onsdag i stedet for mandag, kan denne finde en forekomst i den ugentlige visning og vælge  **Vis/rediger – serie**.

Hvis du redigerer en serie, beder systemet dig om at angive, om ændringen skal foretages i alle eksisterende forekomster eller kun i nye forekomster. Historiske forekomster, der allerede har statussen **Fuldført**, eller som er afsluttet i en  **Fejl** -status, ændres ikke.

Du kan også tilføje en ny forekomst eller ændre en eksisterende forekomst. Den næste forekomst af finansudligning er f.eks. planlagt til at køre onsdag den 1. januar, men denne dato er en helligdag. Du kan ændre forekomsten fra enten siden  **Procesautomatisering** eller ugentlige visning af procesautomatiseringer. Der åbnes en side, som viser oplysninger om tidsplan og søgekriterier. Her kan du redigere den planlagte tid og dato. Du kan også redigere søgekriterierne, hvis der kræves ændringer. 

Du kan også deaktivere en forekomst eller en serie. Hvis du vil deaktivere en forekomst og suspendere behandlingen af den, skal du vælge den i den ugentlige visning af procesautomatiseringer og derefter vælge  **Deaktiver**. Du kan deaktivere en serie på siden **Procesautomatisering** .

## <a name="security-for-ledger-settlement-automation"></a>Sikkerhed for automatisering af finansudligning

Opgaven **Vedligehold Indstillinger for automatisering af finansudligninger** er føjet til rollerne Regnskabschef og Regnskabsansvarlig, og opgaven **Vis Indstillinger for automatisering af finansudligninger** er føjet til rollerne Bogholder, Regnskabschef og Regnskabsansvarlig for finansudligningers automatisering. Disse opgaver er standardsikkerhedsindstillingerne, men de kan ændres ud fra organisationens behov.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Finansparametre for automatisering af finansudligning

Feltet **Typisk udligningssaldo** angiver den rækkefølge, som den automatiske finansudligning behandles i. Hvis du vil konfigurere eller se værdien af **Typisk udligningssaldo**, skal du gå til **Finans \> Opsætning \> Finansparametre** og vælge fanen **Finansudligninger**.

Hvis **Debet** er valgt, starter den automatiske finansudligningsproces på debetsiden, og der søges efter tilsvarende kreditter. Hvis **Kredit** er valgt, starter den automatiske finansudligningsproces på kreditsiden, og der søges efter tilsvarende debiteringer. Denne indstilling skal afspejle den typiske saldo for hovedkontoen.

## <a name="processing-a-ledger-settlement-automation"></a>Behandling af en automatisering af finansudligning

Når automatiseringen køres, vælger systemet finanstransaktioner for de hovedkonti, der er defineret for serien til procesautomatisering. Den bestiller transaktionerne efter dato ved hjælp af et datointerval fra starten af regnskabsåret til den dato, hvor procesautomatiseringen køres. Den afstemmer baseret på de angivne søgekriterier. De absolutte værdier for regnskabsvalutabeløbene i debet og kredit skal stemme overens for at blive udlignet.

Mens en hovedkonto behandles af en forekomst af automatisk finansudligning, kan du ikke få den vist på siden **Finansudligninger**. Du skal vente, indtil automatiseringsprocessen er fuldført. Det anbefales, at du planlægger procesautomatiseringen til at køre uden for arbejdstiden for at undgå konflikter.

Automatiseringsprocessen omfatter alle de transaktioner, der opfylder kriterierne, med undtagelse af transaktioner, der er markeret manuelt til udligning på siden **Finansudligninger**.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Tilbageførsel af transaktioner, der udlignes via automatiseringsprocessen

Du kan tilbageføre en udligning, der er foretaget af den automatiske finansudligningsproces. Hvis en transaktion, der er blevet udlignet med automatiseringsprocessen, tilbageføres, fjernes værdien for **Automatiseringsregel**.
