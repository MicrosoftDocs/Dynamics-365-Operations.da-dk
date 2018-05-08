---
title: "Scanne stregkoder ved hjælp af et kamera i Dynamics 365 for Finance and Operations – Lagersted"
description: "I dette emne beskrives, hvordan du konfigurerer Dynamics 365 for Finance and Operations – Lagersted til at scanne stregkoder ved hjælp af kameraet på en mobilenhed."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: da-dk
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Scanne stregkoder ved hjælp af et kamera i Dynamics 365 for Finance and Operations – Lagersted

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer Dynamics 365 for Finance and Operations – Lagersted til at scanne stregkoder ved hjælp af kameraet på en mobilenhed. 

## <a name="prerequisites"></a>Forudsætninger
For at bruge denne funktion skal du have version 1.2.0.0 af Lagersted installeret, og enheden skal have et kamera. Når du åbner appen efter opdateringen, bliver du spurgt, om du vil tillade, at Dynamics 365 for Finance and Operations – Lagersted-programmet bruger kameraet. Hvis enheden ikke har et kamera, vises der ikke et prompt, og du kan ikke bruge et kamera som scanner. 

## <a name="setup"></a>Konfiguration
I skærmindstillingerne i lagerstedsprogrammet kan du vælge, om kameraet skal bruges til scanning af stregkoder. Hvis du aktiverer **Brug kameraet som scanner**, kan du bruge kameraet til alle inputfelter, hvor den foretrukne inputtilstand er indstillet til **Scannes**. 

Hvis du vil styre, om et inputfelt skal kunne scannes, skal du på siden **Feltnavne for lagerstedsapp** i Dynamics 365 for Finance and Operations indstille **Foretrukket inputtilstand** til **Scannes**. Når denne indstilling er markeret, kan et kamera bruges til scanning i lagerstedsappen. Du kan finde oplysninger om, hvordan du konfigurerer appfeltnavne i Lagersted, under [Konfigurere appfeltnavne i lagerstedsappen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Understøttede stregkodeformater
De mest almindelige stregkodeformater understøttes, herunder kode 128, kode 39, kode 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder. 

## <a name="navigation"></a>Navigation
Kamerasiden bliver initieret på hver side, hvor inputfeltets foretrukne inputtilstand er indstillet til Scannes. Når du er på kamerasiden, skal du bruge følgende indstillinger til at navigere:
- Klik på Tilbage-knappen for at gå tilbage til siden med opgaver og detaljer. 
- Klik på blyanten på siden med opgaver og detaljer for at gå til den side, hvor du kan skrive input manuelt.
- Klik på kameraet på siden med opgaver og detaljer for at gå tilbage til kamerasiden. 

| Side med opgaver og detaljer | Kameraside | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

Når du klikker på knappen Kamera på kamerasiden, vises den nedtonet under forsøg på at identificere en stregkode. Hvis der ikke findes en stregkode i løbet af 5 sekunder, afbrydes processen, og kameraknappen bliver tilgængelig igen. Du kan derefter prøve at scanne en stregkode igen.

Når du holder kameraet over en stregkode, får du det bedste resultat, hvis stregkoden er justeret med parenteserne. Når en stregkode er blevet scannet, bliver resultatet behandlet, og du føres til næste trin. Hvis det næste trin indeholder endnu et inputfelt, hvor den foretrukne inputtilstand er indstillet til Scannes, starter kamerasiden igen. Hvis det næste trin ikke er et scanningsfelt, initieres kamerasiden ikke.


