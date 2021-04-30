---
title: Arbejdsområdet Godkendelse af indkøbsordre til mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet Godkendelse af indkøbsordre til mobilenheder, hvor du får vist indkøbsordrer og reagere på dem med handlinger. Du kan f.eks. godkende eller afvise en indkøbsordre.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26f0dc3b128daf8c7d8a05d6f3cacc5b7de0c756
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909102"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Arbejdsområdet Godkendelse af indkøbsordre til mobilenheder

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om arbejdsområdet **Godkendelse af indkøbsordre** på mobilenheder. I dette arbejdsområde kan du få vist indkøbsordrer og reagere på dem med handlinger. Du kan f.eks. godkende eller afvise en indkøbsordre.
 
## <a name="overview"></a>Overblik 
Indkøbsordrer, der kræver godkendelse, går gennem en godkendelsesarbejdsgang. Arbejdsgangen kan indeholde forskellige trin, der kræver handling af en eller flere personer. Én person kan f.eks. skulle fuldføre en opgave eller godkende indkøbsordren. 

I arbejdsområdet **Godkendelse af indkøbsordre** til mobilenheder kan du nemt få vist og reagere på indkøbsordrer fra din mobilenhed. I dette arbejdsområde kan du også udføre de samme arbejdsgangshandlinger, som du kan udføre fra webklienten.

## <a name="prerequisites"></a>Forudsætninger
Forudsætningerne varierer alt efter, hvilken version af Supply Chain Management der er installeret i din organisation.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Forudsætninger, hvis du bruger Supply Chain Management 
Hvis Supply Chain Management er implementeret for din organisation, skal systemadministratoren publicere mobilarbejdsområdet **Godkendelse af indkøbsordre**. Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere
Hvis Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere er implementeret for organisationen, skal systemadministratoren opfylde følgende forudsætninger. 

<table>
<thead>
<tr class="header">
<th>Forudsætning</th>
<th>Rolle</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementer KB 4017918.</td>
<td>Systemadministrator</td>
<td>KB 4017918 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Godkendelse af indkøbsordre</strong> til mobilenheder. For at implementere KB 4017918 skal systemadministratoren gøre følgende.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Hente metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installere metadatahotfixet</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Anvend den installerbare pakke</a></li>
</ol></td>
</tr>
<tr class="even">
<td>Publicer arbejdsområdet <strong>Godkendelse af indkøbsordre</strong> til mobilenheder.</td>
<td>Systemadministrator</td>
<td>Se <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicere et arbejdsområde til mobilenheder</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Downloade og installere mobilappen
Sådan downloades og installeres Finance and Operations-mobilappen:

- [Til Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [Til iPhones](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Log på mobilappen

1. Start appen på din mobilenhed.
2. Angiv din Microsoft Dynamics 365 URL-adresse.
3. Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode. Angiv dine legitimationsoplysninger.
4. Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed. Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.

![Arbejdsområdet Godkendelse af indkøbsordre på listen over tilgængelige arbejdsområder](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Få vist ordrer, der er tildelt dig
1. På din mobilenhed skal du vælge arbejdsområdet **Godkendelse af indkøbsordre**.
2. Vælg **Ordrer, der er tildelt til mig** for at få vist alle de indkøbsordrer, hvor du er blevet bedt om at udføre en handling i arbejdsgangen til godkendelse af indkøbsordren.
3. Vælg en ordre. På siden **Ordredetaljer** kan du se ordrehovedets oplysninger og linjer. Du kan også finde retningslinjer fra til opgaven i arbejdsgangen.
4. Vælg **Regnskabsfordelinger** for at åbne siden **Overskrift regnskabsfordeling**.
5. Gå tilbage til siden **Ordredetaljer**, og vælg en linje. Du kan også udforske linjespecifikke regnskabsfordelinger fra ordrelinjeoplysningerne.

## <a name="complete-an-action-on-the-purchase-order"></a>Udføre en handling i indkøbsordren
Når du har set den indkøbsordre, der er tildelt til dig, og har læst instruktionerne for arbejdsgangen, er du klar til at udføre en handling.

1. På din mobilenhed skal du vælge arbejdsområdet **Godkendelse af indkøbsordre**.
2. Vælg **Ordrer, der er tildelt til mig** for at få vist alle de indkøbsordrer, hvor du er blevet bedt om at udføre en handling i arbejdsgangen til godkendelse af indkøbsordren.
3. Vælg en ordre, og se på detaljesiden.
4. Vælg **Handlinger** for at få vist de tilgængelige handlinger. Hvilke handlinger der er tilgængelige afhænger af den opgave, der er tildelt til dig.

    | Opgavehandling    | Godkendelseshandling  |
    |----------------|------------------|
    | Komplet       | Godkend          |
    | Returner         | Afvis           |
    | Anmod om ændring | Anmod om ændring   |
    | Stedfortræder       | Stedfortræder         |

5. Vælg den relevante handling.
6. På siden **Fuldfør opgave** skal du angive en kommentar. Bemærk, at hvis du vælger handlingen **Deleger**, skal du vælge en bruger, du vil delegere opgaven til.
7. Vælg **Udført**. Når du har opdateret arbejdsområdet, er indkøbsordren ikke længere på listen. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]