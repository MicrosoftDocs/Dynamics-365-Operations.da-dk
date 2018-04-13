---
title: Likviditetsbudget
description: "Dette emne indeholder en oversigt over likviditetsbudgetteringsprocessen. I emnet beskrives også, hvordan likviditetsbudgettering er integreret med andre moduler i systemet."
author: saraschi2
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 9aefc79897d0abcee14c05f33516181b3eb05e55
ms.contentlocale: da-dk
ms.lasthandoff: 02/07/2018

---

# <a name="cash-flow-forecasting"></a>Likviditetsbudget

[!INCLUDE [banner](../includes/banner.md)]

Du kan bruge funktionerne til budgettering af likviditet til at analysere kommende likviditets- og valutabehov, så du kan anslå virksomhedens fremtidige likviditetsbehov. Udfør følgende opgaver for at få en budgettering af likviditeten:

- Identificer og angiv alle likviditetskonti. Likviditetskonti er virksomhedens konti til kontanter/likvider eller tilsvarende midler.
- Konfigurer funktioner for forkalkulation af posteringer, der har indflydelse på virksomhedens likvide konti.

Når du har fuldført disse opgaver, kan du beregne og analysere likviditetsbudgetter og fremtidige valutabehov.

## <a name="cash-flow-forecasting-integration"></a>Integration af likviditetsbudget

Likviditetsbudgetter kan integreres med Finans, Kreditor, Debitor, Debitor, Budgettering og lagerstyring. Budgetteringsprocessen bruger posteringsoplysninger, der angives i systemet, og beregningsprocessen budgetterer hver posterings forventede påvirkning af likviditeten. Følgende typer posteringer tages i betragtning ved beregning af likviditeten:

- **Salgsordrer** – Salgsordrer, der endnu ikke er faktureret, og som resulterer i fysisk eller økonomisk salg.
- **Indkøbsordrer** – Indkøbsordrer, der endnu ikke er faktureret, og som resulterer i fysiske eller økonomiske indkøb.
- **Debitor** – Åbne debitorposteringer (fakturaer, der endnu ikke er betalt).
- **Kreditor** – Åbne kreditorposteringer (fakturaer, der endnu ikke er betalt).
- **Finansposteringer** – Posteringer, hvor det er angivet, at der sker en fremtidig postering.
- **Budgetregisterposter** – Budgetregisterposteringer, der er valgt til likviditetsbudgetter.
- **Behovsprognose** – Lagerbudgetmodellinjer, der er valgt til likviditetsbudgetter.
- **Forsyningsprognoser** – Lagerbudgetmodellinjer, der er valgt til likviditetsbudgetter.

Selvom der er ingen direkte integration med Projektstyring og regnskab, er der flere måder at medtage projektposter i likviditetsbudgettet. Bogførte projektfakturaer medtages i budgettet som en del af åbne debitorposteringer. Projektdefinerede salgsordrer og indkøbsordrer medtages i budgettet som åbne ordrer, når de er angivet i systemet. Du kan også overføre projektbudgetter til en finansbudgetmodel. Denne finansbudgetmodel medtages derefter i likviditetsbudgettet som en del af posterne i budgetregisteret.

## <a name="configuration"></a>Variantkonfiguration

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

Budgetter, der er oprettet ud fra budgetmodeller, kan medtages i likviditetsbudgetter. Under fanen **Budgettering** på siden **Opsætning af likviditetsbudget** skal du vælge de budgetmodeller, der skal medtages i budgettet. Nye poster i budgetregisteret medtages som standard i budgetter, når budgetmodellen er aktiveret til likviditetsbudgettering. Inkludering i likviditetsbudgettering kan overskrives på individuelle poster i budgetregisteret.

### <a name="inventory-management"></a>Lagerstyring

Lagerforsynings- og behovsbudgetter kan medtages i likviditetsbudgetter. Under fanen **Lagerstyring** på siden **Opsætning af likviditetsbudget** skal du vælge den budgetmodel, der skal medtages i likviditetsbudgettet. Inkludering i likviditetsbudgettering kan overskrives på individuelle forsynings- og behovsbudgetlinjer.

### <a name="calculation"></a>Kalkulation

Før du kan få vist likviditetsbudgetteringsanalyser, skal du køre likviditetsberegningsprocessen. Beregningsprocessen kan beregne den fremtidige indvirkning af likvider, der er angivet.

Beregn likviditetsbudgettet ved hjælp af siden **Beregn likviditetsbudgetter**. Du kan beregne enten det fulde likviditetsbudget eller et trinvist likviditetsbudget. 

- Hvis du vil fjerne alle likviditetsbudgetposteringer og genberegne dem, kan du indstille feltet **Beregningsmetode for likviditetsbudget** til **Samlet**. Det anbefales, at du bruger denne fremgangsmåde, hvis du ikke har opdateret likviditetsbudgettet i lang tid. 
- For at opdatere de eksisterende likviditetsoplysninger for nye posteringer, skal du indstille feltet **Beregningsmetode for likviditetsbudget** til **Ny**. Siden viser den dato, hvor likviditetsberegningen sidst blev kørt.

Du kan også bruge batchbehandling til likviditetsbudgettering. For at sikre, at budgetteringsanalyser opdateres regelmæssigt, kan du konfigurere en tilbagevendende batchproces til likviditetsbudgetberegning.

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

Du kan finde flere oplysninger om likviditetsbudgetteringsanalyser i emnet Power BI-indhold for oversigt over kontanter.

Desuden kan du få vist likviditetsbudgetteringsdata for bestemte konti, ordrer og varer på de følgende sider:

- **Råbalance**: Vælg **Likviditetsbudgetter** for at få vist fremtidige pengestrømme for den valgte hovedkonto.
- **Alle salgsordrer**: Under fanen **Faktura** skal du vælge **Likviditetsbudgetter** for at få vist den budgetterede påvirkning af kontanter for den valgte salgsordre.
- **Alle indkøbsordrer**: Under fanen **Faktura** skal du vælge **Likviditetsbudgetter** for at få vist den budgetterede påvirkning af kontanter for den valgte indkøbsordre.
- **Forsyningsprognose**: Vælg **Likviditetsbudgetter** for at få vist fremtidige pengestrømme, der er knyttet til den valgte vareforsyningsprognose.
- **Behovsprognose**: Vælg **Likviditetsbudgetter** for at få vist fremtidige pengestrømme, der er knyttet til den valgte varebehovsprognose.


