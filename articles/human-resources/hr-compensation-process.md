---
title: Kompensationsbehandling
description: Med kompensationsbehandling kan du beregne nye grundkompensationsbeløb for dine medarbejdere baseret på justeringer af egenkapital, meritstigningsmål og performance.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 413143afb578aed29ce0836aaa3ac98ffc0c6cc3
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2021
ms.locfileid: "7484090"
---
# <a name="process-compensation"></a>Kompensationsbehandling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Med kompensationsbehandling kan du beregne nye grundkompensationsbeløb for dine medarbejdere baseret på justeringer af egenkapital, meritstigningsmål og performance. Dette emne drejer sig om den grundlæggende arbejdsgang ved kompensationsbehandling i forbindelse med faste lønplaner uden indregning af en medarbejderperformance.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Planlægge de nye kompensationsbeløb og budgetter
For at give medarbejderne meritstigning skal du konfigurere et budget for fast stigning for hver af dine afdelinger: **Kompensationsstyring** > **Links** > **Meritstigningsmål**. (Du kan også åbne denne side via afdelingen: **Organisation** > **Afdelinger**). Her kan du angive, om medarbejdere i en bestemt fagforening eller lokalitet skal have en anden stigningsprocent. Felterne **Budget** og **Valuta** er til orientering og kan bruges til at notere et valutabeløb til budgettet.

## <a name="set-up-the-compensation-process"></a>Konfigurere kompensationsprocessen
På siden **Kompensationsprocesser** kan du angive parametrene for kompensationsprocessen. Dette omfatter den datoperiode, der skal evalueres for at bestemme kompensationsbeløbene og den dato, hvor de nye kompensationsbeløb skal træde i kraft.

Du kan eventuelt medtage en **Fast løn iht. vurderet ansættelsesdato**, hvis nogen af dine planer for fast kompensation bruger ansættelsesreglen Procent. I disse planer modtager alle, der er ansat efter **Cyklussens startdato** og før **Fast løn iht. vurderet ansættelsesdato** 100 % af deres beregnede merit eller generelle stigning. Alle, der er ansat efter **Fast løn iht. vurderet ansættelsesdato** og før **Cyklussens slutdato**, modtager en del af deres beregnede stigning baseret på, hvor mange dage af det samlede antal dage i cyklussen, de har været ansat. Eksempelvis hvis din cyklus løber fra den 1. januar til den 31. december, og ansættelsesdato med fast lønsats er den 1. april, modtager en medarbejder, der blev ansat i marts, den fulde beregnede stigning, mens en medarbejder, der blev ansat den 1. juli, modtager ca. halvdelen af den beregnede stigning.

Datoen for **Tidspunkt** i proceshændelsen bruges kun til behandling af visse variable lønstrukturer og bliver ikke gennemgået her. **Gennemse deadline** er fristen for at give anbefalinger, så de nye kompensationsbeløb kan indlæses i medarbejderens post. Denne dato er kun til orientering.

Når du har gemt parametrene for proceshændelsen, kan du klikke på knappen **Opsætning** for at angive de planer, der skal medtages, når denne proces køres, og hvilke fast løn-handlinger der skal udføres for hver enkelt plan.

Klik på knappen **Tilføj** under fanen **Planer** for at føje en kompensationsplan til proceshændelsen. Kolonnerne **Brug anden regulering**, **Reguleringsfaktor** og **Reguleringsbeskrivelse** bruges kun til variable kompensationsplaner og er ikke medtaget i dette emne.

Gem posten, og klik derefter på knappen **Tilføj** under fanen **Handlinger** for at tilføje en fast løn-handlinger for den valgte plan. Du kan bruge indstillingen **Aktiver anbefaling** til at angive et andet beløb end det beregnede resultattillæg for handlingen. Hvis du vil beregne en handling, der er baseret på resultatet af den foregående handling, så flere kompensationshandlinger tilknyttes, skal du markere indstillingen **Brug tidligere resultat**. Fast lønkompensation-handlinger er typer af kompensationslogikken, som du kan give sigende navne. For planer af typen Klasse og Omfang kan du kun tilføje fast løn-handlinger af følgende typer:

| Fast løn-handlingstype | Funktionalitet                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Egenkapital                        | Egenkapital-handlinger sammenligner medarbejderens lønsats pr. cyklusslutdato med det laveste referencepunkt for niveauet angivet på medarbejderens job. Hvis medarbejderens lønsats er mindre end det mindste referencepunkt, beregnes den stigning, der er nødvendigt for at få medarbejderen op på det laveste punkt i intervallet.                                                                                |
| Merit                         | Merit-handlinger beregner en stigning, der er baseret på medarbejderens lønsats pr. cyklusslutdato og den stigningsprocent, der findes i budgettet for fast stigning for medarbejderens afdeling, fagforening og lokalitet.                                                                                                                                                                                         |
| Almindelig                       | Generelle handlinger beregner en stigning, der er baseret på enten en Procent eller give medarbejderne et fast beløb. Dette bestemmes ud fra indstillingerne i **Fast løn** for under fanen **Generelt**.                                                                                                                                                                                                                        |
| Forfremmelse                     | Kampagnehandlinger giver dig et navngivet sted, hvor du kan tildele stigninger. Markér indstillingen **Aktivér anbefaling** for at angive en anbefaling for medarbejdere, der skal modtage forfremmelser.  Handlingen **Forfremmelse** bliver ikke føjet til faste kompensationsposter for medarbejdere uden en anbefalet stigning.                                                                       |
| Anden niveauændring            | I det foregående eksempel er **Degradering** navnet på **Fast løn**-handlingen med typen **Anden niveauændring**. Dette genererer et resultattillæg på 0 (nul-ændring), så du kan angive et anbefalet beløb for at justere medarbejderens lønsats. (Vælg indstillingen **Aktivér anbefaling**). Denne handling føjes ikke til faste kompensationsposter for medarbejdere uden en anbefaling. |

