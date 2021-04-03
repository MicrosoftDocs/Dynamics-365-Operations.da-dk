---
title: Foretage fejlfinding i procesproduktion
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med procesproduktion.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71ff5eeb2065a67281393777937d50237ab78d5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259716"
---
# <a name="troubleshoot-process-manufacturing"></a>Foretage fejlfinding i procesproduktion

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med procesproduktion.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Når jeg bruger jobkortenheden til at rapportere en delmængde på det sidste job i en produktionsordre, vil alle tidligere job på den ordre, der har status som igangværende, automatisk blive afsluttet.

Denne funktionsmåde er tilsigtet. På siden **Produktionsordrestandarder** under fanen **Færdigmelding** er der en indstilling med navnet **Slutmarker rute**. Hvis dette emne er angivet til *Ja*, bogføres en rutekortkladde, når en arbejder bruger jobkortenheden eller jobkortterminalen til at rapportere den sidste operation. I denne kladde markeres alle operationer som fuldført, og alle produktionsjob afsluttes. Når indstillingen **Slutmarker rute** er angivet til *Ja*, betragter systemet ikke den jobstatus, som arbejderen valgte, da denne rapporterede den sidste operation. Systemet overvejer heller ikke, om arbejderen rapporterer en fuld eller delvis mængde.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Når jeg forsøger på lagerlukning, får jeg vist følgende advarselsmeddelelse: "Der er ikke registreret nogen udførelse af beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning".

Hvis du i versioner før 10.0.13 ikke bruger omkostningsforløbet for lean produktionsflow, får du vist følgende fejlmeddelelse under lagerlukningen:

> Du er ved at udføre en lagerlukning med datoen %1. Der er ikke registreret nogen udførelse af beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning. Husk at udføre beregning af efterkalkuleret varetræk med datoen %1 der matcher periodeafslutning. Værdiansættelsen af lagerbeholdning, vareforbrug og afvigelser er måske ikke korrekte i Reskontro eller Finans, før dette er udført.

Dette problem er løst i version 10.0.13 og senere. Du kan finde flere oplysninger i [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]