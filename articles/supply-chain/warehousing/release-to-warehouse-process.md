---
title: Frigiv til lagersted
description: Dette emne indeholder oplysninger om processen for frigivelse til lagersted. Den beskriver enheder, der oprettes, når du frigiver en ordre til lagerstedet, og indstillinger, du kan bruge til at starte processen.
author: mirzaab
ms.date: 8/13/2021
ms.topic: article
ms.search.form: WHSReleaseToWarehouse, WHSReleaseToWarehouseSalesOrder, WHSReleaseToWarehouseTransferOrder, WHSLoadPlanningWorkbench, WHSWaveTemplateTable, WHSWorkTemplateTable, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3269bf3f8a5475fb85e6b51514db29006be9aab1
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376202"
---
# <a name="release-to-warehouse"></a>Frigiv til lagersted

[!include [banner](../../includes/banner.md)]

Dette emne indeholder oplysninger om processen for frigivelse til lagersted. Den beskriver enheder, der oprettes, når du frigiver en ordre til lagerstedet, og indstillinger, du kan bruge til at starte processen.

## <a name="release-to-warehouse-overview"></a>Regel for oversigt over lagersted

Frigivelse til lagersted er den proces, der går ud på at gøre lageret klar til ekspedition. Når du frigiver en ordre til lagerstedet, opretter systemet belastningslinjer og forsendelser. Hvis der er konfigureret automatisk behandling af bølger, oprettes der også belastninger og påkrævet arbejde. Konfigurationen af de enheder, der er involveret, afhænger af systemindstillingerne. Dette afsnit i emnet gennemgår de enheder, der oprettes i løbet af frigivelsen til lagerstedsprocessen, og de systemindstillinger, der definerer dem.

En *forsendelse* er en gruppe salgsordre- eller flytteordrelinjer til samme kunde eller samme leveringsadresse.

En *belastning* er en gruppe salgsordre- eller flytteordrelinjer, der grupperes sammen, og som normalt går ud på en enkelt lastbil, togvogn eller en anden transportmåde. En belastning kan have en eller flere forsendelser. Du kan oprette en belastning manuelt ved at føje ordrelinjer til en ny belastning. I dette tilfælde tildeles ordrelinjer til indlæsningen, før frigivelsen til lagerstedsprocessen initieres, og de kan kun frigives fra siden **Belastningsplanlægning**.

*Lagerstedsarbejde* er en hvilken som helst lagerstedsoperation, der udføres af en lagerarbejder. Arbejdshandlinger på lagersted består typisk af mindst to efterfølgende handlinger: en lagerarbejder plukker disponibel lagerbeholdning på ét sted og sætter derefter det plukkede lager ned på en anden placering.

Når du frigiver en ordre til lagerstedet, opretter systemet *belastningslinjer* og grupperer dem i forsendelser. Processen til konsolidering af forsendelse giver mulighed for automatisk konsolidering af forsendelser under processen for frigivelse til lagersted. Du kan finde flere oplysninger under [Forsendelseskonsolideringspolitikker](about-shipment-consolidation-policies.md).

Systemet bruger *bølger* til at oprette plukarbejde og belastninger til forsendelse. Der skal være en *bølgeskabelon* tilgængelig for den type bølge, du vil oprette, og for ordrelinjens lagersted. Bruge bølgeskabelonen til typen *Forsendelse* til salgsordrer og flytteordrer.

Hver skabelon indeholder *bølgemetoder*. Bølgemetoder til massearbejde udfører aktioner som f.eks. oprettelse af arbejde for bølgen eller oprettelse af belastninger. Bølgeskabelonen til forsendelsesbølger kan eksempelvis indeholde metoder til oprettelse af belastninger, tildeling af linjer til bølger, genopfyldning og oprettelse af plukkearbejde for bølgen. Bølgeskabelonen opretter mange indstillinger for, hvordan bølgen skal genereres og behandles, herunder hvilke trin der skal udføres manuelt, og hvilke der udføres automatisk. Du finder flere oplysninger under [Bølgeskabeloner](wave-templates.md). Afhængigt af konfigurationen af skabelonen til bølger skal du derfor enten automatisk oprette, behandles og frigives, når du frigiver en ordre til lagerstedet, eller også udføres nogle af eller alle disse handlinger manuelt, når frigivelsen til lagerstedet er udført.

