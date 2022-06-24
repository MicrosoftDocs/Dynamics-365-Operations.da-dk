---
title: Konfigurere arbejdsområdet til aktivstyring på mobilenhed
description: Denne artikel beskriver, hvordan Microsoft Dynamics 365 Supply Chain Management og Finance and Operations (Dynamics 365)-mobilappen konfigureres til at køre et mobilarbejdsområde til aktivstyring, som arbejderne kan bruge til at udføre opgaver i forbindelse med aktivstyring.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ee92ed2c0e2a59adaebe20ed3d426ac03c056dac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870836"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Konfigurere arbejdsområdet til aktivstyring på mobilenhed

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan Microsoft Dynamics 365 Supply Chain Management og Finance and Operations (Dynamics 365)-mobilappen konfigureres til at køre et mobilarbejdsområde til **aktivstyring**, som arbejderne kan bruge til at udføre opgaver i forbindelse med aktivstyring.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Konfigurere vedligeholdelsesarbejderbrugere i Supply Chain Management

For hver bruger, der skal have adgang til det mobile arbejdsområde til **aktivstyring**, skal du følge disse trin.

1. I Supply Chain Management skal du gå til **Personale \> Arbejdere** og sørge for, at der findes en arbejderpost for den bruger, du vil konfigurere. Opret en ny arbejderpost efter behov.
1. Gå til **Aktivstyring \> Konfiguration \> Arbejdere \> Arbejdere**, og kontrollér, at den arbejderpost, du har identificeret (eller oprettet) i det forrige trin, er knyttet til en vedligeholdelsesarbejderpost. Opret en ny vedligeholdelsesarbejderpost efter behov, og angiv feltet **Arbejder** til arbejderposten fra det forrige trin.
1. Gå til **Aktivstyring \> Konfiguration \> Arbejdere \> Vedligeholdelsesarbejdergrupper**, og kontrollér, at den vedligeholdelsesarbejder, du har identificeret (eller oprettet) i det forrige trin, er knyttet til en vedligeholdelsesarbejdergruppe.
1. Gå til **Systemadministration \> Brugere**.
1. Vælg den relevante bruger i gitteret.
1. På oversigtspanelet **Brugeroplysninger** skal du angive feltet **Person** til den arbejderkonto, du vil knytte til den aktuelle brugerkonto. Denne arbejderkonto skal være den arbejderpost, du har identificeret (eller oprettet) i trin 1 og knyttet til en vedligeholdelsesarbejderpost i trin 2.

> [!NOTE]
> Brugerrettigheder og sikkerhedsroller gælder for funktionerne i mobilarbejdsområdet til **aktivstyring** på samme måde, som de gælder for funktionerne i brugergrænsefladen til Supply Chain Management. Derfor skal alle brugere, du konfigurerer adgangen til mobilarbejdsområdet til **aktivstyring** for, have de sikkerhedsroller, der er nødvendige for at udføre lignende handlinger direkte i Supply Chain Management.

## <a name="publish-the-asset-management-mobile-workspace"></a>Publicere mobilarbejdsområdet til aktivstyring

Du kan gøre funktioner for aktivstyring tilgængelige i Finans- og drifts-mobilappen (Dynamics 365) ved at publicere mobilarbejdsområdet til **aktivstyring**.

1. I Supply Chain Management skal du vælge knappen **Indstillinger** (tandhjulsymbolet øverst til højre) og derefter vælge **Mobilapp** i menuen.
1. I dialogboksen **Administrer mobilapp** skal du finde feltet **Aktivstyring**. Hvis det indeholder teksten "I metadata – ikke publiceret", er arbejdsområdet endnu ikke publiceret. Hvis det indeholder teksten "I metadata – publiceret", er arbejdsområdet allerede blevet publiceret, og du kan springe resten af denne procedure over.

    ![Dialogboksen Administrer mobilapp.](media/mobile-workspaces.png "Dialogboksen Administrer mobilapp")

1. Vælg feltet **Aktivstyring**, og vælg derefter **Publicer** på værktøjslinjen. Efter nogle få sekunder burde du modtage en besked om, at arbejdsområdet er blevet publiceret korrekt. Teksten i feltet burde desuden ændres til "I metadata – publiceret".

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Installere og konfigurere Finans- og drifts-mobilappen (Dynamics 365)

1. Gå til en af følgende appbutikker for at installere **Microsoft Finans og drift (Dynamics 365)**-appen på din mobilenhed:

    - [For Google Android-enheder](https://go.microsoft.com/fwlink/?linkid=850662)
    - [For Apple iOS-enheder](https://go.microsoft.com/fwlink/?linkid=850663)

1. Åbn appen Finans og drift (Dynamics 365). Logonsiden vises. I feltet **Log på** skal du angive URL-adressen til Supply Chain Management eller vælge en ny URL-adresse på listen **Seneste miljøer** og derefter trykke på **Opret forbindelse**.

    ![Logonside.](media/mobile-app-sign-in.png "Logonside")

1. Hvis du bliver bedt om at bekræfte forbindelsen, skal du markere afkrydsningsfeltet **Jeg forstår** og derefter trykke på **Opret forbindelse**.
1. På siden **Vælg en konto** skal du bruge din Microsoft-konto til at logge på mobilappen.

    Siden **Arbejdsområder** vises. Den viser alle mobilarbejdsområder, der er publiceret af din Supply Chain Management-forekomst.

    ![Liste over arbejdsområder.](media/mobile-app-workspaces.png "Liste over arbejdsområder")

1. Hvis du skal ændre den juridiske enhed (firma), skal du trykke på menuknappen (nogle gange kaldet hamburger eller hamburgerknappen) i øverste venstre hjørne og derefter trykke på **Skift firma**.

    ![Skifte den juridiske enhed.](media/mobile-app-change-comp.png "Skifte den juridiske enhed")

1. På siden **Arbejdsområder** skal du vælge det arbejdsområde, du vil arbejde med, for at åbne det.

    ![Arbejdsområde til aktivstyring på mobilenhed.](media/mobile-app-asset-workspace.png "Arbejdsområde til aktivstyring på mobilenhed")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Arbejde med mobilarbejdsområdet til aktivstyring

Du kan finde flere oplysninger om, hvordan du arbejder med mobilarbejdsområdet til **aktivstyring**, under [Bruge mobilarbejdsområdet til aktivstyring](asset-management-mobile-workspace.md).

Yderligere oplysninger om Finans- og drifts-mobilappen (Dynamics 365) finder du på [Mobilapp-startsiden](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]