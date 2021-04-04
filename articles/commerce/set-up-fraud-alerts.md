---
title: Konfigurere og arbejde med advarsler om svindel i callcentre
description: Dette emne forklarer, hvordan du opretter regler for at advare kundeservicemedarbejdere om potentielt falske oplysninger ved behandling af ordrer. Du kan definere bestemte koder, der bruges til automatisk eller manuelt at sætte mistænkelige ordrer på hold.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 65e6e065317311395a5a5ca2b049d1c277aa5003
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264522"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Konfigurere og arbejde med advarsler om svindel i callcentre

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du definerer kriterier og regler for, hvordan potentielt falske salgsordrer sættes på hold, så de kan gennemgås yderligere. Funktionen til kontrol for svindel bruges til at bestemme gyldigheden af oplysningerne i en salgsordre. Hvis oplysningerne i salgsordren viser sig at være tvivlsomme baseret på en organisations svindelkriterier og -regler, kan ordren sættes på hold for fornyet gennemgang. I så fald kan ordren ikke frigives til lageret til yderligere behandling, før spærringen er blevet ryddet.

> [!NOTE]
> Denne funktion kan kun bruges i forbindelse med behandling af salgsordrer i Commerce-callcenterkanalen.

## <a name="turning-on-the-fraud-check-feature"></a>Aktivering af funktionen til kontrol af svindel

Hvis du vil bruge svindelkontrolfunktionen, skal du indstille **Aktivér ordrefuldførelse** i kanalen til **Ja**, når callcenterkanalen er [defineret](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options). Når ordrefuldførelse er aktiveret, skal callcenterbrugerne vælge **Fuldført** på salgsordresiden for alle salgsordrer, der oprettes. Fuldførelseshandling forårsager, at siden **Salgsordreoversigt** åbnes. Når brugerne angiver den krævede betalingsdato på siden **Salgsordreoversigt**, kan de vælge **Send** for at færdiggøre ordren. Når ordren er sendt, aktiveres svindelkontrolfunktionen, og alle regler, der er aktive i systemet, godkendes automatisk.

Callcenterbrugere kan også manuelt sætte salgsordrer på hold, så de kan gennemgås for svindel, før de vælger **Send**. Hvis du manuelt vil sætte en salgsordre på hold, skal du på siden **Salgsordreoversigt** vælge **Hold** \> **Manuelt svindelhold**. Du bliver derefter bedt om at angive en kommentar for at forklare, hvorfor du vil sætte ordren på hold. Denne kommentar vises i panelet [ordrer på hold](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) for at levere kontekst til den bruger, der gennemgår ordrer på hold, for at vedkommende kan afgøre, om ordren skal frigives.

Ud over at konfigurere **Aktivér ordrefuldførelse** i kanalen, skal du konfigurere svindelkontrolfunktionen, i Callcenter-parametre. Gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Call center-konfiguration** \> **Call center-parametre**. På siden **Call center-parametre** skal du vælge **Ja** for indstillingen **Svindelkontrol** under fanen **Spærringer**.

Under fanen **Spærringer** skal du også definere de [holdkoder](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), der skal anvendes på en ordre, der enten manuelt eller automatisk er sat på hold for gennemsyn for svindel. Indstil holdkoderne i felterne **Manuel svindelholdkode** og **Svindelholdkode**. Du kan finde det nyttigt at oprette to entydige holdkoder, så brugere, der arbejder i holdpanelet, let kan filtrere og skelne automatiske hold fra manuelle hold.

Hvis svindelkontrolfunktionen skal fungere effektivt, skal du også indstille feltet **Min. resultat**. Hvert svindelkriterium og -regel, der defineres i systemet, har et resultat. Når en salgsordre kontrolleres for svindel, og der findes en eller flere forekomster, lægges resultaterne sammen for at give ordren et samlet svindelresultat. Hvis det samlede svindelresultat for en ordre, overstiger værdien i feltet **Min. resultat**, sættes ordren automatisk på hold. Du kan vælge at bruge andre resultatrelaterede felter under fanen **Spærringer** for at definere den e-mailresultatet, telefonresultatet, postnummerresultatet og det udvidede postnummerkoderesultat. Hvis du ikke angiver et resultat for nogen af disse statiske svindelkriterier, når du definerer på dem på siden **Statiske svindeldata**, giver systemet dem et standardresultat, som du angiver under fanen **Spærringer** på siden **Call center-parametre**.

Endelig skal du bruge feltet **Svindelkommentartype** til at angive den dokumenttype, der skal bruges, når brugerne indtaster kommentarer, når de manuelt sætter en ordre på hold for gennemsyn for svindel. Oftest er dette felt indstillet til **Note**.

## <a name="defining-fraud-criteria-and-rules"></a>Definition af svindelkriterier og -regler

Systemet refererer til to typer svindelkriterier for at afgøre, om en ordre skal sættes på hold og kontrolleres for svindel:

