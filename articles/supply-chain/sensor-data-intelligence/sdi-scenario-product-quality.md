---
title: Scenariet for produktkvalitet
description: Denne artikel indeholder oplysninger om produktkvalitetsscenarie. I dette scenario bruges en værdi til at måle kvaliteten af et produktbatch og genererer en påmindelse, hvis en måling falder uden for en defineret grænseværdi.
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
ms.openlocfilehash: c0f1c57251234921779f67faf61d47cdde119e64
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690042"
---
# <a name="the-product-quality-scenario"></a>Scenariet for produktkvalitet

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

I *produktkvalitetsscenariet* er der konfigureret en opsætning til at måle kvaliteten af et produkt-batch i produktionen. Hvis en måling falder uden for en defineret grænse for produktet, vises der en besked på den tilsynsførendes dashboard. Det kan f.eks. være en måling af fugtigheden i et fødevareprodukt, der kommer ud af produktionslinjen. Hvis målingen ligger uden for den tilladte minimum- eller maksimumværdi for fugtighed for produktet, genereres der en besked.

## <a name="scenario-dependencies"></a>Scenarioafhængigheder

Scenariet *Produktkvalitet* har følgende afhængigheder:

- En besked kan kun udløses, hvis en produktionsordre kører på en tilknyttet maskine, og hvis den maskine fremstiller et produkt med en tilknyttet batch-attribut.
- Et signal, der repræsenterer batchattributten, skal sendes til IoT Hub sammen med et entydigt egenskabsnavn.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Forberede demodata til scenariet til produktkvalitet