Du kan kun føje **Fast løn**-handlinger med en Trin-type til en trinplan.

| Fast løn-handlingstype | Funktionalitet                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Trin                           | Angiv under fanen **Generelt**, om denne Trin-handling skal flytte medarbejderne videre med 0 trin, 1 trin eller 2 trin.                                                                                  |
|                                | **0 trin** – Medarbejderen modtager lønsatsen for det trin, de aktuelt ligger på.                                                                                                                      |
|                                | **1 trin** - Systemet kontrollerer, om medarbejderen allerede er på sidste referencepunkt for det pågældende niveau.                                                                                             |
|                                | **2 trin** - Systemet flytter medarbejderen to trin op fra det aktuelle niveau. Systemet kan kun flytte medarbejderen et eller nul trin, hvis vedkommende når det sidste referencepunkt for sit niveau. |

## <a name="run-the-compensation-process"></a>Kør kompensationsprocessen
Når proceshændelsen er konfigureret med de nødvendige datofelter, planer og handlinger, skal du klikke på **Kør proces** på siden **Proceshændelse**. Det åbner dialogboksen **Kør processer til kompensationshændelser**. Klik på indstillingen **Vis resultater af behandling** for at se, hvordan kompensationsbeløbene er beregnet for hver medarbejder. Hvis du klikker på **OK**, kører kompensationsprocessen for alle medarbejdere, der er i de valgte kompensationsplaner pr. cyklussens slutdato.

## <a name="view-the-process-results"></a>Vise procesresultaterne
For at få vist resultaterne af processen skal du åbne siden **Procesresultater**. Der oprettes en kompensationshændelse, hver gang proceshændelsen afvikles. På denne måde kan du foretage prøvekørsler, foretage justeringer og køre kompensationshændelsen flere gange for at se, hvordan de forskellige ændringer påvirker medarbejderkompensation.

Siden **Procesresultater** indeholder oplysninger om proceskørslen, herunder hvornår kørslen fandt sted, den bruger, der har kørt processen, og om der opstod fejl, da processen blev kørt. Vælg indstillingen **Låst** for at deaktivere knappen **Indlæs kompensation** og forhindre andre i at indlæse kompensationshændelser i medarbejderposterne. Hvis du klikker på knappen **Medarbejderresultater** vises en liste over de medarbejdere, der er med i kørslen.

Indstillingen **Medarbejderresultater** viser oplysninger om selve processen samt eventuelle løn-handlinger, der udføres under processen. Sektionen **Fast løn** indeholder en post for hver handling, der er medtaget i proceshændelsen for lønstrukturen. Kolonnerne **Aktuel retningslinje** og **Anbefaling** viser flere oplysninger om den handling, der er valgt i sektionen **Fast løn**. Hvis **Aktivér anbefalinger** var markeret for handlingen, kan **Anbefalet**-felterne redigeres. Derved kunne du manuelt justere beløbene for medarbejderen. Bemærk, at hvis du har markeret **Brug tidligere resultat** for handlingen i proceshændelsen, skal du manuelt opdatere beløbene for eventuelle afhængige handlinger.

Når du har gennemset kompensationsbeløbene for en medarbejder, og du har foretaget eventuelle ændringer i de anbefalede værdier, kan du ændre **Status** på **Medarbejderhændelse**-linjen for at angive, om hændelsen er blevet godkendt eller skal ignoreres. Du kan eventuelt slette ændringer af anbefalingerne for medarbejderen ved at klikke på knappen **Genberegn**. Dette markerer den eksisterende medarbejderhændelse med statussen Ignorer, og der oprettes en ny medarbejderhændelse med genberegnede værdier.

## <a name="loading-approved-compensation-changes"></a>Indlæsning af godkendte kompensationsændringer
Når status for en eller flere medarbejderhændelser er blevet opdateret til **Godkendt**, kan de indlæses i medarbejdernes fast løn-poster. Dette kan gøres ved at vælge én medarbejderhændelse ad gangen og klikke på knappen **Indlæs medarbejderkompensation** på siden **Medarbejderresultater** eller ved at klikke på **Indlæs kompensation** på siden **Procesresultater** for at indlæse alle godkendte medarbejderhændelser på én gang.

Hvis du klikker på **OK** i dialogboksen **Indlæs kompensation**, tilføjes kompensationshandlingslinjer, der ikke er nul, på siden **Fast løn til medarbejder**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
