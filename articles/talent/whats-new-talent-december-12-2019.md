---
title: Nyheder eller ændringer i Dynamics 365 Talent (10. december 2019)
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528165"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Nyheder eller ændringer i Dynamics 365 Talent (10. december 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2660. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Arbejdsområdet Administration af funktioner

Arbejdsområdet **Administration af funktioner** indeholder en oversigt over de funktioner, der er leveret i hver udgave. Nye funktioner er som standard slået fra. Du kan bruge arbejdsområdet til at aktivere dem og få vist dokumentationen til dem. Du kan finde flere oplysninger om Administration af funktioner under [Oversigt over funktionsstyring](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funktioner vises i forhåndsvisning i mindst 30 dage og typisk 30-60 dage. De vigtigste funktioner er normalt tilgængelige i oktober og april hvert år efter forhåndsvisningsperioden. Så snart du ser nye egenskaber i arbejdsområdet **Administration af funktioner**, kan du slå dem til. Nogle funktioner er muligvis som slået til som standard.
 
På visse tidspunkter er en integreret funktion som standard slået til og kan ikke slås fra (f.eks. arbejdsområdet **Administration af funktioner**).
 
Når en funktion er generelt tilgængelig, kan den slås til eller fra i produktionsmiljøer. Arbejdsområdet **Administration af funktioner** angiver, hvornår en visningsfunktion skal være obligatorisk. Denne dato er som regel den 1. oktober eller 1. april for at tilpasse det med de halvårlige frigivelsesplaner. Du kan ikke slå de obligatoriske funktioner fra. Indtil den bliver obligatorisk, kan du slå en funktion til og fra i alle miljøer.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Strømlinet arbejderformel er flyttet til arbejdsområdet Funktionsstyring (390583)

Med denne ændring kan den strømlinede arbejderformel nu aktiveres i arbejdsområdet **Funktionsstyring**. Denne funktion er blevet flyttet fra formen **Systemparametre** i **Systemadministration**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Forhindre, at HcmWorkerPayrollInfo-poster skrives uden en arbejderværdi (394526)

Med denne udgivelse oprettes der ikke længere **HcmWorkerPayrollInfo**-poster under uden arbejderreference i dette scenario. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Meddelelsesloggen, der er knyttet til handlingen, udfyldes ikke, når handlingen ikke fuldføres (374007)

Denne udgivelse indeholder en ændring, der udfylder handlingsmeddelelsesloggen, når en handling mislykkes i bestemte scenarier. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Oprettelse af batchjob til Common Data Service-integration (388030)

Med denne ændring oprettes batchjob til Common Data Service-integration, når tjenesten er aktiveret.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Yderligere pluklisteværdier til brugerdefinerede felter afspejles ikke i Common Data Service, når der klikkes på anvend på brugerdefinerede formularfelter (379599)

Med denne ændring synkroniseres nye pluklisteværdier, der indtastes i Talent, nu med Common Data Service, når du anvender dine ændringer.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Opdater til Common Data Service for at Forlad banktransaktionsenhed bliver til en indsætning på Talent-side (352938)

Denne ændring korrigerer et problem, hvor en opdatering til en Forlad banktransaktion opretter en ny post i Talent.

## <a name="in-preview"></a>Som eksempel

Prøveversionsfunktioner er kun tilgængelige i **Sandkasse**-miljøer.

### <a name="print-performance-reviews"></a>Udskiv performancegennemgange

Se [Udskrive performancegennemgange](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019 frigivelsesbølge 2-plan.



[!INCLUDE[footer-include](../includes/footer-banner.md)]