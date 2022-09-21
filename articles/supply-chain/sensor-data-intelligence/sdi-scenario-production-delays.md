---
title: Scenarie til produktionsforsinkelser
description: Denne artikel beskriver scenarie med produktionsforsinkelser, der genererer en besked, hvis produktionsgennemløb falder under en specifik tærskelværdi.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 073762581d84646ba12b570e57327b7cab8efd3b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428310"
---
# <a name="the-production-delays-scenario"></a>Scenarie til produktionsforsinkelser

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Scenariet *Produktionsforsinkelser* genererer en besked, hvis produktions gennemløb falder under en specifik tærskelværdi. I dette scenarie sendes et *part-out*-signal til Microsoft Azure IoT Hub for hver fremstillet vare. I Dynamics 365 Supply Chain Management beregnes ordreforsinkelsen på basis af den mængde tid, som produktionsordren er planlagt til at køre, det antal varer, der skal produceres, den tid, jobbet har kørt, og antallet af *part-out*-signaler, der er blevet modtaget. Der genereres en forsinkelsesbesked, hvis antallet af *Part-Out*-signaler for jobbet falder under tærskelværdien.

## <a name="scenario-dependencies"></a>Scenarioafhængigheder

Scenariet *Produktionsforsinkelser* har følgende afhængigheder:

- En besked kan kun udløses, hvis en produktionsordrer kører på en tilknyttet maskine.
- Et signal, der repræsenterer en tilknyttet maskines *Part-Out*-signal, skal sendes til IoT Hub sammen med et entydigt egenskabsnavn.
- En UNIX-egenskab for tidsstempel, hvor værdien angives i millisekunder (ms), skal være til stede i Azure IoT Hub-meddelelsen.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Forberede demodata til scenariet til produktforsinkelser

