---
title: Redigere elektroniske rapporteringsformater ved at genanvende Excel-skabeloner
description: Dette emne beskriver, hvordan du kan redigere formatet for elektroniske rapportering (ER), der bruges til at generere forretningsdokumenter ved at anvende en Excel-skabelon, der er ændret.
author: NickSelin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 626450b05789c93f63675a55e050649c862c86f6
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811384"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Redigere elektroniske rapporteringsformater ved at genanvende Excel-skabeloner

[!include [banner](../includes/banner.md)]

Værktøjet til elektronisk rapportering (ER) bruges til at oprette forretningsdokumenter i et elektronisk format. For at generere et forretningsdokument, skal du oprette et ER-format, og derefter bruge ER-designeren til at definere layoutet for forretningsdokumentet og angive de data, der skal medtages i det. Du kan derefter køre ER-formatet for at generere forretningsdokumentet.

ER-værktøjet kan bruges til at generere forretningsdokumenter som Microsoft Excel-filer. Du kan bruge et Excel-dokument som en skabelon for disse dokumenter. For at definere dokumentets layout i ER-designeren kan du importere indholdet af det Excel-dokument, du vil bruge som skabelon til det definerede ER-format. For at få flere oplysninger og øve dig i dette scenarie kan du afspille opgaveguiden **Designe en ER-konfiguration til generering af rapporter i OPENXML-format** (som er en del af forretningsprocessen 7.5.4.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10677)). I det trin i opgaveguiden, hvor du importerer en Excel-skabelon, skal du bruge den indledende skabelon for Excel-filen Betalingsrapport, [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

Hvis du redigerer det Excel-dokument, der bruges som en skabelon til et forretningsdokument, giver ny ER-funktionalitet dig mulighed for at genanvende den opdaterede skabelon på ER-formatet. ER-formatet opdateres derefter, så det overholder den opdaterede skabelon. Du kan få flere oplysninger om denne funktion ved at afspille opgaveguiden **Rediger et elektronisk rapporteringsformat ved at genanvende en Excel-skabelon** (som er en del af forretningsprocessen 7.5.5.3 Anskaffe/udarbejde komponenter til it-servicer og -løsninger (10683)). I det trin i opgaveguiden, hvor du importerer en opdateret skabelon, skal du bruge den ændrede skabelon for Excel-filen Betalingsrapport, [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx)..

## <a name="additional-resources"></a>Yderligere ressourcer

[Opdatere en skabelon](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
