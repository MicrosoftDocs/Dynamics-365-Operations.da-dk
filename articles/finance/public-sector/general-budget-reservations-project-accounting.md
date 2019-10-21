---
title: Projektregnskab med generelle budgetreservationer
description: Dette emne indeholder oplysninger om projektregnskab, der bruger generelle budgetreservationer til den offentlige sektor.
author: AlexRenney
manager: AnnBe
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetReservation_PSN
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3f376de75951e9468ce95a24e9393d9bdca66672
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183510"
---
# <a name="project-accounting-with-general-budget-reservations"></a>Projektregnskab med generelle budgetreservationer

[!include [banner](../includes/banner.md)]

Hvis din organisation bruger projektregnskab, kan du medtage referencer til dit projekt i generelle budgetreservationer. Disse referencer kan påvirke budgettering, bindende omkostninger og reservationer og forbrug af finansieringskilder.

Nogle udgifter er planlagt til at blive faktureres til projekter. Når du opretter en generel budgetreservation, kan du angive det , at det projekt og den projektkategori, som et planlagt indkøb er til. Du kan også angive andre projektrelaterede oplysninger, f.eks. den forventede salgspris. (For enheder i den offentlige sektor er den forventede salgspris typisk kostprisen). Alle disse oplysninger findes i de indkøbsdokumenter, der genereres for projekter senere.

Hvis den generelle budgetreservation indeholder en projektfordeling, skal den købsordre, indkøbsrekvisition eller en kreditorfaktura, der henviser til reservationen, omfatte projektfordelingen og alle projektoplysninger. Disse oplysninger kopieres automatisk til kildedokumentet fra den generelle budgetreservation.

## <a name="turn-on-tracking-of-committed-costs-for-general-budget-reservations"></a>Aktivere sporing af bindende omkostninger for generelle budgetreservationer

Bindende projektomkostninger oprettes, når købsdokumenterne er godkendt, bekræftet eller bogført. Omkostningerne repræsenterer beløb, der skal bruges på et projekt. Projektledere kan få vist ventende omkostninger for et projekt for at spore nøjagtige oplysninger om deres projektomkostninger.

1. Gå til **Projektstyring og regnskab \> Opsætning \> Parametre for projektstyring og regnskab**.
2. Under fanen **Omkostningsstyring** i oversigtspanelet **Udgiftsforpligtelser** skal du vælge **Ja** i indstillingen **Generel budgetreservation**.

    - Indstillingerne **Indkøbsrekvisition**, **Indkøbsordre** og **Kreditorfaktura** bliver automatisk indstillet til **Ja**.
    - Når den generelle budgetreservation er bogført, tæller den med i projektets bindende omkostninger.

## <a name="specify-project-information-in-a-general-budget-reservation"></a>Angive projektoplysninger i en generel budgetreservation

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Opret en generel budgetreservation.
3. Tilføj et projekt-id og en projektkategori for hver relevant reservationslinje i oversigtspanelet **Generelle budgetreservationslinjer**. Oplysninger fra projektet kopieres automatisk til reservationen.
4. Valgfrit: Hvis du vil have vist projektdetaljerne, skal du vælge fanen **Projekt** i oversigtspanelet **Linjedetaljer**.

## <a name="view-project-committed-costs-for-a-general-budget-reservation"></a>Få vist bindende projektomkostninger for en generel budgetreservation

Når du bogfører en generel budgetreservation for et projekt, oprettes der en bindende omkostning for reservationsbeløbet i forhold til projektet. Den bindende omkostning repræsenterer det samlede beløb for fordelingerne til det pågældende projekt.

1. Gå til **Budgettering \> Generelle budgetreservationer**.
2. Åbn den ønskede bogførte generelle budgetreservation, og vælg en reservationslinje.
3. Vælg **Bindende omkostninger**. Siden **Bindende omkostninger** åbnes og viser de bindende omkostninger, der er relateret til den valgte linje.

    Bindende omkostninger for generelle budgetreservationer er baseret på beløb, uanset om den bindende omkostning indeholder et bestemt antal og kostpris. Antallet for bindende omkostninger vil altid være 1.