Hvis du vil bruge et demosystem til at teste scenariet til *produktionsforsinkelser*, skal du bruge et system, hvor [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret, vælge den juridiske enhed *USMF* (firma) og forberede de yderligere demodata som beskrevet i dette afsnit. Hvis du bruger dine egne sensorer og data, kan du springe dette afsnit over.

### <a name="set-up-sensor-simulator"></a>Oprette sensorsimulator

Hvis du vil prøve dette scenario uden at bruge en fysisk opsætning, kan du konfigurere en opsætning til generering af de påkrævede signaler. Du kan finde flere oplysninger i [Konfigurere en simuleret sensor til test](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Kontroller, at ressource 3118 bruges til produktet P0111

En produktionsordre planlægges og frigives. Derfor frigives et produktionsjob til ressource *3118* (*Foam-skæringsmaskine*). Følg disse trin for at kontrollere, at ressource *3118* bruges til produkt *P0111* i dine demodata.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Fing, og vælg det produkt, hvor feltet **Varenummer** er angivet til *P0111*.
1. Gå til handlingsruden, og vælg **Route** i gruppen **Vis** under fanen **Designer**.
1. På siden **Rute** under fanen **Oversigt** nederst på siden skal du vælge den linje, hvor feltet **Oper. No.** er angivet til *30*.
1. Under fanen **Ressourcekrav** nederst på siden skal du kontrollere, at ressource *3118* (*Foam-udskæringsmaskine*) til ressourcer er knyttet til operationen.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Opret og udgiv en produktionsordre for et projekt P0111

Følg disse trin for at oprette og frigive en produktionsordre på produkt *P0111*.

1. Gå til **Produktionsstyring \> Produktionsordrer \> Alle produktionsordrer**.
1. Vælg **Ny batchordre** i handlingsruden på siden **Alle produktionsordrer**.
1. I dialogboksen **Opret batch** skal du angive følgende værdier:

    - **Varenummer:** *P0111*
    - **Antal:** *10*

1. Vælg **Opret** for at oprette produktionsordren og vende tilbage til siden **Alle produktionsordrer**.
1. Brug feltet **Filter** til at søge efter produktionsordrer, hvor feltet **Varenummer** er angivet til *P0111*. Find, og vælg derefter den produktionsordre, du lige har oprettet.
1. I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Estimer**.
1. Vælg **OK** for at køre beregningen i dialogboksen **Estimer**.
1. I handlingsruden under fanen **Produktionsordre** skal du i gruppen **Proces** vælge **Udgiv**.
1. Notér nummeret på den batchordre, du lige har oprettet, i dialogboksen **Frigivelse**.
1. Vælg **OK** for at udgive ordren.

### <a name="configure-the-production-floor-execution-interface"></a>Konfigurere grænsefladen til produktionsudførelse

Hvis du ikke allerede har gjort det, skal du konfigurere brugergrænsefladen til produktionsudførelse, så der vises job, der er tildelt ressource *3118* (*Foam- skæremaskine*). Du kan finde instruktioner i følgende afsnit:

- [Konfigurere grænsefladen til produktionsudførelse](sdi-scenario-equipment-downtime.md#config-pfe)
- [Aktiver søgeindstilling i grænsefladen til kørsel af produktion](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Start det første job i batchordren

Benyt følgende fremgangsmåde for at starte det første job i batchordren.

1. Gå til **Produktionsstyring \> Produktionsudførelse \> Kørsel af produktionsudstyr**.
1. I feltet **Badge-id** skal du angive *123*. Vælg derefter **Log på**.
1. Hvis du bliver bedt om at angive en fraværsårsagen, skal du vælge et af kortene til fravær og derefter vælge **OK**.
1. Angiv det batchordrenummer, du tidligere har notat om, i feltet **Søg**. Vælg derefter nøglen **Retur**.
1. Markér salgsordren, og vælg derefter **Start job**.
1. Vælg **Start** i dialogboksen **Start job**.

## <a name="set-up-the-production-delays-scenario"></a>Konfigurere scenarie til produktionsforsinkelser

Hvis du vil konfigurere *produktionsforsinkelser*-scenariet i Supply Chain Management, skal du følge disse trin.

1. Gå til **Produktionsstyring \> Konfiguration \> Sensordataintelligens \> Scenarier**.
1. I scenariefeltet **produktionsforsinkelser** skal du vælge **Konfigurer** for at åbne installationsguiden for dette scenario.
1. Vælg **Ny** på siden **Sensorer** for at føje en sensor til gitteret. Angiv følgende felter:

    - **Sensor-id** – angiv id for den bruger, du bruger. (Hvis du bruger Raspberry PI Azure IoT Online Simulator og har konfigureret den som beskrevet i [Angiv simuleret sensor til test](sdi-set-up-simulated-sensor.md), skal du angive *ProductionDelay*.)
    - **Sensor-beskrivelse** – Indtast en detaljeret beskrivelse af sensoren.

1. Gentag forrige trin for hvert ekstra sensor, du skal tilføje nu. Du kan altid vende tilbage og tilføje flere oplysninger.
1. Vælg **Næste**.
1. På siden **Tilknytning af forretningspost** i afsnittet **Sensorer** skal du vælge posten for en af de sensorer, du lige har tilføjet.
1. Vælg **Ny** i sektionen **Tilknytning af forretningspost** for at føje en række til gitteret.
1. I den nye række skal du indstille **Forretningspost** til den ressource, du bruger den valgte ressource til at overvåge. (Hvis du bruger de demodata, du oprettede tidligere i denne artikel, skal du angive det *3118, Foam-skæremaskine*.)
1. Vælg **Næste**.
1. Hvis du bruger de demodata, du oprettede tidligere i denne artikel, på siden **Grænse for afvigelse i produktionsforsinkelse**, skal du følge disse trin:

    1. Vælg kolonneoverskriften for **varerelation** for at åbne en rulledialogboks, der indeholder søgefiltre for kolonnen. Skriv *P0111* i søgefeltet, og vælg derefter **Anvend**.
    2. Vælg den linje, hvor feltet **Handling** er angivet til *Trin/Klip*. Indstil feltet **Beskedtærskel for forsinkelse (%)** til den grænseværdi (som procent), som der skal sendes en besked ved.

1. Vælg **Næste**.
1. På siden **Aktivér sensorer** i gitteret skal du vælge den sensor, du har tilføjet, og derefter vælge **Aktivér**. For hvert aktiveret område i gitteret vises en markering i kolonnen **Aktiv**.
1. Vælg **Udfør**.

## <a name="work-with-the-production-delays-scenario"></a>Arbejde med scenarie til produktionsforsinkelser

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Få vist produktionsforsinkelse på siden Ressourcestatus

På siden **Ressourcestatus** kan tilsynsførende overvåge en tidslinje for de signaler, der modtages fra de sensorer, som er knyttet til de enkelte maskinressourcer. Hvis du vil konfigurere tidslinjen, skal du følge disse trin:

1. Gå til **Produktionsstyring \> Produktionsudførelse \> Ressourcestatus**.
1. I dialogboksen **Konfigurer** skal du angive følgende felter.

    - **Ressource** – Vælg de ressourcer, du vil overvåge. (Hvis du arbejder med demodata, skal du vælge *3118*.)
    - **Tidsserier 1** – Vælg den post (den metriske nøgle), der har følgende format for navnet: *ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **Visningsnavn** – Angiv *Parts out-signal*.
