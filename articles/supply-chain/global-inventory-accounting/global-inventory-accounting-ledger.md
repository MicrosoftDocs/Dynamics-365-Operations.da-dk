---
title: Global Inventory Accounting-finansmodul
description: I dette emne beskrives Global Inventory Accounting-finansmodulet, som defineres af en kombination af en valuta, en kalender, et princip og en tilknytning til en juridisk enhed.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b29bb1aea9e96b5ef39303025cb286f0d1fde12c
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678877"
---
# <a name="global-inventory-accounting-ledger"></a>Global Inventory Accounting-finansmodul

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: Until 4/30/2022 -->

Global Inventory Accounting har sit eget sæt finansmoduler. Hver gang en lagerrelateret postering behandles for en relevant juridisk enhed, kan systemet tage højde for denne postering i et vilkårligt antal Global Inventory Accounting-finansmoduler efter behov.

Et finansmodul er et register over debet- og kreditposter. Disse poster klassificeres ved hjælp af omkostningselementer og reskontrokonti. Et Global Inventory Accounting-finansmodul defineres af kombinationen af en valuta, en kalender, et princip og en tilknytning til en juridisk enhed.

Hvis du vil oprette Global Inventory Accounting-finansmoduler, skal du gå til **Global Inventory Accounting \> Konfiguration \> Global Inventory Accounting-finansmoduler**. For hvert finansmodul skal du angive følgende felter:

- **Navn** – Angiv navnet på finansmodulet.
- **Beskrivelse** – Indtast en beskrivelse af finansmodulet.
- **Regnskabskalender** – Angiv regnskabskalenderen til finansmodulet.
- **Valuta og valutakurstype** – Brug felterne i dette oversigtspanel til at vælge den regnskabsvaluta, som finansmodulet bruger, og valutakurstypen. Den valuta, du vælger, kan være forskellig fra den valuta, som den juridiske enhed bruger. I Global Inventory Accounting kan brugerne definere så mange finansmoduler til efterkalkulation, de har brug for. Global Inventory Accounting understøtter lagerregnskab i flere valutaer og i flere vurderinger. Angiv følgende felter:

    - **Valuta** – Vælg den efterkalkulationsvaluta, som lagerrelaterede værdier vedligeholdes i. Disse værdier omfatter lagerværdi, vareforbrug, lager under transport og alle variationer heraf.
    - **Valutakurstype** – Vælg den valutakurs, som systemet skal bruge til at omregne posteringsbeløbet i transaktionsvalutaen og standardomkostningerne for varerne til efterkalkulationsvalutaen.

- **Navn på princip** – Angiv et princip. En princip er en samling politikker, der fastlægger, hvordan omkostninger skal bogføres i dette finansmodul.
- **Juridisk enhed** – Finansmodulet posterer de dokumenter, der er bogført på den valgte juridiske enhed.
- **Optimering** – Vælg, om lagerposteringer, der blev oprettet før finansmodulet blev oprettet, skal behandles i henhold til valutaen og princippet i finansmodulet. Vælg en af følgende værdier:

    - **Aktiveret** – Finansmodulet skal behandle de posteringer, der blev oprettet, før finansmodulet blev oprettet.
    - **Deaktiveret** – Finansmodulet skal kun behandle de posteringer, der er oprettet, efter finansmodulet blev oprettet.

    > [!IMPORTANT]
    > Du kan **ikke** vende tilbage og angive dette felt, når du har indtastet nye dokumenter.

- **Status** – Status angives automatisk til *Forbered* for nyoprettede finansposter.
