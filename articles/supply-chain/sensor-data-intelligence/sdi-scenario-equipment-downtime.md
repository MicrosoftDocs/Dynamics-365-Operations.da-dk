---
title: Statusscenarie for maskinen
description: I denne artikel beskrives scenariet for maskinstatus, hvilket giver dig mulighed for at bruge data til at overvåge tilgængeligheden af udstyr.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 1f2b424dccf1963a7917059d412b5df7937496ee
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428307"
---
# <a name="the-machine-status-scenario"></a>Statusscenarie for maskinen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Scenariet for *maskinstatus*, hvilket giver dig mulighed for at bruge data til at overvåge tilgængeligheden af udstyr. Hvis du konfigurerer en fil, der sender et signal, når et produktionsjob på en maskinressource resulterer i output, men der ikke modtages et signal inden for et bestemt interval, vises der en besked på supervisorens dashboard.

## <a name="scenario-dependencies"></a>Scenarioafhængigheder

Scenariet *maskinstatus* har følgende afhængigheder:

- En besked kan kun udløses, hvis et produktionsjob kører på en tilknyttet maskine.
- Der skal sendes et signal, der repræsenterer et *part-out-signal til IoT-hub*.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Forberede demodata til scenariet til maskinstatus

Hvis du vil bruge et demosystem til at teste scenariet til *maskinstatus*, skal du bruge et system, hvor [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret, vælge den juridiske enhed *USMF* (firma) og forberede de yderligere demodata som beskrevet i dette afsnit. Hvis du bruger dine egne sensorer og data, kan du springe dette afsnit over.

### <a name="set-up-a-sensor-simulator"></a>Oprette en sensorsimulator

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

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Konfigurere grænsefladen til produktionsudførelse

Du vil bruge brugergrænsefladen til produktionsudførelse til at starte det job, der er planlagt og frigivet til varenummer *P0111* i det foregående afsnit. Følg disse trin for at konfigurere grænsefladen til produktionsudførelse.

1. Gå til **Produktionsstyring \> Produktionsudførelse \> Kørsel af produktionsudstyr**.
1. Hvis du ikke tidligere har konfigureret brugergrænsefladen, vises en logonside. Angiv dine legitimationsoplysninger.
1. Vælg **Konfigurer** på velkomstsiden for at åbne guiden **Konfigurer enhed**.
1. Vælg **standardkonfiguration - Trin 1 - Vælg konfiguration**-siden skal du vælge *Standard*-konfiguration.
1. Vælg **Næste**.
1. På **konfigurationsenhed – trin 2 – Definer siden med produktionsområder**, og angiv feltet **Ressource** til *3118*.
1. Vælg **OK**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>Aktiver søgeindstilling i grænsefladen til kørsel af produktion

Hvis du vil gøre det lettere at finde produktionsjobbet for den produktionsordre, der blev frigivet tidligere, skal du udføre følgende trin for at aktivere søgeindstillingen i brugergrænsefladen for produktionsudførelse.

1. Gå til **Produktionsstyring \> Opsætning \> Produktionsudførelse \> Konfigurer kørsel af produktionsudstyr**.
1. Vælg *Standard*-konfiguration.
1. Vælg **Rediger** i handlingsruden.
1. I oversigtspanelet **Generelt** skal du angive indstillingen **Aktiver søgning** til *Ja*.
1. Luk siden.

### <a name="start-the-first-job-in-the-batch-order"></a>Start det første job i batchordren

Benyt følgende fremgangsmåde for at starte det job, der er planlagt for ressource *3118*.

1. Gå til **Produktionsstyring \> Produktionsudførelse \> Kørsel af produktionsudstyr**.
1. I feltet **Badge-id** skal du angive *123*. Vælg derefter **Log på**.
1. Hvis du bliver bedt om at angive en fraværsårsagen, skal du vælge et af kortene til fravær og derefter vælge **OK**.
1. Angiv det batchordrenummer, du tidligere har notat om, i feltet **Søg**. Vælg derefter nøglen **Retur**.
1. Markér salgsordren, og vælg derefter **Start job**.
1. Vælg **Start** i dialogboksen **Start job**.

## <a name="set-up-the-machine-status-scenario"></a>Konfigurer statusscenarie for maskinen

Hvis du vil konfigurere *maskinstatus*-scenariet i Supply Chain Management, skal følge disse trin.

1. Gå til **Produktionsstyring \> Konfiguration \> Sensordataintelligens \> Scenarier**.
1. I scenariefeltet **Maskinstatus** skal du vælge **Konfigurer** for at åbne installationsguiden for dette scenario.
1. Vælg **Ny** på siden **Sensorer** for at føje en sensor til gitteret. Angiv følgende felter:

    - **Sensor-id** – angiv id for den bruger, du bruger. (Hvis du bruger Raspberry PI Azure IoT Online Simulator og har konfigureret den som beskrevet i [Angiv simuleret sensor til test](sdi-set-up-simulated-sensor.md), skal du angive *MachineStatus*.)
    - **Sensor-beskrivelse** – Indtast en detaljeret beskrivelse af sensoren.

1. Gentag forrige trin for hvert ekstra sensor, du skal tilføje nu. Du kan altid vende tilbage og tilføje flere oplysninger.
1. Vælg **Næste**.
1. På siden **Tilknytning af forretningspost** i afsnittet **Sensorer** skal du vælge posten for en af de sensorer, du lige har tilføjet.
1. Vælg **Ny** i sektionen **Tilknytning af forretningspost** for at føje en række til gitteret.
1. I den nye række skal du indstille feltet **Forretningspost** til den ressource, du bruger den valgte ressource til at overvåge. (Hvis du bruger de demodata, du oprettede tidligere i denne artikel, skal du angive feltet *3118, Foam-skæremaskine*.)
1. Vælg **Næste**.
1. På siden **Tærskel for maskinstatus** skal du angive , hvor lang tid efter det sidste *part-out*-signal systemet skal sende en besked om maskinstatus. Der er to måder at definere tærsklen på:

    - **Standardtærskel (minutter)** – Angiv dette felt for at definere standardtærsklen. Værdien anvendes derefter på alle ressourcer, hvor **grænsen for bestemmelse af, at en maskine ikke svarer (minutter)**, er angivet til to minutter eller mindre. Minimumværdien er *2* (minutter).
    - **Tærskelværdi for at bestemme, at maskinen ikke svarer (minutter)** – For hver ressource i gitteret, som du ikke skal bruge standardgrænseværdi for, skal du angive en ændringsværdi i dette felt. Ressourcer, der er angivet til at bruge en grænse på to minutter eller mindre, bruger i stedet indstillingen **Standardgrænseværdi (minutter)**.

    > [!NOTE]
    > Du vil typisk bruge et *part-out*-signal til at overvåge maskinstatus. Du skal derfor kontrollere, at grænsen for hver maskinressource er længere, end maskinen kræver, før de enkelte dele produceres.

1. Vælg **Næste**.
1. På siden **Aktivér sensorer** i gitteret skal du vælge den sensor, du har tilføjet, og derefter vælge **Aktivér**. For hvert aktiveret område i gitteret vises en markering i kolonnen **Aktiv**.
1. Vælg **Udfør**.

## <a name="work-with-the-machine-status-scenario"></a>Arbejde med statusscenarie for maskinen

Når du har installeret din egen leverandør og konfigureret scenariet, kan du få vist hændelser med maskinstatus i Supply Chain Management. Dette afsnit indeholder en beskrivelse af, hvor og hvordan du kan få vist disse oplysninger.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Få vist maskinstatusdata på siden Ressourcestatus

På siden **Ressourcestatus** kan tilsynsførende overvåge en tidslinje for det *part-out*-signal, der modtages fra de sensorer, som er knyttet til de enkelte maskinressourcer. Hvis du vil konfigurere tidslinjen, skal du følge disse trin:

1. Gå til **Produktionsstyring \> Produktionsudførelse \> Ressourcestatus**.
1. I dialogboksen **Konfigurer** skal du angive følgende felter.

    - **Ressource** – Vælg de ressourcer, du vil overvåge. (Hvis du arbejder med demodata, skal du vælge *3118*.)
    - **Tidsserier 1** – Vælg den post (den metriske nøgle), der har følgende format for navnet: *MachineReportingStatus:&lt;Sensor&gt;*
    - **Visningsnavn** – Angiv *Parts out-signal*.

I følgende illustration vises et eksempel på maskinstatusdata på siden **Ressourcestatus** under standardoperationen.

![Maskinstatusdata på siden Ressourcestatus under standarddrift.](media/sdi-resource-status-downtime-up.png "Maskinstatusdata på siden Ressourcestatus under standarddrift")

I følgende illustration vises et eksempel på maskinstatusdata, når der registreres nedetid.

![Maskinstatusdata på ressourcestatussiden, når der registreres nedetid.](media/sdi-resource-status-downtime-down.png "Maskinstatusdata på ressourcestatussiden, når der registreres nedetid")

### <a name="view-machine-status-on-the-notifications-page"></a>Få vist maskinstatus på siden Beskeder

På siden **Beskeder** kan tilsynsførende få vist de beskeder, der genereres, når der er gået for lang tid siden, at det sidste *part-out*-signal blev leveret. Hver besked giver en oversigt over det produktionsjob, der påvirkes af udfaldet, og giver mulighed for at tildele det berørte job til en anden ressource.

Åbn siden **Besked** gå til **Produktionsstyring \> Forespørgsler og rapporter \> Sensordataintelligens \> Meddelelser**.

Følgende illustration viser et eksempel på en maskinstatusmeddelelse.

![Eksempel på maskinstatusmeddelelse.](media/sdi-resource-status-downtime-notification.png "Eksempel på maskinstatusmeddelelse")
