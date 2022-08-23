---
title: Importere og eksportere bedømmelser og anmeldelser
description: Denne artikel beskriver, hvordan vurderinger og anmeldelser af produkter importeres og eksporteres i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f369e3cd208cdfba816f817ead75374ee6982912
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271929"
---
# <a name="import-and-export-ratings-and-reviews"></a>Importere og eksportere bedømmelser og anmeldelser

[!include [banner](includes/banner.md)]

Denne artikel beskriver, hvordan vurderinger og anmeldelser af produkter importeres og eksporteres i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce tilbyder [vurderinger og anmeldelser](ratings-reviews-overview.md) som en omni-kanalløsning. Når du skifter til Dynamics 365 Commerce-løsningen med vurderinger og anmeldelser, kan du flytte dine eksisterende vurderinger og anmeldelser til Commerce-platformen. Du kan også eksportere vurderinger og anmeldelser fra Commerce baseret på dine forretningsbehov. En Power Automate-connector giver dig mulighed for at importere vurderinger og anmeldelser til Commerce og eksportere dem fra Commerce.

> [!NOTE]
> Du kan finde flere oplysninger om, hvordan du kommer i gang med logikflow i Power Automate, i [Oprette et cloudflow i Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Forudsætninger

Før du kan importere og eksportere vurderinger og anmeldelser, skal du opfylde følgende forudsætninger:

- Vurderingers og anmeldelsers løsning skal være aktiveret for dit e-handelswebsted på Commerce-platformen. Du kan finde flere oplysninger i [Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md).
- Power App-connectoren Dynamics 365 Ratings and Reviews skal være konfigureret til at aktivere handlinger for enten "send vurderinger" eller "eksporter anmeldelser" i Power Automate. Du kan finde flere oplysninger i [Dynamics 365 Commerce - vurderinger og anmeldelser (forhåndsversion)](/connectors/dynamics365ratingsre/).
- S2S-godkendelse (service-til-service) skal være konfigureret, så vurderingers og anmeldelsers API (Application Programming Interface) kan kaldes sikkert uden for Commerce. Du kan finde flere oplysninger under [Konfigurere service-til-service-godkendelse](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Importere vurderinger og anmeldelser

Hvis du vil importere vurderinger og anmeldelser fra dit eksisterende system til Commerce, skal du føje Power Automate-connectoren Dynamics 365 Ratings and Review til enten et eksisterende Power Automate-flow eller et nyt. Du kan finde flere oplysninger i [Dynamics 365 Commerce - vurderinger og anmeldelser (forhåndsversion)](/connectors/dynamics365ratingsre/).

> [!IMPORTANT]
> Før du kan udføre denne procedure, skal du [konfigurere S2S-godkendelse](service-to-service-auth.md).

Hvis du vil importere vurderinger og anmeldelser til Commerce ved hjælp af Power Automate-connectoren Dynamics 365 Ratings and Reviews, skal du følge disse trin.

1. Vælg handlingen **Send brugeranmeldelse**.
1. Opret en forbindelse ved at bruge de Azure Active Directory-appoplysninger (Azure AD), der blev oprettet, da du konfigurerede S2S-godkendelse. Du kan finde flere oplysninger under [Konfigurere service-til-service-godkendelse](service-to-service-auth.md).
1. Handlingen **Send brugeranmeldelse** tager én anmeldelse ad gangen. Gentag derfor handlingen. Brug kildeanmeldelserne som en liste til at sende masseanmeldelser.
    
## <a name="export-ratings-and-reviews"></a>Eksportere vurderinger og anmeldelser

Hvis du vil eksportere vurderinger og anmeldelser fra Commerce, skal du føje Power Automate-connectoren Dynamics 365 Ratings and Review til enten et eksisterende Power Automate-flow eller et nyt. Du kan finde flere oplysninger i [Dynamics 365 Commerce - vurderinger og anmeldelser (forhåndsversion)](/connectors/dynamics365ratingsre/).

Hvis du vil eksportere vurderinger og anmeldelser fra Commerce ved hjælp af Power Automate-connectoren Dynamics 365 Ratings and Reviews, skal du følge disse trin.

1. Vælg handlingen **Eksportér alle anmeldelser**.
1. Fuldfør handlingen. 

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger](sync-product-ratings.md)

[Aktiver manuel udgivelse af vurderinger og gennemsyn af en redaktør](manual-publish-rating-reviews.md)

[Konfigurere service-til-service-godkendelse](service-to-service-auth.md)

[Ofte stillede spørgsmål til Vurderinger og anmeldelser](ratings-reviews-faq.md)
