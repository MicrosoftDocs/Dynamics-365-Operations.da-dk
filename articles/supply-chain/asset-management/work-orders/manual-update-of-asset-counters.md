---
title: Manuel opdatering af aktivtællere
description: I dette emne beskrives manuel opdatering af aktivtællere i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875569"
---
# <a name="manual-update-of-asset-counters"></a>Manuel opdatering af aktivtællere

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Tællere bruges til at oprette registreringer på et aktiv, f.eks. antallet af timer i drift eller antallet af producerede varer.

Hvis den tællertype, der er valgt for en tæller, er indstillet til at arve tællerværdier (**Styring af aktiver** > **Opsætning** > **Aktivtyper** > **Tællere** > **Generelt**-oversigtspanelet > **Arv tællerværdier for aktiv**-til/fra knappen indstillet til "ja"), opdateres alle de underordnede aktiver, der bruger samme tællertype, automatisk, når du opretter en ny tællerlinje af denne type.

I **Alle aktiver** kan du oprette registreringer af timer eller antal optællinger for et aktiv ud fra dine aflæsninger af aktivet.

1. Klik på **Styring af aktiver** > **Almindelig** > **Aktiver** > **Alle aktiver**.

2. Vælg aktivet på listen, og klik på **Tællere**. I formularen **Aktivtællere** vises en liste over alle tidligere tællerregistreringer på det valgte aktiv.

3. Klik på **Ny** for at oprette en registrering. Aktiv-id'et indsættes automatisk.

4. Vælg den relevante tæller i feltet **Tæller**. Kun tællere, der er relateret til den aktivtype, der er valgt på aktivet, er tilgængelige. Den relaterede enhed indsættes automatisk i feltet **Enhed**.

5. Vælg dato og klokkeslæt for tællerregistreringen.

6. Indsæt tallet i feltet **Værdi** siden sidste tællerregistrering, eller indsæt det samlede optalte antal i feltet **Akkumuleret værdi**.

- Hvis du fysisk installerer en ny tæller på et aktiv, skal du registrere ændringen af aktivet i **Aktivtællere**. Derefter skal du oprette to registreringslinjer med identiske tidsstempler, og på linjen angående den nye tæller, skal du markere afkrydsningsfeltet **Nulstil tæller**. Når du opretter de to registreringslinjer, skal den første linje være for den tæller, du udskifter. I feltet **Totaler** er det samlede antal summen af tællertotalen for alle registrerede værdier på den pågældende tællertype.  
- Hvis afkrydsningsfeltet **Nulstil tæller** er markeret på et aktiv ved hjælp af en vedligeholdelsesplan med intervaltypen "En gang fra..." eller "Når nået...", er tælleren stadig aktiv på den nye tællerlinje, fordi du opretter en separat tællerlinje og starter forfra med en ny tæller.

![Figur 1](media/11-work-orders.png)


Hvis du har brug for at foretage tællerregistrering på flere anlægsaktiver, kan det gøres i **Styring af aktiver** > **Forespørgsler** > **Aktiver** > **Aktivtællere**.

>[!NOTE]
>Du kan oprette et interval for at definere afvigelser i manuelle tællerregistreringer og den type meddelelse, der skal vises, hvis registreringer ligger uden for det angivne interval. Se emnet [Tællere](../setup-for-objects/counters.md) vedrørende opsætning af tællere.
