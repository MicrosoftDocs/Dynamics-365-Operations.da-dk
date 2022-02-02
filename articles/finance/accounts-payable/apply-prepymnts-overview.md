---
title: Anvende forudbetalinger automatisk for kreditorfakturaer
description: Dette emne beskriver muligheden for automatisk anvendelse af forudbetalinger på kreditorfakturaer.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5b07c1d4c2189184b2ad29d46ec2aef0ee03c1c0
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985356"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Anvende automatisk på kreditorfakturaer

[!include [banner](../includes/banner.md)]

Dette emne beskriver muligheden for automatisk anvendelse af forudbetalinger på kreditorfakturaer. Der kan oprettes en forudbetaling for en indkøbsordre som del af en købsaftale. Når en kreditorfaktura er modtaget, kan forudbetalingen bruges til at udligne kreditor fra kreditorfakturaen. Den nye funktion gør det muligt for systemet automatisk at bruge indkøbsordrenumre på en kreditorfaktura til at søge efter tilsvarende forudbetalinger, når kreditorfakturaen importeres.

Hvis der findes forudbetalinger, som kan anvendes, føjes der linjer til de eksisterende fakturalinjer for at anvende forudbetalingerne. Forudbetalingslinjerne tages aldrig i betragtning under processen til fakturasammenholdelse.

Følgende punkter beskriver, hvordan forudbetalinger anvendes, når forskellige indkøbsprocesser følges:

- **Én kreditorfaktura pr. indkøbsordre** – Forudbetalingen på indkøbsordren anvendes på kreditorfakturaen.
- **Én kreditorfaktura for flere indkøbsordrer** – Forudbetalingerne på alle indkøbsordrer anvendes på kreditorfakturaen.
- **Flere kreditorfakturaer pr. indkøbsordre** – Forudbetalingen på indkøbsordren anvendes på den kreditorfaktura, der importeres først. Hvis forudbetalingsbeløbet overstiger fakturabeløbet, mislykkes forudbetalingsanvendelsen, og du skal anvende forudbetalingen manuelt.
- **Flere kreditorfakturaer for flere indkøbsordrer** – Forudbetalingerne på indkøbsordrerne anvendes på den første relevante faktura. Hvis forudbetalingsbeløbet overstiger fakturabeløbet, mislykkes forudbetalingsanvendelsen, og du skal anvende forudbetalingerne manuelt. Hvis der er forudbetalinger tilbage, efter at forudbetalinger er anvendt på den første faktura, kan de anvendes på de efterfølgende fakturaer.

Hvis systemet forsøger at anvende en forudbetaling, men anvendelsen mislykkes, afhænger funktionaliteten af indstillingen af **Bloker den opfølgende automatiseringsproces i tilfælde af applikationsfejl ved forudbetaling**:

- **Ja** – Fejlmeddelelsen "Automatisk anvendelse af forudbetaling: Mislykket" tilføjes i automatiseringshistorikken, og fakturaen vises stadig på listen over ventende kreditorfakturaer. Fakturaen forbliver spærret, indtil du anvender forudbetalingen manuelt.

    Hvis du vil anvende forudbetalinger manuelt, skal du gå til den ventende kreditorfaktura. Angiv indstillingen **Medtag i automatisk behandling** for den blokerede faktura til **Nej** på siden **Fakturadetaljer**. Du kan nu anvende forudbetalingen manuelt. Når forudbetalingen er anvendt, skal du angive indstillingen **Medtag i automatisk behandling** tilbage til **Ja**, så fakturaen kan behandles automatisk.

    Du kan også undgå automatisk anvendelse af forudbetalingen ved at angive indstillingen **Medtag i automatisk behandling** til **Nej** og derefter angive den tilbage til **Ja**. Du modtager følgende meddelelse: "Der findes allerede en forudbetaling for indkøbsordren. Vil du ignorere den for den valgte kreditorfaktura?" Vælg **Ja**. Meddelelsen "Applikation af forudbetaling blev tilsidesat manuelt" tilføjes i automatiseringshistorikken, og kreditorfakturaen spærres ikke, når den automatiserede proces køres igen.

- **Nej** – Automatiseringen af opfølgning fortsætter. Du kan stadig anvende forudbetalingen under udligning.
