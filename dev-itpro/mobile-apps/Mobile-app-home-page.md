---
title: Startside Dynamics 365 for Operations-mobilapp
description: "I dette emne beskrives Microsoft Dynamics 365 for Operations-mobilappen. Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Startside Dynamics 365 for Operations-mobilapp

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


I dette emne beskrives Microsoft Dynamics 365 for Operations-mobilappen. Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation.

<a name="overview"></a>Overblik
--------

Med Microsoft Dynamics 365 for Operations-mobilappen kan organisationen gøre sine forretningsprocesser tilgængelige på mobilenheder. Når din IT-administrator har aktiveret arbejdsområdet til mobilenheder for din organisation, kan brugerne logge på appen og straks begynde at køre forretningsprocesser fra deres mobilenheder. Dynamics 365 for Operations-mobilappen indeholder følgende funktioner, der kan hjælpe med at øge produktiviteten:

-   Brugerne kan få vist, redigere og bruge forretningsdata, selvom de har uregelmæssig netværksforbindelse, eller deres mobilenheder er helt offline. Når en enhed genopretter en netværksforbindelse, synkroniseres offlinedatahandlinger automatisk med Dynamics 365 for Operations.
-   It-administratorer eller udviklere kan bygge og udgive arbejdsområder til mobilenheder, der er skræddersyet til deres organisation. Appen bruger eksisterende kodeaktiver. Derfor behøver du ikke igen at implementere dine valideringsprocedurer, forretningslogik eller sikkerhedskonfiguration.
-   It-administratorer eller udviklere kan nemt designe arbejdsområder til mobilenheder ved hjælp af peg og klik-arbejdsområdedesigneren, der leveres med Dynamics 365 for Operations-webklienten.
-   It-administratorer eller udviklere kan vælge at optimere offlinefunktionerne for arbejdsområder ved hjælp af udvidelsesstrukturen for forretningslogik. Da data fortsat behandles, mens en enhed er offline, forbliver dine mobilscenarier omfattende og flydende, selvom enhederne ikke har konstant netværksforbindelse.

## <a name="elements-of-the-mobile-app"></a>Elementer i mobilappen
Navigation i mobilappen består af fire enkle begreber: dashboardet, arbejdsområder, sider og handlinger. 

[![Begreber til navigation i mobilappen](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Når du starter appen, kommer du til **dashboardet**.
-   I dashboardet kan du se en liste over **arbejdsområder**, som er publiceret i dit Dynamics 365 for Operations-miljø.
-   I hvert arbejdsområde kan du se en liste over **sider**, der er tilgængelige for det pågældende arbejdsområde.
-   På en side kan du få vist data, der er indsamlet fra en eller flere sider i Dynamics 365 for Operations.
-   Fra en side kan du navigere til andre sider for at se relaterede data, f.eks. oplysninger om enheder eller linjer.
-   På en side kan du også se en liste over **handlinger**, der er tilgængelige for den pågældende side.
-   Med handlinger kan du oprette eller redigere eksisterende data.

## <a name="implementation-process"></a>Implementeringsproces
I følgende illustration vises processen til implementering af Dynamics 365 for Operations-mobilappen i organisationen. 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

Følgende tabel indeholder links til ressourcer, der kan hjælpe dig med implementere Dynamics 365 for Operations-mobilappen i din organisation. Tallene i den første kolonne svarer til de nummererede trin i ovenstående illustration.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Trin</th>
<th>Rolle</th>
<th>Handling</th>
<th>Ressourcer, som du kan bruge til at fuldføre handlingen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Systemadministrator</td>
<td>Implementer Dynamics 365 for Operations i organisationen.</td>
<td>Hvis Dynamics 365 for Operations ikke allerede er installeret i organisationen, kan du se <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Installere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemadministrator</td>
<td>Hent og installer KB'er om de arbejdsområder til mobilenheder, der leveres af Microsoft.</td>
<td>Se afsnittet &quot;Forudsætninger&quot; i emnet om arbejdsområdet til de mobilenheder, som din organisation vil bruge:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Arbejdsområde til omkostningsstyring på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Arbejdsområde for disponibelt lager på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Arbejdsområder for salgsordrer på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilarbejdsområde for kreditorsamarbejde</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Projekttidsregistrering i arbejdsområde til mobilenhed</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Systemadministrator</td>
<td>Publicer de arbejdsområder til mobilenheder, der leveres af Microsoft.</td>
<td>Se afsnittet &quot;Forudsætninger&quot; i emnet om arbejdsområdet til de mobilenheder, som din organisation vil bruge:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Arbejdsområde til omkostningsstyring på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Arbejdsområde for disponibelt lager på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Arbejdsområder for salgsordrer på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilarbejdsområde for kreditorsamarbejde</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Projekttidsregistrering i arbejdsområde til mobilenhed</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>Udvikler eller uafhængig softwareleverandører (ISV)</td>
<td>Du kan bruge Dynamics 365 for Operations-mobilstrukturen til at oprette brugerdefinerede arbejdsområder til mobilenheder.</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operations-mobilstruktur</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">API'er til Dynamics 365 for Operations-arbejdsområde X++</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV (Independent Software Vendor)</td>
<td>Opret en pakke, der kan installeres, og som indeholder brugerdefinerede arbejdsområder til mobilenheder, og overfør pakken til Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Oprette en installerbar pakke</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Systemadministrator</td>
<td>Anvend den installerbare pakke, der indeholder de brugerdefinerede arbejdsområder, der er leveret af ISV'en.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Anvende en installerbar pakke på et Microsoft Dynamics 365 for Operations-system</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Systemadministrator</td>
<td>Publicer de brugerdefinerede arbejdsområder til mobilenheder, der er leveret af ISV'en.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publicere et arbejdsområde til mobilenheder</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Bruger</td>
<td>Hent og installer Dynamics 365 for Operations-mobilappen.</td>
<td><ul>
<li>Til Android: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations i Google Play Butik</a></li>
<li>Til iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations i iTunes-appbutikken</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Bruger</td>
<td>Log på, og brug Dynamics 365 for Operations-mobilappen. Appen indeholder de arbejdsområder til mobilenheder, der er udgivet.</td>
<td>Microsoft har leveret følgende arbejdsområder til mobilenheder:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Arbejdsområde til omkostningsstyring på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Arbejdsområde for disponibelt lager på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Arbejdsområder for salgsordrer på mobilenheder</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobilarbejdsområde for kreditorsamarbejde</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Projekttidsregistrering i arbejdsområde til mobilenhed</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Se også
--------

[Arbejdsområder til mobilenheder, der er udgivet for nylig til Dynamics 365 for Operations-mobilappen](mobile-workspaces-released.md)





