---
title: Intern behovsplanlægning
description: Denne artikel forklarer intern behovsplanlægning
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4993f981b268127af7c9259aa0e73a8e4a75015a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851443"
---
# <a name="intercompany-master-scheduling"></a>Intern behovsplanlægning

[!include [banner](../../includes/banner.md)]

Intern behovsplanlægning består i at beregne behov og generere interne ordreforslag på tværs af flere interne firmaer. Den interne behovsplanlægning foretages i overensstemmelse med det antal gentagelser, du angiver. Hvis du vil aktivere Microsoft Dynamics 365 Supply Chain Management til at foretage intern behovsplanlægning, skal du oprette behovsplanlægning for alle interne firmaer. Dette indebærer flere gentagelser, hvor Microsoft Dynamics 365 Supply Chain Management automatisk opretter en intern indkøbsordre, hvilket fører til automatisk oprettelse af en intern salgsordre, hvilket igen fører til nye behov.

Du kan oprette den interne behovsplan og den interne behovsplanlægning i parametrene **Behovsplanlægning** i alle interne firmaer.

Hvis du vil fordele behovet ud på hele kæden af interne firmaer, skal du angive parametre for at sikre, at indkøbsordreforslagene autoriseres automatisk, dvs., at ordrerne ikke kan ændres, hvad angår tid og antal. Opret et **tidsgitter for autorisation** for disponeringsgruppen eller for **tidsgitter for autorisation** i behovsplanen. Hvis der ikke oprettes nogen **tidsgitter for autorisation**, kan der ikke blive oprettet interne indkøbsordrer automatisk. Det er kun første kørsel af behovsplanlægningen, der resulterer i ordreforslag. Men da der ikke oprettes en intern indkøbsordre, oprettes der ikke en intern salgsordre, og der oprettes derfor ikke flere interne indkøbsordrer osv.

Når du starter den interne behovsplanlægning, foretager Microsoft Dynamics 365 Supply Chain Management først én behovsplanlægning for hvert interne firma og derefter én behovsplanlægning til for hvert interne firma osv., indtil det angivne antal gentagelser er nået. Der kan maksimalt angives 30 gentagelser, men jo flere gentagelser, du vælger, desto længere tager planlægningsopgaverne.

a behovsplanlægningen i firmaerne styres af den interne planlagte rækkefølge, der er den rækkefølge, som programmet prioriterer behovsplanlægninger mellem hvert internt firma i, kan du starte den interne behovsplanlægningen fra ethvert af de interne firmaer. Da rækkefølgen for den interne planlægning bestemmer den rækkefølge, som behovsplanlægningen udføres i i firmaerne, er det ikke vigtigt, hvor den interne behovsplanlægning startes. Det aktuelle firma behandles sidste i hver gentagelse.

> [!NOTE]
> Den bedste fremgangsmåde er at tillade den interne behovsplanlægning at blive startet fra ét Microsoft Dynamics 365 Supply Chain Management-firma.

På siden **Intern behovsplanlægning** kan du starte en behovsplanlægningssekvens, der kører en behovsplanlægning første gang med metoden til opdatering af den behovsberegning, som du har valgt til den første gentagelse for alle interne firmaer. De efterfølgende gentagelser bruger den sekundære metode, som du vælger for den næste gentagelse, og denne metode anvendes, indtil det angivne antal gentagelser er nået.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
