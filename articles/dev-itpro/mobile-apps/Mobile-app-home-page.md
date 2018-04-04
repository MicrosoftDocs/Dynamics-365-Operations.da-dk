---
title: Mobilapp-startside
description: "I dette emne beskrives Microsoft Dynamics 365 for Unified Operations-mobilappen. Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b84778bd67e8c5bad6e8858d2af71f46e0dfe145
ms.contentlocale: da-dk
ms.lasthandoff: 03/26/2018

---

# <a name="mobile-app-home-page"></a>Mobilapp-startside

[!include[banner](../includes/banner.md)]

I dette emne beskrives Microsoft Dynamics 365 for Unified Operations-mobilappen. Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation.

> [!NOTE]
> Mobilappen blev tidligere kaldt *Microsoft Dynamics 365 for Finance and Operations*.

<a name="overview"></a>Overblik
--------

Med mobilappen kan organisationen gøre sine forretningsprocesser tilgængelige på mobilenheder. Når din IT-administrator har aktiveret arbejdsområdet til mobilenheder for din organisation, kan brugerne logge på appen og straks begynde at køre forretningsprocesser fra deres mobilenheder. Mobilappen indeholder følgende funktioner, der kan hjælpe med at øge produktiviteten:

- Brugerne kan få vist, redigere og bruge forretningsdata, selvom de har uregelmæssig netværksforbindelse, eller deres mobilenheder er helt offline. Når en enhed genopretter en netværksforbindelse, synkroniseres offlinedatahandlinger automatisk med Dynamics 365 for Finance and Operations.
- It-administratorer eller udviklere kan bygge og udgive arbejdsområder til mobilenheder, der er skræddersyet til deres organisation. Appen bruger eksisterende kodeaktiver. Derfor behøver du ikke igen at implementere dine valideringsprocedurer, forretningslogik eller sikkerhedskonfiguration.
- It-administratorer eller udviklere kan nemt designe arbejdsområder til mobilenheder ved hjælp af peg og klik-arbejdsområdedesigneren, der leveres med webklienten.
- It-administratorer eller udviklere kan vælge at optimere offlinefunktionerne for arbejdsområder ved hjælp af udvidelsesstrukturen for forretningslogik. Da data fortsat behandles, mens en enhed er offline, forbliver dine mobilscenarier omfattende og flydende, selvom enhederne ikke har konstant netværksforbindelse.

## <a name="elements-of-the-mobile-app"></a>Elementer i mobilappen
Navigation i mobilappen består af fire grundbegreber: dashboardet, arbejdsområder, sider og handlinger. 

[![Begreber til navigation i mobilappen](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Når du starter appen, kommer du til **dashboardet**.
2. I dashboardet kan du se en liste over de **arbejdsområder**, der er publiceret.
3. I hvert arbejdsområde kan du se en liste over **sider**, der er tilgængelige for det pågældende arbejdsområde.
4. Når du er på en side, kan du udføre flere handlinger. Her er nogle eksempler:

    - Se detaljerede data.
    - Navigere til andre sider for at se relaterede data, f.eks. oplysninger om enheder eller linjer.
    - Se en liste over **handlinger**, der er tilgængelige for den pågældende side. Med handlinger kan du oprette eller redigere eksisterende data.

## <a name="implementation-process"></a>Implementeringsproces
I følgende illustration vises processen til implementering af både arbejdsområder til mobilenheder, der leveres af Microsoft, og brugerdefinerede arbejdsområder til mobilenheder. 

![Implementeringsproces for mobilapps](./media/Mobile-implementation-process-5.png)

Tabellen nedenfor indeholder links til ressourcer, der kan hjælpe dig med at implementere både arbejdsområder til mobilenheder, der leveres af Microsoft, og brugerdefinerede arbejdsområder til mobilenheder. Tallene i den første kolonne svarer til de nummererede trin i ovenstående illustration.

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
<td>Implementer Finance and Operations i din organisation.</td>
<td><ul><li>Hvis du endnu ikke har installeret en version af Microsoft Dynamics 365, kan du se under <a href="../deployment/deploy-demo-environment.md">Installere et demomiljø</a>.</li><li>Du kan se en liste over arbejdsområder til mobilenheder, der kan bruges, under <a href="mobile-workspaces-released.md">Arbejdsområde til mobilenheder, der er udgivet for nylig</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemadministrator</td>
<td><strong>Hvis du bruger Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Hent og installer KB'er, der gør det muligt at bruge de arbejdsområder til mobilenheder, der leveres af Microsoft.</td>
<td>Du kan finde flere oplysninger under følgende emner:
<ul>

<li><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Arbejdsområde til omkostningsstyring på mobilenheder</a></li>
<li><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Disponibelt lager i mobilarbejdsområde</a></li>
<li><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Arbejdsområder for salgsordrer på mobilenheder</a></li>
<li><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobilarbejdsområde for kreditorsamarbejde</a></li>
<li><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Projekttidsregistrering i arbejdsområde til mobile enheder</a></li>
<li><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Arbejdsområde til udgiftsstyring på mobilenhed</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Systemadministrator</td>
<td>Publicer de arbejdsområder til mobilenheder, der leveres af Microsoft.</td>
<td><a href="publish-mobile-workspace.md">Publicer et arbejdsområde til mobilenheder</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Udvikler eller uafhængig softwareleverandører (ISV)</td>
<td>Du kan bruge mobilplatformen til at oprette brugerdefinerede arbejdsområder til mobilenheder.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobilplatform</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV (Independent Software Vendor)</td>
<td>Opret en pakke, der kan installeres, og som indeholder brugerdefinerede arbejdsområder til mobilenheder, og overfør pakken til Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Systemadministrator</td>
<td>Anvend den installerbare pakke, der indeholder de brugerdefinerede arbejdsområder, der er leveret af den uafhængige softwareleverandør.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Anvend en installerbar pakke</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Systemadministrator</td>
<td>Publicer de brugerdefinerede arbejdsområder til mobilenheder, der er leveret af ISV'en.</td>
<td><a href="publish-mobile-workspace.md">Publicer et arbejdsområde til mobile enheder</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Bruger</td>
<td>Download og installer mobilappen.</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">Til Android-telefoner</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">Til iPhones</a></li></ul>
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Bruger</td>
<td>Log på og brug mobilappen. Appen indeholder de arbejdsområder til mobilenheder, der er udgivet af systemadministratoren.</td>
<td>Du kan se en liste over arbejdsområder til mobilenheder, der leveres af Microsoft, under <a href="mobile-workspaces-released.md">Arbejdsområde til mobilenheder, der er udgivet for nylig</a>.
</td>
</tr>
</tbody>
</table>

