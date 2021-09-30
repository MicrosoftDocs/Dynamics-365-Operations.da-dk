---
title: Globale parametre for mobilenhed
description: Dette emne forklarer, hvordan du konfigurerer indstillinger for mobilenheder på siden Parametre til lokationsstyring.
author: HuberIvan
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-huberivan
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 03c10232d55c99c73e625170797f89f6c77e812b
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505555"
---
# <a name="global-mobile-device-parameters"></a>Globale parametre for mobilenhed

[!include [banner](../includes/banner.md)]

Dette emne forklarer, hvordan du kan konfigurere parametre til global lokationsstyring, der påvirker, hvordan systemet fungerer sammen med mobilenheder.

Du kan finde flere oplysninger om, hvordan du konfigurerer lagerarbejdere, i [Styre lagerarbejdere](manage-warehouse-workers.md). Du kan finde flere oplysninger om id-håndtering på mobilenheder under [Modtagelse af id via mobilappen Warehouse Management](warehousing-mobile-device-app-license-plate-receiving.md). Yderligere oplysninger om processer for cyklusoptælling finder du i [Cyklusoptælling](cycle-counting.md) og [Eksempelscenarier for cyklusoptælling](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Åbne siden Parametre til lokationsstyring

Du kan åbne siden **Parametre til lokationsstyring** ved at gå til **Lokationsstyring \> Konfiguration \> Parametre til lokationsstyring**. Du kan derefter angive de felter, der er relateret til arbejdet på mobilenheden, som beskrevet i næste afsnit af dette emne.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Oversigtspanelet Mobilenhed under fanen Generelt

De globale indstillinger for mobilenheder findes i oversigtspanelet **Mobilenhed** under fanen **Generelt** på siden **Parametre til lokationsstyring**. Følgende felter er tilgængelige.

| Felt | Betegnelse |
|---|---|
| Notetype for mobilenhed | Vælg den type oplysninger, som arbejdere kan se under salgsordrepluk. |
| Grænse for scannet antal | Angiv det maksimale vareantal, som en arbejder kan scanne i løbet af hver session, ved hjælp af et menupunkt i mobilenheden, hvor værdien af **Arbejdsoprettelsesproces** er *Regulering ind*. Dette felt har ingen indflydelse på de scanninger, der udføres med brug af en anden type menupunkt. |
| Brug logføring af mobilenhedssession | Angiv denne indstilling til *Ja*, hvis du vil beholde en log over arbejderens logonhistorik. Du kan få vist logfilen ved at gå til **Arbejdsbrugersessioner \> Forespørgsler og rapporter \> Mobilenhedslogge \> Arbejdsbrugersessioner**. |
| Antal gemte fejl | Angiv det maksimale antal fejlposter, der skal lagres. Du kan få vist fejlloggen ved at gå til **Arbejdsbrugersessioner \> Forespørgsler og rapporter \> Mobilenhedslogge \> Arbejdsbrugersessioner**. |
| Standardlagerstedsoverførselskladde | Vælg den kladde, der skal bruges, når arbejdere bruger en mobilenhed til at flytte produkter fra ét lagersted til et andet. |
| Tillad registrering af indkøbsordrelinje ved ekstern gennemgang | Angiv denne indstilling til *Ja*, hvis arbejderne skal kunne bruge en mobilenhed til at registrere ordrelinjer for indkøbsordrer, der har værdien **Godkendelsesstatus** til *Til eksternt gennemsyn*. Angiv denne indstilling til *Nej* for at forhindre arbejdere i at registrere linjer for indkøbsordrer, der er til eksternt gennemsyn. |
| Aktivér RSAT-support | Feltet aktiverer opgavevalidatoren for mobilappen Warehouse Management, som logfører og validerer hvert af de trin, som appen udfører. Da denne proces kan gøre systemets ydeevne væsentligt langsommere, skal du kun aktivere validatoren under testen. Den skal aldrig aktiveres i et produktionsmiljø. |
