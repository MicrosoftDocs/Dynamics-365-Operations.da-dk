---
title: "Mobilarbejdsområde for kreditorsamarbejde"
description: "Dette emne indeholder oplysninger om arbejdsområdet Kreditorsamarbejde på mobilenheder. I dette arbejdsområde kan dine kreditorer holde sig opdateret om de indkøbsordrer, der er sendt til dem til godkendelse. De kan også få vist oplysninger om nye og opdaterede indkøbsordrer og kontaktpersoner."
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 83fcf1d0432d5afa71d6f9d7d22cea5a583777bf
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-collaboration-mobile-workspace"></a>Mobilarbejdsområde for kreditorsamarbejde

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om arbejdsområdet **Kreditorsamarbejde** på mobilenheder. I dette arbejdsområde kan dine kreditorer holde sig opdateret om de indkøbsordrer, der er sendt til dem til godkendelse. De kan også få vist oplysninger om nye og opdaterede indkøbsordrer og kontaktpersoner.

Dette arbejdsområdet til mobilenheder er beregnet til brug med Microsoft Dynamics 365 for Unified Operations-mobilappen.

## <a name="overview"></a>Overblik 
Arbejdsområdet **Kreditorsamarbejde** på mobilenheder holder kreditorerne underrettet om nye indkøbsordrer, så de kan se indkøbsordrer og reagere på dem i webklienten til Microsoft Dynamics 365 for Finance and Operations. 

>[!NOTE]
> Det mobile arbejdsområde bør anvendes som et supplement til webgrænsefladen til kreditorsamarbejde, men ikke som en erstatning. 

Med arbejdsområdet **Kreditorsamarbejde** på mobilenheder kan dine kreditorer få vist nye indkøbsordrer, der er sendt til dem til godkendelse. Det viser indkøbsordreoplysninger, f.eks. produkter, antal og ønskede leveringsdatoer. Prisoplysninger er også tilgængelige, afhængigt af konfigurationen af hver kreditor. 

Når en bruger logger på som kreditor, kan brugeren se, hvilke indkøbsordrer der er besvaret, og hvilke indkøbsordrer der stadig afventer kundehandling. En indkøbsordre kan f.eks. afvente kundehandling, fordi leverandøren har foreslået en anden leveringsdato, men kunden har endnu ikke accepteret denne dato. Leverandøren kan også se en liste over indkøbsordrer, der er bekræftet, men som endnu ikke er leveret. 

Hvis leverandøren vil reagere på en indkøbsordre, er vedkommende nødt til at bruge webgrænsefladen til kreditorsamarbejde, der findes i webklienten. Det kan leverandøren også få flere oplysninger om ordren, f.eks. vedhæftede dokumenter, leveringsadresse pr. linje og gebyrer, der er knyttet til leverandøren. 

Med en speciel sikkerhedsrolle kan leverandøren få vist de kontaktpersoner, der er registreret for en kreditorkonto. Med den samme sikkerhedsrolle kan kreditoren få vist status for alle brugeranmodninger, der er sendt. 

Webgrænsefladen for kreditorsamarbejde i webklienten skal bruges til at oprette nye kontakter og sende nye brugeranmodninger. 

Arbejdsområdet **Kreditorsamarbejde** til mobilenheder giver en leverandør mulighed for at udføre disse opgaver:

-   Få vist nye indkøbsordrer, der er sendt til kreditoren.
-   Få vist indkøbsordrer, som kreditoren har besvaret, og som afventer kundehandling.
-   Få vist indkøbsordrer, der er bekræftet, og som ikke er blevet fuldt modtaget.
-   Få vist kontaktpersonens oplysninger, der er registreret for kreditorkontoen. (Denne opgave kræver en ekstra sikkerhedsrolle).
-   Få vist oplysninger om en brugeranmodning, der er afsendt af kreditoren, og følge status for anmodningen. (Denne opgave kræver en ekstra sikkerhedsrolle).

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne varierer alt efter, hvilken version af Microsoft Dynamics 365 der er installeret i din organisation.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Finance and Operations 
Hvis Microsoft Dynamics 365 for Finance and Operations er implementeret for organisationen, skal systemadministratoren publicere arbejdsområdet **Kreditorsamarbejde** til mobilenheder. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere.
Hvis Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere er implementeret for organisationen, kan systemadministratoren skal opfylde følgende forudsætninger. 

