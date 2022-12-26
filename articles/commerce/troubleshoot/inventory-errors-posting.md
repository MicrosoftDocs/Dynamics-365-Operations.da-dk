---
title: Fejl i bogføring af opgørelsen pga. ikke tilgængelig lagerbeholdning eller opdateringskonflikter
description: Denne artikel indeholder mulige løsningsforslag for lagerrelaterede problemer under bogføring i Microsoft Dynamics 365 Commerce.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887624"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Fejl i bogføring af opgørelsen pga. ikke tilgængelig lagerbeholdning eller opdateringskonflikter

[!include [banner](../../includes/banner.md)]

Denne artikel indeholder mulige løsningsforslag for lagerrelaterede problemer under bogføring i Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Beskrivende tekst

Under bogføringen af handelstransaktioner kan du modtage fejlmeddelelser, der er relateret til lagerproblemer eller opdateringskonflikter.

### <a name="inventory-issues-error-message"></a>Fejlmeddelelse for lagerproblemer

Hvis der opstår lagerproblemer, ligner den fejlmeddelelse, du modtager, dette eksempel:

> xx kan ikke plukkes , da der kun er yy disponibelt på lageret

### <a name="update-conflict-error-messages"></a>Opdatere fejlmeddelelser for konflikter

Der kan opstå en opdateringskonflikt, når lagervurderingsmetoden er *Standardomkostning* eller *Glidende gennemsnit*. Da begge disse metoder er metoder til konstant efterkalkulering, fastsættes den endelige omkostning på bogføringstidspunktet.

Hvis du bruger metoden *Glidende gennemsnit*, ligner fejlmeddelelsen, du modtager vedrørende opdateringskonflikten, dette eksempel:

> Lagerværdien xx.xx forventes ikke efter beregningen af den proportionale udgift

Hvis du bruger metoden *Standardomkostning*, ligner fejlmeddelelsen, du modtager vedrørende opdateringskonflikten, dette eksempel:

> Standardomkostningen stemmer ikke overens med den økonomiske lagerværdi efter opdateringen. Værdi = xx.xx, Antal = yy.yy, Standardomkostning = zz.zz

## <a name="resolutions"></a>Løsninger

### <a name="workaround-for-the-inventory-error"></a>Løsning af lagerfejlen

Du kan reducere lagerfejlen ved enten at opdatere lageret for varen manuelt eller ved at aktivere fysisk negativt lager for den varemodelgruppe, der er tilknyttet varen i Commerce Headquarters.

Microsoft anbefaler, at du aktiverer negativt fysisk lager i varemodelgruppen, så du får en problemfri bogføringsoplevelse. I visse scenarier kan negative opgørelser ikke bogføres, medmindre negativt fysisk lager er aktiveret.

Der er f.eks. ikke nogen lagerbeholdning for en vare, men kassereren returnerer varen og føjer den derefter tilbage til samme transaktion til en reduceret pris for at reducere antallet af priser. I dette tilfælde føres både returtransaktionen og salgstransaktionen til samme udtryk for den enkelte kundeordre. Men da der ikke er nogen garanti for, at returlinjen (hvilket øger lageret) bogføres, før salgslinjen (som reducerer lageret) bogføres, kan der opstå lagerfejl. Hvis negativt fysisk lager er aktiveret i dette scenario, påvirkes bogføringen af transaktionen ikke negativt, og systemet afspejler lageret korrekt.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Aktivere negativt fysisk lager for en varemodelgruppe

Hvis du vil aktivere negativt fysisk lager for en varemodelgruppe i Commerce headquarters, skal du følge disse trin.

1. Gå til **Lagerstyring \> Opsætning \> Lager**.
1. Vælg købefeltmodulet i navigationsruden til venstre.
1. I sektionen **Lagerpolitikker** under Negativt **lager skal** du markere afkrydsningsfeltet **Fysisk negativt** lager.

![Fysisk negativt lager aktiveret.](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Løsning af opdateringskonfliktfejlen

Du kan finde mulige løsningsforslag med henblik på at rette fejl i [opdateringskonflikten i en opdateringskonflikt, når lagerværdimetoden enten er standardomkostning eller det bevægelsesgennemsnit](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation).

> [!NOTE]
> I forbindelse med fejl i opdateringskonflikten behøver du ikke at slette de debitorordrer, der er genereret ved hjælp af aggregeringstrinnet til bogføring. Når du har implementeret de foreslåede løsningsforslag, skal opgørelsen bogføres, hvis du bogfører opgørelsen igen.
