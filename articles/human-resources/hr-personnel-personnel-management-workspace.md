---
title: Arbejdsområde til personalestyring
description: Dette emne indeholder en beskrivelse af de grundlæggende elementer i arbejdsområdet til personalestyring.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8b7493aa2df65b42d0da8a451c40cccafbc1cda8
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689460"
---
# <a name="personnel-management-workspace"></a>Arbejdsområde til personalestyring


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbejdsområdet **Personalestyring** indholder en stor mængde indhold. Det indeholder personalebevægelser, sporer medarbejderændringer, ledige stillinger, adresseændringer, udløbsposter og analyser, og det indeholder links til specifikke oplysninger. Dette emne indeholder detaljerede oplysninger om de enkelte dele i arbejdsområdet.

## <a name="activity-tab"></a>Fanen Aktivitet

Fanen **Aktivitet** indeholder sektioner, der grupperer arbejdere baseret på deres stadie i ansættelsesprocessen:

- **Kandidater, der skal ansættes**
- **Starter snart**
- **Seneste ansættelser**
- **Afslutter**
- **Afsluttede**

Når en arbejder er i et af disse stadier, er specifikke handlinger tilgængelige som en knap på kortet eller i den menu, der vises, når du vælger ellipsen (**...**) i øverste højre hjørne. Følgende undersektioner beskriver sektionerne under fanen **Aktivitet** og viser de handlinger, der er tilgængelige.

### <a name="candidates-to-hire"></a>Kandidater, der skal ansættes

Sektionen **Kandidater, der skal ansættes** i arbejdsområdet udfyldes fra flere kilder:

- En OData-enhed (Open Data Protocol)
- Integration af LinkedIn
- Data, der angives manuelt i produktet

Når kandidaterne vises i sektionen **Kandidater, der skal ansættes**, kan du udføre følgende handlinger ved at vælge ellipsen på kandidatkortet:

- **Afvis kandidat**
- **Ansæt ikke**
- **Ansæt**

> [!NOTE]
> Hvis kandidatlisten udfyldes fra Microsoft Dataverse, vises de samme kandidater på tværs af alle juridiske enheder, fordi der ikke er knyttet en juridisk enhed til kandidaten.

### <a name="starting-soon"></a>Starter snart

I sektionen om **Starter snart** vises der en oversigt over arbejdere, der har en startdato i fremtiden. Listen sorteres efter startdato. Den startdato, der er nærmest dags dato, vises først.

Hvis chefen ikke vises på kortet, er der ikke tildelt en stilling til arbejderen.

> [!NOTE] 
> Det anbefales, at du tildeler en stilling til en arbejder, før du anvender en kontrolliste. Til tider tildeles en nyansat medarbejders chef opgaver i forbindelse med onboarding. Men hvis der ikke er tildelt en stilling, kan den nye medarbejders chef ikke afgøres. Hvis det er tilfældet, tildeles de onboardingopgaver, der er tiltænkt chefen, i stedet til ejeren af tjeklisten.

Når arbejdere vises i sektionen **Starter snart**, er følgende handlinger tilgængelige for dem:

- Tildel stilling
- Kontrollér ansættelse
- Tildel fast løn
- Tildel variabel kompensation
- Vis i hierarki
- Anvend tjekliste\*\*

\*\* Denne handling er standardhandlingen. Den vises som en knap på kortet.

### <a name="recent-hires"></a>Seneste ansættelser

Sektionen **Nye ansættelser** indeholder en oversigt over arbejdere, der har en nylig startdato. Listen sorteres efter startdato. Den startdato, der er nærmest dags dato, vises først.

Listen viser som standard arbejdere, der er ansat inden for de seneste syv dage. Hvis du vil ændre denne indstilling, skal du definere en tidsramme for **Nye ansættelser** på siden **Human Resources-parametre** under fanen **Generelt**. Dataene i sektionen **Nye ansættelser** kan vises for et bestemt antal dage, måneder eller år. Hvis du for eksempel vil have vist listen over arbejdere, der er ansat inden for de seneste 14 dage, skal du angive feltet **Periode** til **14** og feltet **Enhed** til **Dage**.

