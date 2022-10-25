---
title: Scenariet for aktiv-vedligeholdelse
description: Denne artikel beskriver scenariet til vedligeholdelse af aktiver, hvilket giver dig mulighed for at bruge data til at oprette tællerposter, der sporer brugen af et maskinaktiv.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2d103406118be4385177b678de424df12af69c2e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689394"
---
# <a name="the-asset-maintenance-scenario"></a>Scenariet for aktiv-vedligeholdelse

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

I scenariet til *vedligeholdelse af aktiver* kan du bruge oplysninger til at oprette tællerposter. Tællerposter sporer brugen af et maskinaktiv og bruges som input til at generere vedligeholdelsesplanen for maskinaktiver.

## <a name="video-instructions"></a>Videovejledning

Følgende video viser, hvordan du kan konfigurere og afprøve scenariet til vedligeholdelse af aktiver ved hjælp af [standarddemodata](../../fin-ops-core/fin-ops/get-started/demo-data.md). De resterende afsnit i denne artikel indeholder de samme instruktioner i et tekstbaseret format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Forberede demodata til scenariet til vedligeholdelse af aktiver

Hvis du vil bruge et demosystem til at teste scenariet til *vedligeholdelse af aktiver*, skal du bruge et system, hvor [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret, vælge den juridiske enhed *USMF* (firma) og forberede de yderligere demodata som beskrevet i dette afsnit. Hvis du bruger dine egne sensorer og data, kan du springe dette afsnit over.

I dette afsnit skal du som eksempel konfigurere *AK-101, Air Knife*-aktiv i demodata. Du kan derefter se, hvordan kommende vedligeholdelsesarbejde kan forudsiges ud fra de radiosignaler, der måler det antal timer, som air knife har kørt. Du vil også oprette en vedligeholdelsesplan, hvor luftfarten skal vedligeholdes hver 10.000 timer.

### <a name="set-up-a-sensor-simulator"></a>Oprette en sensorsimulator

Hvis du vil prøve dette scenario uden at bruge en fysisk opsætning, kan du konfigurere en opsætning til generering af de påkrævede signaler. Du kan finde flere oplysninger i [Konfigurere en simuleret sensor til test](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Oprette en aktivtæller til sporing af produktionstimer

Følg disse trin for at oprette en aktivtæller til sporing af produktionstimer.

1. Gå til **Aktivadministration \> Konfiguration \> Aktivtyper \> Tællere**.
1. Vælg **Ny** i handlingsruden for at oprette en tæller.
1. Angiv følgende værdier på hoveddelen:

    - **Tæller:** *ProductionHr*
    - **Navn:** *Produktionstimer*

1. I oversigtspanelet **Generelt** kan du angive følgende værdier:

    - **Enhed:** *time*
    - **Opdater:** *Manuel*
    - **Samlet aggregeret:** *Sum*

1. Vælg **Tilføj linje** i oversigtspanelet **Aktivtyper**.
1. Angiv feltet **Aktivtype** til *Air Knife* på den nye linje.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Opret en vedligeholdelsesplan for aktivet

Opret en vedligeholdelsesplan for aktivet ved at følge disse trin.

1. Gå til **Styring af aktiver \> Opsætning \> Forebyggende vedligeholdelse \> Vedligeholdelsesplan**.
1. Vælg **Ny** i handlingsruden for at oprette en vedligeholdelsesplan.
1. Angiv følgende værdier på hoveddelen:

    - **Vedligeholdelsesplan:** *AirKnife*
    - **Navn:** *Plan for air knives*

1. I oversigtspanelet **Detaljer** skal du angive følgende værdier:

    - **Plandato:** Angiv dags dato.
    - **Aktiv:** *Ja*

1. Gå til oversigtspanelet **Linjer** og vælg **Tilføj aktiv tællerlinje** for at føje en linje til gitteret. Angiv derefter følgende værdier for den:

    - **Beskrivelse af arbejdsordre:** *Vedligeholdelse af air knife*
    - **Vedligeholdelsesjobtype:** *Forebyggende*
    - **Intervaltype:** *Gentaget fra sidste arbejdsordre*
    - **Periodefrekvens:** *10000*
    - **Tæller:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Konfigurere scenariet for aktiv vedligeholdelse

Hvis du vil konfigurere *aktiv vedligeholdelse*-scenariet i Supply Chain Management, skal følge disse trin.

1. Gå til **Aktivstyring \> Opsætning \> Sensordataintelligens \> Scenarier**.
1. I scenariefeltet **Aktiv vedligeholdelse** skal du vælge **Konfigurer** for at åbne installationsguiden for dette scenario.
1. Vælg **Ny** på siden **Sensorer** for at føje en sensor til gitteret. Angiv følgende felter:

    - **Sensor-id** – angiv id for den bruger, du bruger. (Hvis du bruger Raspberry PI Azure IoT Online Simulator og har konfigureret den som beskrevet i [Angiv simuleret sensor til test](sdi-set-up-simulated-sensor.md), skal du angive *AssetMaintenance*.)
    - **Sensor-beskrivelse** – Indtast en detaljeret beskrivelse af sensoren.

1. Gentag forrige trin for hvert ekstra sensor, du skal tilføje nu. Du kan altid vende tilbage og tilføje flere oplysninger.
1. Vælg **Næste**.
1. På siden **Tilknytning af forretningspost** i afsnittet **Sensorer** skal du vælge posten for en af de sensorer, du lige har tilføjet.
1. Vælg **Ny** i sektionen **Tilknytning af forretningspost** for at føje en række til gitteret.
1. I den nye række skal feltet **Forretningsposttype** automatisk angives til *Assets (EntAssetObjectTable)*. Angiv feltet **Forretningspost** til den ressource, du bruger den valgte ressource til at overvåge. (Hvis du bruger de demodata, du oprettede tidligere i denne artikel, skal du angive dem *AK-101, AK-101 Air Knife for Line 1*).
1. Umiddelbart efter at du har valgt en forretningsposttype for den række, du tilføjede i det forrige trin, føjes der automatisk en anden række til gitteret. På denne række skal feltet **Firmaposttype** angives til *Tællere (EntAssetCounterType)*. Angiv feltet **Forretningspost** til den aktivtæller, du bruger til opdatering baseret på signaler fra den valgte sensor. (Hvis du bruger de demodata, du oprettede tidligere i denne artikel, skal du angive dem *ProductionHr, Production hours*.)
1. Vælg **Næste**.
1. På siden **Aktivér sensorer** i gitteret skal du vælge den sensor, du har tilføjet, og derefter vælge **Aktivér**. For hvert aktiveret område i gitteret vises en markering i kolonnen **Aktiv**.
1. Vælg **Udfør**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Arbejd med scenariet for aktiv vedligeholdelse

### <a name="view-counter-values"></a>Vis tællerværdier

Når dataene er udarbejdet, og scenariet *aktiv vedligeholdelse* er konfigureret og aktiveret, kan du se, hvordan poster til en aktivtæller indsættes på baggrund af data.

1. Gå til **Aktivstyring \> Aktiver \> Alle aktiver**.
1. Find og vælg det aktiv, du vil inspicere. (Hvis du bruger de demodata, du har oprettet tidligere i denne artikel, skal du vælge *AKA-101*.)
1. I handlingsruden under fanen **Aktiv** i gruppen **Forebyggende** skal du vælge **Tællere** for at åbne siden for tællerposter for aktiv *AK-101*.

> [!NOTE]
> Tællerposterne konfigureres som standard til at blive indsat hver tredje time, hvilket betyder, at sensordata samles i det pågældende interval. Du kan ændre intervallet ved at redigere forespørgslen i komponenten Azure Stream Analytics.

### <a name="generate-maintenance-work-orders"></a>Generer arbejdsordrer for vedligeholdelse

Når du har aktiveret scenariet til *vedligeholdelse af aktiver* og konfigureret vedligeholdelsesplanen, kan du køre vedligeholdelsesplanen for at generere arbejdsordrer for vedligeholdelse. Du kan finde flere oplysninger om, hvordan du arbejder med forebyggende vedligeholdelse, under [Forebyggende vedligeholdelse, oversigt](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
