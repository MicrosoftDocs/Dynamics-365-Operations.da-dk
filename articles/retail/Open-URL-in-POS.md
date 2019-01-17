---
title: "Åbne URL-adresse i POS"
description: "Dette emne indeholder en oversigt over de forbedringer, der er foretaget i produkt- og kundesøgefunktionen i Microsoft Dynamics 365 for Retail."
author: AamirAllaq
manager: AnnBe
ms.date: 11/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: d2b692ac86244eca31780a558112167391fc6d77
ms.contentlocale: da-dk
ms.lasthandoff: 01/04/2019

---

# <a name="open-url-in-pos"></a>Åbne URL-adresse i POS

[!include [banner](includes/banner.md)]

I dette emne beskrives, hvordan du kan konfigurere en knap i Retail POS til at åbne en URL-adresse. Denne funktion kræver ikke tilpasning af kode og kan konfigureres af en person, der ikke har rollen som udvikler.

Denne funktion gør det muligt ved hjælp af knapmatrixdesigneren at konfigurere en knap i POS til at åbne en URL-adresse. Dette understøttes i øjeblikket i følgende konfigurationer:

- Åbne i et nyt vindue
- Åbne i POS
- Åbne en oprindelig app

## <a name="open-in-new-window"></a>Åbn i et nyt vindue

Denne konfiguration definerer, om URL-adressen skal åbnes i et nyt vindue eller i appen. Når konfigurationen er indstillet til at åbne en URL-adresse i appen, er sidenavigationspanelet og øverste søjle i POS synlige og tilgængelige for brugerne. Når konfigurationen er indstillet til at åbne i et nyt vindue, åbnes URL-adressen i et nyt appvindue i Modern POS til Windows og i en ny fane i browseren i alle andre POS-klienter. Du kan aktivere denne ved at konfigurere URL-adressen med indstillingen **Åbn i nyt vindue** valgt.

## <a name="open-within-pos"></a>Åbne i POS

Åbning af en URL-adresse i POS understøttes i øjeblikket kun for Modern POS i Windows. På andre klienter er denne funktion under udvikling og planlagt til frigivelse i fremtidige opdateringer. Du kan aktivere denne ved at konfigurere URL-adressen uden at vælge indstillingen **Åbn i nyt vindue**.

## <a name="open-a-native-app"></a>Åbne en oprindelig app

Med denne funktion kan du også indstille ikke-web-URL-adresser til at åbne en oprindelig app. Du kan for eksempel angive URL-protokoller som MailTo, SIP, IM eller MSTEAMS, som derefter kan håndteres af de respektive oprindelige apps på værtsenheden. Du kan aktivere denne ved at konfigurere URL-adressen med indstillingen **Åbn i nyt vindue** valgt.

- For Windows-computere kan du i [Eksportere eller importere standardprogramtilknytninger](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) finde oplysninger om, hvordan du indstiller standardprotokoltilknytninger, hvis du konfigurerer computeren ved hjælp af DISM (Deployment Image Servicing and Management).
- Hvis du bruger MDM, f.eks. Intune, til at administrere Windows-computere, skal du se [Politik CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).
- Hvis du er udvikler og bygger et brugerdefineret websted, skal du se [Start standardappen for en URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Åbne en oprindelig app problemfrit

I Windows, iOS og Android er det også muligt at åbne apps mere problemfrit ved hjælp af app-protokoltilknytning. Hvis din app ikke allerede er konfigureret til at håndtere åbning fra en webbrowser, skal du muligvis bede en udvikler om at konfigurere dette.

- For Windows, se [Aktivere apps til websteder ved hjælp af app-URI-handlere](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).
- For IOS, se [Universal Links til udviklere](https://developer.apple.com/ios/universal-links/).
- For Android, se [Håndtering af Android App Links](https://developer.android.com/training/app-links/).

| Klient                | Åbn i et nyt vindue | Åbne en oprindelig app | Åbne i POS | Oplysninger                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Modern POS i Windows | ✓\*                | ✓               | ✓              | \* Åbner i et nyt Modern POS-vindue |
| Cloud POS             | ✓\*                | ✓               | X              | \* Åbner under en ny fane i browseren        |
| Moderne POS i iOS     | ✓\*                | ✓               | X              | \* Åbner under en ny fane i browseren        |
| Modern POS i Android | ✓\*                | ✓               | X              | \* Åbner under en ny fane i browseren        |

## <a name="before-you-begin"></a>Før du begynder

Før du begynder, skal du gennemgå, hvordan du konfigurerer [Skærmlayout til POS](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>Åbne URL-adresse i POS

Hvis du vil konfigurere en URL-adresse, så den kan åbnes i POS, skal du udføre følgende trin.

1. I hovedkontoret skal du gå til **Detail \> Konfiguration af kanal \> POS-opsætning \> POS \> Skærmlayout**.
2. Vælg **Knapmatricer \> Designer**.
3. Opret en ny knap.
4. Vælg **Knap**-egenskaber.
5. Vælg **Åbn URL** som handling.
6. Angiv den URL-adresse, du vil bruge.
7. Angiv, om URL-adressen skal åbnes i et nyt vindue.

