---
title: Likviditetsbudget
description: Dette emne indeholder en oversigt over likviditetsbudgetteringsprocessen. I emnet beskrives også, hvordan likviditetsbudgettering er integreret med andre moduler i systemet.
author: panolte
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7d462992816a5a2dee73979ed4cb1521ca4ce4f7
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945748"
---
# <a name="cash-flow-forecasting"></a>Likviditetsbudget

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Du kan bruge funktionerne til budgettering af likviditet til at analysere kommende likviditets- og valutabehov, så du kan anslå virksomhedens fremtidige likviditetsbehov. Udfør følgende opgaver for at få en budgettering af likviditeten:

- Identificer og angiv alle likviditetskonti. Likviditetskonti er virksomhedens konti til kontanter/likvider eller tilsvarende midler.
- Konfigurer funktioner for forkalkulation af posteringer, der har indflydelse på virksomhedens likvide konti.

Når du har fuldført disse opgaver, kan du beregne og analysere likviditetsbudgetter og fremtidige valutabehov.

## <a name="cash-flow-forecasting-integration"></a>Integration af likviditetsbudget

Likviditetsbudgetter kan integreres med Finans, Kreditor, Debitor, Debitor, Budgettering og lagerstyring. Budgetteringsprocessen bruger posteringsoplysninger, der angives i systemet, og beregningsprocessen budgetterer hver posterings forventede påvirkning af likviditeten. Følgende typer posteringer tages i betragtning ved beregning af likviditeten:

- **Salgsordrer** – Salgsordrer, der endnu ikke er faktureret, og som resulterer i fysisk eller økonomisk salg.
- **Fritekstfakturaer** – Fritekstfakturaer, der endnu ikke er bogført, og som resulterer i økonomisk salg. 
- **Indkøbsordrer** – Indkøbsordrer, der endnu ikke er faktureret, og som resulterer i fysiske eller økonomiske indkøb.
- **Debitor** – Åbne debitorposteringer (fakturaer, der endnu ikke er betalt).
- **Kreditor** – Åbne kreditorposteringer (fakturaer, der endnu ikke er betalt).
- **Finansposteringer** – Posteringer, hvor det er angivet, at der sker en fremtidig postering.
- **Budgetregisterposter** – Budgetregisterposteringer, der er valgt til likviditetsbudgetter.
- **Behovsprognose** – Lagerbudgetmodellinjer, der er valgt til likviditetsbudgetter.
- **Forsyningsprognoser** – Lagerbudgetmodellinjer, der er valgt til likviditetsbudgetter.
- **Ekstern datakilde** – Eksterne data, der angives eller importeres til likviditetsbudgetter ved hjælp af regnearksskabeloner.
- **Projektprognoser** – Projektstyring og regnskabsprognoser ved hjælp af budgetmodel.
- **Pengestrøm for betalinger til momsmyndigheder** – Forventet betalingsbeløb til momsmyndigheder og timing, der resulterer i økonomiske betalinger. Aktivér funktionen Pengestrøm for betalinger til momsmyndigheder.

## <a name="configuration"></a>Konfiguration

Du kan konfigurere likviditetsbudgetteringsprocessen på siden **Opsætning af likviditetsbudget**. På denne side kan du angive de likviditetskonti, der skal spores, og standardbudgetteringsfunktionsmåder for hvert område.

### <a name="general-ledger"></a>Finans

Du skal først definere de likviditetskonti, du vil spore under likviditetsbudgetteringen. Disse likviditetskonti er typisk hovedkonti, der er tilknyttet de bankkonti, der skal modtage kontanter til udbetaling. På siden **Opsætning af likviditetsbudget** skal du under fanen **Finans** vælge de hovedkonti, der skal medtages til budgettering. Hvis en bankkonto er knyttet til hovedkontoen på siden **Bankkonto**, vises det i feltet **Bankkonto**.

Du kan oprette et afhængigt likviditetsbudget til en hovedkonto, der indeholder posteringer, der er direkte relateret til posteringer i en anden hovedkonto. Hver linje, du tilføjer til afsnittet **I de afhængige konti**, opretter et likviditetsbudgetbeløb på en afhængig hovedkonto. Dette beløb er en procentdel af de likviditetsbeløb til den primære hovedkonto, du har valgt.

