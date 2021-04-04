---
title: Oprette et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1
description: Dette emne beskriver oprettelse af et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1 (VM).
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585240"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Oprette et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1

[!include [banner](../../includes/banner.md)]

Dette emne beskriver oprettelse af et udviklingsmiljø til e-handel for at fejlfinde en Retail Server virtuel maskine på niveau 1 (VM).

## <a name="description"></a>Betegnelse

Microsoft Dynamics 365 Commerce Lag 1-miljøer implementeres typisk til udvikling af commerce runtime (CRT) og POS-udvidelse. De er enkeltstående miljøer. På grund af arkitekturens art (a service as a service, inkluderer de ikke komponenter til e-handel).

I visse scenarier kan det være en god ide at teste kald til udvidelser i et Lag 1-miljø, så du kan fejlfinde udvidelser fra e-handelskomponenter. De generelle instruktioner findes i [Foretage fejlfinding i forhold til et niveau 1 Commerce-udviklingsmiljø](../e-commerce-extensibility/debug-tier-1.md).

Når du bruger fejlfinding i et Niveau 1-miljø, kan krydsserverkald på tværs af servere forårsage forskellige fejl, der er relateret til sikkerhedspolitiken for indhold, da webstedet nu kalder en anden Retail Server.

I følgende illustration vises et eksempel på en fejl, der kan forekomme, når der er valgt en variant på en side med produktdetaljer.

![Fejl, når der er valgt en variant på en side med produktdetaljer](media/unhandled-rejection-error.jpg)

I følgende illustration vises et eksempel på en lignende fejl i en browsers fejlfindingsværktøjer (F12 Developer Tools). Fejlmeddelelsen nævner overtrædelse af sikkerhedspolitikdirektiverne for indhold.

![Fejl i fejlfindingsværktøjer](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Løsning

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Deaktivere politikken for indholdssikkerhed for webstedet i Commerce Site Builder

1. Vælg det sted, du arbejder på.
1. Vælg **Indstillinger**, og vælg derefter **Udvidelse**.
1. Vælg **Deaktiver indholdssikkerhedspolitik** under fanen **Indholdssikkerhedspolitik**.
1. Vælg **Gem og udgiv**.

> [!NOTE]
> Det er ikke muligt at logge på business-to-consumer (B2C) i et lokalt udviklingsmiljø. Du kan dog bruge gæsteudbetaling eller build-side-id'er til at simulere en brugers logon efter behov.

## <a name="additional-resources"></a>Yderligere ressourcer

[Introduktion til e-handelonlineudvidelsesudvikling](../e-commerce-extensibility/sdk-getting-started.md)

[Administrere sikkerhedspolitik for indhold (CSP) på e-handelswebsted](../manage-csp.md)
