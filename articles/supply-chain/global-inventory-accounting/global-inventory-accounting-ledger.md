---
title: Global Inventory Accounting-finansmodul
description: Denne artikel beskriver Global Inventory Accounting-finansmodulet, som defineres af en kombination af en valuta, en kalender, et princip og en tilknytning til en juridisk enhed.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f860e0c64573ccfe60e4854697c1e06feeed0c2
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135383"
---
# <a name="global-inventory-accounting-ledger"></a>Global Inventory Accounting-finansmodul

[!include [banner](../includes/banner.md)]

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
