---
title: Sikkerhedsgruppen kan ikke konfigureres for Commerce-webstedsgenerator under den første installation
description: Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når Microsoft Azure Active Directory (Azure AD)-sikkerhedsgruppen for Commerce-webstedsgenerator ikke vises som en mulighed, når du opretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under den indledende implementering af en ny e-handelslejer.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 7098c853c262fd7e0d48231634b232eef71c2b8d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291994"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Sikkerhedsgruppen kan ikke konfigureres for Commerce-webstedsgenerator under den første installation

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder en vejledning til fejlfinding, der kan hjælpe, når Microsoft Azure Active Directory (Azure AD)-sikkerhedsgruppen for Commerce-webstedsgenerator ikke vises som en mulighed, når du opretter e-handelskomponenter i Microsoft Dynamics Lifecycle Services (LCS) under den indledende implementering af en ny e-handelslejer.

## <a name="description"></a>Betegnelse

Når du opretter e-handelskomponenterne som en del af implementeringsprocessen af en ny e-commerce-lejer, der omfatter komponenten Commerce-webstedsgenerator, vises Azure AD-sikkerhedsgruppen ikke som en indstilling i dialogboksen.

## <a name="resolution"></a>Løsning

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>Klargør e-handelswebstedet med en bruger i den korrekte lejer

1. Gå til [Azure-portalen](https://portal.azure.com/).
1. Under den lejer, som LCS-projektet til dit e-handelswebsted er klargjort til, skal du følge instruktionerne i [Opret en basisgruppe og tilføj medlemmer ved hjælp Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Gå til [LCS](https://lcs.dynamics.com/), og log på med en konto, der deler samme lejer som den Azure AD-sikkerhedsgruppe, du lige har oprettet. Kontoen skal have adgang til for at få vist Azure AD-sikkerhedsgruppen.
1. Gennemfør opsætningstrinnene for at konfigurere e-handelswebstedet. Når du klargør e-handelskomponenterne, skal sikkerhedsgruppen nu vises som en mulighed i dialogboksen.

> [!NOTE]
> Hvis du vil sikre dig, at feltet i dialogboksen er udfyldt med listen over sikkerhedsgrupper, skal du vælge **Enter**, når du har indtastet navnet på den Azure AD-sikkerhedsgruppe, du har oprettet. Søgeresultaterne viser alle Azure AD-sikkerhedsgrupper, der starter med søgeteksten, og som brugeren har adgang til. Du kan bruge en kortere søgeudsigt for at give mere generelle søgeresultater.

## <a name="additional-resources"></a>Yderligere ressourcer

[Oprette en basisgruppe og tilføje medlemmer ved hjælp af Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Implementere en ny e-handelslejer](../deploy-ecommerce-site.md)
