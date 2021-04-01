---
title: Foretage fejlfinding af indgående lagerstedsoperationer
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med indgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250876"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Foretage fejlfinding af indgående lagerstedsoperationer

[!include [banner](../includes/banner.md)]

Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med indgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Jeg får vist følgende fejlmeddelelse: "Kvalitetsordren %1 er blevet genereret. Klyngeprofil blev ikke fundet. Kontrollér din konfiguration."

### <a name="issue-description"></a>Problembeskrivelse

Denne fejlmeddelelse er relateret til en modtagelsesproces, hvor kvalitetsstyring (QMS) er slået til. Afhængigt af konfigurationerne i dit miljø kan yderligere oplysninger om den transaktion, der genererer fejlmeddelelsen, måske løse problemet.

### <a name="issue-resolution"></a>Problemløsning

Først skal du gennemse opsætningen for [klyngepluk](set-up-cluster-picking.md) og kontrollere, at dine klyngeprofiler er konfigureret korrekt. Du kan ikke bruge et menupunkt til klyngepluk i mobilenheden, medmindre der er konfigureret klyngeprofiler. Afhængigt af miljøet skal du muligvis også gennemse andre relaterede konfigurationer.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Modtagelse af blandede id'er fungerer ikke for nogen dispositionskode undtagen Kredit.

### <a name="issue-description"></a>Problembeskrivelse

Når **Handling**-feltet for en dispositionskode er sat til *Kredit* eller *Kasseres*, kan du kun bruge menupunktet [Modtagelse af blandede id'er](mixed-license-plate-receiving.md) til at behandle returvarer.

### <a name="issue-resolution"></a>Problemløsning

Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning. Aktuelt er det kun [dispositionskoder](../service-management/set-up-disposition-codes.md), hvor feltet **Handling** er indstillet til *Kredit* eller *Kasseres*, der understøttes til modtagelse af blandede id'er.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Når jeg kører den periodiske opgave Opdater produktkvitteringer, bekræftes ubekræftede indkøbsordrer.

### <a name="issue-description"></a>Problembeskrivelse

Når du har kørt den periodiske opgave *Opdater produktkvitteringer*, bekræfter systemet automatisk ubekræftede indkøbsordrer, der har lagertransaktionstatus *Registreret*.

### <a name="issue-resolution"></a>Problemløsning

En ny funktion til håndtering af indgående last, *Overtilgang af lastantal*, løser dette problem. Hvis du aktivere denne funktion, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funktioner (i deres viste rækkefølge):

1. Tilknyt lagertransaktioner med belastning for indkøbsordre
1. Overtilgang af lastantal

Du kan finde flere oplysninger under [Bogføre registrerede produktantal i forhold til indkøbsordrer](inbound-load-handling.md#post-registered-quantities).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]