Først skal du indstille feltet **Hovedkonto** til den primære hovedkonto, hvor posteringer først forventes udført. Indstil feltet **Afhængig hovedkonto** til den konto, der påvirkes af den første postering i forhold til den primære hovedkonto. Angiv relevante værdi i de øvrige felter på linjen. Du kan ændre værdien i feltet **Procent**, så den afspejler effekten af den primære hovedkonto på den afhængige hovedkonto. Når det drejer sig om salgsprognoser eller købsbudgetter, skal du vælge en værdi for **Betalingsbetingelse**, der er typisk for de fleste debitorer eller kreditorer. Indstil feltet **Bogføringstype** til den forventede bogføringstype, der er relateret til likviditetsbudgettet.

### <a name="accounts-payable"></a>Kreditor

Du kan beregne købsbudgettet ved hjælp af konfigurationsindstillingerne under fanen **Kreditor** på siden **Opsætning af likviditetsbudget**. Før du kan konfigurere likviditetsbudgettering for Kreditor, skal du konfigurere betalingsbetingelser, kreditorgrupper og kreditorposteringsprofiler.

I afsnittet **Budgetteringsstandarder for indkøb** kan du vælge standardkøbsfunktioner for likviditetsbudgettering. Tre felter afgør tiden for, hvornår påvirkningen af likviditeten: **Tid mellem leveringsdato og fakturadato**, **Betalingsbetingelser** og **Tid mellem fakturaens forfaldsdato og betalingsdato**. Budgettet bruger kun standardindstillingen for feltet **Betalingsbetingelser**, hvis der ikke blev angivet en værdi ved posteringen. Brug en betalingsbetingelse til at beskriver det mest almindelige antal dage for hver del af processen.

Feltet **Likviditetskonto for betalinger** specificerer den likviditetskonto, der oftest bruges til betalinger. Brug feltet **Procent af beløb, der skal fordeles til likviditetsbudget** til at angive, om der skal bruges en procentdel af beløbene under budgetteringen. Lad feltet være tomt, hvis det fulde posteringsbeløb skal bruges til budgetteringen.

Du kan tilsidesætte standardindstillingen for **Tid mellem fakturaens forfaldsdato og betalingsdato** for bestemte kreditorgrupper. Budgettet bruger standardværdien fra afsnittet **Budgetteringsstandarder for indkøb**, medmindre en anden værdi er angivet for den kreditorgruppe, der er relateret til kreditoren ved posteringen. Hvis du vil tilsidesætte standardværdien, skal du vælge en kreditorgruppe og derefter angive den nye værdi for feltet **Indkøbstid**.

Du kan tilsidesætte standardindstillingen for feltet **Likviditetskonto** for specifikke kreditorbogføringsprofiler. Budgettet bruger standardværdien fra afsnittet **Budgetteringsstandarder for indkøb**, medmindre der er angivet en anden likviditetskonto for den posteringsprofil, der er relateret til kreditoren ved posteringen. Du kan tilsidesætte standardværdien ved at vælge en posteringsprofil og derefter angive den likviditetskonto, som forventes at blive påvirket.

### <a name="accounts-receivable"></a>Debitor

Du kan beregne salgsbudgettet ved hjælp af konfigurationsindstillingerne under fanen **Debitor** på siden **Opsætning af likviditetsbudget**. Før du kan konfigurere likviditetsbudgettering for Debitor, skal du konfigurere betalingsbetingelser, debitorgrupper og debitorposteringsprofiler.

I afsnittet **Salgsbudgetstandarder** kan du vælge standardsalgsfunktioner for likviditetsbudgettering. Tre felter afgør tiden for, hvornår påvirkningen af likviditeten: **Tid mellem afsendelsesdato og fakturadato**, **Betalingsbetingelser** og **Tid mellem fakturaens forfaldsdato og betalingsdato**. Budgettet bruger kun standardindstillingen for feltet **Betalingsbetingelser**, hvis der ikke blev angivet en værdi ved posteringen. Brug en betalingsbetingelse til at beskriver det mest almindelige antal dage for hver del af processen. 

