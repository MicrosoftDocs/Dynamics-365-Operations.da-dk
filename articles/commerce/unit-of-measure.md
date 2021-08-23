---
title: Anvende indstillinger for måleenheder
description: Dette emne dækker indstillinger for måleenheder og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fe5cf6b57a8897a0bd541146cb1ad17b496d5633c0a1df9d58b2a4fbc868139
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761508"
---
# <a name="apply-unit-of-measure-settings"></a>Anvende indstillinger for måleenheder

[!include [banner](includes/banner.md)]

Dette emne dækker indstillinger for måleenheder og beskriver, hvordan du anvender dem i Microsoft Dynamics 365 Commerce.

Et produkt kan sælges i forskellige enheder, f.eks. "stk.", "par" og "dusin". I Commerce-hovedkvarteret kan måleenheden for salg defineres for et produkt og vises på en e-handelswebsted. Hvis en detailsælger f.eks. sælger et produkt både enkeltvis og i dusiner, kan de tilgængelige måleenheder vises sammen med andre produktoplysninger.

I eksemplet i følgende illustration er måleenheden for salg **stk.** (hver) konfigureret for et produkt i Commerce-hovedkvarteret.

![Eksempel på et produkt, der er konfigureret med en måleenhed i Commerce Headquarters.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Understøttelse af anvendelse og visning af måleenheden er tilgængelig fra og med Commerce version 10.0.19.

## <a name="unit-of-measure-settings"></a>Indstillinger for måleenheder

Visningsindstillinger for måleenheder er defineret i Commerce Site Builder under **Webstedsindstillinger \> Udvidelser \> Vis måleenhed for produkter**. Der findes tre understøttede indstillinger:

- **Vis ikke** – Når denne indstilling er valgt, viser e-handelswebstedet ikke måleenheden for produktet. Denne funktionsmåde er standard.
- **Vis i købsoplevelsen for produkt** – Når denne indstilling er valgt, vises måleenheden i produktoplysninger, indkøbsvogn, betaling, ordrehistorik og ordredetaljer.
- **Vis i gennemsyn af produkter og købsoplevelse** – Når denne indstilling er valgt, vises måleenheden på siderne med købsoplevelsen for produktet og når produkter gennemses. Som en del af denne funktionsmåde vises måleenheder i søgeresultater og moduler til produktsamling.

> [!IMPORTANT]
> Visningsindstillinger for måleenhed er tilgængelige med frigivelsen af Commerce version 10.0.19. Hvis du opdaterer fra en ældre version af Commerce, skal du opdatere filen appsettings.json manuelt. Du kan finde instruktioner i [Opdateringer af SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Moduler, der bruger indstillinger for måleenhed

Moduler, der bruger indstillingerne for måleenhed, omfatter modulerne for købsfelt, ønskeliste, indkøbsvogn, indkøbsvogn, container med søgeresultater, produktsamling, betaling og ordredetaljer.

I eksemplet i følgende illustration viser en PDP (Product Details Page) måleenheden (**stk.**) for et produkt.

![Eksempel på en PDP, der viser måleenheden.](./media/Productunit-PDP.png)

I eksemplet i følgende illustration viser et produktsamlingsmodeul måleenheden (**stk.**) for et produkt.

![Eksempel på et produktsamlingsmodul, der viser måleenheden.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulbibliotek, oversigt](starter-kit-overview.md)

[Indkøbskurvsmodul](add-cart-module.md)

[Boksmodul til køb](add-buy-box.md)

[Kontostyringssider og -moduler](account-management.md)

[Opdateringer til SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