<table>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 3216943 skal implementeres, hvis du bruger platformsopdatering 3.</td>
<td>Systemadministrator</td>
<td>KB 3216943 er en binær opdatering, der skal bruges, hvis du bruger platformsopdatering 3. For at implementere denne KB skal systemadministratoren gøre følgende.
<ol>
<li>Hent KB 3216943 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li>Installer den binære opdatering, der leveres som en pakke, der kan installeres. Du kan finde oplysninger om, hvordan du anvender en pakke, der kan installeres, i <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Anvende en installerbar pakke</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>KB 4013633 skal være implementeret.</td>
<td>Systemadministrator</td>
<td>KB 4013633 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Disponibelt lager</strong> til mobilenheder. For at implementere KB 4013633 skal systemadministratoren gøre følgende.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Hent metadata-hotfixet fra LCS</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installere metadatahotfixet</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Anvend den installerbare pakke</a></li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilarbejdsområdet <strong>Kreditorsamarbejde</strong> skal være publiceret.</td><td>Systemadministrator</td>
<td>Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
<tr class="even">
<td>Kreditorbrugeren skal have adgang til webgrænsefladen for kreditorsamarbejde i webklienten og skal konfigurere en bruger til kreditorsamarbejd.</td><td>Indkøbsmedarbejdere og systemadministratoren</td>
<td>Følg trinnene i følgende emner for at oprette og arbejde med webgrænsefladen til kreditorsamarbejde.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Brug kreditorsamarbejde til at arbejde sammen med eksterne kreditorer</a></li>
<li><a href="manage-vendor-collaboration-users.md">Administrere brugere af kreditorsamarbejde</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Konfigurere og vedligeholde kreditorsamarbejde</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Brug kreditorsamarbejde til at arbejde sammen med kunder i Finance and Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen

Download og installer Dynamics 365 for Unified Operations-mobilappen:

