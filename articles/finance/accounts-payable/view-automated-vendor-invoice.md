---
title: Se automatiseringsresultater for kreditorfaktura (prøveversion)
description: Denne artikel forklarer, hvordan du kan få vist status for kreditorfakturaer i den automatiske send-til-arbejdsgang-proces.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd9b74d2ed34399aff455563504c296a5a25a874
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895161"
---
# <a name="view-vendor-invoice-automation-results"></a>Få vist resultater af automatisering af kreditorfaktura

[!include [banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan få vist status for kreditorfakturaer i den automatiske send-til-arbejdsgang-proces. Detaljerede oplysninger om automatiseringshistorikken opretholdes for hver af de importerede kreditorfakturaer. Afhængigt af de forretningsprocesser, du har automatiseret, viser siden **Ventende kreditorfakturaer** **Status for automatisk kvitteringsafstemning** og **Status for automatisk afsendelse til arbejdsproces**. Du kan få vist detaljerne og oprette en plan for at fokusere på de fakturaer, der ikke kunne udføres i et automatiseret trin. Derefter kan du genoptage den automatiserede proces for den importerede faktura, når du har løst problemet.

Før du kan redigere en faktura, der er sendt, skal du afbryde den automatiserede behandling midlertidigt. Hvis en faktura i den automatiske afsendelse til arbejdsgang-proces skal afbrydes midlertidigt, skal du angive indstillingen **Medtag i automatisk behandling** til **Nej** på siden **Kreditorfakturaer**. Automatisering kører derefter ikke, før **Medtag i automatisk behandling** er angivet til **Ja**. En faktura kan afbrydes midlertidigt fra yderligere automatisering, hvis den endnu ikke er i arbejdsprocessystemet, og den ikke bruges af den automatiserede proces.

Hvis en importeret faktura er underlagt afsendelse til arbejdsgang-processen, kan du få vist værdien af dens **Status for automatisering** på siden **Kreditorfakturaer**. Følgende statusangivelser registreres:

- **Medtages** – De automatiserede processer, der er defineret på siden **Kreditorparametre**, kører korrekt, men er endnu ikke fuldført.
- **Midlertidigt afbrudt** – De automatiserede processer, der er defineret på siden **Kreditorparametre**, er kørt, men mindst ét trin i processen mislykkedes. Statussen **Afbrudt midlertidigt** anvendes også, hvis feltet **Medtag i automatisk behandling** er angivet til **Nej**. Du kan få vist fejlene ved at vælge **Vis seneste resultater**.
- **I arbejdsgang** – Den importerede faktura er sendt til arbejdsgangssystemet enten af den automatiske afsendelse til arbejdsgang eller manuelt.
- **Fuldført arbejdsgang** – Arbejdsgangsprocessen er fuldført for den importerede faktura.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
