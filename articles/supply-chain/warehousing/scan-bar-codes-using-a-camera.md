---
title: Scanne stregkoder med et kamera i lagerstedsappen
description: I dette emne beskrives, hvordan du konfigurerer lagerstedsappen til at scanne stregkoder ved hjælp af kameraet på en mobilenhed.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530000"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Scanne stregkoder med et kamera i lagerstedsappen

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer lagerstedsappen til at scanne stregkoder ved hjælp af kameraet på en mobilenhed. 

## <a name="prerequisites"></a>Forudsætninger
For at bruge denne funktion skal du have version 1.2.0.0 af lagerstedsappen installeret, og enheden skal have et kamera. Når du åbner appen efter opdateringen, bliver du spurgt, om du vil tillade, at appen bruger kameraet. Hvis enheden ikke har et kamera, vises der ikke et prompt, og du kan ikke bruge et kamera som scanner. 

## <a name="setup"></a>Konfiguration
I skærmindstillingerne i lagerstedsprogrammet kan du vælge, om kameraet skal bruges til scanning af stregkoder. Hvis du aktiverer **Brug kameraet som scanner**, kan du bruge kameraet til alle inputfelter, hvor den foretrukne inputtilstand er indstillet til **Scannes**. 

Hvis du vil styre, om et inputfelt skal kunne scannes, skal du på siden **Feltnavne for lagerstedsapp** indstille **Foretrukket inputtilstand** til **Scanning**. Når denne indstilling er markeret, kan et kamera bruges til scanning i lagerstedsappen. Du kan finde oplysninger om, hvordan du konfigurerer appfeltnavne i Lagersted, under [Konfigurere appfeltnavne i lagerstedsappen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Understøttede stregkodeformater
De mest almindelige stregkodeformater understøttes, herunder kode 128, kode 39, kode 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder. 

## <a name="navigation"></a>Navigation
Kamerasiden bliver initieret på hver side, hvor inputfeltets foretrukne inputtilstand er indstillet til Scannes. Når du er på kamerasiden, skal du bruge følgende indstillinger til at navigere:
- Klik på Tilbage-knappen for at gå tilbage til siden med opgaver og detaljer. 
- Klik på blyanten på siden med opgaver og detaljer for at gå til den side, hvor du kan skrive input manuelt.
- Klik på kameraet på siden med opgaver og detaljer for at gå tilbage til kamerasiden. 

| Side med opgaver og detaljer | Kameraside | 
| :---------------------: | :--------------------: |
| ![Detaljeside med opgaveeksempel på kamerascanning](./media/camera-scanning-example-task-detail-page50.png)          | ![Mindre kameraside med eksempel på kamerascanning](./media/camera-scanning-example-camera-page50.png)          |

Når du klikker på knappen Kamera på kamerasiden, vises den nedtonet under forsøg på at identificere en stregkode. Hvis der ikke findes en stregkode i løbet af 5 sekunder, afbrydes processen, og kameraknappen bliver tilgængelig igen. Du kan derefter prøve at scanne en stregkode igen.

Når du holder kameraet over en stregkode, får du det bedste resultat, hvis stregkoden er justeret med parenteserne. Når en stregkode er blevet scannet, bliver resultatet behandlet, og du føres til næste trin. Hvis det næste trin indeholder endnu et inputfelt, hvor den foretrukne inputtilstand er indstillet til Scannes, starter kamerasiden igen. Hvis det næste trin ikke er et scanningsfelt, initieres kamerasiden ikke.

