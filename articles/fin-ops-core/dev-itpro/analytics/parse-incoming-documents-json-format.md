---
title: Analysere indgående dokumenter i JSON-format
description: Dette emne forklarer, hvordan du opretter ER-formater (Electronic reporting) til at parse indgående dokumenter i JSON-format (JavaScript Object Notation).
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba30b06cc0c4af230113d532a932594278e13b29a87e6252849483c9dfcbc198
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713912"
---
# <a name="parse-incoming-documents-in-json-format"></a>Analysere indgående dokumenter i JSON-format

[!include[banner](../includes/banner.md)]

Du kan designe ER-formater (Electronic reporting) til at parse indgående elektroniske dokumenter, der repræsenterer data i et tekstformat, der er baseret på JavaScript (med andre ord filer i \[JSON\]-formatet (JavaScript Object Notation)).

Hvis du vil vide mere om denne funktion, skal du hente filerne i følgende tabel og derefter afspille ER-konfigurationen Opret et format fra en ekstern JSON-filopgaveguide. I denne opgaveguide viser, hvordan et ER-format kan bruges til at analysere en indgående JSON-fil for at opdatere programdata.

| Stilling                                  | Filnavn |
|----------------------------------------|-----------|
| Konfiguration af ER-format                | [Format til import af kreditorers trans_JSON.xml](https://go.microsoft.com/fwlink/?linkid=874111) |
| Eksempel på indgående fil i .csv-format | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Behov

Før du fuldfører ER-konfigurationen Opret et format for at importere data fra en ekstern JSON-filopgaveguide, skal følgende krav opfyldes:

- Overordnede elementer i JSON-filen kan kun være objektelementer.
- Indlejrede elementer for et objekt skal være egenskabselementer, så der oprettes en gyldig JSON-struktur.
- JSON-arrays kan kun være indlejrede elementer for et objekts egenskabselementer.
- JSON-arrays kan kun indeholde JSON-objekter. De må ikke indeholde direkte strengværdier/numeriske værdier og indlejrede arrays. Elementerne i disse arrays parses i den rækkefølge, de er angivet i i formatet. Indstillingerne for multiplicitet på alle JSON-objekter vil blive taget i betragtning.

Derudover skal du fuldføre opgaveguiden [Opret de krævede konfigurationer til import af data fra en ekstern fil](tasks/er-required-configurations-import-data.md), hvis du ikke allerede har fuldført den. Hent følgende fil for at fuldføre opgaveguiden.

| Stilling                  | Filnavn |
|------------------------|-----------|
| ER-modelkonfiguration | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]