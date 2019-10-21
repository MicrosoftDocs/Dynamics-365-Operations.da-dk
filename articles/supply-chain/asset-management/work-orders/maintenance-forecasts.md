---
title: Vedligeholdelsesprognoser
description: I dette emne beskrives vedligeholdelsesprognoser i Styring af aktiver.
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
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024493"
---
# <a name="maintenance-forecasts"></a>Vedligeholdelsesprognoser

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Når du opretter en arbejdsordre, opretter du arbejdsordrejob med relaterede aktiver og vedligeholdelsesjobtyper. Når du vælger en vedligeholdelsesjobtype, der indeholder vedligeholdelsesprognoser, kopieres prognoserne automatisk til arbejdsordren.

Du kan muligvis tilføje eller slette prognoselinjer på en arbejdsordre. Opsætningen af en livscyklustilstand for en arbejdsordre, den relaterede projekttype og stadiereglerne for projekttypen bestemmer, om du kan tilføje eller redigere prognoselinjer. 

1. Klik på **Styring af aktiver** > **Generelt** > **Arbejdsordrer** > **Alle arbejdsordrer** eller **Aktive arbejdsordrer**.

2. Vælg arbejdsordren på listen, og klik på **Prognose**. I **Vedligeholdelsesprognose for arbejdsordre** vises prognoselinjer fra den type af vedligeholdelsesjob, der er valgt på arbejdsordrejobbet.


## <a name="add-hours-forecast-to-a-work-order"></a>Føje timeprognose til en arbejdsordre

1. Vælg det arbejdsordrejob, hvor du vil tilføje en prognose.

2. I oversigtspanelet **Timer** skal du klikke på **Tilføj** for at oprette en ny linje.

3. Vælg en kategori i feltet **Kategori**.

4. Indsæt antal budgetterede timer i feltet **Timer**.

5. Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.


## <a name="add-items-forecast-to-a-work-order"></a>Føje vareprognose til en arbejdsordre

Der er tre måder at tilføje varer i en arbejdsordres vedligeholdelsesprognose: Du kan oprette linjer for varer (reservedele), der ikke er medtaget på listen over reservedele eller aktivstyklisten, du kan vælge reservedele på listen over godkendte reservedele, og du kan vælge varer fra aktivstyklisten.

1. Vælg det arbejdsordrejob, hvor du vil tilføje en prognose.

2. Vælg oversigtspanelet **Varer**.

3. Klik på **Tilføj** for at oprette en ny linje til en reservedel, der ikke findes på listen over reservedele eller aktivstyklisten.

4. Vælg elementet i feltet **Varenummer**.

5. Indsæt antal i feltet **Salgsantal**, og vælg en antalsenhed i feltet **Enhed**.

6. Indsæt kostpris og valuta i de relevante felter, og vælg en **Linjeegenskab**.

7. Hvis du vil ændre listen over de dimensioner, der vises på varelinjerne, skal du klikke på **Inventory** > **Vis dimensioner**, vælge dimensioner og vælge "Ja" på knappen **Gem opsætning**.

8. Hvis du vil føje en godkendt reservedel til vedligeholdelsesprognosen, skal du klikke på **Tilføj reservedele**, vælge reservedelen, redigere relaterede oplysninger, hvis det er nødvendigt, og klikke på **OK**.

9. Hvis du vil føje varer fra aktivstyklisten til prognosen, skal du klikke på **Tilføj styklistevarer**, vælge varen, redigere relaterede oplysninger, hvis det er nødvendigt, og klikke på **OK**.

10. Klik på **Hvor er varen brugt?**, hvis du vil have en oversigt over, hvor i Styring af aktiver varen på den valgte linje bruges i relation til aktiver, typestandarder for vedligeholdelsesjob, reservedele og arbejdsordrer. 



## <a name="add-expense-forecast-to-a-work-order"></a>Føje udgiftsbudget til en arbejdsordre

1. Dette emne forklarer, hvordan du kan føje et udgiftsbudget til en arbejdsordre. I venstre side af formen skal du vælge det arbejdsordrejob, hvor du vil tilføje et budget.

2. Vælg oversigtspanelet **Udgift**.

3. Klik på **Tilføj** for at oprette en ny linje.

4. Vælg en kategori i feltet **Kategori**.

5. Angiv antallet i feltet **Antal**.

6. Indsæt kostpris, salgsvaluta og salgspris i de relevante felter.

7. Vælg den gebyrtype, der skal bruges på linjen, i feltet **Linjeegenskab**.

>[!NOTE]
>I oversigtspanelet **Vedligeholdelsesprognosetotaler** kan du få vist en oversigt over antallet af linjer, der er oprettet under hver fane, for det valgte arbejdsordrejob og for arbejdsordren. Du kan også se en sum af de budgetterede arbejdstimer for arbejdsordrejobbet og for arbejdsordren.

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automatisk opdatering af prognoser for arbejdsordrer

I Styring af aktiver kan du automatisk opdatere eventuelle ændringer i arbejdsordrebudgetter for timeomkostninger, vareomkostninger og udgifter, der er opdateret i andre moduler. Dette gøres for at sikre, at de seneste kostpriser altid bruges i dine prognoser for arbejdsordrer. Det er også muligt at foretage lignende opdateringer af [budgetter for vedligeholdelsesjobtyper](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Klik på **Styring af aktiver** > **Periodisk** > **Prognose** > **Opdater prognose for arbejdsordre**.

2. I dialogboksen **Opdater prognose for arbejdsordre** kan du tilføje valg for bestemte arbejdsordrer eller arbejdsordrejob, hvis det er nødvendigt. Klik på **Filter** for at foretage disse valg.

3. I oversigtspanelet **Kør i baggrunden** kan du konfigurere automatisk opdatering som et batchjob efter behov.

4. Klik på **OK** for at starte prognoseopdateringen.


![Figur 2](media/07-work-orders.png)