-   [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen
1.  Start appen på din mobilenhed.
2.  Angiv URL-adressen til din Microsoft Dynamics 365.
4.  Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
5.  Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

    [![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Brug mobilarbejdsområdet for kreditorsamarbejde
Når du vælger **Kreditorsamarbejde**-arbejdsområdet, kan du se følgende indstillinger.

![Mobilarbejdsområde for kreditorsamarbejde](./media/vendor-collaboration-mobile-app.png)

**Kreditorsamarbejde**-arbejdsområdet indeholder følgende sider.

### <a name="contacts"></a>Kontaktpersoner
På siden **Kontakter** kan du se alle de kontakter, der er angivet for kreditorkontoen. Den viser kontaktpersonens navn, primære mailadresse og brugeralias, hvis kontaktpersonen har et alias. Siden viser også, om kontaktpersonens brugerkonto er aktiv. Når du vælger en kontakt, får du vist kontaktoplysninger, f.eks. de juridiske enheder, som personen er kontakt for. Du kan også se kontaktoplysninger som telefonnummer eller en alternativ mailadresse.

### <a name="user-requests"></a>Brugeranmodninger
På siden **Brugeranmodninger** kan du se alle brugeranmodninger, som du har sendt via webgrænsefladen til leverandørsamarbejde. Du kan også følge status for disse anmodninger. Når du vælger en brugeranmodning, kan du se, hvad der blev anmodet om, tilføje eller deaktivere en bruger, ændre sikkerhed og se, hvilke sikkerhedsroller der blev anmodet om for brugeren.

### <a name="purchase-orders-ready-for-review"></a>Indkøbsordrer klar til gennemsyn
På siden **Indkøbsordrer, der er klar til gennemsyn** kan du se alle de indkøbsordrer, der er sendt af kunden, men endnu ikke er reageret på. Du kan se udvalgte oplysninger om ordren, f.eks. hvilke produkter, der er anmodet om, og hvornår de skal leveres. Prisoplysninger er også tilgængelige, afhængigt af konfigurationen af kreditoren.

Du kan også se, om indkøbsordren indeholder noter og vedhæftede filer. Hvis du vil åbne noter og vedhæftede filer, skal du bruge webgrænsefladen til kreditorsamarbejde i webklienten. Vælg **Indkøbsordrelinje** for at få vist alle linjer sammen med detaljer. For hver linje vises en indikator, om der er noter eller vedhæftede filer, eller om leveringsadressen er forskellig fra den, der vises i hovedet.

For at reagere på indkøbsordren skal du bruge webgrænsefladen til kreditorsamarbejde i webklienten.

### <a name="awaiting-customer-action"></a>Afventer kundehandling
Siden **Afventer kundehandling** giver dig mulighed for at søge efter de indkøbsordrer, som du eller en anden person i virksomheden, der også har adgang til kreditorsamarbejde, har reageret på. Indkøbsordrer er kun synlige på denne liste, hvis kunden skal udføre en af følgende handlinger på indkøbsordren:

-   Hvis indkøbsordren blev afvist, skal kunden enten opdatere eller annullere den oprindelige ordre og sende den igen. Når indkøbsordren sendes igen, vises den ikke længere på siden **Afventer kundehandling**.
-   Hvis indkøbsordren blev accepteret med ændringer, skal kunden enten opdatere den oprindelige ordre og sende den igen til gennemsyn eller opdatere den i overensstemmelse med de anmodede ændringer og straks bekræfte den. I begge tilfælde vises indkøbsordren ikke længere på siden **Afventer kundehandling**.
-   Hvis indkøbsordren blev accepteret, men stadig vises på siden **Afventer kundehandling**, er indkøbsordren ikke automatisk blevet bekræftet, da den blev accepteret. Den venter på, at en indkøber skal ændre status til **Bekræftet**. Indkøbsordren betragtes normalt som en aftale mellem debitor og kreditor, så snart kreditoren accepterer ordren. Derfor er en opdatering af **Bekræftet**-status normalt kun en formalitet.

Når du vælger en indkøbsordre, vises yderligere oplysninger om svaret. Du kan se linjedetaljerne og besvare hver linje. På statuslinjen vises, hvilke af følgende svar der er givet:

-   Accepteret
-   Afvist
-   Accepteret med ændringer
-   Erstattet/erstatning
-   Opdel i tidsplan/tidsplanslinje

Bemærk, at feltet **Leverer** er indstillet til enten **Ja** eller **Nej** for at angive, om linjerne skal afleveres. En linje kan ikke leveres af følgende årsager:

- Linjen er afvist.
- En erstatning blev foretaget, og den oprindelige linje forventes ikke leveret som anmodet i den modtagne ordre.
- Linjen er opdelt i flere planlægningslinjer, og den oprindelige linje forventes ikke leveret som anmodet i den modtagne ordre.

Eventuelle ændringer, der er foretaget i svaret til ordrelinjen, vises. Dog vises overførte noter og vedhæftede filer ikke. Hvis du se noter og vedhæftede filer, skal du bruge webgrænsefladen til kreditorsamarbejde i webklienten.

### <a name="open-confirmed-orders"></a>Åbn bekræftede ordrer
Når indkøbsordren er bekræftet af kunden (hvilket betyder, at status for købsordren er ændret til **Bekræftet**), vises den i den åbne bekræftede ordre. Den forbliver på listen, indtil den registreres som modtaget af kunden.

