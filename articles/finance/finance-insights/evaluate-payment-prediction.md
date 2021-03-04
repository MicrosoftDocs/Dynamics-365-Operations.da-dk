---
title: Evaluer den indledende forudsigelsesmodel for debitorbetalinger (prøveversion)
description: I dette emne beskrives de trin, du kan tage for at forstå forudsigelsesmodellen for debitorbetaling og evaluerer effektiviteten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d761e31c4e4169b09711e351948390d2d40f3739
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644963"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Evaluer den indledende forudsigelsesmodel for debitorbetalinger (prøveversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emne forklarer, hvordan du evaluerer en forudsigelsesmodel, når du har aktiveret Finance Insights og derefter genererede og afprøvede din første model. Dette emne omhandler modeller til forudsigelse af debitorbetalinger. Dette emne beskrives de trin, du kan tage for at forstå forudsigelsesmodellen for debitorbetaling og evaluerer effektiviteten.

## <a name="getting-details-about-the-model"></a>Hente oplysninger om modellen

På siden **Finance Insights-parametre** i Microsoft Dynamics 365 Finance vises der et link **Forbedring af modellens nøjagtighed** ud for præcisionsscoren.

[![Forbedring af modellens nøjagtighed](./media/prediction-model.png)](./media/prediction-model.png)

Dette link fører dig til AI Builder, hvor du kan lære mere om den aktuelle model og gennemgå forholdsregler for at forbedre den. I følgende illustration vises den side, der er åbnet.

[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)

Den side, der er åbnet, viser følgende oplysninger:

- I afsnittet **Ydeevne** giver modellens ydeevne et overslag over modellens kvalitet. Du kan finde flere oplysninger om denne klasse i [Forudsigelsesmodel-ydeevne](https://docs.microsoft.com/ai-builder/prediction-performance) i dokumentationen til AI Builder.
- Afsnittet **Data med mest indflydelse** viser, hvordan vigtige andre inputtyper for data var for din model. Du kan evaluere denne liste og de tilsvarende procenter for at afgøre, om oplysningerne er i overensstemmelse med det, du kender til din virksomhed og dit marked.

    [![Ydeevne og de dataafsnit med mest indflydelse til forudsigelsesmodellen](./media/models.png)](./media/models.png)

- I afsnittet **Ydeevne** skal du vælge **Se detaljer** for at få mere at vide om karakteren og andre overvejelser. Følgende illustration viser detaljerne, at modellen bruger færre oplysninger, end der anbefales. Systemet har derfor oprettet en advarselsmeddelelse.

    [![Advarsler om modellens ydeevne](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Graver dybere

Selvom nøjagtigheden er et godt udgangspunkt for evaluering af en model, og performance-klassen indeholder perspektiv, giver AI Builder mere detaljerede målepunkter, som du kan bruge til evalueringen. Hvis du vil hente oplysningerne, skal du vælge ellipseknappen (**....**) ved siden af knappen **Brug model** i afsnittet **Ydeevne** og derefter vælge **Hent detaljerede målepunkter**.

[![Kommandoen Hent detaljerede måleoplysninger](./media/performance.png)](./media/performance.png)

Følgende illustration viser det format, du kan hente dataene i.

[![Format for hentede data](./media/data-format.png)](./media/data-format.png)

For at opnå en dybere analyse af resultaterne er det et godt udgangspunkt at gennemgå måleværdien "Forvekslingsmatrix". Her er f. eks. de data, der vises for denne måleværdi i den foregående illustration.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Du kan udvide disse data på følgende måde.

|                          | Forventet til tiden | Forventede forsinkede | Forventede meget forsinkede |
|--------------------------|-------------------|----------------|---------------------|
| Betaling til tiden   | **71**            | 0              | 21                  |
| Forsinket betaling      | 5                 | **0**          | 27                  |
| Meget forsinket betaling | 2                 | 0              | **45**              |

Forvekslingsmatricen viser resultaterne af et tilfældigt valgt testdatasæt fra øvelsesprocessen. Da disse lukkede fakturaer ikke blev brugt til at træne modellen, er de gode testsager for modellen. Desuden kan modellens ydeevne også ses, fordi fakturaens faktiske status er kendt.

Det første, du skal søge efter, er den mest almindelige værdi. Selvom denne værdi ikke kan justeres perfekt i forhold til det generelle datasæt, er det en rimelig tilnærmelse. I dette tilfælde indtræffer **Betaling til tiden** for 92 af de 171 fakturaer, og det er den mest almindelige værdi. Det er derfor en god grundlinje til modellen. Hvis du netop har gættet, at alle fakturaer ville være til tiden, er det korrekt i 92 ud af 171 fakturaer (dvs. 54 procent af det samlede antal).

Det er vigtigt, at du forstår, hvor afstemt dit datasæt er. Her blev 92 af 171 fakturaer betalt til tiden, 32 blev betalt forsinket, og 47 blev betalt meget for sent. Disse værdier angiver et datasæt, der er forholdsvis afstemt, fordi der er ikke-trivielle resultater i de enkelte klassifikationer. En situation, hvor en af tilstandene har meget få resultater, kan være udfordrende for en model til maskinel indlæring.

Modellens nøjagtighed angiver antallet af korrekte forudsigelser for testsættet. Disse rigtige forudsigelser er de værdier, der vises med fed skrift i det foregående eksempel. I dette tilfælde giver værdierne en beregnet nøjagtighed på 67,8 % (= \[71 + 0 + 45\] ÷ 171). Denne værdi repræsenterer en forbedring på 14 procent over det oprindelige gæt på 54 % og er en indikator for modellens kvalitet.

Hvis du ser mere i forvekslingsmatricen, vil du bemærke, at modellen er god til at forudsige betalinger til tiden og meget forsinkede fakturabetalinger. Der er dog ikke noget problem med alle de 32 fakturaer, der faktisk blev betalt sent (men ikke helt sent). Dette medfører, at der kræves yderligere udforskning og forbedring af modellen.

Et tal, der repræsenterer modellens ydeevne, som er bedre end nøjagtighed, som er F1-makroens score. Denne score tager højde for resultaterne af hver klassifikationstilstand (til tiden, sent og meget sent). Her er f. eks. de data, der vises for "F1 Makro"-måleværdien i den foregående illustration.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

I dette tilfælde angiver F1-makroscoren cirka ca. 49,3 procent, at modellen ikke giver effektive forudsigelser på tværs af hver tilstand på trods af et samlet præcisionsresultat, der forekommer rimelig højt.

## <a name="improving-the-model"></a>Forbedring af modellen

Når du har forstået resultatet af din første model bedre, kan det være en god ide at forbedre modellen ved at tilføje eller fjerne funktionskolonner eller ved at filtrere alle dele af det datasæt, der ikke understøtter de nøjagtige forudsigelser. Luk AI Builder, og brug derefter linket **Forbedring af model** i Dynamics 365 Finance til at genstarte AI Builder-processen. Du kan eksperimentere med forskellige egenskaber, uden at det påvirker den udgivne model. Den udgivne model påvirkes kun, når du vælger **Udgiv**. Husk, at der bruges en enkelt model til din forekomst af Dynamics 365 Finance. Du bør derfor gennemgå eventuelle nye modeller omhyggeligt, før du udgiver den.

## <a name="for-more-information"></a>Hvis du vil have flere oplysninger

Du kan finde flere oplysninger om, hvordan du evaluerer forudsigelsesmodeller, [Resultater af maskinel indlæringsmodeller](/confusion-matrix.md)

#### <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger
Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]