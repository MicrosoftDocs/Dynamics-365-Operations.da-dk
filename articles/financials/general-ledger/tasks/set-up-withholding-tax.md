---
title: Konfigurere A-skat
description: Dette emne beskriver, hvordan du konfigurerer A-skat.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834728"
---
# <a name="set-up-withholding-tax"></a>Konfigurere A-skat

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emne beskriver, hvordan du konfigurerer A-skat. *A-skat* er en skat på leverandører, der ikke opretter momstransaktioner. A-skat, der beregnes på leverandørbetalinger, er et passiv. Derfor er det kun statuskonti eller passivkonti, der kan bruges til bogføring af A-skat. Denne opgaveguide viser, hvordan du konfigurerer A-skat.

1. Gå til **Navigationsrude > Moduler > Skat > Indirekte skatter > A-skat > Koder for A-skat**.
2. Vælg **Ny**.
3. Skrive en værdi i feltet **Koder for A-skat**.
4. Angiv navnet for koden for A-skat i feltet **Navn på A-skat**.
5. Vælg hovedkontoen til bogføring af A-skattetilsvar i feltet **Hovedkonto**.
6. Vælg **Gem**.
7. Vælg **Værdier** og markér den ønskede post i listen.
8. Angiv en procentsats, der bruges til beregning af A-skat i feltet **Værdi**.
9. Vælg **Gem**.
10. Luk siden.
11. Vælg **Gem**.
12. Luk siden.
13. Gå til **Navigationsrude > Moduler > Skat > Indirekte skatter > A-skat > Grupper for A-skat**.
14. Vælg **Ny**.
15. Angiv identifikatoren for gruppen for A-skat i feltet **Grupper for A-skat**.
16. Skriv navnet på gruppen for A-skat i feltet **Beskrivelse**.
17. Vælg kode for A-skat i feltet **Kode for A-skat**.
18. Vælg **Gem**.
19. Luk siden.

