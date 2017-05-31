---
title: "Registrering af tid og fremmøde"
description: "Arbejdere, der registrerer tid, kan angive forskellige former for tidsregistreringer. De kan f.eks. angive, hvornår de kommer og går, og de kan registrere indirekte aktiviteter og fravær. I denne artikel beskrives registreringer, deres beregning, godkendelse og anvendelse af arbejdsgang til at føje struktur og automatisk godkendelse til processen til godkendelse af timesedler."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 12193e4c266abc7bf0349ba9a78dbbbd9d00938d
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="time-and-attendance-registration"></a>Registrering af tid og fremmøde

[!include[banner](../includes/banner.md)]


Arbejdere, der registrerer tid, kan angive forskellige former for tidsregistreringer. De kan f.eks. angive, hvornår de kommer og går, og de kan registrere indirekte aktiviteter og fravær. I denne artikel beskrives registreringer, deres beregning, godkendelse og anvendelse af arbejdsgang til at føje struktur og automatisk godkendelse til processen til godkendelse af timesedler. 

<a name="registrations"></a>Registreringer
-------------

Arbejdere skal registrere den tid, de bruger på arbejdet, samt deres fremmøde, i virksomheder, der bruger Tid og fremmøde. I nogle firmaer er det kun nødvendigt, at arbejderne registrerer, hvornår de kommer og går. I andre firmaer skal arbejdere måske også registrere, hvor meget tid de bruger på de faktiske aktiviteter, de udfører, og de pauser, de tager. Tid og fremmøde henvender sig primært til:
-   Arbejdere, der skal registrere tid og fremmøde regelmæssigt, f.eks. hver dag, hver uge eller hver 14. dag.
-   Ledende medarbejdere, ledere og lønningsmedarbejdere, der beregner, godkender og overfører arbejderregistreringer med henblik på yderligere behandling.

| **Bemærk!**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis du kører Tid og fremmøde sammen med Produktionsudførelse, registreres alle registreringer for projekter, projektaktiviteter, indirekte aktiviteter, fraværskoder, overtid og flekstid, og de bruges til at beregne løn i begge moduler. |

## <a name="time-registrations-workers"></a> Tidsregistrering for arbejdere
Arbejdere skal oprettes som arbejdere, der registrerer tid, i det firma, hvor de er ansat, for at kunne registrere tid og fravær.

Efter konfigurationen kan arbejderne angive forskellige former for registreringer.

-   Komme og gå-tider, når de ankommer til eller forlader arbejdet.
-   Tids- og vareforbrug på produktionsjob.
-   Tid brugt på en maskine i produktionen, hvis maskinen er defineret som en ressource.

| **Bemærk!**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En arbejder tildeles automatisk de tidsregistreringer, der er oprettet for en bestemt maskine i produktionen, hvis medarbejderen vælger at arbejde som assistent for maskinen, når han eller hun starter produktionsjobbet. |

-   Tidsregistreringer på projekter og projektaktiviteter.
-   Registrering af projektgebyrer og vareforbrug via de respektive gebyrkladder for projekter og projektvarekladder.
-   Planlagt fravær.
-   Fravær, når arbejderen ankommer for sent til arbejde eller går tidligere end planlagt.
-   Arbejdspauser, enten registreret manuelt eller automatisk beregnet af systemet.
-   Indirekte aktiviteter, der er ikke-produktive aktiviteter, en arbejder kan deltage i i løbet af arbejdsdagen. Eksempler på disse aktiviteter kan være møder eller rengøring af arbejdsområdet.
-   Overtid, som kan registreres enten som ekstra timer, flekstid eller overtid.

## <a name="adding-clockout-registrations"></a>Tilføjelse af udstemplingsregistreringer
Hvis arbejdere glemmer at stemple ud ved afslutningen af deres arbejdsdag, kan den manglende registrering tilføjes ved at køre et batchjob. Systemet sammenligner komme-tiden og gå-tiden i henhold til den profil, der er knyttet til arbejderen, og indsætter automatisk den manglende gå-registrering, så den stemmer overens med profilens sluttidspunkt. Både komme- og gå-registreringer er afgørende for den efterfølgende beregning og godkendelse af tidsregistreringer, før de kan overføres til lønregnskabet.

## <a name="calculating-registrations"></a>Beregne registreringer
En arbejder, der registrerer tid, tildeles en beregningsgruppe, der typisk er relateret til et bestemt team, et bestemt skiftehold eller en bestemt arbejdsgruppe. Teamlederen eller den tilsynsførende validerer typisk registreringer, der er foretaget af arbejderne, og er derfor også den person, der er ansvarlig for at udføre den daglige beregningen for de respektive beregningsgrupper. Som led i beregningsprocessen kan teamlederen eller den tilsynsførende gøre følgende:
-   Rette fejlbehæftede registreringer. For eksempel ændre Switch-koder og justere tilbagemeldinger om produktionsjob.
-   Tilføje manglende registreringer. For eksempel oprette gå-registreringer og oprette fraværsposter.
-   Slette forkerte registreringer.

