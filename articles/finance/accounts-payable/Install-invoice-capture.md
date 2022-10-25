---
title: Installere løsningen Invoice Capture
description: Denne artikel indeholder oplysninger om, hvordan du installerer løsningen Invoice Capture og integrerer den med Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691173"
---
# <a name="install-the-invoice-capture-solution"></a>Installere løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Hvis du har installeret løsningen i personlig prøveversion, skal du afinstallere den gamle løsning, før du fortsætter.

## <a name="prerequisites"></a>Forudsætninger

Før du kan installere løsningen Invoice Capture, skal du opfylde følgende forudsætninger:

1. Registrer et program, og føj en klienthemmelighed til Microsoft Azure Active Directory (Azure AD) under dit Azure-abonnement. Du kan finde flere oplysninger under [Registrere et webprogram med AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Du skal notere værdierne for **Program-id (klient)**, **Klienthemmelighed** og **Lejer-id**, da du skal bruge dem senere.

2. Registrer Azure-programmet i et Dynamics 365 Finance-miljø. Du kan finde flere oplysninger under [Registrere dit eksterne program](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Installere og konfigurere løsningen

Hvis du vil installere løsningen Invoice Capture, skal du gå til AppSource og vælge linket til forhåndsversionen af [Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). Når installationen er fuldført, kan du se løsningen installeret i det valgte miljø i Power Apps.

Gør følgende for at fuldføre konfigurationen.

1. Download [assistentløsningen](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip) for at konfigurere følgende oplysninger:

    - Kommunikationen mellem Microsoft Power Platform og Finance-miljøet
    - Forbindelsesreferencen til Dataverse og Office 365 Outlook, der bruges af kanalen

2. Gå i Power Apps til dit miljø, og vælg **Importér løsning**.
3. Vælg **Gennemse**, vælg den pakke med assistentløsningen, du har downloadet, og vælg derefter **Næste**.
4. Vælg **Næste**.
5. Tildel en eksisterende forbindelse, eller opret en ny ved at vælge **Ny forbindelse**.
6. Når pakken er importeret, skal du åbne **Dynamics 365 Invoice Capture – installationsværktøjer**.
7. Kør cloudflowet for at oprette forbindelsen mellem løsningen Invoice Capture i Microsoft Power Platform og Finance.
8. Vælg **Kør**, og angiv følgende parametre:

    - **URL-adresse til Dynamics 365 Finance** – URL-adressen til det Finance-miljø, du vil integrere med.
    - **Lejer-id** – Lejer-id for Finance-miljøet.
    - **Klient-id** – Det Azure-program-id, der er registreret.
    - **Klienthemmelighed** – Den klienthemmelighed, der er oprettet for Azure-programmet.
