---
title: Vurderingsprofiler
description: Dette emne beskriver, hvordan du konfigurerer data til vurderingsprofiler.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973954"
---
# <a name="rating-profiles"></a>Vurderingsprofiler

En vurderingsprofil ligner en logistikkontrakt (men ikke en juridisk kontrakt). Den anvendes til at bestemme transporttariffer for laster. 

Hver vurderingsprofil er entydig for en fragtmand. I profilen knytter du fragtmanden til en satsmaster. Satsmasteren definerer tildelingen af satsgrundlaget og selve satsgrundlaget. Satsgrundlaget bestemmer satsen for fragtmanden.

Du kan konfigurere en vurderingsprofil ved hjælp af en generisk side, der indeholder en oversigt over alle eksisterende vurderingsprofiler. Du kan også angive en vurderingsprofil direkte fra fragtmanden. I begge tilfælde er de oplysninger, du konfigurerer for vurderingsprofilen, de samme.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Oprette eller redigere en vurderingsprofil på siden Vurderingsprofiler

På siden **Vurderingsprofiler** kan du gennemse alle tilgængelige vurderingsprofiler. Du kan også redigere eksisterende profiler og oprette nye profiler.

1. Gå til **Transportstyring \> Opsætning \> Vurdering \> Vurderingsprofil**.
1. Vælg **Ny** i handlingsruden for at tilføje en ny vurderingsprofil eller **Rediger** for at redigere en eksisterende profil.
1. Angiv følgende felter i rækken for den nye eller eksisterende vurderingsprofil:

    - **Vurderingsprofil** – Angiv et entydigt id for vurderingsprofilen.
    - **Navn** – Angiv et sigende navn til vurderingsprofilen.
    - **Fragtmand** – Vælg en fragtmand. Den vurderingsprofil, du konfigurerer, vil også blive vist på siden **Fragtmænd** for den valgte fragtmand.
    - **Lokation** og **Lagersted** – Vælg en lokation og et lagersted.
    - **Satsprogram** – Vælg satsprogrammet for vurderingsprofilen.
    - **Satsmaster** – Vælg satsmasteren for vurderingsprofilen. Du kan bruge satsmasteren til at definere en satsgrundlagstype og et satsgrundlag. Du kan finde flere oplysninger i [Konfigurere satsmaster](set-up-rate-masters.md).
    - **Program til transittid** – Vælg programmet til transittid for vurderingsprofilen.
    - **Brændstofindeks** – Vælg fragtmandens brændstofindeks for vurderingsprofilen.
    - **Gældende startdato og -klokkeslæt** og **Gældende slutdato og -klokkeslæt** – Definer den periode, hvor vurderingsprofilen skal være aktiv.

1. Vælg **Gem** i handlingsruden.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Oprette en vurderingsprofil direkte på siden Fragtmænd

1. Gå til **Transportstyring \> Opsætning \> Fragtmænd \> Fragtmænd**.
1. Vælg en fragtmand på listen.
1. I oversigtspanelet **Vurderingsprofiler** skal du vælge **Ny** for at oprette en vurderingsprofil.
1. Angiv felterne for den nye vurderingsprofil. Disse felter svarer til felterne på siden **Vurderingsprofiler** som beskrevet i det forrige afsnit i dette emne.

> [!NOTE]
> Profiler, der oprettes på siden **Fragtmænd**, vises også på siden **Vurderingsprofiler**.
