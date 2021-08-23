---
title: Handling for tilbagekald af ordre i POS
description: Dette emne indeholder en beskrivelse af de funktionsegenskaber, der er tilgængelige på forbedrede sider med tilbagekaldsordrer i POS.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 43d6b2e4e5d923b16b02337432fc5259f66c0bf1a8ba1dbf311fb76cb3f085e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737598"
---
# <a name="recall-order-operation-in-pos"></a>Handling for tilbagekald af ordre i POS

[!include [banner](includes/banner.md)]

Handlingen **Tilbagekald af ordre** i Commerce POS indeholder har opdaterede søge- og filtreringsfunktioner for ordren samt ordrespecifikke oplysninger. Denne funktion er tilgængelig i Commerce version 10.0.15 og nyere.

Hvis du vil aktivere denne funktion, skal du deaktivere **Forbedret handling for ordretilbagekald i POS**-funktionen i arbejdsområdet **Funktionsstyring** i Commerce Headquarters. Når du har aktiveret funktionen, bør du overveje at opdatere [skærmlayout](pos-screen-layouts.md) i POS for at udnytte nogle af de ændrede muligheder.

Konfigurationen af handlingsknappen **Tilbagekald ordre** giver organisationer mulighed for at implementere handlingen med en foruddefineret skærm.

![Konfiguration af knapmatrix.](media/recallorderbuttongrid.png)

Der findes følgende skærmindstillinger.
- **Ingen** – Denne indstilling installerer handlingen uden en bestemt visning. Når en bruger åbner handlingen med denne konfiguration, vil de blive bedt om at søge efter og finde ordrer eller vælge fra et foruddefineret ordrefilter.
- **Ordrer, der skal opfyldes** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der skal opfyldes af brugerens aktuelle butik. Disse ordrer er konfigureret til butiksafhentning eller butiksafsendelse, og linjerne i disse ordrer er endnu ikke plukket eller pakket.
- **Ordrer, der skal afhentes** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der er konfigureret til afhentning i brugerens aktuelle butik.
- **Ordrer, der skal leveres** – Når en bruger starter handlingen, køres der automatisk en forespørgsel for at søge efter og få vist en liste over ordrer, der er konfigureret til levering fra brugerens aktuelle butik.

Når du starter handlingen **Tilbagekald ordre** fra POS, hvis visningen er konfigureret til **Ingen**, kan brugeren søge efter og hente ordrer på en af følgende måder.
- Scan ordrestregkoder. Dette søger efter match i felter med ordrenummer, kanalreference og kvitterings-id.
- Vælg ikonet **Søg efter ordrer** eller **Søg og filtrer** på applinjen for at bruge filtreringsmekanismen til at finde ordrer, der opfylder filterkriterierne.
- Vælg mellem et foruddefineret filter fra rullemenuen **Vis ordrer** (ordrer, der skal opfyldes, ordrer, der skal afhentes, eller ordrer, der skal leveres).

![RecallOrderMainMenu.](media/recallordermain.png)

Når søgekriterierne er anvendt, vises der en liste over tilsvarende salgsordrer i programmet. Det er vigtigt at bemærke, at når du bruger søge-/filterindstillingerne, behøver de hentede ordrer ikke at være ordrer, der er knyttet til brugerens aktuelle butik. Denne søgeproces henter og viser alle kundeordre, der svarer til søgekriterierne, også selvom ordren blev oprettet eller angivet til at blive opfyldt af en anden butik/kanal eller lagerstedslokation.

![RecallOrderDetail.](media/orderrecalldetail.png)

En bruger kan vælge en ordre på listen for at få vist flere detaljer. I panelet med oplysninger i højre side af skærmen vises der oplysninger om den valgte ordre, herunder ordrelinjedetaljer, leveringsdetaljer og oplysninger om opfyldning.

Fra applinjen kan en bruger vælge en operation. Afhængigt af status for ordren er det ikke sikkert, at bestemte handlinger er aktiveret.

- **Retur** – starter processen til oprettelse af en returnering for et eller flere af de fakturerede produkter på den valgte kundeordre.

- **Annuller** – Udsted en fuld annullering af den valgte salgsordre. Denne indstilling er ikke tilgængelig for ordrer, der er startet via en callcenter-kanal og kan ikke bruges til delvist at annullere en ordre.

- **Opfyld** – Overfører brugeren til siden med ordreopfyldning, som er filtreret for den valgte ordre. Det er kun de ordrelinjer, der er åbne for opfyldelse af brugerens butik for den valgte ordre, der vises.

- **Rediger** – Giver brugerne mulighed for at foretage ændringer i den valgte kundeordre. Ordrerne kan kun redigeres i [bestemte scenarier](customer-orders-overview.md#edit-an-existing-customer-order).

- **Afhentning** – Denne indstilling er tilgængelig, hvis der er angivet en eller flere linjer til afhentning af ordren i brugerens aktuelle butik. Denne handling starter afhentningsflowet, hvilket giver brugeren mulighed for at vælge de produkter, der skal afhentes, og opretter salgsposteringen for afhentning.

## <a name="add-notifications-to-the-recall-order-operation"></a>Føje beskeder til handlingen for tilbagekaldsordre

I version 10.0.18 og senere kan du konfigurere POS-beskeder og live tile-påmindelser for handlingen til **Tilbagekaldelse af ordre**, hvis det ønskes. Yderligere oplysninger finder du i [Vis ordrebeskeder i POS](notifications-pos.md).  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
