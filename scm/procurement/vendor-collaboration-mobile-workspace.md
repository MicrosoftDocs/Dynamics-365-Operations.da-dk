---
title: "Arbejdsområde til kreditorsamarbejde på mobilenheder i Microsoft Dynamics 365 for Operations-app"
description: "Med arbejdsområdet til kreditorsamarbejde på mobilenheder kan dine kreditorer være ajour med indkøbsordrer, der er blevet sendt til dem til godkendelse og få vist oplysninger om nye og opdaterede indkøbsordrer og kontaktpersoner."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e19fee87dae6e5d425f36dac0db4ea89534a8510
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Arbejdsområde til kreditorsamarbejde på mobilenheder i Microsoft Dynamics 365 for Operations-app

[!include[banner](../includes/banner.md)]


Med arbejdsområdet til kreditorsamarbejde på mobilenheder kan dine kreditorer være ajour med indkøbsordrer, der er blevet sendt til dem til godkendelse og få vist oplysninger om nye og opdaterede indkøbsordrer og kontaktpersoner.

<a name="prerequisites"></a>Forudsætninger
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Læs om Microsoft Dynamics 365 for Operations-mobilplatformen</td>
<td><a href="https://ax.help.dynamics.com/en/wiki/mobile-development-handbook/">Dynamics 365 for Operations-mobilplatform</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Sørg for, at du bruger et miljø, der har Microsoft Dynamics 365 for Operations version 1611 og opdatering 3 til Microsoft Dynamics for Operations platformen (november 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000">Mobileenhed, hvor Dynamics 365 for Operations-appen er installeret</span></td>
<td><span style="color: #000000">Hent og installer Dynamics 365 for Operations-appen fra din mobilapp-butik.</span></td>
</tr>
<tr class="even">
<td>Hotfix KB 4013633</td>
<td>Installer hotfixet, hvis du vil aktivere de arbejdsområder, der findes i Dynamics 365 for Operations.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000"><span style="color: #000000">Hotfix KB 3216943</span> </span></td>
<td>Installere hotfixet, hvis du vil aktivere arbejdsområdet til kreditorsamarbejde på mobilenheder.</td>
</tr>
<tr class="even">
<td>Kreditorbrugeren skal have adgang til webgrænsefladen for kreditorsamarbejde i Dynamics 365 for Operations og konfigurere en kreditorsamarbejdsbruger.</td>
<td>Følg de trin, der er beskrevet i følgende emner til at oprette og arbejde med webgrænsefladen til kreditorsamarbejde.
<ul>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-external-vendors/">Brug kreditorsamarbejde til at arbejde sammen med eksterne kreditorer</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/manage-vendor-collaboration-users/">Administrere brugere af kreditorsamarbejde</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/set-up-and-maintain-vendor-collaboration/">Konfigurere og vedligeholde kreditorsamarbejde</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations/">Brug kreditorsamarbejde til at arbejde sammen med kunder i Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Overblik
Arbejdsområdet til kreditorsamarbejde på mobilenheder holder kreditorerne underrettet om nye indkøbsordrer, så de kan se og reagere på indkøbsordrer i Dynamics-365 for Operations-webklienten. 

**Bemærk!** Det mobile arbejdsområde bør anvendes som et supplement til webgrænsefladen til kreditorsamarbejde, men ikke som en erstatning. 

Med arbejdsområdet til kreditorsamarbejde på mobilenheder kan dine kreditorer få vist nye indkøbsordrer, der er sendt til godkendelse. Det viser indkøbsordreoplysninger, f.eks. produkter, antal og ønskede leveringsdatoer. Prisoplysninger er tilgængelige, afhængigt af konfigurationen for hver kreditor. 

Når en bruger logger på som en kreditor, kan de se hvilke indkøbsordrer er blevet besvaret, eller hvilke indkøbsordrer der stadig afventer kundehandling. Kreditoren kan have foreslået en anden dato for levering, der endnu ikke er aftalt med kunden, så indkøbsordren afventer kundehandling. Kreditoren kan også se en liste over indkøbsordrer, der er bekræftet, men som endnu ikke er leveret. 

Hvis kreditoren vil besvare en indkøbsordre, er vedkommende nødt til at bruge webgrænsefladen til kreditorsamarbejde, der findes i Dynamics-365 for Operations-webklienten. Dette er også der, hvor kreditoren kan få flere oplysninger om ordren, f.eks. vedhæftede dokumenter, leveringsadresse pr. linje og gebyrer, der er knyttet til kreditoren. 

Med en speciel sikkerhedsrolle, kan kreditoren få vist hvilke kontaktpersoner, der er registreret for en kreditorkonto. Med den samme sikkerhedsrolle kan kreditoren få vist status for alle brugeranmodninger, der er sendt. 

Oprettelse af nye kontaktpersoner og afsendelse af nye brugeranmodninger, skal det ske i grænsefladen til kreditorsamarbejde, der findes i Dynamics-365 for Operations-webklienten. 

Med det mobile arbejdsområde kan kreditoren:

-   Få vist nye indkøbsordrer, der er sendt til kreditoren.
-   Få vist indkøbsordrer, som kreditoren har besvaret, og som afventer kundehandling.
-   Få vist indkøbsordrer, der er bekræftet, og som ikke er blevet fuldt modtaget.
-   Få vist oplysninger om kontaktperson, der er registreret for kreditorkontoen (kræver en ekstra sikkerhedsrolle).
-   Få vist oplysninger og følge status for en brugeranmodning afsendt af kreditoren (kræver en ekstra sikkerhedsrolle).

## <a name="get-started"></a>Introduktion
Sådan kommer du i gang på din mobilenhed:

1.  På din mobilapp-store skal du hente og installere Microsoft Dynamics 365 for Operations-appen.
2.  Start appen på din enhed.
3.  Angiv URL-adressen til din Dynamics 365.
4.  Angiv det firma, du vil logge på. Du kan f.eks. skrive **USMF**.
5.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Microsoft Dynamics 365 for Operations-konto.

Når du logger på appen, vises der ingen arbejdsområder. For at få vist arbejdsområder på din mobilapp skal du først publicere de ønskede arbejdsområder til Dynamics 365 for Operations-appen. Du skal bruge systemadministrationsrettighed til at udgive arbejdsområdet.

1.  Start Dynamics 365 for Operations.
2.  Gå til **Systemadministration** &gt; **Opsætning** &gt; **systemparametre**.
3.  Vælg **Administrer mobilapp**.
4.  Vælg arbejdsområdet **Kreditorsamarbejde** for at publicere til mobilplatformen.
5.  Vælg **Publicer arbejdsområde**.
6.  Opdater din enhed for at se de publicerede arbejdsområder.
7.  Vælg arbejdsområdet **Kreditorsamarbejde**. Du får vist følgende side.

    [![mobilapp til kreditorsamarbejde](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktpersoner
På siden **Kontakter** kan du se alle de kontakter, der er angivet for kreditorkontoen. Det viser kontaktpersonens navn, primære mail og brugeralias, hvis det er tilgængelig. Det viser også, om kontaktpersonens brugerkonto er aktiv. Når du markerer en kontakt, kan du se kontaktoplysninger, f.eks. de juridiske enheder, personen er kontaktperson for og kontaktoplysninger, f.eks. telefonnummer eller en anden mailadresse.

## <a name="user-requests"></a>Brugeranmodninger
På siden **Brugeranmodninger** kan du se alle brugeranmodninger, som du har sendt via webgrænsefladen til leverandørsamarbejde, og følge status. Når du vælger en brugeranmodning, kan du se, hvad der blev anmodet om, tilføje eller deaktivere en bruger, ændre sikkerhed og se, hvilke sikkerhedsroller der blev anmodet om for brugeren.

## <a name="purchase-orders-ready-for-review"></a>Indkøbsordrer klar til gennemsyn
På siden **Indkøbsordrer, der er klar til gennemsyn** kan du se alle de indkøbsordrer, der er sendt af kunden og ikke er besvaret. Du kan se udvalgte oplysninger om ordren, f.eks. hvilke produkter, der er anmodet om, og hvornår de skal leveres. Prisoplysninger er kun tilgængelige, hvis det er konfigureret for kreditoren. Du kan se, om indkøbsordren indeholder noter og vedhæftede filer. For at åbne vedhæftede filer, skal du bruge kreditorsamarbejde i webklienten. Vælg **Indkøbsordrelinje** for at få vist alle linjer med detaljer. Bemærk, at for hver linje viser en indikator, om der er noter eller vedhæftede filer, eller om der er en leveringsadresse, som er forskellig fra, hvad der vises i hovedet. For at besvare indkøbsordren, skal du bruge webklienten til kreditorsamarbejde.

## <a name="awaiting-customer-action"></a>Afventer kundehandling
Siden **Afventer kundehandling** giver dig mulighed for at søge efter de indkøbsordrer, som du eller en person i virksomheden, der også har adgang til kreditorsamarbejde, har reageret på. Indkøbsordrer er kun synlige på denne liste, hvis kunden har brug at udføre en af følgende handlinger på indkøbsordren.

-   Hvis indkøbsordren blev afvist, skal kunden enten skal opdatere den sendte ordre og sende igen, eller annullere ordren og sende den igen. Når indkøbsordren sendes igen, forsvinder den fra siden **Afventer kundehandling**.
-   Hvis indkøbsordren blev accepteret med ændringer, skal kunden opdatere den oprindelige ordre og sende den til gennemsyn igen, eller opdatere den i overensstemmelse med ændringerne, og straks bekræfte den. I begge tilfælde forsvinder indkøbsordren fra siden **Afventer kundehandling**.
-   Hvis indkøbsordren blev accepteret og vises på siden **Afventer kundehandling**, er det, fordi indkøbsordren ikke automatisk blev bekræftet, da den blev accepteret. Den venter på, at en indkøber skal ændre rækkefølgen til Bekræftet. Indkøbsordren betragtes normalt som en aftale mellem debitor og kreditor, så snart kreditoren accepterer ordren. Flytning af indkøbsordren til tilstanden Bekræftet, vil være en formalitet.

Når indkøbsordren vælges, vises yderligere oplysninger om svaret. Du kan se linjedetaljerne og besvare hver linje. I linjen status vises, hvilke af følgende svar der er givet.

-   Accepteret
-   Afvist
-   Accepteret med ændringer
-   Erstattet/erstatning
-   Opdel i tidsplan/tidsplanslinje

Bemærk, at en indikator viser **Levering**= Ja/nej, som bruges til at angive, at linjerne ikke er blevet leveret. Dette kan skyldes, at linjen blev afvist eller erstattes, hvor de oprindelige linjer ikke forventes at blive leveret, eller at en linje er blevet opdelt i flere tidsplanlinjer, og den oprindelige linje ikke forventes at blive leveret som anmodet i den modtagne ordre. Eventuelle ændringer til ordrelinjesvaret vises, med undtagelse af de overførte noter og vedhæftede filer, som du kan se ved hjælp af webgrænsefladen til kreditorsamarbejde.

## <a name="open-confirmed-orders"></a>Åbn bekræftede ordrer
Når indkøbsordren er bekræftet af kunden, hvilket betyder, at købsordren ændres til tilstanden Bekræftet, vises den i den åbne bekræftede ordre. Den forbliver på listen, indtil den registreres af kunden.





