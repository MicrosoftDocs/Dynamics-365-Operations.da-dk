---
title: Livscyklustilstande for vedligeholdelsesanmodninger
description: Dette emne beskriver, hvordan du konfigurerer livscyklustilstande for vedligeholdelsesanmodninger i Styring af aktiver.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b54b58a29dc23e19f5065363c331351f24267ac
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360940"
---
# <a name="maintenance-request-lifecycle-states"></a>Levetidstilstande for vedligeholdelsesanmodninger

[!include [banner](../../includes/banner.md)]

 


Livscyklustilstande for vedligeholdelsesanmodninger definerer de stadier, som en anmodning kan gennemgå. Som eksempler kan nævnes **Oprettede**, **Aktive** og **Afsluttede**. Når en vedligeholdelsesanmodning konverteres til en arbejdsordre, skal vedligeholdelsesanmodningens livscyklustilstand opdateres til **Afsluttet** eller **Lukket** for at angive, at vedligeholdelsesanmodningen ikke længere er aktiv. På listesiden **Alle vedligeholdelsesanmodninger** kan du se alle vedligeholdelsesanmodninger, uanset deres livscyklustilstand.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Konfigurer livscyklustilstande for vedligeholdelsesanmodninger

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Livscyklustilstande**.
2. Vælg **Ny** for at oprette en tilstand for vedligeholdelsesanmodningens livscyklus.
3. Angiv et ID for livscyklustilstand i feltet **Livscyklustilstand**.
4. Indtast et navn i feltet **Navn**.

    I oversigtspanelet **Detaljer** viser feltet **Livscyklusmodeller** antallet af livscyklusmodeller for vedligeholdelsesanmodninger, der bruger denne livscyklustilstand.

5. I oversigtspanelet **Generelt** skal du angive indstillingen **Aktiv** til **Ja**, hvis en vedligeholdelsesanmodning bør være aktiv, mens den er i denne livscyklustilstand.
6. Angiv indstillingen **Angiv faktisk slutning** til **Ja**, hvis der automatisk skal angives en faktisk slutdato og tidspunkt på en vedligeholdelsesanmodning i denne livscyklustilstand.
7. Angiv indstillingen **Opret arbejdsordre** til **Ja**, hvis der kan oprettes en arbejdsordre ud fra en vedligeholdelsesanmodning i denne livscyklustilstand.
8. Angiv indstillingen **Slet** til **Ja**, hvis en vedligeholdelsesanmodning kan slettes, mens den er i denne livscyklustilstand.
9. I oversigtspanelet **Opdater** er indstillingerne **Indgående** og **Udgående** i afsnittet **Aktiv** relevante, hvis du bruger reparation af depot. Angiv den relevante indstilling til **ja**, hvis livscyklustilstanden for aktiver, der er valgt på en vedligeholdelsesanmodning, automatisk skal opdateres til **Indgående** eller **Udgående**, når vedligeholdelsesanmodningens livscyklustilstand for den pågældende vedligeholdelsesanmodning er angivet til **Indgående** eller **Udgående**.

Følgende illustration viser et eksempel på listesiden **Vedligeholdelsesanmodningers livscyklustilstande**.

![Siden Livscyklustilstande for vedligeholdelsesanmodning.](media/02-setup-for-requests.png)

> [!NOTE]
> Livscyklustilstande for vedligeholdelsesanmodninger, livscyklustilstandsgrupper og -typer er relateret til og bruges på samme måde som arbejdsordres livscyklustilstande, livscyklustilstandsgrupper og -typer. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Konfigurer livscyklusmodeller for vedligeholdelsesanmodninger

Når du har oprettet de livscyklustilstande, der kræves til dine vedligeholdelsesanmodninger, kan de opdeles i livscyklustilstandsgrupper eller livscyklusmodeller. Livscyklusmodeller for vedligeholdelsesanmodning bruges til at oprette det flow, der kan anvendes til forskellige typer af vedligeholdelsesanmodninger. Der skal som minimum oprettes én standardlivscyklusmodel for vedligeholdelsesanmodninger.

1. Vælg **Styring af aktiver** \> **Opsætning** \> **Vedligeholdelsesanmodninger** \> **Livscyklusmodeller**.
2. Vælg **Ny** for at oprette en model for vedligeholdelsesanmodningens livscyklus.
3. Angiv et ID for livscyklusmodellen i feltet **Livscyklusmodel**.
4. Indtast et navn i feltet **Navn**.

    I oversigtspanelet **Detaljer** viser feltet **Livscyklustilstande** antallet af livscyklustilstande, der er valgt i denne livscyklusmodel. Feltet **Vedligeholdelsesanmodningstyper** viser antallet af vedligeholdelsesanmodningstyper, der bruger denne livscyklusmodel.

5. I oversigts panelet **Livscyklustilstande** skal du vælge de livscyklustilstande, der bør inkluderes i livscyklusmodellen:

    - Hvis du vil inkludere en livscyklustilstand i livscyklusmodellen, skal du vælge den i sektionen **Resterende livscyklustilstande** og derefter vælge knappen med højre pil ![Højre pil.](media/03-setup-for-requests.png) for at flytte den til sektionen **Valgte livscyklustilstande**.
    - Hvis du vil inkludere alle de tilgængelige livscyklustilstande i livscyklusmodellen, skal du vælge knappen **Vælg alle tilgængelige tilstande** ![Vælg alle tilgængelige tilstande.](media/04-setup-for-requests.png). Alle livscyklustilstande flyttes til sektionen **Valgte livscyklustilstande**.
    - Hvis du vil fjerne en livscyklustilstand fra livscyklusmodellen, skal du vælge den i sektionen **Valgte livscyklustilstande** og derefter vælge knappen med venstre pil ![Venstre pil.](media/05-setup-for-requests.png) for at flytte den til sektionen **Resterende livscyklustilstande**.

6. I oversigtspanelet **Generelt** er felterne i sektionen **Opdateringer** relevante, hvis du bruger reparation af depot.

    - I feltet **Livscyklustilstand for modtaget aktiv** skal du vælge den for aktivlivscyklustilstand, som aktiver, der er valgt på en vedligeholdelsesanmodning, automatisk skal opdateres til, når de modtages til reparation af depot.
    - I feltet **Livscyklustilstand for leveret aktiv** skal du vælge den for livscyklustilstand, som aktiver, der er valgt på en vedligeholdelsesanmodning, automatisk skal opdateres til, når de returneres efter reparation.

Følgende illustration viser et eksempel på listesiden **Vedligeholdelsesanmodningers livscyklusmodeller**.

![Siden Livscyklusmodeller for vedligeholdelsesanmodning.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]