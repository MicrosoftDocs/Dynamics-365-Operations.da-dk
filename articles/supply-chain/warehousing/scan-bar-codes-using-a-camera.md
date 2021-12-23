---
title: Scanne stregkoder med et kamera i mobilappen Lokationsstyring
description: I dette emne beskrives, hvordan du konfigurerer mobilappen Lokationsstyring til at scanne stregkoder ved hjælp af kameraet på en mobilenhed.
author: Mirzaab
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: cc58d88865fea17e0e27463b25e2ba815ee1a5b1
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901966"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Scanne stregkoder med et kamera i mobilappen Lokationsstyring

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du konfigurerer mobilappen Lokationsstyring til at scanne stregkoder ved hjælp af kameraet på en mobilenhed.

## <a name="setup"></a>Konfiguration

I skærmindstillingerne i mobilappen Lokationsstyring kan du vælge, om kameraet skal bruges til scanning af stregkoder. Hvis du aktiverer **Brug kameraet som scanner**, kan du bruge kameraet til alle inputfelter, hvor den foretrukne inputtilstand er indstillet til **Scannes**.

Hvis du vil styre, om et inputfelt skal kunne scannes, skal du på siden **Feltnavne for lagerstedsapp** indstille **Foretrukket inputtilstand** til **Scanning**. Når denne indstilling er markeret, kan et kamera bruges til scanning i mobilappen Lokationsstyring. Du kan finde flere oplysninger i [Konfigurere felter til mobilappen Lokationsstyring](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Understøttede stregkodeformater

De mest almindelige stregkodeformater understøttes, herunder kode 128, kode 39, kode 93, EAN-8, EAN-13, UPC-E, UPC-A og QR-koder.

## <a name="navigation"></a>Navigation

Kamerasiden bliver initieret på hver side, hvor inputfeltets **Foretrukne inputtilstand** er indstillet til *Scanning*. Når du er på kamerasiden, skal du bruge følgende indstillinger til at navigere:

- Vælg Tilbage-knappen for at gå tilbage til siden med **Opgaver og detaljer**.
- Vælg blyanten på siden **Opgaver og detaljer** for at gå til den side, hvor du kan skrive input manuelt.
- Væl kameraet på siden **Opgaver og detaljer** for at gå tilbage til kamerasiden.

Når du vælger knappen Kamera på kamerasiden, vises den nedtonet under forsøg på at identificere en stregkode. Hvis der ikke findes en stregkode i løbet af 5 sekunder, får processen timeout, og kameraknappen bliver tilgængelig igen. Du kan derefter prøve at scanne en stregkode igen.

Når du holder kameraet over en stregkode, får du det bedste resultat, hvis stregkoden er justeret med parenteserne. Når en stregkode er blevet scannet, bliver resultatet behandlet, og du føres til næste trin. Hvis det næste trin indeholder endnu et inputfelt, hvor den foretrukne inputtilstand er indstillet til Scannes, starter kamerasiden igen. Hvis det næste trin ikke er et scanningsfelt, initieres kamerasiden ikke.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]