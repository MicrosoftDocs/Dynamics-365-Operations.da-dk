---
title: Pluklinjegruppering
description: Dette emne indeholder en oversigt over pluklinjegruppering.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4b9cd7dac680c1691fb4c6dd4078f109254be784
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215587"
---
# <a name="pick-line-grouping"></a>Pluklinjegruppering

[!include [banner](../includes/banner.md)]

I pluklinjegruppering kan flere arbejdslinjer, der har samme vare og lokation, kombineres til et enkelt pluk, der præsenteres for brugeren på en mobilenhed. Derfor kan lagermedarbejderne modtage de mest mulige effektive instruktioner, men den påkrævede adskillelse af arbejdslinjer i systemet bibeholdes ligeså (f.eks. for forskellige containere og ordrer).

## <a name="set-up-pick-line-grouping"></a>Opsætning af pluklinjegruppering

### <a name="create-a-mobile-device-menu-item"></a>Oprette et menupunkt på en mobilenhed

1. Gå til **Lokationsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenupunkter**, og opret et nyt menupunkt kaldet **Salgsgruppelinjepluk – brugerstyret**.
2. Under **Mobilenhedsmenupunkt** angives følgende værdier:

    - I feltet **Navn for menupunkt** indtastes **Salgspluk - gruppelinje**.
    - I feltet **Titel** indtastes **Salgspluk - gruppelinje**.
    - Vælg **Arbejde** i feltet **Tilstand**.
    - Angiv indstillingen **Brug eksisterende arbejde** til **Ja**.

3. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - I feltet **Styret af** skal du vælge **Brugerstyret**.
    - Angiv indstillingen **Generer nummerplade** til **Ja**.
    - Angiv indstillingen **Gruppepluk** til **Ja**.

4. I oversigtspanelet **Arbejdsklasser** skal du følge disse trin for at konfigurere de gyldige arbejdsklasser for menupunktet mobilenhed:

    1. Vælg **Ny**.
    2. I feltet **Arbejdsklasse-ID** skal du vælge **Salg** eller **SO pluk**, afhængigt af det lagersted, du vil bruge.
    3. I feltet **Arbejdsordretype** skal du vælge **Salgsordrer**.

### <a name="set-up-a-mobile-device-menu"></a>Opsætning af en mobilenhedsmenu

1. Gå til **Lagerstedsstyring \> Opsætning \> Mobilenhed \> Mobilenhedsmenu**. 
1. Tilføj det menupunkt, du lige har oprettet, til den ønskede menu.

### <a name="set-up-a-work-template"></a>Opsætning af en arbejdsskabelon

1. Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.
1. Find den arbejdsskabelon, der skal bruges med denne funktion. I dette eksempel skal du vælge Contoso-standardarbejdsskabelonen **51 pluk til stadie**.
1. Vælg **Rediger forespørgsel** i menuen.
1. Under fanen **Sortering** skal du vælge **Tilføj** og derefter angive følgende værdier:

    - Vælg **Midlertidige arbejdstransaktioner** i feltet **Tabel**.
    - Vælg **Midlertidige arbejdstransaktioner** i feltet **Afledt tabel**.
    - I feltet **Felt** skal du vælge **Varenummer**.
    - I feltet **Søgeretning** skal du vælge **Stigende**.

> [!NOTE]
> Hvis funktionen pluklinjegruppering skal fungere, skal arbejdslinjerne sorteres efter vare-ID. Hvis de linjer, der har de samme elementer, ikke sorteres en efter en, grupperes de ikke.

## <a name="example"></a>Eksempel

### <a name="create-picking-work"></a>Opret plukarbejde

Før du kan konfigurere pluklinjegruppering, skal du oprette noget kvalificeret udgående arbejde.

1. Gå til **Sales and MArketing \> Salgsordrer \> Alle salgsordrer**.
2. Vælg **Ny** for at oprette en ny salgsordre. 
3. Vælg en kunde i feltet **Kundekonto**. 
4. I oversigtspanelet **Generelt** skal du i feltet **Lagersted** vælge **51**. Vælg derefter **OK**.
5. Tilføj følgende seks linjer under **Salgsordrelinjer**:

    - **Linje 1:** I feltet **Varenummer** skal du vælge **M9200**. Angiv **3** i feltet **Antal**.
    - **Linje 2:** I feltet **Varenummer** skal du vælge **M9201**. Angiv **3** i feltet **Antal**. 
    - **Linje 3:** I feltet **Varenummer** skal du vælge **M9202**. Angiv **2** i feltet **Antal**. 
    - **Linje 4:** I feltet **Varenummer** skal du vælge **M9200**. Angiv **1** i feltet **Antal**. 
    - **Linje 5:** I feltet **Varenummer** skal du vælge **M9200**. Angiv **3** i feltet **Antal**.
    - **Linje 6:** I feltet **Varenummer** skal du vælge **M9202**. Angiv **7** i feltet **Antal**. 

    Her er en oversigt over de samlede mængder af hver vare:

    - **Vare M9200:** 7 hver
    - **Vare M9201:** 3 hver
    - **Vare M9202:** 9 hver

6. Før du frigiver ordrerne til lageret, skal du sørge for, at plukstederne har tilstrækkelig lagerbeholdning af alle varerne på alle ordrerne. Gennemse indstillingen **Lokationsvejledning** for at bestemme, hvilke pluksteder der skal bruges til salgsordrepluk.
7. Reserver lageret, og frigør det til lagerstedet. Der oprettes et arbejds-ID med seks linjer. Linjerne sorteres efter varenummer.

### <a name="run-the-mobile-device-flow"></a>Kør mobilenhedsprocessen

1. På mobilenheden skal du vælge den menu, der indeholder det nye mobilenhedsmenupunkt.
1. Vælg menupunktet **Salgspluk – gruppelinje**, og påbegynd plukningen.

    Når du har valgt menuen og indtastet arbejds-ID'et, får du vist trinnet pluk, hvor alle pluklinjer for vare M9200 grupperes. Du modtager en instruktion om at plukke 7 hver af vare M9200.

1. Bekræft plukningstrinnet. 
1. Gå til klientens skærm for det igangværende arbejde, og læg mærke til, at alle tre pluklinjer for vare M9200 blev lukket samtidigt.

    Arbejdslinje 4 præsenteres.

1. Bekræft plukningstrinnet.

    Det sidste plukningstrin på mobilenheden aggregerer de sidste to pluklinjer fra arbejdsordren.

1. Fuldfør pluktrinnet for 9 hver af vare M9202.
1. Bekræft læg på lager-trinnet og eventuelle ekstra pluk-/læg på lager-par for at fuldføre arbejdet.

> [!NOTE]
> - Arbejdslinjer kan kun grupperes, hvis de er i rækkefølge.
> - Følgende funktionalitet understøttes ikke:
>
>    - Fastvægtvarer. Hvis der er nogen fastvægtvarer på arbejdet, får du vist en fejlmeddelelse, før du begynder at plukke.
>    - Stykplukning
>    - Arbejdslinjer, der har uafsluttede genopfyldningsarbejde.
>    - Overplukning.