> [!NOTE]
> Indstillingerne på siden **Human Resources-parametre** er firmaspecifikke. Derfor kan den tidsramme, du får vist nye ansættelser for, variere efter firma. I firmaet USMF vil du for eksempel have vist alle nye ansættelser fra de seneste syv dage. Men i firmaet USSI vil du måske se alle nyansættelser fra de seneste 14 dage. I dette tilfælde skal du åbne siden **Human Resources-parametre** i hvert firma og angive parametrene efter behov.

Hvis chefen ikke vises på kortet, er der ikke tildelt en stilling til arbejderen.

Når arbejdere vises i sektionen **Nye ansættelser**, er følgende handlinger tilgængelige for dem:

- Tildel stilling
- Kontrollér ansættelse
- Fast løn
- Tildel variabel kompensation
- Vis i hierarki
- Anvend tjekliste\*\*

\*\* Denne handling er standardhandlingen. Den vises som en knap på kortet.

### <a name="exiting"></a>Afslutter

I sektionen om **Fratrædende** vises der en oversigt over arbejdere, der har en fratrædelsesdato i fremtiden. Listen sorteres efter fratrædelsesdato. Den fratrædelsesdato, der er nærmest dags dato, vises først. 

Som standard viser listen arbejdere, der har en fratrædelsesdato i løbet af de næste syv dage. Hvis du vil ændre denne indstilling, skal du definere en tidsramme for **Vis fratrædende arbejdere** på siden **Human Resources-parametre** under fanen **Generelt**. Dataene i sektionen **Fratrædende** kan vises for et bestemt antal dage, måneder eller år. Hvis du for eksempel vil have vist listen over arbejdere, der fratræder i løbet af de næste 14 dage, skal du angive feltet **Periode** til **14** og feltet **Enhed** til **Dage**.

Når arbejdere vises i sektionen **Fratrædende**, er følgende handlinger tilgængelige for dem:

- Anvend tjekliste\*\*
- Kontrollér ansættelse
- Vis i hierarki

\*\* Denne handling er standardhandlingen. Den vises som en knap på kortet.

### <a name="exited"></a>Afsluttede

Sektionen **Fratrådt** indeholder en oversigt over arbejdere, der har en nylig fratrædelsesdato. Listen sorteres efter fratrædelsesdato. Den fratrædelsesdato, der er nærmest dags dato, vises først.

Som standard viser listen arbejdere, der har en fratrædelsesdato inden for de seneste syv dage. Hvis du vil ændre denne indstilling, skal du definere en tidsramme for **Vis fratrådte arbejdere** på siden **Human Resources-parametre** under fanen **Generelt**. Dataene i sektionen **Fratrådt** kan vises for et bestemt antal dage, måneder eller år. Hvis du for eksempel vil have vist listen over arbejdere, der er fratrådt inden for de seneste 14 dage, skal du angive feltet **Periode** til **14** og feltet **Enhed** til **Dage**.

Når arbejdere vises i sektionen **Fratrådt**, er følgende handlinger tilgængelige for dem:

- Anvend tjekliste\*\*
- Kontrollér ansættelse
- Vis i hierarki

\*\* Denne handling er standardhandlingen. Den vises som en knap på kortet.

## <a name="employee-changes-tab"></a>Fanen Medarbejderændringer

Fanen **Medarbejderændringer** indeholder en liste over alle arbejderens personalehandlinger. Denne liste er som standard ikke tilgængelig. Hvis du vil aktivere funktionaliteten, skal du angive indstillingen **Aktivér arbejderhandlinger** til **Ja** under fanen **Personalehandlinger** på siden **Delte Human Resources-parametre**.

## <a name="position-changes-tab"></a>Fanen Stillingsændringer

Fanen **Stillingsændringer** indeholder en liste over alle personalehandlinger for stillinger. Denne liste er som standard ikke tilgængelig. Hvis du vil aktivere funktionaliteten, skal du angive indstillingen **Aktivér stillingshandlinger** til **Ja** under fanen **Personalehandlinger** på siden **Delte Human Resources-parametre**.

