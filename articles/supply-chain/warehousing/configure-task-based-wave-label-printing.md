---
title: Planlægge bølgeetiketudskrivning under bølgen
description: Denne artikel indeholder en beskrivelse af, hvordan du kan konfigurere og bruge funktionerne til opgavebaseret bølgeetiketudskrivning.
author: perlynne
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ac2bc4cce42bada43334b82301d716414cd6d654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889451"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Planlægge bølgeetiketudskrivning under bølgen

[!include [banner](../../includes/banner.md)]

Brug funktionen *Opgavebaseret bølgeetiketudskrivning* som en del af bølgeprocessen for at øge effektiviteten og for at få systemet til at oprette bølgeetiketter og arbejde i separate opgaver.

Konfigurationsprocessen for udskrivning af bølgeetiketter er avanceret og skal bruge nøjagtige konfigurations- og masterdata. Det er ikke ualmindeligt, at generering af bølgeetiketposter mislykkes, og når det sker, annulleres hele bølgebehandlingen. Funktionen *Opgavebaseret bølgeetiketudskrivning* hjælper dig med at undgå at skulle genoprette arbejde og arbejdslinjer, hver gang en bølgeetiket udskrives forkert.

Når du bruger funktionen *Opgavebaseret bølgeetiketudskrivning*, opretter systemet først arbejde og arbejdslinjer. Derefter oprettes og udskrives der bølgeetiketter. Endelig frigives arbejdet og bølgen til plukning, hvis bølgeetiketterne oprettes korrekt.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Aktivere funktionen Opgavebaseret bølgeetiketudskrivning i funktionsstyring

Hvis du vil bruge de funktioner, der er beskrevet i denne artikel, skal de være aktiverede for systemet. I arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) skal du aktivere funktionerne i følgende rækkefølge:

1. *Udskrivning af bølgeetiket* – Denne funktion kræves for at aktivere metode til behandling af bølgeetiketudskrivning.
1. *Arbejdsblokering for hele organisationen* – Denne funktion kræves til både manuel og automatisk konfiguration af planlagt oprettelse af arbejde. (Fra og med Supply Chain Management version 10.0.21 er denne funktion obligatorisk, så den er som standard aktiveret og kan ikke deaktiveres igen).
1. *Opgavebaseret bølgeetiketudskrivning* – Denne funktion kræves for at opdele udskrivning af bølgeetiketter i et separat transaktionsområde.

## <a name="manually-enable-the-new-wave-step-method"></a>Aktivere den nye metode til bølgetrin manuelt

Du skal først oprette den nye metode til bølgetrin og aktivere den til parallel asynkron opgavebehandling.

1. Gå til **Warehouse Management \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.
1. Vælg **Genopret metode** i handlingsruden. Bemærk, at *waveLabelPrinting* føjes til listen over metoder til behandling af bølger, som du kan bruge i dine forsendelsesbølgeskabeloner.
1. Vælg den post, hvor feltet **Metodenavn** er angivet til *waveLabelPrinting*, og vælg derefter **Opgavekonfiguration** i handlingsruden.
1. Gå til handlingsruden, og vælg **Ny** for at føje en række til gitteret. Angiv følgende felter til den nye række:

    - **Lagersted** – Vælg det lagersted, som du vil bruge til at planlægge behandling af oprettelse af arbejde. (Hvis du bruger demodata til testformål, kan du vælge lagersted *24*).
    - **Maksimalt antal batchopgaver** – Angiv et maksimalt antal batchopgaver. I de fleste tilfælde skal værdien være fra *8* til *16*. Det anbefales dog, at du prøver dig frem for at finde den optimale indstilling for dine scenarier.
    - **Batchgruppe til bølgebehandling** – Vælg en dedikeret batchgruppe til behandling af bølger for at optimere batchkøbehandlingen.

Du kan nu opdatere en eksisterende bølgeskabelon, så den bruger metoden *Bølgeetiketudskrivning* til behandling af bølger. Du kan også oprette en ny bølgeskabelon, der bruger den.

1. Gå til **Warehouse Management \> Konfiguration \> Bølger \> Bølgeskabeloner**.
1. Vælg **Rediger** i handlingsruden.
1. Vælg den bølgeskabelon, der skal opdateres, i listeruden. (Hvis du bruger demodata til testformål, kan du vælge *24 Standard for forsendelse*).
1. Gå til oversigtspanelet **Metoder** i kolonnen **Resterende metoder**, og vælg den række, hvor feltet **Navn** er angivet til *waveLabelPrinting*.
1. Vælg knappen **tilføj** (højre pil) for at flytte den valgte række til kolonnen **Valgte metoder**.
1. I feltet **Kode for bølgetrin** skal du angive en bølgetrinskode, der skal bruges til at knytte bølgeskabelonen til en bølgeetiketskabelon.

## <a name="set-wave-task-processing-threshold-data"></a>Angive tærskeldata for behandling af bølgeopgave

Første gang en bølgeproces køres ved hjælp af opgavebaseret behandling, opretter systemet standardtærskeldata for behandling af bølgeopgaver. Disse data bruges til at styre, om behandling af bølger skal køre asynkront og være opgavebaseret, så bølgeetiketter kan behandles og oprettes parallelt.

Standarddataene bruger først en grænseværdi på *1* for minimumantallet af arbejds-id'er (`MinimumWorkThresholdForLabelPrinting`). Når systemet behandler en bølge, der har mere end ét arbejds-id, vil systemet derfor bruge opgavebaseret behandling af bølgeetiketter i en separat transaktion. Du kan manuelt indsætte eller opdatere disse data i `WHSWaveTaskProcessingThresholdParameters`-tabellen i testmiljøet. Hvis du vil ændre indstillingen i et produktionsmiljø, skal du kontakte Microsoft Support for at anmode om opdateringen.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Ændringer i logikken til behandling af bølger, når der bruges opgavebaseret udskrivning af bølgeetiketter

Hvis behandlingen af en bølgeetiket overskrider grænseværdien for behandling af bølgeopgaver, startes opgavebaseret behandling. I den næste bølgebehandling, der passer til bølgeskabelonen, køres udskrivning af bølgeetiketter i en enkeltstående *ttsbegin*/*ttscommit*-transaktion umiddelbart efter oprettelsen af arbejdet. Hvis der er konfigureret en frigivelse af arbejde (spærringen er fjernet) i bølgeskabelonen, så den kører automatisk, køres den først, når udskrivningsprocessen for bølgeetiketter er fuldført.

Hvis der opstår fejl under generering af en bølgeetiket (hvis for eksempel konvertering af arbejdsmængden til antallet af bølgeetiketter mislykkes, og der opstår fejl), er det kun den relevante transaktion, der mislykkes. Det arbejde, der er oprettet tidligere, forbliver frosset. Benyt følgende fremgangsmåde for at rette fejl og udskrive bølgeetiketterne.

1. Gå til **Lokationsstyring \> Udgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Vælg den relevante bølge i gitteret.
1. I handlingsruden under fanen **Bølge** i gruppen **Udskriv** skal du vælge **Bølgeetiketter**.
1. Følg instruktionerne på skærmen for at sende etiketterne til udskrivning.
1. I gruppen **Bølge** under fanen **Bølge** i handlingsruden skal du vælge **Frigiv** for manuelt at frigive arbejdet for den valgte bølge.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Bølgeetiketudskrivning](configure-wave-label-printing.md)
- [Planlægge oprettelse af arbejde under bølgen](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