- **Statiske svindeldata** bruger en bestemt værdi, f.eks. et telefonnummer, der er placeret på en liste over blokerede numre, eller en e-mailadresse, der er markeret, fordi den tidligere har været brugt til svindeltransaktioner. Du kan angive statiske svindeldata ved at gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Call center-konfiguration** \> **Svindel** \> **Statiske svindeldata**. På siden **Statiske svindeldata** kan du tilføje kriterier for svindel manuelt eller via dataimport. Resultater er tilknyttet oplysningerne om svindel. Hvis svindelkontrolfunktionen er aktiveret, sammenlignes hver salgsordre, der er indtastes, med de statiske data. Hvis dataene findes i debitorens faktureringsadresse eller den leveringsadresse, som er knyttet til ordrehovedet, eller hvis dataene findes i leveringsadresser, der er knyttet til nogen af linjerne i denne salgsordre, lægges resultaterne for alle entydige matches sammen og sammenlignes med **Min. resultat**-værdien for at afgøre, om ordren skal sættes på hold.

- **Regler for svindel** består af brugerdefinerede variabler og de betingelser, der er defineret for disse variabler. Du kan oprette regler ved at gå til **Retail og Commerce** \> **Konfiguration af kanal** \> **Call center-konfiguration** \> **Svindel** \> **Regler**. Et firma kan bruge svindelregler til at konfigurere et mere komplekst regelsæt, som kan indeholde **AND** eller **OR** -sætninger til evaluering af flere betingelser. En bruger vil f.eks. have, at alle ordrer fra kunder, der hører til en bestemt kundegruppe, og som har bestilt et bestemt produkt, skal sættes på hold og kontrolleres for svindel. I så fald defineres betingelser validering af kunde og produkter på siden **Regler**, og der bruges en AND-betingelse. En ordre sættes derefter kun på hold, hvis begge betingelser er opfyldt, og hvis resultatværdien, der er tildelt denne regel, samt resultatværdien af evt. andre regler, som ordren matcher, medfører, at ordrens samlede svindelresultat overskrider **Min. resultat**-værdien, der er defineret på siden **Call center-parametre**.

> [!NOTE]
> Flere regler eller overdrevent komplekse regler resulterer i dårlig systemydeevne, når salgsordrer sendes. Svindelkontrolfunktionen er ikke optimeret til at håndtere en stor mængde statiske svindeldataværdier og mange aktive regler. Husk, at alle regler evalueres, når callcenterbrugere vælger **Send** under indtastning af salgsordren. Reglerne skal evalueres mod salgsordrehovedet og alle ordrelinjer. Jo flere regler og jo mere avancerede regelsætninger der er, desto længere tid tager behandlingen. Hvis der er mange linjeelementer i din ordre, og mange aktive regler og statiske dataværdier, kan den automatiske proces for gennemsyn og validering af alle data og beregning af et svindelresultat påvirke ydeevnen markant. Organisationer, der bruger denne funktion skal altid teste og bekræfte, at behandlingstiden ved ordreafgivelse er acceptabelt, før de anvender ændringer af regler eller statiske svindelkriterier på produktionsmiljøet.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Identificere ordrer, der er på hold for at blive kontrolleret for svindel

Når callcenterbrugere sender en salgsordre, og hvis ordren matcher kriterierne for svindel eller regler, og hvis resultatet er større end minimumresultatet, modtager brugerne en advarsel om, at ordren er blevet sat på hold. Brugerne kan lukke denne meddelelse, fordi den kun er til orientering. Brugerne kan vælge at kommunikere disse oplysninger til kunden. Virksomheden skal undersøge, hvilken protokol brugerne følger i denne situation.

Ordren gemmes, men flaget **Udfør ikke behandling** er angivet for den. Dette flag er med til at sikre, at ordren ikke kan frigives til lagerstedet. Når som helst kan brugere se indstillingen af flaget **Udfør ikke behandling** for en salgsordre på siden **Detaljeret status**. Denne side kan åbnes fra siderne **Alle salgsordrer** og **Kundeservice**. Systemet opdaterer også værdien af feltet **Detaljeret status** for ordren til **Svindelhold**.

Du kan se og administrere de ordrer, der er på hold for kontrol af svindel, ved at gå til **Retail og Commerce** \> **Kunder** \> **Ordrer på hold**. På siden **Ordrer på hold** skal du vælge en post på listen og derefter klikke på **Ordre på hold** for at se en mere detaljeret visning, der omfatter oplysninger om årsagen til spærringen. I oversigtspanelet **Svindeldetaljer** kan du se de systematiske svindelkriterier, der er fundet som match for ordren, og de resultater, der er anvendt. Hvis ordren blev sat på hold manuelt, kan du gennemse eventuelle kommentarer, der er angivet af den bruger, der satte ordren på hold, ved at se i sektionen **Svindelnoter** i oversigtspanelet **Noter**.

Du kan finde flere oplysninger om, hvordan du arbejder med ordrer på hold, under [Ordrer på hold](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).


[!INCLUDE[footer-include](../includes/footer-banner.md)]