---
title: Arbejdsområde for fakturagodkendelser på mobilenheder
description: Denne artikel indeholder oplysninger om arbejdsområdet til fakturagodkendelse på mobilenheder.
author: abruer
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4cc05d9fcea129cfb2ed8ed8df4bd4034a1fed4c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066384"
---
# <a name="invoice-approvals-mobile-workspace"></a>Arbejdsområde for fakturagodkendelser på mobilenheder

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

Denne artikel indeholder oplysninger om mobilarbejdsområdet **Fakturagodkendelser**. Arbejdsområdet indeholder en liste over fakturaer, der er tildelt til dig via arbejdsgangen for kreditorfakturahovedet. 

Dette mobile arbejdsområde er beregnet til brug sammen med finans og drift-mobilappen.

## <a name="overview"></a>Overblik

I arbejdsområdet **Fakturagodkendelser** til mobilenheder kan kreditormedarbejdere og -chefer få vist fakturaer, der er tildelt til dem som en del af arbejdsgangen for kreditorfakturahovedet. Du kan få vist fakturaoplysninger og også linje- og distributionsoplysninger, så du kan træffe kvalificerede godkendelsesbeslutninger. Fra arbejdsområdet kan du tage skridt til at flytte fakturaen gennem arbejdsgangsprocessen. 

## <a name="prerequisites"></a>Forudsætninger

Før du kan bruge dette mobilarbejdsområde, skal følgende forudsætninger være opfyldt.

<table>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Beskrivende tekst</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 Finance skal udrulles i din organisation.</td>
<td>Systemadministrator</td>
<td>Se <a href="../deployment/deploy-demo-environment.md">Installere et demomiljø</a>.
</td>
</tr>
<tr class="even">
<td>Mobilarbejdsområdet <strong>Fakturagodkendelser</strong> skal være publiceret.</td>
<td>Systemadministrator</td>
<td>Se <a href="publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen

Download og installer finans og drift-mobilappen:

-   [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen

1.  Start appen på din mobilenhed.
2.  Angiv din Microsoft Dynamics 365 URL-adresse.
3.  Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
4.  Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

    [![Træk ned for at opdatere.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Godkend fakturaer ved hjælp af arbejdsområdet Fakturagodkendelser til mobilenheder
1.  På din mobilenhed skal du vælge arbejdsområdet **Fakturagodkendelser**.
2.  Vælg den faktura, der er tildelt til dig af arbejdsgangen for kreditorfakturahovedet.
3.  På siden **Fakturadetaljer** skal du gennemse oplysningerne i fakturahovedet, f.eks. oplysninger om leverandør og dato.
4.  Vælg en linje på fakturaen for at få vist mere detaljerede oplysninger om den i visningen **Detaljer om fakturalinje**.
5.  Vælg **Fordelinger** i visningen **Detaljer om fakturalinje** for at se linjefordelingerne. Her kan du se regnskabet for fakturalinjen. De oplysninger, der vises, omfatter de økonomiske dimensioner og hovedkontoen.
6.  Vælg **Fordelinger** på siden **Fakturadetaljer** for at se alle fordelinger. Her kan du se regnskabet for hele fakturaen. De oplysninger, der vises, omfatter de økonomiske dimensioner og hovedkontiene. 
7.  Vælg **Vedhæftede filer** for at få vist noter eller filer, der er tilknyttet fakturaen.
8.  På siden **Fakturadetaljer** skal du vælge den relevante handling i arbejdsgangen for at fuldføre valideringsprocessen.
9.  Vælg **Udført**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

