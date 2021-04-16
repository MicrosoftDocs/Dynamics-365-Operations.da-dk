---
title: Foretage fejlfinding af indgående lagerstedsoperationer
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med indgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828220"
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

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>Når jeg registrerer indgående ordrer, modtager jeg følgende fejlmeddelelse: "Antallet er ikke gyldigt".

### <a name="issue-description"></a>Problembeskrivelse

Hvis feltet **Politik for nummerpladegruppering** er indstillet til *Brugerdefineret* for et menupunkt på en mobilenhed, som bruges til at registrere indgående ordrer, får du vist en fejlmeddelelse ("Antallet er ikke gyldigt"), og du kan ikke fuldføre registreringen.

### <a name="issue-cause"></a>Problemårsag

Når *Brugerdefineret* bruges som nummerpladegrupperingspolitik, opdeles den indgående lagerbeholdning i separate nummerplader, som angivet af enhedsseriegruppen. Hvis der bruges batch- eller serienumre til at spore den vare, der modtages, skal antallene for hver batch eller serie angives pr. nummerplade, der registreres. Hvis det antal, der er angivet for nummerplade, overstiger det antal, der stadig skal modtages for de aktuelle dimensioner, får du vist fejlmeddelelsen.

### <a name="issue-resolution"></a>Problemløsning

Når du registrerer en vare ved hjælp af menupunktet på en mobilenhed, hvor feltet **Politik for nummerpladegruppering** er angivet til *Brugerdefineret*, kan systemet kræve, at du bekræfter eller angiver nummerpladenumre, batchnumre eller serienumre.

På siden til bekræftelse af nummerplade vil systemet vise det antal, der er tildelt den aktuelle nummerplade. På batch- eller seriebekræftelsessiderne viser systemet det antal, der stadig skal modtages på den aktuelle nummerplade. Der findes også et felt, hvor du kan angive det antal, der skal registreres for denne kombination af nummerplade og batch- eller serienummer. Hvis det er tilfældet, skal du sikre dig, at det antal, der registreres for nummerpladen, ikke overstiger det antal, der stadig skal modtages.

Hvis der genereres for mange nummerplader ved indgående ordreregistrering, kan værdien i feltet **Politik for nummerpladegruppering** ændres til *Nummerpladegruppering*, og derfor kan der tildeles en ny enhedsseriegruppe til varen, eller indstillingen af **Nummerpladegruppering** for enhedsseriegruppen kan deaktiveres.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
