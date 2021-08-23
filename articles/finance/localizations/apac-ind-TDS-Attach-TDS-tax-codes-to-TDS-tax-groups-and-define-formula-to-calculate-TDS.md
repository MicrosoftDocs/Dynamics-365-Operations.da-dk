---
title: Knytte kildeskattekoder til kildeskattegrupper og definere formlen til beregning af kildeskat
description: Dette emne forklarer, hvordan du kan oprette grupper for kildeskat (TDS – Tax Deducted at Source) og knytte kildeskattekoder til kildeskattegrupper. Hvis du vil beregne kildskat for en kildeskattegruppe, skal du definere formlen for de kildeskattekoder, der er tilknyttet den.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 81aac53cca91a75cde811c314bd6f7039852d32505fe6540921e17f3d1bbc7ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739304"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>Knytte kildeskattekoder til kildeskattegrupper og definere formlen til beregning af kildeskat

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan oprette grupper for kildeskat (TDS – Tax Deducted at Source) og knytte kildeskattekoder til kildeskattegrupper. Hvis du vil beregne kildskat for en kildeskattegruppe, skal du definere formlen for de kildeskattekoder, der er tilknyttet den.

Benyt følgende fremgangsmåde for at konfigurere en kildeskattegruppe, knytte kildeskattekoder til den og definere formlen til beregning af kildeskat.

1. Gå til **Skat \> Indirekte skatter \> A-skat \> Grupper for A-skat**.

    [![Siden Grupper for A-skat.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Vælg **Ny** i handlingsruden for at oprette en gruppe for A-skat til kildeskat, og angiv de nødvendige oplysninger.
3. I feltet **Skattetype** skal du vælge **KIldeskat**.
4. I oversigtspanelet **Opsætning** skal du vælge **Tilføj** for at oprette en ny linje.
5. Vælg kildeskattekoden for kildeskattegruppen i feltet **Kode for A-skat**. Feltet **Navn på A-skat** viser navnet på kildeskattekoden, og feltet **Værdi** viser værdien.
6. Hvis du vil ignorere grænseværdien og den tærskel for fritagelse, der er defineret for den kildeskattekomponent, som er tilknyttet kildeskattekoden i skattetranskationer, skal du markere afkrydsningsfeltet **Ignorer grænseværdi**.
7. Hvis du vil forhindre, at skattegruppen indgår i beregninger for transaktioner, skal du markere afkrydsningsfeltet **Fritaget**.
8. I handlingsruden skal du vælge **Designer** for at åbne formeldesigneren, så du kan definere formlen til beregning af kildeskat for kildeskattegruppen. På siden **Designer** viser fanen **Skatter** de kildeskattekoder, der er valgt for kildeskattegruppen.

    [![Siden Designer.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Vælg **Alt+N** under fanen **Beregning** for at oprette en linje. Feltet **Id** viser det automatisk genererede prioritets-id for skatteberegningen.
10. Vælg den kildeskattekode, du vil definere formlen for, i feltet **Skattekode**. Alle de kildeskattekoder, der er valgt for kildeskattegruppen, kan vælges i dette felt.
11. Vælg grundlaget for beregning af kildeskat i feltet **Skattegrundlag**:

    - **Bruttobeløb** – Beregn skattebeløbet ud fra bruttotransaktionsbeløbet (dvs. fakturabeløbet) ved hjælp af det beregningsudtryk, der er defineret for skattekoden.
    - **Uden bruttobeløb** – Beregn kildeskatten baseret på det beregningsudtryk, der er defineret for skattekoden.

    > [!NOTE]
    > Feltet **Skattegrundlag** kan ikke angives til **Uden bruttobeløb** for kildeskattekoden med et prioritets-id på **1**.

12. Skatteberegningen er baseret på den formel, der er defineret i feltet **Beregningsudtryk** for hver skattekode, der knyttes til kildeskattegruppen. Vælg knappen plustegn (**+**), minustegn (**-**), multiplikationstegn (**\**_) eller divisionstegn (_*/**) for at angive beregningsudtrykket for den valgte kildeskattekode i feltet **Beregningsudtryk**.

    > [!NOTE]
    > Der kan ikke defineres et beregningsudtryk for kildeskattekoden med et prioritets-id på **1**.

13. Hvis du vil definere beregningsudtrykket for kildeskattekoden i feltet **Beregningsudtryk**, skal du tilføje kildeskattekoder, der er tilgængelige under fanen **Skatter**. Hvis du vil tilføje kildeskattekoder i feltet **Beregningsudtryk**, kan du bruge en af følgende metoder:

    - Træk den nødvendige skattekode fra fanen **Skatter** til feltet **Beregningsudtryk**.
    - Dobbeltklik på den krævede skattekode under fanen **Skatter**.
    - Vælg og hold (eller højreklik) den krævede skattekode nede under fanen **Skatter**, og vælg derefter **Tilføj skattekode**.

    > [!NOTE]
    > Indsæt et beregningsudtryk før hver kildeskattekode. De kildeskattekoder, der er føjet til beregningsudtrykket, vises i kantede parenteser (\[...\]).

14. Hvis du vil fjerne det beregningsudtryk, der er defineret for en skattekode i **feltet Beregningsudtryk**, skal du vælge knappen **C**.
15. Hvis du vil slette en post under fanen **Beregning**, skal du vælge **Slet**.
16. Luk siden.
