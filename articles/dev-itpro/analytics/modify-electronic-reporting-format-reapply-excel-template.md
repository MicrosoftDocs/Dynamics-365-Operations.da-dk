---
title: Rediger et elektronisk rapporteringsformat ved at genanvende en Microsoft Excel-skabelon
description: "Dette emne indeholder oplysninger om, hvordan du kan redigere formatet for elektroniske rapportering (ER), der bruges til at generere forretningsdokumenter ved at anvende en Excel-skabelon, der er ændret."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: fca7fb75b965886c2ebc06b12940434f2ffc2543
ms.contentlocale: da-dk
ms.lasthandoff: 02/27/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a>Rediger et elektronisk rapporteringsformat ved at genanvende en Microsoft Excel-skabelon

[!INCLUDE [banner](../includes/banner.md)]

Værktøjet til elektronisk rapportering (ER) bruges til at oprette forretningsdokumenter i et elektronisk format. For at generere et forretningsdokument, skal du oprette et ER-format, og derefter bruge ER-designeren til at definere layoutet for forretningsdokumentet og angive de data, der skal medtages i det. Du kan derefter køre ER-formatet for at generere forretningsdokumentet.

ER-værktøjet kan bruges til at generere forretningsdokumenter som Microsoft Excel-filer. Du kan bruge et Excel-dokument som en skabelon for disse dokumenter. For at definere dokumentets layout i ER-designeren kan du importere indholdet af det Excel-dokument, du vil bruge som skabelon til det definerede ER-format. For at få flere oplysninger og øve dig i dette scenarie kan du afspille opgaveguiden **Designe en ER-konfiguration til generering af rapporter i OPENXML-format** (som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10677)).

Hvis du redigerer det Excel-dokument, der bruges som en skabelon til et forretningsdokument, giver ny ER-funktionalitet dig mulighed for at genanvende den opdaterede skabelon på ER-formatet. ER-formatet opdateres derefter, så det overholder den opdaterede skabelon. Du kan få flere oplysninger om denne funktion ved at afspille opgaveguiden **Rediger et elektronisk rapporteringsformat ved at genanvende en Microsoft Excel-skabelon** (som er en del af forretningsprocessen 7.5.5.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10683)). I det trin i opgaveguiden, hvor du importerer en opdateret skabelon, skal du bruge den ændrede skabelon for Excel-filen Betalingsrapport, SampleVendPaymWsReport2, som skabelon.

