---
title: Eksterne data i likviditetsbudgetter
description: Denne artikel beskriver de opsætningstrin, der skal udføres, så eksterne data kan angives eller importeres i likviditetsbudgetter.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846938"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Eksterne data i likviditetsbudgetter

[!include [banner](../includes/banner.md)]

Eksterne data kan indtastes eller importeres i likviditetsbudgetter. Denne artikel beskriver de opsætningstrin, der er specifikke for brugen af eksterne data, og som gør det muligt at inkludere de eksterne data i et likviditetsbudget.

## <a name="external-data-setup"></a>Ekstern opsætning af data

Brug fanen **Ekstern kilde** på siden **Opsætning af likviditetsbudget** (**Likviditets- og bankstyring \> Likviditetsbudget \> Opsætning af likviditetsbudget**) til at angive indstillinger, der understøtter brugen af eksterne data i likviditetsbudgetter.

Eksterne data kan indtastes eller importeres i likviditetsbudgetter. Før eksterne data angives eller importeres, skal der konfigureres eksterne kilder. Under fanen **Ekstern kilde** skal du konfigurere eksterne likviditetskategorier. En kategori kan enten være **Udgående** eller **Indgående**. **Likviditet** skal vælges som bogføringstype. I gitteret **Indstillinger for juridisk enhed** skal du vælge de juridiske enheder og de tilsvarende hovedkonti, som de eksterne likviditetskategorier gælder for.

Du kan finde flere oplysninger om, hvordan du konfigurerer likviditetsbudgetter, i [Likviditetsbudget](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Angive eksterne data

Hvis du vil angive og redigere eksterne data til likviditetsbudgetter, kan du bruge funktionen **Åbn i Excel**. Vælg knappen **Eksterne data** i arbejdsområdet **Likviditetsbudget**, og vælg derefter enten **Tilføj eksterne data** eller **Rediger eksisterende eksterne data**. Når Microsoft Excel-filen åbnes, kan du angive oplysninger i følgende felter:

- **Post-id** (entydigt)
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
