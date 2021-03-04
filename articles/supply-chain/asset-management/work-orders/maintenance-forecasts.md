---
title: Vedligeholdelsesprognoser
description: I dette emne beskrives vedligeholdelsesprognoser i Styring af aktiver.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2686dd6db032239e2a3aac03f3998cee055302f6
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425078"
---
# <a name="maintenance-forecasts"></a>Vedligeholdelsesbudgetter

[!include [banner](../../includes/banner.md)]



Når du opretter en arbejdsordre, opretter du arbejdsordrejob, der har relaterede aktiver og vedligeholdelsesjobtyper. Når du vælger en vedligeholdelsesjobtype, der indeholder vedligeholdelsesprognoser, kopieres prognoserne automatisk til arbejdsordren.

Du kan muligvis føje prognoselinjer til en arbejdsordre eller slette dem fra en arbejdsordre. Opsætningen af en livscyklustilstand for en arbejdsordre, den relaterede projekttype og stadiereglerne, der er relateret til projekttypen, bestemmer, om du kan tilføje eller redigere prognoselinjer. Du kan finde flere oplysninger om arbejdsordrers livscyklustilstande og relaterede projektstadier i [Budgetter, arbejdsordrer og projekter](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Vælg **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren på listen, og vælg derefter **Budget** i gruppen **Projekt** under fanen **Arbejdsordre** i handlingsruden. På siden **Vedligeholdelsesprognose for arbejdsordre** vises prognoselinjer fra den type af vedligeholdelsesjob, der er valgt på arbejdsordrejobbet.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Føje en timeprognose til en arbejdsordre

1. Vælg det arbejdsordrejob, der skal føjes et budget til, på siden **Vedligeholdelsesprognose for arbejdsordre**.

2. I oversigtspanelet **Timer** skal du vælge **Tilføj** for at oprette en ny linje.

3. Vælg en kategori i feltet **Kategori**.

4. Indsæt antal budgetterede timer i feltet **Timer**.

5. Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.


## <a name="add-an-items-forecast-to-a-work-order"></a>Føje en vareprognose til en arbejdsordre

Du kan føje varer til en vedligeholdelsesprognose for en arbejdsordre på tre måder. Du kan oprette linjer for varer (reservedele), der ikke er medtaget på listen over reservedele eller aktivstyklisten, du kan vælge reservedele på listen over godkendte reservedele, og du kan vælge varer fra aktivstyklisten.

- Vælg det arbejdsordrejob, der skal føjes et budget til, på siden **Vedligeholdelsesprognose for arbejdsordre**.

- I oversigtspanelet **Varer** kan du føje varer til vedligeholdelsesprognosen ved at bruge den relevante metode.

Følg disse trin for at oprette en ny linje til en reservedel, der ikke findes på listen over reservedele eller aktivstyklisten:

1. Vælg **Tilføj**.
2. Vælg varen i feltet **Varenummer**.
3. Angiv antallet i feltet **Salgsantal**.
4. Vælg måleenheden for antallet i feltet **Enhed**.
5. I felterne **Kostpris** og **Valuta** skal du angive relevante værdier.
6. Vælg en linjeegenskab i feltet **Linjeegenskab**.
7. Hvis du vil ændre listen over de dimensioner, der vises på varelinjerne, skal du vælge **Lager** > **Vis dimensioner**, vælge dimensioner og indstille **Gem opsætning** til **Ja**.

Hvis du vil tilføje en reservedel fra en godkendt reservedelsliste, skal du følge disse trin:

1. Vælg **Tilføj reservedele**.
2. Vælg reservedelen, og rediger de relaterede oplysninger efter behov.
3. Vælg **OK**.

Udfør følgende trin for at tilføje en vare fra aktivstyklisten:

1. Vælg **Tilføj styklistevarer**.
2. Vælg varen, og rediger de relaterede oplysninger efter behov.
3. Vælg **OK**.

Hvis du vil have en oversigt over, hvor varen på den valgte linje bruges i relation til aktiver,typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer i Styring af aktiver, skal du vælge **Hvor er varen brugt?**. Yderligere oplysninger om denne oversigt finder du under [Hvor er varen brugt?](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Føje et udgiftsbudget til en arbejdsordre

1. Vælg det arbejdsordrejob, der skal føjes et budget til, på siden **Vedligeholdelsesprognose for arbejdsordre**.

2. I oversigtspanelet **Udgift** skal du vælge **Tilføj** for at oprette en ny linje.

3. Vælg en kategori i feltet **Kategori**.

4. Angiv antallet i feltet **Antal**.

5. Indsæt relevante værdier i felterne **Kostpris**, **Salgsvaluta** og **Salgspris**.

6. Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.

>[!NOTE]
>I oversigtspanelet **Vedligeholdelsesprognosetotaler** vises en oversigt over antallet af linjer, der er oprettet for det valgte arbejdsordrejob og for arbejdsordren, i hvert oversigtspanel. Du kan også se en total af de budgetterede arbejdstimer for arbejdsordrejobbet og arbejdsordren.

I illustrationen herunder vises et eksempel på siden **Vedligeholdelsesprognose for arbejdsordre**.

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automatisk opdatering af prognoser for arbejdsordrer

I Styring af aktiver kan du automatisk opdatere eventuelle ændringer i arbejdsordrebudgetter for timeomkostninger, vareomkostninger og udgifter, der er opdateret i andre moduler i Microsoft Dynamics 365 for Finance and Operations. Dette er med til at sikre, at de seneste kostpriser altid bruges i dine prognoser for arbejdsordrer. Det er også muligt at foretage lignende opdateringer af [budgetter for vedligeholdelsesjobtyper](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Vælg **Styring af aktiver** > **Periodisk** > **Prognose** > **Opdater prognose for arbejdsordre**.

2. I dialogboksen **Opdater prognose for arbejdsordre** i oversigtspanelet **Poster, der skal indgå** kan du tilføje valg for bestemte arbejdsordrer eller arbejdsordrejob efter behov. Klik på **Filter** for at foretage de relevante valg.

3. I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.

4. Vælg **OK** for at starte budgetopdateringen.


I illustrationen herunder vises et eksempel på dialogboksen **Opdater prognose for arbejdsordre**.

![Figur 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]