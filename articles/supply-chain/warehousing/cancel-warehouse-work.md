---
title: Annullere lagerstedsarbejde for undtagelseshåndtering
description: I dette emne beskrives den funktion til annullering af arbejdet, der giver lagerstedets tilsynsførende mulighed for at håndtere blokeret arbejde.
author: omulvad
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6aa073f72a3ece81d945f75b32f906d5846f7ce9
ms.sourcegitcommit: bc9b65b73bf6443581c2869a9ecfd0675f0be566
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2019
ms.locfileid: "2625853"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Annullere lagerstedsarbejde for undtagelseshåndtering

[!include [banner](../includes/banner.md)]

Med funktionen Annuller arbejde i Microsoft Dynamics 365 Supply Chain Management kan administratorbrugeren annullere specifikt lagerstedsarbejde, der er i gang, men som blokeres af systemet eller ikke kan fuldføres på grund af usædvanlige omstændigheder. Denne funktionalitet er et attraktivt og sikkert alternativ til SQL-korrigerende scripts, der reparerer uoverensstemmende data. Mens disse scripts typisk benyttes af IT-fagfolk, kan funktionen Annuller arbejde bruges af brugere i firmaet, der har administratorrettigheder.

Du kan få adgang til funktionen Annuller arbejde via **Lokationsstyring** \> **Periodiske opgaver** \> **Oprydning \> Annuller arbejde**. Angiv arbejds-id'et for det arbejde, du vil annullere, i dialogboksen **Annuller arbejde**, og vælg derefter **OK**.

## <a name="warehouse-work-that-can-be-canceled"></a>Lagerstedsarbejde, der kan annulleres

Under pluk af lagersted kan arbejdere støde på situationer, hvor de har registreret antal som plukket fra en lagerlokation til deres brugerlokation, men de kan ikke registrere Læg på lager-handlingen. Inkonsekvente lagerdata er ofte, men ikke altid, årsagen til, at arbejdet er blokeret.

I modsætning til den almindelige annullerings funktion, der kan åbnes med knappen **Annuller** i arbejdshovedet, kræver funktionen Annuller arbejde ikke, at den sidste fuldførte arbejdslinje er en linje af typen **Læg på lager**. Med andre ord kan funktionen Annuller arbejde køres med annulleringslogik, selvom vareantallet på en arbejdslinje befinder sig på en brugerlokation.

> [!NOTE]
> For arbejde, der skal annulleres af driftsårsager, skal lagerstedsbrugerne fortsætte med at bruge den almindelige annulleringsfunktion på arbejdssiden.

Det er kun arbejde af typen **Salg**, **Flytteafgang**, **Råvarepluk** eller **Genopfyldning**, der kan annulleres ved hjælp af funktionen Annuller arbejde. Annulleringslogik køres ikke for frosset råvareplukarbejde eller arbejde, der kan annulleres ved hjælp af den almindelige annulleringsfunktion (se den foregående bemærkning).

For at fjerne blokeringen af arbejdet annullerer systemet eventuelle resterende arbejdslinjer og reparerer de lagerstedsdata, der er tilknyttet det arbejds-id, som brugeren har angivet. De almindelige lagerhåndteringsoperationer, der omfatter det berørte vareantal, kan derefter genoptages.

Hvis du vil lægge den berørte vare på en bestemt lokation, efter at arbejdet er annulleret, skal brugeren bruge en lagerbevægelse eller antalsregulering på en mobilenhed.