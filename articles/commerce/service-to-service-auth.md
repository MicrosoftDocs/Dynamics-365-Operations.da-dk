---
title: Konfigurere service-til-service-godkendelse
description: Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurerer service-til-service-godkendelse i Microsoft Dynamics 365 Commerce for sikkert at kunne kalde tjeneste-API'er til vurderinger og anmeldelser.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: acb3a6220d146d32bbeb5bd8169033bc897ec3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871601"
---
# <a name="configure-service-to-service-authentication"></a>Konfigurere service-til-service-godkendelse

[!include [banner](includes/banner.md)]

Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurerer service-til-service-godkendelse (S2S) i Microsoft Dynamics 365 Commerce for sikkert at kunne kalde tjeneste-API'er til vurderinger og anmeldelser.

Dynamics 365 Commerce tilbyder [vurderinger og anmeldelser](ratings-reviews-overview.md) som en omni-kanalløsning. Denne løsning giver adgang til tjeneste-API'er uden for Commerce, så der kan udføres forskellige opgaver. Disse opgaver omfatter import af vurderinger og anmeldelser fra det eksterne system til Commerce og eksport af vurderinger og anmeldelser fra Commerce. Hvis Commerce skal kunne kalde vurderingers og anmeldelsers tjeneste-API'er sikkert, skal du først konfigurere S2S-godkendelse ved at gennemføre procedurerne i denne artikel.

## <a name="add-a-new-app-registration"></a>Tilføje en ny registrering af app

Før du tilføjer en ny appregistrering, skal du oprette en app ved hjælp af [Azure-portalen](https://portal.azure.com). Hvis du vil registrere en app i Azure Active Directory (Azure AD) og aktivere godkendelse, skal du følge trinnene i [Bruge Azure Active Directory med en brugerdefineret connector i Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Indhent følgende id'er fra Azure-portalen. Du skal bruge disse id'er i de trin, der følger.

- Klientprogram-id
- Klientmappe-id (lejer)

Udfør følgende trin for at tilføje en ny appregistrering i Commerce-webstedsgenerator.

1. Gå til **Startside \> Anmeldelser \> Indstillinger**.
1. Under **Service-til-service--godkendelse (S2S)** skal du vælge **Administrer**.

    ![Administrer-knap i afsnittet Service-til-service-godkendelse (S2S) i Commerce-webstedsgenerator.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. I ruden **S2S-app-poster**, der vises til højre, skal du vælge **Tilføj en ny S2S-appregistrering**.
1. I dialogboksen **Tilføj S2S-app-post** skal du angive følgende påkrævede oplysninger. Brug værdierne fra din Azure-programregistrering.

    - **Navn** – Angiv navnet på din app (for kesmpel **Fabrikam-app**).
    - **Klient-app-id** – Angiv app-id (for eksempel **00000000-0000-0000-0000-000000000000**).
    - **Mappe-id (lejer)** – Angiv mappe-id'et (f.eks. **00000000-0000-0000-0000-000000000000**).

    ![Dialogboksen Tilføj S2S-app-post i Commerce-webstedsgenerator.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Vælg **Send**. Navnet på din app skulle nu vises på listen i ruden **S2S-app-poster**.
1. Luk ruden **S2S-app-poster**.
1. Vælg **Gem**.

## <a name="edit-an-existing-app-registration"></a>Redigere en eksisterende appregistrering

Udfør følgende trin for at redigere en appregistrering i Commerce-webstedsgenerator.

1. Gå til **Startside \> Anmeldelser \> Indstillinger**.
1. Under **Service-til-service--godkendelse (S2S)** skal du vælge **Administrer**.
1. Vælg blyantssymbolet ud for den post, du vil redigere, i ruden **S2S-app-poster**.
1. Opdater værdierne i felterne **Navn**, **Klient-app-id** og **Mappe-id (lejer)** efter behov.
1. Vælg **Send**.
1. Luk ruden **S2S-app-poster**.
1. Vælg **Gem**.

## <a name="remove-an-existing-app-registration"></a>Fjerne en eksisterende appregistrering

Udfør følgende trin for at fjerne en appregistrering i Commerce-webstedsgenerator.

1. Gå til **Startside \> Anmeldelser \> Indstillinger**.
1. Under **Service-til-service--godkendelse (S2S)** skal du vælge **Administrer**.
1. Vælg papirkurvens symbol ud for den post, du vil fjerne, i ruden **S2S-app-poster**. Posten fjernes fra listen.
1. Luk ruden **S2S-app-poster**.
1. Vælg **Gem**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Tilvælge brug af vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger](sync-product-ratings.md)

[Aktiver manuel udgivelse af vurderinger og gennemsyn af en redaktør](manual-publish-rating-reviews.md)

[Importere og eksportere bedømmelser og anmeldelser](import-export-reviews.md)

[Ofte stillede spørgsmål til Vurderinger og anmeldelser](ratings-reviews-faq.md) 
