---
title: Brug Hurtig import/eksport
description: "Formålet med Hurtig import/eksport er at give dig mulighed for import og eksport i færre trin."
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: ax-2012
audience: Application User
ms.search.scope: AX 2012 R3 CU8
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11cf53af2db453471175cec5de63d38f8b680c9b
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a>Kør Værktøj til testdataoverførsel (beta) til Dynamics AX (AX 2012)

[!include[banner](../../includes/banner.md)]


Formålet med Hurtig import/eksport er at give dig mulighed for import og eksport i færre trin.

Vi har tilføjet funktionen Hurtig import/eksport for at lade brugerne importere eller eksportere simple job, der skal udføres hurtigt. Ideelt set bruges denne funktion i scenarier, hvor en fil automatisk knyttes til systemet, og hvor brugeren ikke behøver at gå gennem avancerede tilknytning eller oprette gentagne import- eller eksportjob.

-   Denne funktion understøtter arbejde med både standardenheder og brugerdefinerede enheder.
-   Du kan importere fra filer, og hvis du bruger en ODBC-datakilde, kan du vælge en forespørgsel, der kan bruges til at definere importen.
-   Du skal tidligere have defineret kildedataformater for enten AX eller Fil og vide, hvor de er placeret.
-   Du behøver ikke at oprette en behandlingsgruppe for at bruge Hurtig import/eksport. Der oprettes automatisk en af systemet under udførelse af import- eller eksportjobbet. Du kan også vælge at bevare historikken for de data, der importeres af Hurtig import/eksport.

  Bemærk, at Hurtig import/eksport antager, at du er fortrolig med DIXF-begreberne.