Hvis du vil bruge et demosystem til at teste scenariet til *produktkvalitet*, skal du bruge et system, hvor [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installeret, vælge den juridiske enhed *USMF* (firma) og forberede de yderligere demodata som beskrevet i dette afsnit. Hvis du bruger dine egne sensorer og data, kan du springe dette afsnit over.

I dette afsnit skal du konfigurere demodataene, så du kan bruge det frigivne produkt *P0111* (*Composite Case*) med scenariet for *produktkvalitet*. I dette scenario sporer systemet, om en batchattributværdi, der måles ved hjælp af en attribut, ligger uden for den definerede grænse for en batchattribut, der er knyttet til produktet.

### <a name="set-up-a-sensor-simulator"></a>Oprette en sensorsimulator

Hvis du vil prøve dette scenario uden at bruge en fysisk opsætning, kan du konfigurere en opsætning til generering af de påkrævede signaler. Du kan finde flere oplysninger i [Konfigurere en simuleret sensor til test](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Knytte en batchattribut og en ressource til produkt P0111

Benyt følgende fremgangsmåde for at knytte en batchattribut til produkt *P0111* (*sammensat kasse*) og kontrollere, at der bruges ressource *3118* (*Foam-skæremaskine*) til den.

1. Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.
1. Fing, og vælg det produkt, hvor feltet **Varenummer** er angivet til *P0111*.
1. Klik på **Produktspecifik** i gruppen **Batchattributter** under fanen **Administrer lager** i handlingsruden.
1. På den **produktspecifikke** side skal du vælge **Ny** for at oprette en produktspecifik batchattribut.
1. Angiv følgende felter på headeren:

    - **Attributkode** – Vælg området af attributter, du vil overvåge (*Tabel*, *Gruppe* eller *Alle*). Vælg *tabel* i dette scenario, fordi du altid vil overvåge en enkelt attribut.
    - **Attributrelation** – Vælg den attribut, som du vil bruge *produktkvalitetsscenariet* til at overvåge værdien af. I dette eksempel skal du vælge *Koncentration*, som er en attribut, der inkluderes i standarddemodataene.

1. Gå til oversigtspanelet **Værdier**, og definer intervallet for acceptable værdier, som attributten skal rapportere for at bestå kvalitetskontrollen, i felterne **Minimum** og **Maksimum**. Hvis en værdi uden for dette interval rapporteres, vil systemet identificere den som en kvalitetsovertrædelse. De andre felter i dette oversigtspanel er ikke relevante for *produktkvalitetsscenariet*. De standardværdier, du ser i øjeblikket, kommer fra demo-dataene. Lad dem derfor blive, som de er, og luk den **produktspecifikke** side for at vende tilbage til siden **Få vist oplysninger om frigivne produkter** for varen *P0111*.
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

## <a name="set-up-the-product-quality-scenario"></a>Konfigurere produktkvalitetsscenarie

Hvis du vil konfigurere *produktkvalitet*-scenariet i Supply Chain Management, skal du følge disse trin.

1. Gå til **Produktionsstyring \> Konfiguration \> Sensordataintelligens \> Scenarier**.
1. I scenariefeltet **produktionskvalitet** skal du vælge **Konfigurer** for at åbne installationsguiden for dette scenario.
1. Vælg **Ny** på siden **Sensorer** for at føje en sensor til gitteret. Angiv følgende felter:

    - **Sensor-id** – angiv id for den bruger, du bruger. (Hvis du bruger Raspberry PI Azure IoT Online-simulator og har konfigureret den som beskrevet i [Angiv simuleret sensor til test](sdi-set-up-simulated-sensor.md), skal du angive *Kvalitet*.)
    - **Sensor-beskrivelse** – Indtast en detaljeret beskrivelse af sensoren.

1. Gentag forrige trin for hvert ekstra sensor, du skal tilføje nu. Du kan altid vende tilbage og tilføje flere oplysninger.
1. Vælg **Næste**.
1. På siden **Tilknytning af forretningspost** i afsnittet **Sensorer** skal du vælge posten for en af de sensorer, du lige har tilføjet.
1. Vælg **Ny** i sektionen **Tilknytning af forretningspost** for at føje en række til gitteret.
1. I den nye række skal feltet **Forretningsposttype** automatisk angives til *Resources(WrkCtrTable)*. Angiv feltet **Forretningspost** til den ressource, du bruger den valgte ressource til at overvåge. (Hvis du bruger de demodata, du oprettede tidligere i denne artikel, skal du angive det *3118, Foam-skæremaskine*.)
1. Umiddelbart efter at du har valgt en forretningsposttype for den række, du tilføjede i det forrige trin, føjes der automatisk en anden række til gitteret. På denne række skal feltet **Forretningsposttype** angives til *Batch attributes(PdsBatchAttrib)*. Angiv feltet **Forretningspost** til den batch-ressource, du bruger den valgte sensor til at overvåge. (Hvis du bruger de demodata, du oprettede tidligere i denne artikel, skal du angive det til *Concentration, Concentration Percentage*.)
1. Vælg **Næste**.
1. På siden **Aktivér sensorer** i gitteret skal du vælge den sensor, du har tilføjet, og derefter vælge **Aktivér**. For hvert aktiveret område i gitteret vises en markering i kolonnen **Aktiv**.
1. Vælg **Udfør**.

## <a name="work-with-the-product-quality-scenario"></a>Arbejde med produktkvalitetsscenarie

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Få vist produktionskvalitetsdata på siden Ressourcestatus

På siden **Resource status** kan tilsynsførende overvåge en tidslinje for det produktkvalitetssignal, der modtages fra de sensorer, som er knyttet til de enkelte maskinressourcer. Hvis du vil konfigurere tidslinjen, skal du følge disse trin:

1. Gå til **Produktionsstyring \> Produktionsudførelse \> Ressourcestatus**.
1. I dialogboksen **Konfigurer** skal du angive følgende felter.

    - **Ressource** – Vælg de ressourcer, du vil overvåge. (Hvis du arbejder med demodata, skal du vælge *3118*.)
    - **Tidsserier 1** – Vælg den post (den metriske nøgle), der har følgende format for navnet: *ProductQuality:&lt;JobId&gt;:&lt;AttributeName&gt;*
    - **Visningsnavn** – Angiv *Batchattributværdier*.

I følgende illustration vises et eksempel på data om produktkvalitet på siden **Ressourcestatus**, når værdien ligger inden for intervallet af acceptable værdier.

![Produktkvalitetsdata på ressourcestatussiden, når værdien er i interval.](media/sdi-product-quality-in-range.png "Produktkvalitetsdata på ressourcestatussiden, når værdien er i interval")

I følgende illustration vises et eksempel på data om produktkvalitet, når der registreres en værdi uden for området.

![Produktkvalitetsdata på ressourcestatussiden, når der registreres en værdi uden for værdien.](media/sdi-product-quality-out-of-range.png "Produktkvalitetsdata på ressourcestatussiden, når der registreres en værdi uden for værdien")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Få vist produktionskvalitetsdata på siden Meddelelser

På siden **Meddelelser** kan tilsynsførende få vist den besked, der genereres, når batchattributten måler en batchattributværdi, der ligger uden for den definerede grænse for batchattributten. Hver besked giver en oversigt over det produktionsjob, der påvirkes af udfaldet, og giver mulighed for at tildele det berørte job til en anden ressource.

Åbn siden **Besked** gå til **Produktionsstyring \> Forespørgsler og rapporter \> Sensordataintelligens \> Meddelelser**.

Følgende illustration viser et eksempel på en side med produktkvalitetsmeddelelse.

![Eksempel på en produktkvalitetsmeddelelse.](media/sdi-product-quality-notification.png "Eksempel på en produktkvalitetsmeddelelse")