Når en bølge behandles, opretter systemet plukarbejde baseret på et passende *arbejdsskabelon* og *lokalitetsdirektiv*, og gør dette arbejde tilgængeligt på mobile enheder. Arbejdsskabelonen bestemmer, hvordan arbejdet udføres for hver enkelt lagerstedsproces, og lokationsdirektivet angiver pluk og angiver lokationer for lagerbevægelser. Få flere oplysninger under [Styre lagerarbejde ved hjælp af arbejdsskabeloner og lokationsvejledninger](control-warehouse-location-directives.md).

> [!NOTE]
> Som standard behandles bølger i batchtilstand.

Under bølgebehandling opretter systemet normalt en ny last for hver forsendelse, hvortil der ikke er tildelt nogen last. Hvis du vil have, at systemet skal tildele ikke-tildelte forsendelser til eksisterende belastninger i stedet, kan du bruge funktionaliteten til avanceret belastningsbelastning. Du kan finde flere oplysninger under [Avanceret lastopbygning under en bølge](advanced-load-building-during-wave.md).

På siderne **Salgsordrer** og **Flytteordrer** kan du gennemse de enheder, der er oprettet for ordrelinjer i forbindelse med processen for frigivelse til lagersted.

- **Salgsordrer**-side:

    - I oversigtspanelet **Salgsordrelinjer** skal du vælge **Lagersted** og derefter vælge **forsendelsesdetaljer** i menuen for at åbne relaterede forsendelser, **Indlæse oplysninger** for at åbne relaterede belastninger eller **Arbejdsdetaljer** for at åbne relaterede arbejdsoplysninger.
    - Vælg fanen **Indlæs** for at gennemse relaterede belastninger i oversigtspanelet **Linjedetaljer**.

- **Overførselsordrer** side:

    - I handlingsruden under fanen **Forsendelse** skal du vælge **Forsendelsesoplysninger** for at åbne relaterede forsendelser eller **Indlæs oplysninger** for at åbne relaterede belastninger.
    - Vælg **arbejdsdetaljer** i oversigtspanelet **Flytteordrelinjer** for at åbne relaterede arbejdsdetaljer.

Når en ordre frigives til lagerstedet, fungerer den mest automatiske proces derfor på følgende måde:

1. Systemet opretter en forsendelse for ordren og en bølge.
1. Bølgen behandles.
1. Systemet opretter en belastning og et arbejds-id.

Afhængigt af indstillinger for skabeloner til skabeloner, arbejdsskabeloner og lokalitetsdirektiver kan nogle trin i dette flow blive manuelle. Det overordnede flow forbliver dog det samme.

Du har flere muligheder for, hvordan du frigiver en ordre til lagerstedet. Du kan udføre operationen manuelt, eller du kan konfigurere et batchjob. I de resterende afsnit af dette emne gennemgås de forskellige måder, du kan udføre en frigivelse til lagerstedsoperationen på.

## <a name="manual-release-to-the-warehouse-from-the-sales-orders-and-transfer-orders-pages"></a>Manuel frigivelse til lagerstedet fra siderne Salgsordrer og Flytteordrer

Du kan frigive en ordre til lagerstedet direkte fra siden **Salgsordrer** eller siden **Flytteordrer** ved at vælge **Frigiv til lagersted**.

- På siden **Salgsordrer** findes knappen under fanen **Lagersted** i handlingsruden.
- På siden **Overførselsordrer** findes knappen under fanen **Send** i handlingsruden.

Fra siden **Salgsordrer** kan du frigive flere salgsordrer på samme tid.

## <a name="manual-release-to-the-warehouse-from-the-release-to-warehouse-pages"></a>Manuel frigivelse til lagerstedet fra siderne Frigiv til lagersted

Systemet indeholder i øjeblikket tre sider, hvor du kan gennemse linjer for flere ordrer og frigive dem til lagerstedet:

- **Frigiv til lagersted** (**Warehouse management \> Frigiv til lagersted \> Frigiv til lagersted**) - På denne side kan du arbejde med både salgsordrer og flytteordrer. Men det giver en langsommere ydeevne end de to andre sider. Det vil snart blive frarådet at bruge denne side.
- **Frigiv salgsordrer til lagersted** (**Warehouse management \> Frigiv til lagersted \> Frigiv salgsordrer til lagersted**) - På denne side kan du arbejde med både salgsordrer og flytteordrer. Det giver dog en bedre ydeevne end siden **Frigiv til lagersted**.
- **Frigiv overførselsordrer til lagersted** (**Warehouse management \> Frigiv til lagersted \> Frigiv overførselsordrer til lagersted**) - På denne side kan du arbejde med både salgsordrer og flytteordrer. Det giver dog en bedre ydeevne end siden **Frigiv til lagersted**.

