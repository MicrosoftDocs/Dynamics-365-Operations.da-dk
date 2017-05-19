---
title: "Arbejdsområde for salgsordrer på mobilenheder"
description: "Dette emne indeholder oplysninger om arbejdsområdet for salgsordrer på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Operations-mobilappen. Dette arbejdsområde hjælper dig med at holde dig opdateret om salgsordrer hvor som helst og hvor som helst."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 119b80e5d8067ffbf75d8b067f4803558c2c94b0
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Arbejdsområde for salgsordrer på mobilenheder

[!include[banner](../includes/banner.md)]


Dette emne indeholder oplysninger om arbejdsområdet for salgsordrer på mobilenheder, som kan anvendes på Microsoft Dynamics 365 for Operations-mobilappen. Dette arbejdsområde hjælper dig med at holde dig opdateret om salgsordrer hvor som helst og hvor som helst. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Oversigt over arbejdsområde for salgsordrer på mobilenheder
---------------------------------------------

I arbejdsområdet **Salgsordrer** til mobilenheder er der adgang til Microsoft Dynamics 365 for Operations, hvor du kan få vist detaljerede oplysninger om de enkelte salgsordrer. Disse oplysninger omfatter ordrestatus, kontaktoplysninger for debitoren og kontaktoplysninger for ordretageren. Arbejdsområdet **Salgsordrer** til mobilenheder giver en øjeblikkelig visning af salgsordrer. Du kan få vist alle salgsordrer, salgsordrer pr. kunde eller oplysninger om en bestemt salgsordre. Arbejdsområdet til mobile enheder indeholder to visninger, der hjælper dig med at analysere salgsordrer i dybden.

### <a name="view-all-sales-orders"></a>Vis alle salgsordrer

Denne visning viser alle salgsordrer.

-   Brug ét af følgende filtre til at vælge de salgsordrer, du vil have vist:
    -   Søg efter salgsordre
    -   Søg efter kundekonto
    -   Søg efter kundenavn
    -   Søg efter status
    -   Søg efter status for frigivelse
    -   Søg efter dato og klokkeslæt for oprettelse
-   Når du har valgt salgsordrerne, kan du få vist detaljerede oplysninger om bestemte ordrer. Du kan især se følgende oplysninger:
    -   Oplysninger om kundens navn og adresse
    -   Forskellige datoer for salgsordrerne, f.eks. den ønskede afsendelsesdato og den bekræftede afsendelsesdato
    -   Kontaktoplysninger for ordretageren
    -   Kundekontaktoplysninger
    -   Ordrelinjer
    -   Forsendelser, der viser, hvordan og hvornår en salgsordre blev leveret

### <a name="view-orders-for-a-customer"></a>Vis ordrer for en kunde

Denne visning angiver salgsordrer pr. kunde.

-   Brug et af følgende filtre til at se ordrer for en kunde:
    -   Søg efter navn
    -   Søg efter konto
-   Når du har valgt en kunde, kan du få vist følgende oplysninger:
    -   Kundenavn og -gruppe
    -   Kundekontaktoplysninger
    -   Salgsordrer for kunden og oplysninger om disse salgsordrer:
        -   Oplysninger om kundens navn og adresse
        -   Diverse salgsordredatoer
        -   Kontaktoplysninger for ordretageren
        -   Kundekontaktoplysninger
        -   Ordrelinjer
        -   Forsendelser, der viser, hvordan og hvornår en salgsordre blev leveret

## <a name="prerequisites"></a>Forudsætninger
Før du kan bruge arbejdsområdet **Salgsordrer** til mobilenheder, skal systemadministratoren have sørget for, at følgende forudsætninger er opfyldt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Betegnelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere skal være implementeret.</td>
<td>Systemadministrator</td>
<td>Hvis Dynamics 365 for Operations ikke allerede er installeret i organisationen, kan systemadministratoren se under <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Installere et Microsoft Dynamics 365 for Operations-demomiljø</a>.</td>
</tr>
<tr class="even">
<td>KB 4013633 skal være implementeret.</td>
<td>Systemadministrator</td>
<td>KB 4013633 (en X ++ opdatering eller et metadatahotfix) indeholder fire arbejdsområder til mobilenheder til supply chain management. For at implementere KB 4013633 skal systemadministratoren benytte følgende fremgangsmåde:
<ol>
<li>Hent KB 4013633 fra Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Installere metadatahotfixet</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Anvend den installerbare pakke</a> på dit Microsoft Dynamics 365 for Operations-system.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Arbejdsområdet <strong>Salgsordrer</strong> til mobilenheder skal være publiceret til Dynamics 365 for Operations-mobilappen.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Start Dynamics 365 for Operations i din browser.</li>
<li>På siden <strong>Systemparametre</strong> skal du vælge <strong>Administrer arbejdsområder til mobile enheder</strong>.</li>
<li>Vælg arbejdsområdet <strong>Salgsordrer</strong>.</li>
<li>Klik på <strong>Publicer arbejdsområde til mobilenheder</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Hent og installer Dynamics 365 for Operations-mobilappen
Hent og installer Microsoft Dynamics 365 for Operations-mobilappen i din mobilappbutik.

-   Til Android: [Dynamics 365 for Operations i Google Play Butik](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Til iPhone: [Dynamics 365 for Operations i iTunes-appbutikken](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Log på Dynamics 365 for Operations-mobilappen
1.  Start appen på din mobilenhed.
2.  Angiv din URL til Dynamics 365 for Operations.
3.  Angiv det firma, du vil logge på. Du kan f.eks. skrive **USMF**.
4.  Første gang du logger på, bliver du bedt om brugernavn og adgangskode til din Dynamics 365 for Operations-konto. Angiv dine legitimationsoplysninger.
5.  Når du har logget på, kan du se de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren senere publicerer et nyt arbejdsområde, kan du trække for at opdatere listen over arbejdsområder til mobilenheder. 

    [![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Få vist oplysninger om salgsordrer for en kunde ved hjælp af arbejdsområdet til mobilenheder
1.  På din mobilenhed skal du vælge arbejdsområdet **Salgsordrer**.
2.  Vælg **Vis ordrer for en kunde**.
3.  Brug oplysningerne om konto eller kundenavn til at finde kunden.
4.  Vælg kunden.
5.  Vælg **Kontaktoplysninger** eller **Salgsordrer**. Hvis du vælger **Salgsordrer**, vises der en liste over salgsordrer for kunden.
6.  Vælg **Salgsordre**. Du kan nu få vist oplysninger om salgsordrelinjer, oplysninger om forsendelser, kundekontaktoplysninger og kontaktoplysninger for ordretageren.





