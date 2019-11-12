---
title: Manuel opdatering af aktivtællere
description: I dette emne beskrives manuel opdatering af aktivtællere i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3072ab204b53b16988d2973b28a697041cb84c27
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626126"
---
# <a name="manual-update-of-asset-counters"></a>Manuel opdatering af aktivtællere

[!include [banner](../../includes/banner.md)]



Tællere bruges til at oprette registreringer på et aktiv, f.eks. registreringer af det antal timer, som aktivet har været i drift, eller det antal, der er produceret.

Den tællertype, der er valgt for en tæller, kan være angivet til at arve tællerværdier. Indstillingen **Arv tællerværdier for aktiv** er med andre ord angivet til **Ja** i oversigtspanelet **Generelt** på siden **Tællere** (**Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere**). Hvis du i dette tilfælde opretter en ny tællerlinje af denne type, opdateres alle underordnede aktiver, der bruger samme tællertype, automatisk.

På siden **Alle aktiver** kan du oprette tællerregistreringer af timer eller antal for et aktiv ud fra dine aflæsninger af aktivet.

1. Vælg **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.

2. Vælg aktivet, og vælg **Tællere** i handlingsrudegruppen **Forebyggende** under fanen **Aktiv**. På siden **Aktivtællere** vises en liste over alle tidligere tællerregistreringer, der er foretaget på det valgte aktiv.

3. Vælg **Ny** for at oprette en ny registrering. Aktiv-id indtastes automatisk i feltet **Aktiv**.

4. Vælg den relevante tæller i feltet **Tæller**. Kun tællere, der er relateret til den aktivtype, der er valgt på aktivet, kan vælges. Den relaterede enhed indsættes automatisk i feltet **Enhed**.

5. Vælg dato og klokkeslæt for tællerregistreringen i feltet **Registreret**.

6. I feltet **Værdi** skal du angive nummeret siden sidste tællerregistrering. Du kan også angive det samlede antal i feltet **Akkumuleret værdi**.

Vær opmærksom på følgende punkter:

- Hvis du fysisk installerer en ny tæller på et aktiv, skal du registrere ændringen af aktivet på siden **Aktivtællere**. Derefter skal du oprette to registreringslinjer, der har identiske tidsstemplinger. Den første linje skal være for den tæller, du er ved at udskifte. Markér afkrydsningsfeltet **Nulstil tæller** på den linje, der er relateret til den nye tæller. I feltet **Totaler** er det samlede antal summen af tællertotalerne for alle registrerede værdier på den pågældende tællertype.

- Hvis afkrydsningsfeltet **Nulstil tæller** er markeret på et aktiv ved hjælp af en vedligeholdelsesplan med intervaltypen "Én gang fra..." eller "Når nået...", er tælleren stadig aktiv på den nye tællerlinje, fordi du opretter en separat tællerlinje og starter forfra med en ny tæller.

I illustrationen nedenfor vises et eksempel på siden **Aktivtællere**.

![Figur 1](media/11-work-orders.png)

På siden **Aktivtællere** (**Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivtællere**) kan du foretage tællerregistreringer på flere aktiver på samme tid efter behov.

>[!NOTE]
>Du kan konfigurere et interval for at definere afvigelser i manuelle tællerregistreringer. Du kan også angive den type meddelelse, der vises, hvis registreringerne er uden for det angivne interval. Du kan finde flere oplysninger om, hvordan du konfigurerer tællere, i [Tællere](../setup-for-objects/counters.md).