Feltet **Likviditetskonto for betalinger** specificerer den likviditetskonto, der oftest bruges til betalinger. Brug feltet **Procent af beløb, der skal fordeles til likviditetsbudget** til at angive, om der skal bruges en procentdel af beløbene under budgetteringen. Lad feltet være tomt, hvis det fulde posteringsbeløb skal bruges til budgetteringen.

Du kan tilsidesætte standardindstillingen for **Tid mellem fakturaens forfaldsdato og betalingsdato** for bestemte debitorgrupper. Budgettet bruger standardværdien fra afsnittet **Salgsbudgetstandarder**, medmindre en anden værdi er angivet for den debitorgruppe, der er relateret til debitoren ved posteringen. Hvis du vil tilsidesætte standardværdien, skal du vælge en debitorgruppe og derefter angive den nye værdi for feltet **Salgstid**.

Du kan tilsidesætte standardindstillingen for feltet **Likviditetskonto** for specifikke debitorbogføringsprofiler. Budgettet bruger standardværdien fra afsnittet **Salgsbudgetstandarder**, medmindre der er angivet en anden likviditetskonto for den posteringsprofil, der er relateret til debitoren ved posteringen. Du kan tilsidesætte standardværdien ved at vælge en posteringsprofil og derefter angive den likviditetskonto, som forventes at blive påvirket.

### <a name="budgeting"></a>Budgettering

Budgetter, der er oprettet ud fra budgetmodeller, kan medtages i likviditetsbudgetter. Under fanen **Budgettering** på siden **Opsætning af likviditetsbudget** skal du vælge de budgetmodeller, der skal medtages i budgettet. Nye poster i budgetregisteret medtages som standard i budgetter, når budgetmodellen er aktiveret til likviditetsbudgettering.

Budgetregisterposter kan medtages i likviditetsbudgettet individuelt via tilpasning. Når du føjer kolonnen "Medtag i likviditetsbudgetter" til siden **Budgetregisterpost**, overskriver systemet indstillingerne på **opsætningssiden for likviditetsbudgetter**, så der medtages en individuel budgetregisterpost i budgettet.


### <a name="inventory-management"></a>Lagerstyring

Lagerforsynings- og behovsbudgetter kan medtages i likviditetsbudgetter. Under fanen **Lagerstyring** på siden **Opsætning af likviditetsbudget** skal du vælge den budgetmodel, der skal medtages i likviditetsbudgettet. Inkludering i likviditetsbudgettering kan overskrives på individuelle forsynings- og behovsbudgetlinjer.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Konfigurere dimensioner for likviditetsbudgettering
En ny fane på siden **Konfiguration af likviditetsbudgettering** giver dig mulighed for at styre, hvilke økonomiske dimensioner der skal bruges til filtrering i arbejdsområdet **Likviditetsbudgettering** . Denne fane vises kun, når funktionen Likviditetsbudgetter er aktiveret.

Under fanen **Dimensioner** skal du vælge på den liste over dimensioner, der skal bruges til filtrering, og bruge piletasterne til at flytte dem til højre kolonne. Der kan kun vælges to dimensioner til filtrering af data i likviditetsbudgettet. 

### <a name="setting-up-external-source"></a>Konfigurere ekstern kilde
Eksterne data kan indtastes eller importeres i likviditetsbudgetter. Før eksterne data angives eller importeres, skal der konfigureres eksterne kilder. Under fanen **Ekstern kilde** skal du konfigurere eksterne likviditetskategorier. En kategori kan enten være **Udgående** eller **Indgående**. **Likviditet** skal vælges som bogføringstype. I gitteret **Indstillinger for juridisk enhed** skal du vælge de juridiske enheder og de tilsvarende hovedkonti, som de eksterne likviditetskategorier gælder for.

### <a name="project-management-and-accounting"></a>Projektstyring og regnskab

I version 10.0.17 giver en ny funktion mulighed for integration med projektstyring og regnskab og likviditetsbudgettering. I arbejdsområdet **Funktionsstyring** skal du aktivere funktionen **Likviditetsprojektbudget** for at medtage de budgetterede omkostninger og indtægter i likviditetsbudgettet. Vælg de projekttyper og posteringstyper, der skal medtages i likviditetsbudgettet, under fanen **Projektstyring og regnskab** på siden **Opsætning af likviditetsbudget**. Vælg derefter projektprognosemodellen. En undermodel af typen reduktion fungerer bedst. De likviditetskonti, der blev angivet i debitoropsætningen, bruges som standardlikviditetskonti. Du behøver derfor ikke angive standardlikviditetskonti, når du opretter likviditetsbudgettet. En budgetmodel kan også bruges, men der kan kun vælges én type på siden **Opsætning af likviditetsbudget** til projektstyring og regnskab. En budgetmodel giver mest fleksibilitet, når der bruges Projektstyring og regnskab eller Project Operations.