Alle tre sider indeholder ens funktioner som beskrevet i resten af dette afsnit. Du kan alle vælge ordrelinjer eller hele ordrer og derefter frigive dem til lagerstedet.

Hver af siderne består af en øvre sektion, hvor du kan vælge ordrelinjer, og en nederste sektion, hvor du kan starte processen til frigivelse til lagersted. Du kan bruge filtre i den øverste sektion til at søge efter de salgsordrelinjer, du vil frigive. Siden **Frigiv til lagersted** indeholder en separat fane for salgsordrer og flytteordrer i den øverste sektion, mens hver af de to andre sider kun indeholder én ordretype.

Værktøjslinjen i den øverste sektion indeholder følgende knapper, du kan bruge til at vælge ordrelinjer til frigivelse til lagerstedet:

- **Tilføj** – Vælg en eller flere ordrelinjer i den øverste sektion, og vælg derefter denne knap til de pågældende linjer i den nederste sektion.
- **Tilføj alle** – Tilføj alle linjer fra den øverste sektion til den nederste sektion.
- **Tilføj ordre** – Vælg en ordre, og vælg derefter denne knap for at tilføje alle linjer fra den pågældende ordre til den nederste sektion.

Når du er færdig med at føje linjer til den nederste sektion, skal du markere hver af de linjer, du vil frigive. Vælg derefter **Frigiv til lagersted** på værktøjslinjen for at frigive disse linjer til lagerstedet.

## <a name="manual-release-to-the-warehouse-from-the-load-planning-workbench-page"></a>Manuel frigivelse til lagersted fra siden Panelet Lastplanlægning

Du kan også manuelt frigive ordrer til lagerstedet ved hjælp af siden **Belastningsplanlægning**. På denne side kan du organisere ordrelinjer i belastninger og derefter frigive disse belastninger til lagerstedet.

Åbn siden **Lastplanlægningspanel**, gå til **Warehouse management \> Laster**. Du kan også åbne den fra siderne **Salgsordrer** og **Flytteordrer**. I den øverste del af siden kan du markere salgsordrelinjer under fanen **Salgslinjer** og flytteordrelinjer under fanen **Flyttelinjer** og derefter føje disse linjer til en ny eller eksisterende belastning.

Fanen **Udbud og efterspørgsel** i handlingsruden indeholder følgende knapper, du kan bruge til at føje ordrelinjer i den øverste sektion til en belastning:

- **Til ny last** – Vælg en eller flere ordrelinjer i den øverste sektion, og vælg derefter denne knap for at oprette en ny last og tilføje disse linjer.
- **Til eksisterende last** – Vælg en eller flere ordrelinjer i den øverste sektion, og vælg derefter denne knap for at tilføje disse linjer til en eksisterende last.
- **Hel ordre til ny last** – Vælg ordrer, og vælg derefter denne knap for at oprette en ny last og tilføje alle linjer fra disse tilhørende ordrer.
- **Hel ordre til eksisterende last** – Vælg en ordre, og vælg derefter denne knap for at tilføje alle linjer fra samme ordre til en eksisterende last.

I den nederste sektion kan du gennemse de belastninger, der er oprettet. Frigiv laster til lagerstedet ved at vælge dem og vælg **Frigiv \> Frigiv til lagersted** på værktøjslinjen. Hvis du bruger automatisk behandling af bølger, fordi der allerede er knyttet belastninger til ordrelinjerne, opretter systemet forsendelser og arbejds-id'er, når frigivelsen til lagerstedsoperationen udføres.

## <a name="automatic-release-to-the-warehouse"></a>Automatisk frigivelse til lagerstedet

Brug automatisk frigivelse af salgsordrer til lagerstedet ved hjælp af **automatisk frigivelse af salgsordrer** og **automatisk frigivelse af flytteordrejob**.

For at konfigurere et batchjob til frigivelse af salgsordrer, skal du gøre følgende:

