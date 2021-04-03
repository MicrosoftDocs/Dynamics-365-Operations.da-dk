---
title: Sikkerhedsgruppen kan ikke konfigureres for Commerce-webstedsgenerator under den første installation
description: Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når Microsoft Azure Active Directory (Azure AD)-sikkerhedsgruppen for Commerce-webstedsgenerator ikke vises som en mulighed, når du opretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under den indledende implementering af en ny e-handelslejer.
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
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585252"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Sikkerhedsgruppen kan ikke konfigureres for Commerce-webstedsgenerator under den første installation

[!include [banner](../../includes/banner.md)]

Dette emne indeholder en vejledning til fejlfinding, der kan hjælpe, når Microsoft Azure Active Directory (Azure AD)-sikkerhedsgruppen for Commerce-webstedsgenerator ikke vises som en mulighed, når du opretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under den indledende implementering af en ny e-handelslejer.

## <a name="description"></a>Betegnelse

Når du opretter e-handelskomponenterne som en del af implementeringsprocessen af en ny e-commerce-lejer, der omfatter komponenten Commerce-webstedsgenerator, vises Azure AD-sikkerhedsgruppen ikke som en indstilling i dialogboksen.

## <a name="resolution"></a>Løsning

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Klargør e-handelswebstedet med en bruger i den korrekte lejer

1. Gå til [Azure-portalen](https://portal.azure.com/).
1. Under den lejer, som LCS-projektet til dit e-handelswebsted er klargjort til, skal du følge instruktionerne i [Opret en basisgruppe og tilføj medlemmer ved hjælp Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Gå til [LCS](https://lcs.dynamics.com/), og log på med en konto, der deler samme lejer som den Azure AD-sikkerhedsgruppe, du lige har oprettet. Kontoen skal have adgang til for at få vist Azure AD-sikkerhedsgruppen.
1. Gennemfør opsætningstrinnene for at konfigurere e-handelswebstedet. Når du klargør e-handelskomponenterne, skal sikkerhedsgruppen nu vises som en mulighed i dialogboksen.

> [!NOTE]
> Hvis du vil sikre dig, at feltet i dialogboksen er udfyldt med listen over sikkerhedsgrupper, skal du vælge **Enter**, når du har indtastet navnet på den Azure AD-sikkerhedsgruppe, du har oprettet. Søgeresultaterne viser alle Azure AD-sikkerhedsgrupper, der starter med søgeteksten, og som brugeren har adgang til. Du kan bruge en kortere søgeudsigt for at give mere generelle søgeresultater.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette en basisgruppe og tilføje medlemmer ved hjælp af Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Implementere en ny e-handelslejer](../deploy-ecommerce-site.md)
