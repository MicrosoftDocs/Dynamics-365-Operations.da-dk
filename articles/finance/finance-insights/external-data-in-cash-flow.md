---
title: Bruge eksterne data i likviditetsbudgetter (prøveversion)
description: I dette emne beskrives de opsætningstrin, du skal udføre, så eksterne data kan angives eller importeres i likviditetsbudgetter.
author: rcarlson
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b728314f4c4e18543e4f3b75fe1e7dcddc448ea0
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638530"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Bruge eksterne data i likviditetsbudgetter (prøveversion)

[!include [banner](../includes/banner.md)]

Eksterne data kan indtastes eller importeres i likviditetsbudgetter. I dette emne beskrives de opsætningstrin, der er specifikke for brugen af eksterne data, og som gør det muligt at inkludere de eksterne data i et likviditetsbudget.

## <a name="external-data-setup"></a>Ekstern opsætning af data

Brug fanen **Ekstern kilde** på siden **Opsætning af likviditetsbudget** (**Likviditets- og bankstyring \> Likviditetsbudget**) til at angive indstillinger, der understøtter brugen af eksterne data i likviditetsbudgetter.

Du kan finde flere oplysninger om opsætningen finder du i [Likviditetsbudget](../cash-bank-management/cash-flow-forecasting.md).

Hvis du vil angive eksterne data til likviditetsbudgetter, kan du bruge funktionen Åbn i Excel til at indtaste og redigere eksterne data. Vælg knappen **Eksterne data**, og vælg derefter enten **Tilføj eksterne data** eller **Rediger eksisterende eksterne data**. Når Microsoft Excel-filen åbnes, kan du angive oplysninger i følgende felter:

- **Adgangskode**
- **Beskrivelse** (valgfri)
- **Navn på ekstern kilde** – Vælg en af de værdier på listen, som du definerede, da du konfigurerede Finance Insights.
- **Juridisk enhed**
- **Dato**
- **Beløb i transaktionsvaluta**
- **Valutakode**
- **Standarddimension** (valgfrit)
- **Dokumentnummer** (valgfrit)
- **Kontonummer** (valgfrit)
- **Kontonavn** (valgfrit)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Importere eksterne data ved hjælp af data Management Framework

Du kan importere eksterne data til likviditetsbudgetter ved hjælp af arbejdsområdet **Datastyring** og den enhed, der hedder **Eksternt likviditetsbudget**.

Hvis du desuden skal flytte konfigurationsdata fra ét miljø til et andet, er området for følgende objekter tilgængelige for de opsætningstabeller, der er nødvendige:

- Konfiguration af ekstern kilde til likviditetsbudget
- Konfiguration af ekstern kildes juridiske enhed til likviditetsbudget

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
