---
title: Livscyklus for modeladministration (forhåndsversion)
description: I dette emne beskrives, hvordan du kan vedligeholde organisationens modeller til maskinel indlæring for at optimere de forudsigelser, de genererer.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d5566bde97a2e60d050f4a7b499b554df4848bf9
ms.sourcegitcommit: f6050b444e636ba662c00d0443c94a99f8ea0b0d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/28/2021
ms.locfileid: "6309784"
---
# <a name="model-management-lifecycle-preview"></a>Livscyklus for modeladministration (forhåndsversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I dette emne beskrives, hvordan du kan vedligeholde organisationens modeller til maskinel indlæring for at optimere de forudsigelser, de genererer.

Det anbefales, at du øver dig i modellen til kunstig intelligens i et sandkassemiljø og derefter bruger administrerede løsninger til at installere den i et produktionsmiljø. Denne tilgang er med til at sikre, at de korrekte kontroller er på plads til administration af modellens livscyklus.

Da modellen til kunstig intelligens er baseret på de tilgængelige faktura- og kundedata, er det vigtigt, at sandkassemiljøet har en nyere kopi af produktionsdataene. Du kan begynde at øve dig i modellen ved at følge trinnene i [Bruge forudsigelser om debitorbetalinger](use-customer-payment-predictions.md). Når du har øvet dig i modellen, skal du evaluere resultaterne som beskrevet i [Evaluer den indledende forudsigelsesmodel for debitorbetalinger](evaluate-payment-prediction.md). Brug oplysningerne i [Gøre forudsigelsesmodellen bedre](improve-model.md) til at eksperimentere med kombinationer af funktioner og filtre, som kan være med til at forbedre modellen.

Når du er tilfreds med træningsresultaterne, skal du følge trinnene i [Distribuere din model til kunstig intelligens](https://docs.microsoft.com/ai-builder/distribute-model) for at overføre modellen til produktionsmiljøet.