1. Gå til **Lagerstedsstyring \> Frigiv til lagersted \> Automatisk frigivelse af salgsordrer**.
1. Angiv følgende felter i dialogboksen **Automatisk frigivelse af salgsordre** i oversigtspanelet **Parametre**.

    - **Antal til frigivelse** - Vælg om hele antallet skal frigives, eller om det fysisk reserverede antal skal frigives til lagerstedet.
    - **Tillad frigivelse af delvist frigivne ordrer** – Angiv, om restantal for delvist frigivne ordrer skal frigives til lagerstedet.
    - **Behold reservationer af frigivelsesfejl** – Angiv, om antal, der blev automatisk reserveret for en salgsordre, skal forblive reserveret, hvis processen for frigivelsen til lagerstedet mislykkes.
    - **Gruppere udgivelser efter kunde** – Angiv, om systemet skal behandle udgivelse til lagerstedsoperationer separat for hver kunde, eller om alle salgsordrer skal udgives samtidig. Når denne indstilling er angivet til *Ja*, indsamler systemet alle salgsordrelinjer for en valgt kunde, udgiver disse ordrer til lagerstedet og behandler derefter næste kunde. Når denne indstilling er angivet til *Nej*, udgives alle tilgængelige salgsordrelinjer i én enkelt version til lagerstedshandlingen. Aktivering af denne indstilling forbedrer ydeevnen og robustheden af processen for udgivelse til lagersted. Du skal dog være forsigtig, når du bruger denne indstilling sammen med bølgeskabeloner, der er konfigureret til at behandle bølger ved udgivelse til lagerstedet, da denne kombination kan generere mange enkeltkundebølger, der hver især har arbejde, som kun er genereret for den pågældende kunde. Hvis du vil generere arbejde, der kombinerer forsendelser til flere kunder, skal du deaktivere indstillingen *Gruppere udgivelser efter kunde* eller konfigurere skabelonerne, så du kan bruge udskudt behandling.
    - **Låst ordrehåndtering** – Vælg, hvordan salgsordrer, der aktuelt er låst, skal behandles af andre brugere eller processer:

        - *Vent, indtil ordrer låses op* – systemet skal vente, indtil ordrerne låses op, før de frigives til lagerstedet. I dette tilfælde kan det tage mere tid at frigive til lagerstedet.
        - *Spring låste ordrer over* – Systemet skal springe låste ordrer over.

    - **Gyldige ordretyper** – Vælg de typer salgsordrer, der skal medtages i et batch.
    - **Kreditmaksimumtype** – Vælg, om kontrol af kreditmaksimum skal udføres under processen for frigivelse til lagersted, og angiv de posteringsoplysninger, der skal medtages i kontrollerne, hvis kontrollerne skal udføres.

1. Hvis du vil styre, hvilke ordrer der skal behandles, skal du vælge **Filter** i oversigtspanelet **Poster, der skal medtages**. Der vises en standarddialogboks for forespørgsler, hvor du kan definere udvælgelseskriterier, sorteringskriterier og joinforbindelser. Felterne fungerer på samme måde som for andre typer af forespørgsler i Microsoft Dynamics 365 Supply Chain Management.
1. På oversigtspanelet **Kør i baggrunden** skal du vælge, om jobbet, så det kører i batchtilstand, og/eller konfigurere en tilbagevendende tidsplan. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK**, hvis du vil anvende indstillingerne og igangsætte frigivelse til lagerstedsproces.

For at konfigurere et batchjob til frigivelse af overførselsordrer, skal du gøre følgende:

1. Gå til **Lagerstedsstyring \> Frigiv til lagersted \> Automatisk frigivelse af flytteordrer**.
1. Angiv følgende felter i dialogboksen **Automatisk frigivelse af overførselsordre** i oversigtspanelet **Parametre**:

    - **Antal til frigivelse** - Vælg om hele antallet skal frigives, eller om det fysisk reserverede antal skal frigives til lagerstedet.
    - **Tillad frigivelse af delvist frigivne ordrer** – Angiv, om restantal for delvist frigivne ordrer skal frigives til lagerstedet.
    - **Gruppere versioner efter destinationslagersted** – Angiv, om systemet skal frigive alle flytteordrer samtidig, eller om flytteforslagslinjerne skal grupperes efter destinationslagersted, og derefter frigives hver gruppe til lagerstedet særskilt.

1. Hvis du vil styre, hvilke ordrer der skal behandles, skal du vælge **Filter** i oversigtspanelet **Poster, der skal medtages**. Der vises en standarddialogboks for forespørgsler, hvor du kan definere udvælgelseskriterier, sorteringskriterier og joinforbindelser. Felterne fungerer på samme måde som for andre typer af forespørgsler i Supply Chain Management.
1. På oversigtspanelet **Kør i baggrunden** skal du vælge, om jobbet, så det kører i batchtilstand, og/eller konfigurere en tilbagevendende tidsplan. Felterne fungerer på samme måde som for andre typer af [baggrundsjob](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Vælg **OK**, hvis du vil anvende indstillingerne og igangsætte frigivelse til lagerstedsproces.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
