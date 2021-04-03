---
title: Generere elektroniske dokumenter og opdatere programdata ved brug af ER
description: Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet til at generere udgående elektroniske dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdf595548ac1e67b99018495d2f0278dc305254d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568647"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Generere elektroniske dokumenter og opdatere programdata ved brug af ER

[!include [banner](../includes/banner.md)]

Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet til at generere udgående elektroniske dokumenter. Du kan også designe ER-formater, der fortolker indgående elektroniske dokumenter, og bruge indholdet i disse dokumenter til at opdatere programdata.

På denne måde kan et enkelt ER-format bruges til at generere udgående elektroniske dokumenter og derefter opdatere programdataene. Denne funktion kan også anvendes i følgende situationer:

- For at forhindre gentagen brug af programdata kan du markere et programs data i de efterfølgende processer med det samme, når dataene er brugt til at generere elektroniske dokumenter. For eksempel kan du markere betalingstransaktioner som allerede behandlet umiddelbart efter, at der er medtaget i en genereret betalingsmeddelelse.
- For at gemme behandlingsdetaljerne for elektroniske dokumenter, der er genereret ved hjælp af ER-logik. F.eks. et entydigt betalingsmeddelelses-id, der genereres ved hjælp af ER-udtrykket. Udtrykket er baseret på oplysninger, der er angivet i ER-dialogboksen, når ER-formatet køres for at oprette dokumenter.

Du kan få flere oplysninger om denne funktion ved at afspille sættet af opgaveguider Generere ER-dokumenter med opdatering af programdata (en del af 7.5.4.3 forretningsprocessen Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)), som fører dig gennem detaljerede oplysninger om Intrastat-rapportering og -arkivering. Følgende filer kræves for at fuldføre bestemte trin i disse opgaveguider. Hent og gem filerne til din lokale computer.

- [Konfiguration af ER-datamodel: Intrastat (model)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Konfiguration af model ER: Intrastat (tilknytning)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER-formatkonfiguration: Intrastat (format)](https://go.microsoft.com/fwlink/?linkid=849038)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]