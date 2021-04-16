---
title: Analysere indgående dokumenter i Excel-format
description: Dette emne indeholder oplysninger om design af elektronisk rapporteringsformater (ER) for at analysere indhold af indgående Microsoft Excel-filer.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755174"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Analysere indgående dokumenter i Excel-format

[!include[banner](../includes/banner.md)]

Du kan designe ER-formater for at analysere indgående Microsoft Excel-filer, der repræsenterer data i Microsoft Excel-projektmapper (filer i XLSX format). Derefter kan du bruge indholdet fra disse filer til at opdatere programdata. Dette er nyttigt, hvis du:

- Designer en ny model og formaterer og vil teste den under kørsel. I så fald simulerer Excel faktiske programdata.
- Administrer andre data end dit program i Excel og ønsker at importere dataene for at sende en bestemt rapport.

Du kan finde oplysninger om denne funktion ved at afspiller opgaveguiderne **ER Import af data fra en Microsoft Excel-fil (del 1: Designformat)** og **ER Import af data fra en Microsoft Excel-fil (del 2: Importere data)** (dele af 7.5.4.3 Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)). Disse opgaveguider gennemgår, hvordan den indgående Excel-filen kan analyseres ved hjælp af ER-formatet for at importere oplysninger fra indgående dokumenter og opdatere programdata. Du kan hente filerne med opgaveguiderne i [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).

Hent følgende filer for at fuldføre opgaveguiderne nævnt ovenfor.

| Indholdsbeskrivelse                         | Filer                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Indgående fil i . XLSX-format - skabelon    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Indgående fil i . XLSX-format - eksempeldata | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Hvis du endnu ikke har afspillet følgende opgaveguide, [ER Oprette nødvendige konfigurationer for at importere data fra en ekstern fil](./tasks/er-required-configurations-import-data.md) i det aktuelle Finance and Operations-program, kan du downloade følgende fil.

| Indholdsbeskrivelse    | Filer                                                            |
|------------------------|-----------------------------------------------------------------|
| ER-modelkonfiguration | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]