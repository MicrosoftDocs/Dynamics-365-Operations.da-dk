---
title: Avancerede indstillinger for løsningen Invoice Capture
description: Denne artikel indeholder oplysninger om avancerede indstillinger i løsningen Invoice Capture.
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
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691156"
---
# <a name="invoice-capture-solution-advanced-settings"></a>Avancerede indstillinger for løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikel indeholder oplysninger om avancerede indstillinger i løsningen Invoice Capture.

## <a name="create-additional-connections-for-channels"></a>Oprette ekstra forbindelser til kanaler

Du skal oprette forbindelser til mail eller fillager for at aktivere overvågning af indgående fakturaer fra forskellige kanaler. Du skal registrere forbindelser i starten for at give adgang til automatiske flows, der bruges i løsningen.

Følgende forbindelsestyper bruges til at importere fakturaer:

- Office 365 Outlook
- Outlook.com
- OneDrive
- SharePoint

Kanalen til fakturaimport bruger forbindelserne i yderligere konfigurationstrin. Før brugere kan oprette en kanal med en bestemt forbindelse, skal de tildeles sikkerhedsrollen **Administrator**, og de skal oprette forbindelser.

Følg disse trin for at oprette en forbindelse til Microsoft Dataverse.

1. Gå til **Administrationssystem \> Standardløsning**.
2. Vælg **Ny**, og vælg derefter **Forbindelsesreference**.
3. Angiv et navn i feltet **Vist navn**.
4. Vælg **Microsoft Dataverse** som connector.
5. Hvis du konfigurerer forbindelsen første gang, skal du vælge **Ny forbindelse**.
6. I dialogboksen skal du oprette en Dataverse-forbindelse og derefter vælge **Opret**.
7. Angiv Dataverse-kontoen og -adgangskoden.
8. Når valideringen er bestået, skal du gå til forbindelsessiden, vælge **Opdater**, vælge kontoen og derefter vælge **Opret**.

Benyt følgende fremgangsmåde for at oprette en mail- eller fillagerforbindelse.

1. Vælg **Office 365 Outlook** i feltet **Forbindelsestype** på siden **Oprettelse af forbindelse**.
2. Til mailforbindelsen kan du vælge **Outlook.com** eller **Office 365 Outlook** som connector. Som fillagerforbindelse kan du vælge enten **OneDrive** eller **SharePoint**.

Du kan gennemgå eksisterende forbindelser ved at gå til **Standardløsning \> Objekter \> Forbindelsesreferencer**. Den bruger, der opretter kanaler, skal have mindst én Dataverse-forbindelse foruden bestemte mail- eller fillagringsforbindelser. Den, der har oprettet den nye kanal, skal være ejeren af forbindelsen.
