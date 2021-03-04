---
title: Oprette arbejdsordrer
description: Dette emne beskriver, hvordan du opretter arbejdsordrer i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424668"
---
# <a name="creating-work-orders"></a>Oprette arbejdsordrer

[!include [banner](../../includes/banner.md)]

 

Når du har planlagt præventive vedligeholdelsesjob, er næste trin at oprette arbejdsordrer for jobbene. Du kan gøre det i en af vedligeholdelsestidsplanerne. De planlagte job i en vedligeholdelsestidsplan kan have forskellige referencetyper:

| Referencetype | Beskrivelse                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Vedligeholdelsesplaner     | Præventivee vedligeholdelsesjob baseret på vedligeholdelsesplantyperne "Tid" eller "Tæller".                       |
| Vedligeholdelsesrunder    | Præventive vedligeholdelsesjob med flere aktiver, der kræver en lignende form for vedligeholdelse.           |
| Vedligeholdelsesanmodning   | Manuelt oprettet anmodning om vedligeholdelse eller reparation af et aktiv, som kan konverteres til en arbejdsordre. |


1. Klik på **Styring af aktiver** > **Generelt** > **Alle vedligeholdelsestidsplaner** eller **Åbne vedligeholdelsestidsplanslinjer** eller **Åbne vedligeholdelsestidsplanspuljer**.

2. Vælg de planlagte vedligeholdelsesjob, du vil oprette en arbejdsordre for, og klik på **Arbejdsordre**. Det samlede antal budgetterede timer for de valgte linjer vises i feltet **Vedligeholdelsesprognosetimer** i dialogboksen **Opret arbejdsordrer**.

3. Vælg, hvor mange arbejdsordrer der skal oprettes, i sektionen **Parametre**. Du kan oprette én arbejdsordre pr. vedligeholdelsestidsplanslinje eller et antal arbejdsordrer ud fra dine valg i sektionen **Én arbejdsordre pr.**.

4. Vælg en **Arbejdsordretype**, der skal bruges på alle de arbejdsordrer, du opretter. I illustrationen nedenfor vises et eksempel på dialogboksen **Opret arbejdsordrer**.

![Figur 1](media/18-preventive-maintenance.png)

5. Klik på **OK**. Der oprettes en eller flere arbejdsordrer.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]