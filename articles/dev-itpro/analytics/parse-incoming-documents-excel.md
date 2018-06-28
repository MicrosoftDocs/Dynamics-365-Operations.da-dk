---
title: "Analysere indgående dokumenter i Microsoft Excel"
description: "Dette emne indeholder oplysninger om design af elektronisk rapporteringsformater (ER) for at analysere indhold af indgående Microsoft Excel-filer."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 001e287590b9f43ed38de803bcace3a25a6f6637
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2018

---

# <a name="parse-incoming-microsoft-excel-files"></a>Analysere indgående Microsoft Excel-filer

[!include[banner](../includes/banner.md)]

Du kan designe ER-formater for at analysere indgående Microsoft Excel-filer, der repræsenterer data i Microsoft Excel-projektmapper (filer i XLSX format). Derefter kan du bruge indholdet fra disse filer til at opdatere programdata. Dette er nyttigt, hvis du:

-   Designer en ny model og formaterer og vil teste den under kørsel. I så fald simulerer Excel faktiske programdata.
-   Administrer andre data end dit program i Excel og ønsker at importere dataene for at sende en bestemt rapport.

Du kan finde oplysninger om denne funktion ved at afspiller opgaveguiderne **ER Import af data fra en Microsoft Excel-fil (del 1: Designformat)** og **ER Import af data fra en Microsoft Excel-fil (del 2: Importere data)** (dele af 7.5.4.3 Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)). Disse opgaveguider gennemgår, hvordan den indgående Excel-filen kan analyseres ved hjælp af ER-formatet for at importere oplysninger fra indgående dokumenter og opdatere programdata. Du kan hente filerne med opgaveguiderne i [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).

Hent følgende filer for at fuldføre opgaveguiderne nævnt ovenfor.

| Indholdsbeskrivelse                        | Filer                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| Indgående fil i . XLSX-format - skabelon   | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)  |
| Indgående fil i . XLSX-format - eksempeldata| [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Hvis du endnu ikke har afspillet følgende opgaveguide, [ER Oprette nødvendige konfigurationer for at importere data fra en ekstern fil](./tasks/er-required-configurations-import-data.md), i det aktuelle Dynamics 365 for Finance and Operation-program, kan du hente følgende fil.

| Indholdsbeskrivelse                        | Filer                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| ER-modelkonfiguration                     | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266)            |


