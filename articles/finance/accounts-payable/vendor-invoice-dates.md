---
title: Datoer på kreditorfakturaer
description: Denne artikel beskriver de datoer, der vises på kreditorfakturaer. Det forklares også, hvordan du automatisk kan justere bogføringsdatoen.
author: sunfzam
ms.date: 2/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 022fd0ce07fbb4c54afcf7334c1c9411e01dcf26
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775262"
---
# <a name="vendor-invoice-dates"></a>Datoer på kreditorfakturaer

[!include [banner](../includes/banner.md)]

Denne artikel beskriver de datoer, der vises på kreditorfakturaer. Det forklares også, hvordan du automatisk kan justere bogføringsdatoen.

På siden **Ventende kreditorfaktura i detaljer** viser fakturahovedet fire datoer: **datoen for modtagelse af fakturaen**, **fakturadatoen**, **bogføringsdatoen** og **forfaldsdatoen**. Når der oprettes en kreditorfaktura, angives følgende datoer som standard:

- **Modtagelsesdato for faktura** – Dette felt angives til den aktuelle systemdato.
- **Bogføringsdato** – Dette felt angives til den aktuelle systemdato. 
- **Forfaldsdato** – Datoen i dette felt beregnes på baggrund af bogføringsdatoen og betalingsbetingelserne.
- **Fakturadato** – Dette felt er som standard tomt. Du kan dog angive en værdi efter behov. I dette tilfælde genberegnes feltet **Forfaldsdato** på baggrund af fakturadatoen og betalingsbetingelserne.

Nogle gange kan en kreditorfaktura være i ventende tilstand i lang tid efter periodens afslutning. Når den er klar til at blive bogfør, bruges den gamle bogføringsdato for den tidligere bogføringsperiode stadig. Denne periode er dog lukket nu. Derfor skal kreditorassistenten manuelt ændre alle bogføringsdatoer til den nye bogføringsperiode for alle ventende fakturaer, der er oprettet tidligere.

Den funktion, der er beskrevet i denne artikel, giver dig mulighed for automatisk at justere bogføringsdatoen i forhold til virksomhedens krav.

## <a name="parameter-for-automatically-adjusting-the-vendor-invoice-posting-date"></a>Parameter for automatisk regulering af bogføringsdatoen for kreditorfakturaer

Benyt følgende trin for automatisk at justere bogføringsdatoen for kreditorfakturaer.

1.  Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
2.  Vælg en af følgende værdier i feltet **Juster bogføringsdatoen automatisk** under fanen **Finans og moms**:

    - **Ingen ændring** – Systemet ændrer ikke automatisk bogføringsdatoen under bogføringen. Denne værdi er valgt som standard.
    - **Ret altid bogføringsdatoen til systemdatoen** – Systemet ændrer automatisk bogføringsdatoen til systemdatoen under bogføring.
    - **Ret bogføringsdatoen til systemdatoen, når bogføringsdatoperioden er lukket eller på hold** – Systemet ændrer automatisk bogføringsdatoen til systemdatoen under bogføringen, men kun hvis den tilsvarende periode for bogføringsdatoen har statussen **Lukket** eller **På hold**.
    - **Ret bogføringsdatoen til den første dag i den nye periode, når bogføringsdatoperioden er lukket eller på hold** – Systemet ændrer bogføringsdatoen til den første dag i den nye åbne periode, men kun hvis den tilsvarende periode for bogføringsdatoen har statussen **Lukket** eller **På hold**.

> [!NOTE]
> Hvis den nye bogføringsdato, der blev reguleret automatisk, ligger i et nyt regnskabsår, opdateres fakturaens bogføringsdato ikke. Brugeren vil modtage en fejl "Regnskabsåret er ændret. Kontrollér og angiv bogføringsdatoen igen." Fakturabogføringsdatoen skal opdateres til den nye regnskabsårsdato, før den kan bogføres.

## <a name="impact-of-posting-date-changes"></a>Effekten af ændringer i bogføringsdato

Når bogføringsdatoen på en ventende kreditorfaktura ændres, har ændringen følgende effekt:

- **Forfaldsdato**

    - Hvis feltet **Fakturadato** er tomt, genberegnes forfaldsdatoen på baggrund af den nye bogføringsdato og betalingsbetingelserne.
    - Hvis feltet **Fakturadato** er angivet tidligere, påvirker ændringen af bogføringsdatoen ikke forfaldsdatoen.

- **Kasserabatdato**

    - Hvis feltet **Fakturadato** er tomt, bruges den nye bogføringsdato til at beregne kasserabatten.
    - Hvis feltet **Fakturadato** er angivet tidligere, ændres kasserabatten ikke.

- **Valutakurs** – Valutakursdatoen bestemmes af, hvordan indstillingen **Opdater kreditorregnskabet ved hjælp af fakturadato** er angivet under fanen **Faktura** på siden **Kreditorparametre** (**Kreditor \> Opsætning \> Kreditorparametre**).

    - Hvis denne indstilling er angivet til **Ja**, bruges **fakturadatoen**, og ændringen af **bogføringsdatoen** påvirker ikke valutakursen.
    - Hvis denne indstilling er angivet til **Nej**, anvendes bogføringsdatoen til at beregne valutakursen. Når bogføringsdatoen opdateres, genberegnes regnskabs- og rapporteringsbeløbene. Validering af sammenholdelse skal derfor udføres igen.

## <a name="validation"></a>Validering

To andre felter under fanen **Faktura** på siden **Kreditorparametre** (**Kreditor \> Opsætning \> Kreditorparametre**) påvirker behandlingen af fakturaen:

- Hvis feltet **Tjek det anvendte fakturanummer** er angivet til **Afvis dubletter inden for regnskabsåret**, bruger systemet bogføringsdatoen til at kontrollere, om der er dubletfakturaer, under bogføringen af fakturaer.
- Hvis feltet **Gør angivelse af dokumentdato på kreditorfakturaer obligatorisk** er angivet til **indstillingen Fejl**, skal feltet **Fakturadato i overskrift for ventende faktura** angives. Hvis fakturadatoen ligger senere end bogføringsdatoen, vises der en fejlmeddelelse.