## <a name="open-positions-tab"></a>Fanen Ledige stillinger

Fanen **Ledige stillinger** viser alle ledige stillinger. For at blive vist på listen skal stillinger have aktiveringsdatoen dags dato eller tidligere, og de må ikke have en aktuel arbejdertildeling.

> [!NOTE]
> Listen tager højde for arbejdertildelingen pr. dags dato. Alle stillinger, der har en arbejdertildeling, der er dateret i fremtiden, vises fortsat på listen. Men når ikrafttrædelsesdatoen for arbejdertildelingen er nået, fjernes stillingen fra listen.

## <a name="expiring-records-tab"></a>Fanen Udløbende poster

Fanen **Udløbende poster** indeholder alle elementer, der er udløbet, eller som vil udløbe for arbejderne i det firma, som brugeren er logget på. Følgende elementer vises på listen:

- **Certifikater**
- **Identifikation**
- **Prøvetid**
- **Screeninger**
- **Tests**

Hvis du vil angive, om listen skal vise udløbne poster eller udløbende poster, skal du definere en tidsramme for enten **Udløbende poster** eller **Udløbne poster** på siden **Human Resources-parametre** under fanen **Generelt**. Dataene under fanen **Udløbende poster** kan vises i et bestemt antal dage. Hvis du for eksempel vil have vist listen over poster, der udløber inden for de næste 14 dage, skal du angive feltet **Antal dage** til **14**.

> [!NOTE] 
> Hvis du angiver tidsrammen for **Udløbne poster** eller **Udløbende poster** til **0** på siden **Human Resources-parametre**, vises ingen af disse poster på listen.

## <a name="employees-tile"></a>Feltet Medarbejdere

Feltet **Medarbejdere** viser antallet af alle medarbejdere, der er ansat i det firma, som brugeren i øjeblikket er logget på. Når du vælger feltet **Medarbejdere**, vises medarbejderdetaljerne på en ny side.

## <a name="contractors-tile"></a>Feltet Kontrahenter

Feltet **Kontrahenter** viser antallet af alle kontrahenter, der er ansat i det firma, som brugeren i øjeblikket er logget på. Når du vælger feltet **Kontrahenter**, vises kontrahentdetaljerne på en ny side.

## <a name="open-positions-tile"></a>Feltet Ledige stillinger

Feltet **Ledige stillinger** viser antallet af alle ledige stillinger. Når du vælger feltet **Ledige stillinger**, vises detaljerne om ledige stillinger på en ny side. For at blive inkluderet i optællingen skal stillinger have aktiveringsdatoen dags dato eller tidligere, og de må ikke have en aktuel arbejdertildeling.

> [!NOTE]
> Feltet tager højde for arbejdertildelingen pr. dags dato. Alle stillinger, der har en arbejdertildeling, der er dateret i fremtiden, inkluderes fortsat i optællingen. Men når ikrafttrædelsesdatoen for arbejdertildelingen er nået, fjernes stillingen fra optællingen.

## <a name="approvals-tile"></a>Feltet Godkendelser

Feltet **Godkendelser** viser antallet af alle arbejdsgangselementer, der afventer den aktuelle brugers godkendelse. Når du vælger feltet **Godkendelser**, vises der en ny side med detaljer om de arbejdsgangselementer, der kræver din godkendelse.

## <a name="address-changes-tile"></a>Feltet Adresseændringer

Feltet **Adresseændringer** viser antallet af alle adresseændringer, der er foretaget i løbet af det antal dage, der er angivet på siden **Human Resources-parametre**. Når du markerer feltet **Adresseændringer**, vises oplysningerne om eventuelle adresseændringer på en ny side. Du kan eventuelt vælge **Medtag fremtidige adresseændringer** i øverste højre hjørne på siden for at få vist adresseændringer, der har en fremtidig dato.

Du kan finde flere oplysninger om, hvordan du får vist og administrerer adresseændringer, i [Få vist og administrere adresseændringer](hr-personnel-view-address-changes.md).
