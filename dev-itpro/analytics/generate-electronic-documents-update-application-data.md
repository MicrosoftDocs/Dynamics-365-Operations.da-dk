---
title: "Generere elektroniske dokumenter og opdatere programdata ved hjælp af værktøjet Elektronisk rapportering"
description: "Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet Finans and Operations til at generere udgående elektroniske dokumenter. Du kan også designe ER-formater, der fortolker indgående elektroniske dokumenter, og bruge indholdet i disse dokumenter til at opdatere programdata."
author: kfend
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: Lifecycle Services
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.2, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d37d20b26d8ae755a6c5a688afd1ad0541d1f693
ms.openlocfilehash: 7e4e0acb374fe091c0e099355204116345c62997
ms.contentlocale: da-dk
ms.lasthandoff: 06/13/2017

---


Du kan designe elektroniske rapporteringsformater (ER), der kan bruges i programmet Finans and Operations til at generere udgående elektroniske dokumenter. Du kan også designe ER-formater, der fortolker indgående elektroniske dokumenter, og bruge indholdet i disse dokumenter til at opdatere programdata. 

På denne måde kan et enkelt ER-format bruges til at generere udgående elektroniske dokumenter og derefter opdatere programdataene. Denne funktion kan også anvendes i følgende situationer:

- For at forhindre gentagen brug af programdata kan du markere et programs data i de efterfølgende processer med det samme, når dataene er brugt til at generere elektroniske dokumenter. For eksempel kan du markere betalingstransaktioner som allerede behandlet umiddelbart efter, at der er medtaget i en genereret betalingsmeddelelse.
- For at gemme behandlingsdetaljerne for elektroniske dokumenter, der er genereret ved hjælp af ER-logik. F.eks. et entydigt betalingsmeddelelses-id, der genereres ved hjælp af ER-udtrykket. Udtrykket er baseret på oplysninger, der er angivet i ER-dialogboksen, når ER-formatet køres for at oprette dokumenter.

Du kan få flere oplysninger om denne funktion ved at afspille sættet af opgaveguider Generere ER-dokumenter med opdatering af programdata (en del af 7.5.4.3 forretningsprocessen Anskaf/udarbejd komponenter til it-ydelser og -løsninger (10677)), som fører dig gennem detaljerede oplysninger om Intrastat-rapportering og -arkivering. Følgende filer kræves for at fuldføre bestemte trin i disse opgaveguider. Hent og gem filerne til din lokale computer.

- [Konfiguration af ER-datamodel: Intrastat (model)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Konfiguration af model ER: Intrastat (tilknytning)](https://go.microsoft.com/fwlink/?linkid=849038)
- [ER-formatkonfiguration: Intrastat (format)](https://go.microsoft.com/fwlink/?linkid=849038)

