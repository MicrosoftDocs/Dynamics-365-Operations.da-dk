---
title: Oprette arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer i Styring af aktiver.
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
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875562"
---
# <a name="creating-work-orders"></a>Oprette arbejdsordrer


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer for jobbene. Du kan gøre det i en af vedligeholdelsestidsplanerne. De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper:

| Referencetype | Beskrivelse                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Vedligeholdelsesplaner     | Præventivee vedligeholdelsesjob baseret på vedligeholdelsesplantyperne "Tid" eller "Tæller".                       |
| Vedligeholdelsesrunder    | Præventive vedligeholdelsesjob med flere aktiver, der kræver en lignende form for vedligeholdelse.           |
| Vedligeholdelsesanmodning   | Manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv, som kan konverteres til en arbejdsordre. |


1. Klik på **Styring af aktiver** > **Generelt** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer**.

2. Vælg de planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for, og klik på **Arbejdsordre**. Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer**.

3. Vælg, hvor mange arbejdsordrer der skal oprettes, i sektionen **Parametre**. Du kan oprette én arbejdsordre pr. vedligeholdelsestidsplanslinje eller et antal arbejdsordrer ud fra dine valg i sektionen **Én arbejdsordre pr.**.

4. Vælg en **Arbejdsordretype**, der skal bruges på alle de arbejdsordrer, du opretter.

5. Klik på **OK**. Der oprettes en eller flere arbejdsordrer.

![Figur 1](media/18-preventive-maintenance.png)

