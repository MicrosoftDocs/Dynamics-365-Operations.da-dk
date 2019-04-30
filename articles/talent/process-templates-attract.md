---
title: Oprette en processkabelon i Attract
description: Dette emne indeholder oplysninger om, hvordan du opretter en processkabelon i Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: ca04bb623b9ddd19f02efbf99289461a78ddd7f1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/19/2019
ms.locfileid: "856617"
---
# <a name="create-a-process-template-in-attract"></a>Oprette en processkabelon i Attract

[!include [banner](includes/banner.md)]

En *ansættelsesprocesskabelon* indeholder alle de aktiviteter, der skal medtages som en del af ansættelsesprocessen for et job. I dette emne beskrives elementerne i en processkabelon i Microsoft Dynamics 365 for Talent: Attract. Det beskrives også, hvordan du opretter en skabelon.

> [!NOTE]
> Skabelonoprettelse er en del af tilføjelsesprogrammet til omfattende ansættelser i Attract.

## <a name="template-management"></a>Skabelonstyring

Organisationer kan bestemme, om teammedlemmer eller kun administratorer kan oprette processkabeloner i Attract. Du kan konfigurere skabelonstyring ved at gå til **Administration** \> **Skabelonstyring**. Hvis teammedlemmer opretter deres egne skabeloner, skal du aktivere skabelonstyring. Hvis du ikke aktiverer skabelonstyring, kan kun administratorer oprette skabeloner.

## <a name="default-template"></a>Standardskabelon

Kun administratorer kan indstille standardskabelonen. Standardskabelonen bruges, hvis der ikke er markeret en skabelon, når der oprettes et job. Du kan indstille standardskabelonen ved at gå til **Administration** \> **Skabelonstyring**. På kortet for den skabelon, der skal være standardskabelon, skal du vælge ellipseknappen (**...**) og derefter vælge **Angiv som standard**.

## <a name="create-a-process-template"></a>Oprette en processkabelon

Administratorer, rekrutteringsmedarbejdere og ansættelsesansvarlige kan oprette processkabelon. En processkabelon består af *stadier* og *aktiviteter*. Stadier grupperer en eller flere aktiviteter sammen. Hver processkabelon har som standard jobkandidat-, ansøgnings- og tilbudsaktiviteter. De stadier, der indeholder disse aktiviteter kan omdøbes. Du kan tilføje flere stadier ved at vælge **+ Nyt stadie**. Du kan føje aktiviteter til et stadie ved enten at trække dem til det relevante stadie eller ved at dobbeltklikke på dem på aktivitetslisten.

> [!NOTE]
> Stadienavne er synlige for kandidater på siden **Ansøgningsstatus**. Du bør overveje dette, når du vælger navne til stadier.

Du kan få mere at vide om aktiviteter i [Ansættelsesprocesaktiviteter i Attract](./activities-attract.md).

Følg disse trin for at oprette en ansættelsesprocesskabelon.

1. Gå til **Skabeloner**.
2. Vælg **Ny**.
3. I feltet **Skabelonnavn** skal du angive et navn til skabelonen og derefter vælge **Opret**.
4. På listen **Vælg godkendelsesprocessen** skal du vælge **Standard** for at kræve godkendelse af et job.
5. Vælg at aktivere eller deaktivere jobkandidater.
6. Valgfrit: Tilføj eller fjern stadier.

    - For at tilføje et stadie skal du vælge **+ Nyt stadie**.
    - Hvis du vil fjerne et stadie, skal du placere markøren over stadiet og derefter vælge den papirkurvsknap, der vises.

        > [!NOTE]
        > Stadierne Jobkandidat, Ansøgning og Tilbud kan ikke fjernes, men de kan omdøbes.

7. Valgfrit: Tilføj eller fjern aktiviteter.

    - Hvis du vil tilføje en aktivitet, skal du trække den fra listen til højre til det relevante stadie. Du kan også dobbeltklikke på aktiviteten og derefter vælge det stadie, den skal føjes til.
    - Hvis du vil fjerne en aktivitet, skal du udvide den og derefter vælge papirkurvsknappen i overskriften til aktiviteten.

8. Vælg **Gem**.