Når funktionen til likviditetsprojektbudget er aktiveret, kan du få vist likviditetsbudgettet for hvert projekt på siden **Alle projekter**. Vælg **Likviditetsbudget** i gruppen **Prognose** under fanen **Planlæg** i handlingsruden. I arbejdsområderne **Oversigt over kontanter** (se afsnittet om [Rapportering](#reporting) senere i dette emne) viser posteringstypen Projektprognose indgående (projektbudgetindtægter) og udgående pengestrømme (projektbudgetomkostninger). Beløbene kan kun medtages, hvis feltet **Projektstadie** i arbejdsområderne **Oversigt over kontanter** er angivet til **I gang**.

Projektposteringer medtages stadig i likviditetsbudgettet på flere måder, uanset om funktionen **Likviditetsprojektbudget** er aktiveret. Bogførte projektfakturaer medtages i budgettet som en del af åbne debitorposteringer. Projektdefinerede salgsordrer og indkøbsordrer medtages i budgettet som åbne ordrer, når de er angivet i systemet. Du kan også overføre projektbudgetter til en finansbudgetmodel. Denne finansbudgetmodel medtages derefter i likviditetsbudgettet som en del af posterne i budgetregisteret. Hvis du har aktiveret funktionen **Likviditetsprojektprognose**, skal du ikke overføre projektprognoser til en finansbudgetmodel, da denne handling bevirker, at projektprognoserne tælles to gange.

### <a name="sales-tax-authority-payments"></a>Betalinger til momsmyndigheder 

Funktionen Pengestrøm for betalinger til momsmyndigheder forudsiger momsbetalingers påvirkning af likviditet. Den bruger ubetalte momsposteringer, momsafregningsperioder og momsbetalingsbetingelser for momsperioden til at forudsige datoen og beløbet for likviditetsbetalinger. 

### <a name="calculation"></a>Beregning

Før du kan få vist likviditetsbudgetteringsanalyser, skal du køre likviditetsberegningsprocessen. Beregningsprocessen kan beregne den fremtidige indvirkning af likvider, der er angivet.

Beregn likviditetsbudgettet ved hjælp af siden **Beregn likviditetsbudgetter**. Du kan beregne enten det fulde likviditetsbudget eller et trinvist likviditetsbudget. 

- Hvis du vil fjerne alle likviditetsbudgetposteringer og genberegne dem, kan du indstille feltet **Beregningsmetode for likviditetsbudget** til **Samlet**. Det anbefales, at du bruger denne fremgangsmåde, hvis du ikke har opdateret likviditetsbudgettet i lang tid. 
- For at opdatere de eksisterende likviditetsoplysninger for nye posteringer, skal du indstille feltet **Beregningsmetode for likviditetsbudget** til **Ny**. Siden viser den dato, hvor likviditetsberegningen sidst blev kørt.

Du kan også bruge batchbehandling til likviditetsbudgettering. For at sikre, at budgetteringsanalyser opdateres regelmæssigt, kan du konfigurere en tilbagevendende batchproces til likviditetsbudgetberegning.

I version 10.0.13 blev der frigivet en forbedring til beregningsprocessen, der bruger procesautomatiseringsstrukturen til at planlægge jobbet til likviditetsberegning. Dette aktiveres ved hjælp af funktionen **Automatisering af likviditetsbudget** i arbejdsområdet **Funktionsstyring**. Når den er aktiveret, skal du vælge linket **Automatisering af likviditetsbudget** for at få vist den nye automatiseringsside, hvor du kan planlægge processen for likviditetsberegning. Hvis du vil oprette en ny plan for likviditetsbudgetter, skal du vælge **Opret ny procesautomatisering** og derefter vælge **Automatisering af likviditetsbudget** i rullemenuen **Planlægningstype**. Du skal angive en tidsplan for hvert af de firmaer, du opdaterer data til likviditetsbudgettet for.  Denne side viser også, hvilke automatiseringsjobs for likviditetsbudgettet der afventer, og hvornår det sidste job blev fuldført.  

> [!NOTE] 
> Hvis eksisterende batchjob allerede er planlagt til likviditetsbudgetter, modtager du en fejlmeddelelse, og du vil ikke kunne aktivere denne funktion. Eksisterende batchjob skal ryddes, før du kan aktivere denne funktion. 

Du kan finde flere oplysninger under [Procesautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Rapportering

Når likviditetsbudgettet er beregnet, skal du opdatere de tilknyttede enhedsoplysninger for analyserapportering. På siden **Enhedslager** skal du vælge målet **LedgerCovLiquidityMeasurement samlet** og derefter klikke på **Opdater**.

Der er to arbejdsområder, der indeholder likviditetsbudgetteringsdata. Et arbejdsområde indeholder data for alle firmaer, og det andet arbejdsområde indeholder kun data for det aktuelle firma.

Adgang til arbejdsområdet for alle firmaer kontrolleres via pligten **Vis pengestrømmens arbejdsområde for alle firmaer**. Som standard er arbejdsområdet **Oversigt over kontanter - alle firmaer** tilgængeligt for følgende roller:

- Administrerende direktør
- Økonomidirektør
- Finansinspektør

Adgang til arbejdsområdet for det aktuelle firma kontrolleres via pligten for arbejdsområdet **Vis pengestrømmens aktuelle firmaarbejdsområde**. Som standard er arbejdsområdet **Oversigt over kontanter – aktuelt firma** tilgængeligt for følgende roller:

- Bogholder
- Regnskabschef
- Regnskabsansvarlig
- Kreditorchef
- Debitorchef

Arbejdsområdet **Oversigt over kontanter – alle firmaer** viser likviditetsbudgetteringsanalyser i systemvalutaen. Systemvalutaen og systemets valutakurstypen, der bruges til analyser, defineres på siden **Systemparametre**. Dette arbejdsområde viser en oversigt over likviditetsbudgettering og bankkontosaldi for alle firmaer. Et diagram over indgående og udgående pengestrømme giver et overblik over de fremtidige kontantbevægelser og -saldi i systemvalutaen sammen med detaljerede oplysninger om de budgetterede posteringer. Du kan også se saldi for budgetteret valuta.

Arbejdsområdet **Oversigt over kontanter - aktuelt firma** viser likviditetsbudgetteringsanalyser i firmaets definerede regnskabsvaluta. Den regnskabsvaluta, der bruges til analyser, defineres på siden **Finans**. Dette arbejdsområde viser en oversigt over likviditetsbudgettering og bankkontosaldi for det aktuelle firma. Et diagram over indgående og udgående pengestrømme giver et overblik over de fremtidige kontantbevægelser og -saldi i regnskabsvalutaen sammen med detaljerede oplysninger om de budgetterede posteringer. Du kan også se saldi for budgetteret valuta.

Du kan finde flere oplysninger om likviditetsbudgetteringsanalyser i [Power BI-indhold for oversigt over kontanter](Cash-Overview-Power-BI-content.md).

Desuden kan du få vist likviditetsbudgetteringsdata for bestemte konti, ordrer og varer på de følgende sider:

- **Råbalance**: Vælg **Likviditetsbudgetter** for at få vist fremtidige pengestrømme for den valgte hovedkonto.
- **Alle salgsordrer**: Under fanen **Faktura** skal du vælge **Likviditetsbudgetter** for at få vist den budgetterede påvirkning af kontanter for den valgte salgsordre.
- **Alle indkøbsordrer**: Under fanen **Faktura** skal du vælge **Likviditetsbudgetter** for at få vist den budgetterede påvirkning af kontanter for den valgte indkøbsordre.
- **Forsyningsprognose**: Vælg **Likviditetsbudgetter** for at få vist fremtidige pengestrømme, der er knyttet til den valgte vareforsyningsprognose.
- **Behovsprognose**: Vælg **Likviditetsbudgetter** for at få vist fremtidige pengestrømme, der er knyttet til den valgte varebehovsprognose.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
