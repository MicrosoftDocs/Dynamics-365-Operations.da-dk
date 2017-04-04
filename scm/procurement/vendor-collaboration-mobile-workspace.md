---
title: "Kreditor mobile arbejdsområde til samarbejde for Microsoft Dynamics 365 for operationer app"
description: "Med kreditor mobile arbejdsområdet til samarbejde ajour kreditorerne på indkøbsordrer, der er blevet sendt til dem til godkendelse og få vist oplysninger om nye og opdaterede indkøbsordrer og kontaktpersoner."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kreditor mobile arbejdsområde til samarbejde for Microsoft Dynamics 365 for operationer app

Med kreditor mobile arbejdsområdet til samarbejde ajour kreditorerne på indkøbsordrer, der er blevet sendt til dem til godkendelse og få vist oplysninger om nye og opdaterede indkøbsordrer og kontaktpersoner.

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
<td>Læs om Microsoft Dynamics-365 for operationer mobilplatform</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for operationer mobilplatform</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 til operationer</td>
<td>Sørg for, at du bruger et miljø, hvor Microsoft Dynamics 365 for operationer version 1611 opdager og Microsoft Dynamics for operationer platform update 3 (November 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobile enhed, der har den Dynamics 365 for operationer app installeret</span></td>
<td><span style="color: #000000;">Hent den Dynamics 365 for operationer app fra din mobile app butik.</span></td>
</tr>
<tr class="even">
<td>Hotfix KB 3215650</td>
<td>Installere hotfixet, hvis du vil aktivere de arbejdsområder, der findes i Dynamics 365 for operationer.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Hotfix KB 3216943</span> </span></td>
<td>Installere hotfixet, hvis du vil aktivere kreditoren mobile arbejdsområdet til samarbejde.</td>
</tr>
<tr class="even">
<td>Kreditorbrugeren skal have adgang til webgrænsefladen leverandør samarbejde i Dynamics 365 for operationer og konfigurere en kreditorbruger samarbejde.</td>
<td>Følg de trin, der er beskrevet i følgende emner til at oprette og arbejde med webgrænsefladen leverandør samarbejde.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Leverandør samarbejde kan bruge til at arbejde sammen med eksterne leverandører</a></li>
<li><a href="manage-vendor-collaboration-users.md">Administrere brugere af kreditorsamarbejde</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Konfigurere og vedligeholde kreditorsamarbejde</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Bruge leverandør samarbejde til at arbejde med kunder i Dynamics 365 til operationer</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Overblik
Arbejdsområdet leverandør samarbejde mobile holder kreditorer underrettet om nye indkøbsordrer, så de kan se og reagere på indkøbsordrer i Dynamics-365 for operationer-webklienten.  

**Bemærk:** mobile arbejdsområdet bør anvendes som et supplement til webgrænsefladen leverandør samarbejde, men ikke en erstatning.  

Med kreditor mobile arbejdsområdet til samarbejde, dine kreditorer kan få vist nye indkøbsordrer, der er sendt til godkendelse. Det viser indkøbsordreoplysninger, produkter, antal og ønskede leveringsdatoer. Prisoplysninger er tilgængelige, afhængigt af konfigurationen for hver kreditor.  

Når en bruger logger på som en kreditor, kan de se hvilke indkøbsordrer er blevet besvaret, eller hvilke indkøbsordrer der stadig afventer kunde handling. Leverandøren kan har foreslået en anden dato for levering, ikke endnu har aftalt med kunden, så kunden handling venter på indkøbsordren. Leverandøren kan også se en liste over indkøbsordrer, der er bekræftet, men som endnu ikke er leveret.  

Hvis du vil besvare en indkøbsordre, har kreditoren bruge leverandør samarbejde-webgrænseflade, der findes i Dynamics-365 for operationer-webklienten. Dette er også hvor leverandøren får flere oplysninger om leveringsadressen pr. linje og gebyrer, der er knyttet til kreditoren, ordre, som dokumentet vedhæftede filer.  

Med en speciel sikkerhedsrolle, kreditoren kan få vist hvilken Kontakt personer, der er registreret for en kreditorkonto. Med den samme sikkerhedsrolle kreditoren kan få vist status for enhver anmodning, der er sendt.  

Oprette nye kontaktpersoner og sende nye brugeranmodninger, skal det ske i grænsefladen leverandør samarbejde, der findes i Dynamics-365 for operationer-webklienten.  

Med mobile arbejdsområde kan leverandøren:

-   Få vist nye indkøbsordrer, der er sendt til leverandøren.
-   Få vist indkøbsordrer, at leverandøren har besvaret og afventer kunde handling.
-   Få vist indkøbsordrer, der er bekræftet, og er ikke blevet fuldt modtaget.
-   Få vist oplysninger om kontaktperson, der er registreret for kreditorkontoen (kræver en ekstra sikkerhedsrolle).
-   Få vist oplysninger og følge status for en anmodning indgivet af kreditor (kræver en ekstra sikkerhedsrolle).

## <a name="get-started"></a>Introduktion
At komme i gang på din mobilenhed:

1.  Din mobile app store, Hent og Installer Microsoft Dynamics-365 for operationer app.
2.  Du kan starte programmet på din enhed.
3.  Angiv URL-adressen for din Dynamics 365.
4.  Angiv firma til at logge på. F.eks. **USMF**.
5.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Microsoft Dynamics-365 for operationer konto. 

Når du logger på app, vises ingen arbejdsområder. For at få vist arbejdsområder på din mobile app, skal du først udgive de ønskede arbejdsområder til Dynamics-365 for operationer app. Du skal bruge system administration tilladelse til at udgive arbejdsområdet.

1.  Start Dynamics 365 for operationer.
2.  Gå til **systemadministration**&gt;**Setup**&gt;**systemparametre**.
3.  Vælg **Manage mobile app**.
4.  Vælg arbejdsområdet **leverandør samarbejde** at udgive til mobil platform.
5.  Vælg **udgive arbejdsområde**.
6.  Opdater din enhed for at se de udgivne arbejdsområder.
7.  Vælg den **leverandør samarbejde** arbejdsområde. Du kan blive den følgende side.

[![kreditor-samarbejde-mobil-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktpersoner
Den **kontakter** på siden kan du se alle de kontaktpersoner, der er angivet for kreditorkontoen. Det viser kontaktpersonens navn, primær e-mail- og brugeralias, hvis den er tilgængelig. Det viser også, om kontaktpersonens brugerkonto er aktiv. Når du markerer en kontaktperson, kan du se kontaktoplysninger, som de juridiske enheder, personen, der er kontaktperson for, og kontakt oplysninger som telefonnummer eller en anden e-mail-adresse.

## <a name="user-requests"></a>Brugeranmodninger
Den **brugeranmodninger** side kan du se alle bruger anmoder om, at du har sendt via webgrænsefladen leverandør samarbejde og følge status. Når du vælger en brugeranmodning, kan du se, hvad der blev anmodet om, tilføje eller deaktivere en bruger, sikkerhed og se, hvilke sikkerhedsroller der blev anmodet om for brugeren.

## <a name="purchase-orders-ready-for-review"></a>Indkøbsordrer, der er klar til gennemsyn
Den **indkøbsordrer, der er klar til gennemsyn** side kan du se alle de indkøbsordrer, der er sendt af kunden og ikke er besvaret. Du kan se markerede oplysninger om den rækkefølge, som har anmodet om hvilke produkter, og hvornår du kan levere. Prisoplysninger er kun tilgængelig, hvis det er konfigureret for kreditoren.  

Du kan se, om indkøbsordren, der indeholder noter og vedhæftede filer. For at åbne vedhæftede filer, skal du bruge leverandør samarbejde i webklienten. Vælg **indkøbsordrelinje** til at få vist alle linjer med detaljer. Bemærk, at for hver linje, en indikator, der viser om der er noter og vedhæftede filer, eller hvis der er en leveringsadresse, som er forskellig fra, hvad der skal vises i hovedet.  

For at besvare indkøbsordren, skal du bruge webklienten leverandør samarbejde.

## <a name="awaiting-customer-action"></a>Afventer kundehandling
Den **afventer kunde handling** side kan du søge efter de indkøbsordrer, som du eller en person i virksomheden, der også har adgang til leverandør samarbejde har reageret på. Købsordrer er kun synlige på denne liste, hvis kunden har brug at udføre en af følgende handlinger på indkøbsordren.

-   Hvis indkøbsordren blev afvist, vil kunden enten skal opdatere sendte ordren og sende igen, eller annullere ordren og sende igen. Når indkøbsordren sendes igen, forsvinder den fra den **afventer kunde handling** side.
-   Hvis indkøbsordren blev accepteret med ændringer, skal kunden til at opdatere den oprindelige ordre og Send til gennemsyn, eller Opdater den i overensstemmelse med ændringerne og bekræfte den straks. I begge tilfælde købsordren forsvinder fra den **afventer kunde handling** side.
-   Hvis indkøbsordren blev accepteret og vises i den **afventer kunde handling** side, det er fordi indkøbsordren ikke bekræftedes automatisk, når accepten blev udført. Der ventes på en indkøberen tilladelse til at ændre rækkefølgen til bekræftet. Indkøbsordren ville normalt betragtes som en aftale mellem debitor og kreditor, som leverandøren accepterer ordren. Flytning af indkøbsordren til tilstanden bekræftet, ville det være en formalitet.

Ved at vælge indkøbsordren, vises yderligere oplysninger om svaret. Du kan se detaljer om og svar for hver linje. I linjen status vises, hvilke af følgende svar er givet.

-   Accepteret
-   Afvist
-   Accepteret med ændringer
-   Erstattede/erstatning
-   Opdelt i tidsplan/Schedule linje

Bemærk, at en indikator, der viser **levere**= Ja/Nej, som bruges til at angive, at linjerne ikke leveres. Dette kan skyldes, at linjen blev afvist eller erstattes, hvor de oprindelige linjer ikke forventes at blive leveret eller en linje, der er opdelt i flere linjer, og den oprindelige linje ikke forventes at blive leveret som krævet i den rækkefølge, der er modtaget.  

Eventuelle ændringer til ordren linjen svar vises, med undtagelse af de overførte noter og vedhæftede filer, som du kan se ved hjælp af webgrænsefladen leverandør samarbejde.

## <a name="open-confirmed-orders"></a>Åbn bekræftede ordrer
Når indkøbsordren er bekræftet af kunden, ændres hvilket betyder, at købsordren til tilstanden bekræftet, vises det i den åbne bekræftede ordre. Indtil det er registreret som modtaget af kunden, vil den forblive på listen.


