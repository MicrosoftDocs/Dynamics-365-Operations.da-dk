---
title: Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten
description: Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756697"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten

Fejlkoder: WHSLoadWeightOnLinesDoNotMatchLoadWarning

## <a name="symptoms"></a>Symptomer

Systemet viser følgende fejlmeddelelse:

> Vægtfelterne på lastlinjerne svarer ikke til vægtfelterne i lasten %1. Kør Konsistenskontrol af lastvægt for lagersted for at genberegne vægtfelterne.

## <a name="cause"></a>Årsag

Felterne **Nettovægt** og **Taravægt** er angivet til *0* (nul) på lastlinjen. Vægtfelterne er dog ikke angivet til *0* for vægtmålingerne for produktet. Når der ikke er angivet vægtfelter på lastlinjen, kan eventuelle rettelser i antallet på lastlinjen medføre forkert vægtberegning af lasten. Dette problem kan forekomme, hvis vægten på produktet er blevet ændret, siden lastlinjen blev oprettet.

## <a name="resolution"></a>Løsning

Når der oprettes en lastlinje, angives vægtfelterne fra produktet som standard på den. Hvis vægten er nul, kan du genberegne den ved hjælp af funktionen *Konsistenskontrol af lastvægt for lagersted*.

1. Gå til **Systemadministration \> Periodiske opgaver \> Database \> Konsistenskontrol**.
1. Angiv feltet **Modul** til **Lagerstedsstyring** i dialogboksen *Konsistenskontrol*.
1. Angiv feltet **Kontrollér/ret** til *Ret fejl*.
1. Marker afkrydsningsfeltet **Konsistenskontrol af lastvægt for lagersted**, og kontroller, at rækken for dette afkrydsningsfelt er markeret.
1. Øverst på listen med afkrydsningsfelter skal du vælge ellipseknappen (**...**) og derefter vælge **Dialog** i menuen.
1. I dialogboksen **Konsistenskontrol af lastvægt for lagersted** skal du angive følgende felter for at angive de kriterier, som konsistenskontrollen skal køres for:

    - **Last-id:** Angiv et last-id. Lad feltet stå tomt for at markere alle last-id'er.
    - **Varenummer:** Angiv et varenummer. Lad feltet stå tomt for at markere alle elementer.
    - **Genberegn altid vægt på laster:** Angiv denne indstilling til *Ja*.
    - **Tillad overskrivning af vægt på lastlinjer:** Angiv denne indstilling til *Ja*.

1. Vælg **OK** for at lukke dialogboksen **Konsistenskontrol af lastvægt for lagersted**.
1. Vælg ellipseknappen, og vælg derefter **Udfør** i menuen.

Vægten genberegnes baseret på de kriterier, du har angivet. Vælg linket **Meddelelsesdetaljer** for at få vist resultatet af konsistenskontrollen.
