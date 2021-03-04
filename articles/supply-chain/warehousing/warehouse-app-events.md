---
title: Hændelser for lagerapp
description: I dette emne beskrives den hændelsesbehandling i lagerstedsappen, der bruges til at behandle hændelsesmeddelelser i lagerstedsapps som en del af et batchjob.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424489"
---
# <a name="warehouse-app-event-processing"></a>Hændelsesbehandling i lagerstedsapp

[!include [banner](../includes/banner.md)]

Batchjob, der kører i Supply Chain Management, kan bruge data fra en kø til behandling af hændelser, der er udstedt af lagerstedsappen, til at reagere efter behov på de signalerede hændelser. Denne funktion føjer relevante hændelser til køen som svar på bestemte typer handlinger, der udføres af arbejdere, der bruger appen. Hvis du f.eks. bruger funktionen **Opret og behandl overførselsordrer fra lagerstedsappen**, oprettes og opdateres overflytningsordrehovedet og -linjerne automatisk i back-end, når systemet kører batchjobbet **Hændelsesbehandling i lagerstedsapp**.

## <a name="enable-the-process-warehouse-app-events-feature"></a>Aktivere funktionen Hændelsesbehandling i lagerstedsapp

Før du kan bruge denne funktion, skal den aktiveres i dit system. Administratorer kan bruge siden [funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionsstatus og aktivere den, hvis det er nødvendigt. Funktionen Hændelsesbehandling i lagerstedsapp vises som:

- **Modul** – Lokationsstyring
- **Funktionsnavn** - Hændelsesbehandling i lagerstedsapp

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Konfigurere et batchjob, der skal behandle hændelser i lagerstedsapp

### <a name="process-warehouse-app-events"></a>Proces for hændelser for lagerapp

Konfigurere et planlagt batchjob, der skal behandle hændelser i lagerstedsapp for oprettelse af overførselsordrer og linjeopdateringer.

1. Gå til **Lokationsstyring \> Periodiske opgaver \> Hændelsesbehandling i lagerstedsapp**.
1. Dialogboksen Hændelsesbehandling i lagerstedsapp vises. Angiv **Batchbehandling** til **Ja** i oversigtspanelet **Kør i baggrunden**.
1. Vælg **Gentagelse** i oversigtspanelet **Kør i baggrunden**.
1. Dialogboksen **Definer gentagelse** åbnes. Angiv kørselsplanen efter behov for din virksomhed.
1. Klik på **OK** for at vende tilbage til dialogboksen **Hændelsesbehandling i lagerstedsapp**.
1. Vælg **OK** i dialogboksen **Hændelsesbehandling i lagerstedsapp** for at føje batchjobbet til batchkøen.

## <a name="query-warehouse-app-events"></a>Forespørge på hændelser i lagerstedsapp

Du kan få vist hændelseskøen og de hændelsesmeddelelser, der er genereret af lagerstedsappen, ved at gå til **Lokationsstyring \> Forespørgsler og rapporter \> Mobilenhedslogge \> Hændelser i lagerstedsapp**.

## <a name="the-standard-event-queue-process"></a>Standardprocessen for hændelseskøer

Køen for hændelser i lagerstedsapps vil typisk blive brugt sammen med følgende beskrevet flow:

1. Der bliver føjet en hændelse til køen med en hændelsesmeddelelse. Den nye meddelelse har til at begynde med hændelsestilstanden **Ventende**, hvilket betyder, at batchjobbet **Hændelsesbehandling i lagerstedsapp** ikke vil hente og behandle denne meddelelse.
1. Så snart meddelelsestilstanden er opdateret til **Sat i kø**, henter batchjobbet **Hændelsesbehandling i lagerstedsapp** hændelsen og behandler den.
1. Batchjobbet opdaterer hændelsestilstandene til enten **Fuldført** eller **Mislykket**, afhængigt af om den anmodede proces var mulig.
1. Når alle relaterede hændelsesmeddelelser er **Fuldført**, slettes hændelsen fra køen.

 Du kan få vist et detaljeret eksempel under [Oprette en flytteordre fra en lagerstedsapp-proces](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Håndtere hændelsesfejl

Som en del af behandlingen af lagerstedshændelsen vil den anmodede meddelelsesaktivitet muligvis ikke modtage processer fra batchjobbet. Hvis dette er tilfældet, ændres hændelsesmeddelelsen til **Mislykket**. Du kan bruge oplysningerne i **Batchlogfilen** til at se hvorfor og foretage de nødvendige handlinger for at løse eventuelle problemer.

Du kan få vist et detaljeret eksempel under [Oprette en flytteordre fra lagerstedsapp](create-transfer-order-from-warehouse-app.md).

Sådan nulstiller du en mislykket hændelsesmeddelelse i lagerstedsappen:

1. Gå til **Lokationsstyring \> Forespørgsler og rapporter \> Mobilenhedslogge \> Hændelser i lagerstedsapp**.
1. Find og vælg en relevant hændelse, der vises som **Mislykket** i kolonnen **Hændelsestilstand** i oversigtspanelet **Hændelsesmeddelelser i lagerstedsapp**.
1. Vælg **Nulstil** fra værktøjslinjen **Hændelsesmeddelelser i lagerstedsapp**.
1. Fortsæt med at arbejde, indtil alle relevante meddelelser er nulstillet.

Du kan også fjerne en **Mislykket** hændelsesmeddelelse ved hjælp af indstillingen **Slet** på værktøjslinjen **Hændelsesmeddelelser i lagerstedsapp**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]