---
title: Tilstande for aktivlivscyklus
description: Denne artikel forklarer aktivers livscyklustilstand og livscyklusmodeller i Styring af aktiver.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b1ff9438437e6c1ff33bab9a7ba0361029cb6d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901054"
---
# <a name="asset-lifecycle-states"></a>Tilstande for aktivlivscyklus

[!include [banner](../../includes/banner.md)]

 

Denne artikel forklarer aktivers livscyklustilstand og livscyklusmodeller i Styring af aktiver. Aktivers livscyklustilstande bruges til at definere, om et aktiv er aktivt eller inaktivt. Du kan for eksempel konfigurere livscyklustilstande for aktiver som **Oprettet**, **Aktiv** og **Afsluttet**.

> [!NOTE]
> - Livscyklustilstande for anmodninger er knyttet til aktivernes livscyklustilstande. Når en anmodning ændres til en ny livscyklustilstand for en anmodning, ændres det aktiv, der er tilknyttet anmodningen, derfor til en ny livscyklustilstand for aktivet. Hvis livscyklustilstanden for en anmodning eksempelvis ændres til **Indgående**, ændres livscyklustilstanden for det tilknyttede aktiv til den livscyklustilstand, der er valgt i feltet **Indgående livscyklustilstand** på oversigtspanelet for **Aktivets livscyklustilstand** på siden **Aktivets livscyklustilstandmodeller**. 


Aktivers livscyklustilstande kan konfigureres i aktivernes livscyklusmodeller, hvor du kan definere de påkrævede livscyklustilstande for forskellige typer aktiver. Du konfigurerer først livscyklustilstandene. Derefter opretter du en livscyklusmodel og vælger livscyklustilstande for den.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Livscyklustilstande**.
2. Vælg **Ny** for at oprette en ny tilstand for aktivets livscyklus.
3. Indtast ID'et for livscyklustilstanden i feltet **Livscyklustilstand**.
4. Angiv en beskrivelse i feltet **Navn**.

    Feltet **Livscyklusmodeller** viser antallet af livscyklusmodeller for aktiver, der bruger denne aktivlivscyklustilstand.

5. Angiv indstillingen **Aktiv** til **Ja**, hvis denne livscyklustilstand skal være en aktiv livscyklustilstand (med andre ord hvis der kan oprettes arbejdsordrer for aktiver i denne livscyklustilstand).
6. Angiv indstillingen **Slet åbne kalenderlinjer** til **Ja**, hvis åbne kalenderlinjer for et aktiv, der har en aktivlivscyklustilstand med status **Oprettet**, skal slettes, når de er i denne livscyklustilstand. Denne indstilling er nyttig, hvis du vil rydde op i eventuelle åbne vedligeholdelsesplaner, der ikke længere er relevante for aktivet (f.eks. hvis aktivet ikke længere er aktivt).

> [!NOTE]
> Aktivers livscyklustilstande, livscyklusmodeller for aktiver og aktivtyper er relateret. De bruges på samme måde som arbejdsordrers livscyklustilstande, arbejdsordrers livscyklusmodeller og arbejdsordretyper. 


Når du har oprettet de påkrævede livscyklustilstande for aktiver, kan du konfigurere livscyklustilstande i aktivlivscyklusmodeller.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Aktiver** \> **Livscyklusmodeller**.
2. Vælg **Ny** for at oprette en ny model for aktivets livscyklus.
3. Angiv ID'et for livscyklusmodellen i feltet **Livscyklusmodel**.
4. Angiv en beskrivelse i feltet **Navn**.

    Feltet **Livscyklustilstande** viser antallet af aktivlivscyklustilstande, der er valgt i denne aktivlivscyklusmodel. Feltet **Aktivtyper** viser antallet af aktivtyper, der bruger livscyklusmodellen.

5. I oversigtspanelet **Livscyklustilstande** skal du vælge de aktivlivscyklustilstande, der bør inkluderes i aktivlivscyklusmodellen:

    - Hvis du vil bruge en livscyklustilstand for modellen, skal du vælge den i sektionen **Resterende livscyklustilstande** og derefter vælge knappen med højre pil ![Højre pil.](media/15-setup-for-objects.png) for at flytte den til sektionen **Valgte livscyklustilstande**.
    - Hvis du vil bruge alle de tilgængelige livscyklustilstande for modellen, skal du vælge knappen **Alle tilgængelige livscyklustilstande** ![Alle tilgængelige livscyklustilstande.](media/20-setup-for-objects.png). Alle livscyklustilstande overføres til sektionen **Valgte livscyklustilstande**.
    - Hvis du vil fjerne en livscyklustilstand fra modellen, skal du vælge den i sektionen **valgte livscyklustilstande** og derefter vælge knappen med venstre pil ![Venstre pil.](media/16-setup-for-objects.png) for at flytte den til sektionen **Resterende livscyklustilstande**.

6. Vælg **Opdateringer til livscyklustilstande** for at definere de aktivlivscyklustilstande, der kan følge en valgt livscyklustilstand.
7. Du kan bruge oversigtspanelet **Aktivtilstand**, hvis du håndterer aktiver, som du modtager til reparation. I sektionen **Indgående/udgående** kan du vælge livscyklustilstand for aktiver for at angive arbejdsgangen for et aktiv, som du modtager til reparation. Hvis du tilbyder udlånsaktiver til kunder eller afdelinger, kan du i sektionen **Udlån** vælge livscyklustilstande for udlånsaktiver.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]