Da den registrerede tid skal svare til arbejderens arbejdstidsprofil inden beregning af registreringerne, skal du tilsidesætte arbejdstidsprofilen for en arbejder, der har en undtagelse i forhold til standardarbejdstidsprofilen. I det tilfælde, hvor arbejderens profil er på dagholdet, og arbejderen har indvilliget i at arbejde på et nathold uden overtidsbetaling, skal teamlederen eller den tilsynsførende tilsidesætte standardarbejderprofilen for at beregne arbejdstiden med standardnattaksten og ikke som overarbejde. Beregningen viser også en fejl, hvis der mangler en fraværsregistrering. Den skal tilføjes, før beregningen kan fuldføres.

## <a name="approving-registrations"></a>Godkende registreringer
På samme måde som du tildeler en beregningsgruppe til en tidsregistreringsarbejder, skal du også tildele en godkendelsesgruppe. Gruppen oprettes som regel for et bestemt team, et bestemt skiftehold eller en bestemt arbejdsgruppe. Du skal godkende de tidsregistreringer, der blev beregnet korrekt – det vil sige, at beregning sker uden fejl – før der kan oprettes lønposter, som bagefter kan overføres til et lønsystem. Lønadministratoren vil normalt udføre godkendelse af registreringer, og forud for godkendelsen kan han:
-   Tilsidesætte lønaftaler for de enkelte arbejdere.
-   Tilføje manuelle tillæg.
-   Angive yderligere oplysninger om registrering af fravær.

| **Bemærk!**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis der er beregnet overtid for bestemte arbejdere, kan overtiden tildeles bestemte job i løbet af dagen. Det er relevant, hvis jobomkostningerne er beregnet på basis af arbejderløn. |

## <a name="approving-registrations-using-workflow"></a> Godkende registreringer ved hjælp af arbejdsgang
Du kan oprette en godkendelsesproces som en arbejdsgang, der automatisk godkender registreringer, som overholder arbejdsgangsregler, så det kun er afvigelser, der skal håndteres manuelt. Hvis godkendelse via arbejdsgang er aktiveret, sender teamlederen eller den tilsynsførende de beregnede registreringer til godkendelse. I arbejdsgangens proces oprettes de relevante godkendelser og opgaver, og de tildeles de rette brugere og roller, som er identificeret i arbejdsgangen. Der er to arbejdsgangsgodkendelser for tid og fremmøde.

| Arbejdsgang                                  | Formål                                                                                                   | Registreringstype                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tid og fremmøde - Dage i alt            | Arbejdsgangen validerer registreringer i forhold til f.eks. det forventede antal arbejdstimer om dagen. |                                                                                                                                                                                                                                                       |
| Kladderegistrering af tid og fremmøde. | Arbejdsgangen validerer hver registreringstype for registreringsdatoen.                           | Tid og fremmøde • Komme • Gå • Fravær • Pause • Switch-kode • Projekt • Projektaktivitet • Indirekte aktivitet • Produktionsjob • Kø før • Konfiguration • Proces • Overlapning • Transportér • Kø efter • Start medhjælp • Stop medhjælp |

 

## <a name="transferring-approved-registrations"></a>Overføre godkendte registreringer
Når registreringerne er godkendt, kan du overføre dem til et periodisk lønjob. En overført registrering posteres til en aktivitet eller et job, som den vedrører, for eksempel en produktionsordre eller et projekt. Der oprettes løntransaktioner for hver arbejder på basis af registreringerne.  

## <a name="reversing-transferred-registrations"></a>Tilbageføre overførte registreringer
Tilbageførsel af posteringer – annullering af dem – kan ske indtil det tidspunkt, hvor lønperiodens lønoverførsel køres. Det betyder, at løndata er overført til en ekstern fil. Ved tilbageførsel tilbagetrækkes alle registreringer, og eventuelle transaktioner, der er bogført på produktionsordrer eller projekter, modregnes og neutraliseres.

| **Bemærk!**                                                 |
|----------------------------------------------------------|
| Den eksterne fil kan importeres til et lønsystem. |

## <a name="registrations-in-electronic-timecards"></a>Registreringer på elektronisk timeseddel
Arbejdere med jobopgaver, der ikke kræver øjeblikkelig feedback, som det er tilfældet med produktionsjob, men som arbejder på projektaktiviteter, kan med fordel bruge den elektroniske timeseddel. Elektroniske timesedler gør det muligt at angive registreringer når som helst og på den måde, der passer din virksomhed bedst – dagligt, ugentligt, eller når en arbejder er på kontoret igen efter at have været ude. Hvis du vil bruge elektroniske timesedler eller disse arbejdere, skal du vælge Brug timeseddel i arbejderoplysningerne. Elektroniske timesedler giver arbejderen mulighed for at registrere:

-   Dato
-   Registreringstype
-   Jobreference, f.eks. projekt, indirekte aktivitet eller produktionsordre
-   Job-id
-   Tidsforbrug
-   Projektgebyrer
-   Projektvarer





