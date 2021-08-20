---
title: Lagerbudgetter
description: I dette emne beskrives den funktion for udbuds- og efterspørgselsprognoser, der kan bruges til at oprette lagerbudgetter i Microsoft Dynamics 365 Supply Chain Management.
author: crytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0919706ddcc70fecd15df6bf1cbdd58fe9a8e337b2d45cd61a4fb9d821e4114
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757800"
---
# <a name="inventory-forecasts"></a>Lagerbudgetter

[!include [banner](../includes/banner.md)]

I dette emne beskrives, hvordan du kan se og oprette lagerbudgetter. Du kan oprette og se linjer i udbuds- og efterspørgselsprognosen for varer, varegrupper, varefordelingsnøgler, debitorkonti, debitorgrupper, kreditorkonti og kreditorgrupper.

For hver budgetlinje kan du vælge den budgetmodel, der bruges. Du kan derefter angive varen eller varegruppen samt antallet eller transaktionsbeløbet. Du kan også konfigurere en tidsplan for fordeling af budgetantallet.

Linjerne i udbuds- og efterspørgselsprognosen opretter et lagerbudget for samme kombination af en vare og en model. Dette lagerbudget repræsenterer en saldo mellem udbud og efterspørgsel, der er angivet for samme vare. Det kan ikke redigeres. Lagerbudgettet hjælper lagerstyringsteamet med at gennemgå forventede ændringer af lagerbeholdningen af en vare i løbet af den kommende periode, der er udarbejdet budget for.

Når du har angivet din udbud og/eller efterspørgsel, kan du udføre hovedplanlægning for at beregne bruttobehov for materialer og kapacitet og for at oprette ordreforslag.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Se og manuelt angive budgetlinjer

Brug denne procedure til manuelt at oprette budgetlinjer for produkter.

Budgetlinjer kan også oprettes på andre måder:

- [Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md).
- [Importere historiske data til behovsprognoser](import-historical-data.md).
- [Generere prognosen ved at anvender en Microsoft Azure Machine Learning-webtjeneste](demand-forecasting-setup.md).
- [Importere udbuds- og efterspørgselsprognoselinjer ved hjælp af datastyringsstrukturen (dataenhederne ForecastDemandForecastEntryStaging og ForecastSupplyForecastEntryStaging)](../../dev-itpro/data-entities/data-entities-data-packages.md).

Som tabellen i trin 1 viser, er der forskellige måder at få adgang til de sider, der bruges.

1. Afhængigt af, hvilken type enhed du vil oprette en prognose for, og den type prognose, du vil oprette, skal du åbne en side med udbud, efterspørgsel eller lagerbudget som beskrevet i følgende tabel.

    | Objekt | Instruktioner |
    |---|---|
    | Frigivne produkter | <ol><li>Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</li><li>Vælg det produkt, der skal oprettes et budget for.</li><li>I gruppen **Prognose** under fanen **Plan** i handlingsruden skal du vælge **Behovsprognose**, **Forsyningsprognose** eller **Lagerbudget** afhængigt af, hvilken type prognose du vil arbejde med.</li></ol> |
    | Frigivne produktvarianter | <ol><li>Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produktvarianter**.</li><li>Vælg den variant, der skal oprettes et budget for.</li><li>I gruppen **Prognose** under fanen **Plan** i handlingsruden skal du vælge **Behovsprognose**, **Forsyningsprognose** eller **Lagerbudget** afhængigt af, hvilken type prognose du vil arbejde med.</li></ol> |
    | Varegrupper | <ol><li>Gå til **Lagerstyring \> Opsætning \> Lager \> Varegrupper**.</li><li>Vælg den varegruppe, der skal oprettes et budget for.</li><li>I handlingsruden skal du vælge **Budgettering \> Behov**, **Budgettering \> Forsyning** eller **Budgettering \> Lagerbudget** afhængigt af, hvilken type prognose du vil arbejde med.</li></ol> |
    | Varefordelingsnøgler | <ol><li>Gå til **Lagerstyring \> Opsætning \> Prognose**.</li><li>Vælg den varefordelingsnøgle, der skal oprettes et budget for.</li><li>Vælg **Behovsprognose** i handlingsruden.</li></ol> |
    | Debitorer | <ol><li>Gå til **Varedisponering \> Budgettering \> Manuel indtastning af prognose \> Debitorer**.</li><li>Vælg den debitor, der skal oprettes et budget for.</li><li>Vælg **Definer behovsprognose** i handlingsruden.</li></ol> |
    | Debitorgrupper | <ol><li>Gå til **Varedisponering \> Budgettering \> Manuel indtastning af prognose \> Debitorgrupper**.</li><li>Vælg den debitorgruppe, der skal oprettes et budget for.</li><li>Vælg **Definer behovsprognose** i handlingsruden.</li></ol> |
    | Kreditorer | <ol><li>Gå til **Varedisponering \> Budgettering \> Manuel indtastning af prognose \> Kreditorer**.</li><li>Vælg den kreditor, der skal oprettes et budget for.</li><li>Gå til handlingsruden, og vælg **Inddatering** for at åbne siden **Forsyningsprognose**.</li></ol> |
    | Kreditorgrupper | <ol><li>Gå til **Varedisponering \> Budgettering \> Manuel indtastning af prognose \> Kreditorgrupper**.</li><li>Vælg den kreditorgruppe, der skal oprettes et budget for.</li><li>Gå til handlingsruden, og vælg **Inddatering** for at åbne siden **Forsyningsprognose**.</li></ol> | 
    | Alle linjer | <ul><li>Gå til **Varedisponering \> Budgettering \> Behovsprognoselinjer** eller **Varedisponering \> Budgettering \> Forsyningsprognoselinjer** afhængigt af den type prognose du vil arbejde med.</li></ul> |

    Afhængigt af dit valg vises siden **Forsyningsprognose** eller **Behovsprognose**. Den viser eventuelle eksisterende budgetlinjer for den post, du har valgt, før du åbnede siden.

1. Vælg **Ny** i handlingsruden for at tilføje en budgetlinje i gitteret i øverste del af siden.
1. Vælg den budgetmodel, der skal bruges, i feltet **Model** på den nye linje. Angiv derefter andre nødvendige oplysninger, f.eks. vare, varegruppe, debitor- eller kreditorkonto eller -gruppe, vareantal eller det samlede transaktionsbeløb. Du kan finde fuldstændige oplysninger om de felter, der er tilgængelige på siderne **Forsyningsprognose** og **Behovsprognose**, i de senere afsnit i dette emne.
1. Hvis du vil fordele budgettet hen over perioden, skal du vælge **Fordel prognose** på værktøjslinjen under fanen **Oversigt**.
1. I gitteret **Tildeling** skal du gennemgå den tidshorisont og de tidsintervaller, der bruges til at distribuere budgetantallene.

## <a name="supply-forecast-lines"></a>Forsyningsprognoselinjer

Med forsyningsprognosen kan du oprette en plan for varer, der skal købes. Den fortæller indkøbs- og forsyningsassistenter, hvad de forventes at bestille.

Du kan angive en forsyningsprognose efter vare, varegruppe, varefordelingsnøgle, kreditor og kreditorgruppe. Du kan finde flere oplysninger om alle de måder, du kan åbne siden **Forsyningsprognose** for forskellige enheder og poster på, i afsnittet [Se og manuelt angive budgetlinjer](#manual-entry) tidligere i dette emne.

Den øverste del af siden **Forsyningsprognose** indeholder et gitter med forsyningsprognoselinjer og et sæt faner, som du kan bruge til at se og angive flere oplysninger om en valgt budgetlinje. Den nederste del af siden indeholder et **Tildeling**-gitter.

Følgende undersektioner beskriver alle de felter, der er tilgængelige under hver fane, og alle de kommandoer, der er tilgængelige i sidens handlingsrude og på værktøjslinjen under fanen **Oversigt**.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Kommandoer i handlingsruden på siden Forsyningsprognose

I følgende tabel beskrives de kommandoer, der er tilgængelige i handlingsruden på siden **Forsyningsprognose**.

| Kommando | Betegnelse |
|---|---|
| Gem | Gem de aktuelle indstillinger. |
| Redigér | Aktivér indstillinger på siden, så de kan redigeres. |
| Nye | Tilføj en prognoselinje i det øverste gitter. |
| Delete | Fjern den valgte budgetlinje fra det øverste gitter. |
| Budgetsaldi | Få vist de budgetsaldi, der er beregnet for den valgte linjes model-id for det aktuelle regnskabsår. Saldi er opdelt efter periode (måned). |
| Likviditetsbudgetter | Se de prognosetransaktioner, der er tildelt finansmodulet. Du kan finde flere oplysninger under [Likviditetsbudget](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Lager \> Vis dimensioner | Vælg de lagerdimensioner, der skal vises i gitteret, under fanen **Oversigt**. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Værktøjslinjekommandoer under fanen Oversigt på siden Forsyningsprognose

I følgende tabel beskrives de kommandoer, der er tilgængelige på værktøjslinjen under fanen **Oversigt** på siden **Forsyningsprognose**.

| Kommando | Betegnelse |
|---|---|
| Fordel prognose | Hvis du bruger en fordelingsmetode, skal du generere de enkelte planlægningslinjer til budgetposteringen. Linjens antal fordeles så efter dato (i overensstemmelse med de valgte tidsintervaller), antal og beløb for hele tidshorisonten. |
| Masseopdatering | Åbn siden **Rediger budgetposter**. (Se sektionen [Masseopdatere budgetposter](#bulk-update) senere i dette emne). |
| Lagerbudget | Åbn en visning af siden **Lagerbudget**, der er filtreret for den valgte kombination af vare/model. (Se afsnittet [Lagerbudget](#inventory-forecast) senere i dette emne). |
| Opret varebehov | Åbn en dialogboks, hvor du kan oprette varekrav, salgsordrer eller varekladdelinjer for projektrelaterede budgetposter. Selvom denne kommando kan bruges til både forsyningsprognoselinjer og behovsprognoselinjer, kan den ikke bruges på siden **Forsyningsprognose**. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Fanen Oversigt på siden Forsyningsprognose

Felterne under fanen **Oversigt** på siden **Forsyningsprognose** er beskrevet i følgende tabel.

| Felt | Betegnelse |
|---|---|
| **Model** | Den budgetmodel, som posteringen er knyttet til. |
| **Dato** | Transaktionens startdato. |
| **Kreditorkonto** | Den kreditorkonto, som transaktionen er knyttet til. |
| **Leverandørgruppe** | Den kreditorgruppe, som transaktionen er knyttet til. |
| **Varenummer** | Identifikationen for varen. |
| **Varegruppe** | Den varegruppe, som transaktionen er knyttet til. |
| **Varefordelingsnøgle** | Den varefordelingsnøgle, der er tilknyttet budgettet. |
| **Fastvægtantal** | Budgetantallet i den angivne fastvægtenhed. |
| **Fastvægtenhed** | Den fastvægtenhed, som varen købes i. Værdien hentes automatisk fra vareopsætningen. |
| **Mængde** | Budgetantallet i den angivne købsenhed. |
| **Enhed** | Den enhed, som varen er købt i. Værdien hentes automatisk fra vareopsætningen. Du kan dog ændre den, hvis der er konfigureret enhedsomregninger. |
| **Beløb** | Det bruttobeløb, minus rabatter, som budgetposteringen bidrager med til budgettet. |
| **Valuta** | Den valuta, der bruges til budgetposten. Standardvalutaen angives automatisk, men du kan vælge en anden valuta. |
| (Andre dimensioner) | Yderligere dimensioner kan vises som kolonner i gitteret. Vælg **Vis dimensioner** i handlingsruden for at vælge de ekstra dimensioner, der vises. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Fanen Generelt på siden Forsyningsprognose

Fanen **Generelt** viser yderligere oplysninger om den linje, der aktuelt er valgt under fanen **Oversigt**. Nogle af disse oplysninger gentages fra fanen **Oversigt**. I følgende tabel beskrives de felter, der er entydige for fanen **Generelt**.

| Felt | Betegnelse |
|---|---|
| Rapportér | Angiv denne indstilling til *Ja* for at medtage transaktionen i rapporter. |
| Bemærkninger | Indtast eventuelle kommentarer til budgetposten. |
| Aktive | Markér afkrydsningsfeltet for at medtage posteringen i budgetrapporter. |
| Medtag i likviditetsbudgetter | Markér afkrydsningsfeltet for at fordele budgettransaktionen til Finans. Indstillingen af dette afkrydsningsfelt kan ikke ændres for rapporteringstransaktioner. |
| Momsgruppe | Den momsgruppe, der anvendes til at angive momsen for budgetposteringen. |
| Varemomsgruppe | Den varemomsgruppe, der anvendes til at angive momsen for budgetposteringen. |
| metode | <p>Vælg den metode, der skal bruges til fordeling af budgetposteringen:</p><ul><li>**Ingen** – Der sker ingen fordeling.</li><li>**Periode** – Budgettér det samme antal for hver periode. Hvis du vælger denne værdi, skal du angive et antal i feltet **Pr.** og en tidsenhed i feltet **Enhed**.</li><li>**Nøgle** – Alloker budgettet i henhold til den periodefordelingsnøgle, du angiver i feltet **Periodenøgle**. Du kan bruge denne metode, hvis du vil tage hensyn til sæsonudsving.</li></ol>|
| Pr. | <p>Angiv det antal tidsintervaller, som budgettet rækker ud i fremtiden. Feltet er kun tilgængeligt, hvis du vælger *Periode* i feltet **Metode**.</p><p>Du kan f.eks. vælge *Periode* i feltet **Metode**, angive *1* i feltet **Pr.** og vælge *Måneder* i feltet **Enhed**. Angiv en slutdato i feltet **Slut**, der rækker et år ud i fremtiden. Der oprettes én budgetlinje for hver måned i det kommende år baseret på den vare og det antal, der er angivet i hovedlinjen.</p> |
| Enhed | Vælg enheden for tidsintervallet: *Dage*, *Måneder* eller *År*. Fordelingen svarer til det antal dage, måneder eller år, du angiver i feltet **Pr**.|
| Periodenøgle | Angiv periodefordelingsnøglen. |
| Afslut | Angiv slutdatoen ved brug af felterne **Pr.** og **Enhed**. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Fanen Vare på siden Forsyningsprognose

Fanen **Vare** viser flere vareoplysninger om den linje, der aktuelt er valgt under fanen **Oversigt**.

Gitteret øverst under fanen **Vare** gentager de vareoplysninger, der også vises under fanen **Oversigt**. Det omfatter desuden feltet **Enhedspris**, der viser købsprisen for det antal enheder, der er angivet i feltet **Enhed**. Enhedsprisen hentes automatisk fra vareopsætningen, men du kan redigere den.

Felterne under gitteret giver flere varedetaljer. Nogle af disse oplysninger gentages fra fanen **Oversigt**. I følgende tabel beskrives de felter, der er entydige for fanen **Vare**.

| Felt | Betegnelse |
|---|---|
| Prisenhed | Antallet af enheder, som købsprisen gælder for. Værdien hentes automatisk fra varetabellen, men du kan ændre den. |
| Indkøbsgebyrer | Faste gebyr på købsprisen. Gebyrerne er uafhængige af antallet. |
| Rabat % | Rabatten som en procentdel. |
| Rabatbeløb | Rabatten som et beløb pr. salgsenhed. |
| Bruttobeløb | Beløbet, hvis der ikke anvendes rabatter. |
| Mængde | Posteringsantallet i varens lagerenhed. |
| Understykliste | Styklistenummeret på en bestemt understykliste. |
| Underrute | Rutenummeret på en bestemt underrute. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Fanen Økonomiske dimensioner på siden Forsyningsprognose

Fanen **Økonomiske dimensioner** viser alle de økonomiske dimensionsværdier for den linje, der aktuelt er valgt under fanen **Oversigt**.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Fanen Lagerdimensioner på siden Forsyningsprognose

Fanen **Lagerdimensioner** viser alle de lagerdimensionsværdier for den linje, der aktuelt er valgt under fanen **Oversigt**.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Gitteret Fordeling på siden Forsyningsprognose

Hvis du bruger en varefordelingsnøgle, eller hvis du har angivet et varebudget for en eller flere fremtidige perioder, kan du fordele budgettet ved at vælge **Fordel budget** på værktøjslinjen under fanen **Oversigt**. Antallet fordeles derefter på den måde, der er angivet af linjerne i **Fordeling**-gitteret.

## <a name="demand-forecast-lines"></a>Behovsprognoselinjer

Behovsprognosen giver dig mulighed for at angive eller generere behov for en kunde. Det hjælper salgs- og marketingassistenter med at informere varedisponeringsansatte om den forventede efterspørgsel i løbet af den kommende budgetperiode.

Du kan angive en behovsprognose efter vare, varegruppe, varefordelingsnøgle, debitor og debitorgruppe. Du kan finde oplysninger om alle de måder, du kan åbne siden **Behovsprognose** for forskellige enheder og poster på, i afsnittet [Se og manuelt angive budgetlinjer](#manual-entry) tidligere i dette emne.

Den øverste del af siden **Behovsprognose** indeholder et gitter med behovsprognoselinjer og et sæt faner, som du kan bruge til at se og angive flere oplysninger om en valgt budgetlinje. Den nederste del af siden indeholder et **Tildeling**-gitter.

Følgende undersektioner beskriver alle de felter, der er tilgængelige under hver fane, og alle de kommandoer, der er tilgængelige i sidens handlingsrude og på værktøjslinjen under fanen **Oversigt**.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Kommandoer i handlingsruden på siden Behovsprognose

I følgende tabel beskrives de kommandoer, der er tilgængelige i handlingsruden på siden **Behovsprognose**.

| Kommando | Betegnelse |
|---|---|
| Gem | Gem de aktuelle indstillinger. |
| Redigér | Aktivér indstillinger på siden, så de kan redigeres. |
| Nye | Tilføj en prognoselinje i det øverste gitter. |
| Delete | Fjern den valgte budgetlinje fra det øverste gitter. |
| Budgetsaldi | Få vist de budgetsaldi, der er beregnet for den valgte linjes model-id for det aktuelle regnskabsår. Saldi er opdelt efter periode (måned). |
| Likviditetsbudget | Se de prognosetransaktioner, der skal tildeles finansmodulet. Du kan finde flere oplysninger under [Likviditetsbudget](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Vis dimensioner | Vælg de produkt-, lager- og sporingsdimensioner, der skal vises i gitteret, under fanen **Oversigt**. |
| Vis Finans | Se posterne i finansmodulet for den valgte postering. |
| Overfør tilbudslinjer | Overfør tilbudslinjer til det valgte projekt. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Værktøjslinjekommandoer under fanen Oversigt på siden Behovsprognose

I følgende tabel beskrives de kommandoer, der er tilgængelige på værktøjslinjen under fanen **Oversigt** på siden **Behovsprognose**.

| Kommando | Betegnelse |
|---|---|
| Fordel prognose | Hvis du bruger en fordelingsmetode, skal du generere de enkelte planlægningslinjer til budgetposteringen. Linjens antal fordeles så efter dato (i overensstemmelse med de valgte tidsintervaller), antal og beløb for hele tidshorisonten. |
| Masseopdatering | Åbn siden **Rediger budgetposter**. (Se sektionen [Masseopdatere budgetposter](#bulk-update) senere i dette emne). |
| Lagerbudget | Åbn en visning af siden **Lagerbudget**, der er filtreret for den valgte kombination af vare/model. (Se afsnittet [Lagerbudget](#inventory-forecast) senere i dette emne). |
| Opret varebehov | Åbn en dialogboks, hvor du kan oprette varekrav, salgsordrer eller varekladdelinjer for projektrelaterede budgetposter. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Fanen Oversigt på siden Behovsprognose

Felterne under fanen **Oversigt** på siden **Behovsprognose** er beskrevet i følgende tabel.

| Felt | Betegnelse |
|---|---|
| **Arbejdsrutinenavn** | Navnet på den batchopgave, der blev brugt til at oprette prognoselinjen. |
| **Model** | Den budgetmodel, som posteringen er knyttet til. |
| **Dato** | Transaktionens startdato. |
| **Debitorkonto** | Den debitorkonto, der er knyttet til posteringen. |
| **Kundegruppe** | Den debitorgruppe, der er knyttet til posteringen. |
| **Varenummer** | Identifikationen for varen. |
| **Produktnavn** | Beskrivelsen af varen. |
| **Varefordelingsnøgle** | Varefordelingsnøgle, der bruges i lagerbudgetfordeling. |
| **Salgsantal** | Budgetantallet i den angivne salgsenhed. |
| **Enhed** | Den enhed, som varen sælges i. |
| **Beløb** | Det bruttobeløb, uden rabatter, som budgetposteringen bidrager med til budgettet. |
| **Salgspris** | Salgsprisen for det antal enheder, der er angivet i feltet **Prisenhed**. Denne værdi hentes fra vareopsætningen, men du kan redigere den. |
| **Salgsvaluta** | Den valuta, der bruges til budgetposten. Standardvalutaen angives automatisk, men du kan vælge en anden valuta. |
| **Fastvægtantal** | Budgetantallet i den angivne fastvægtenhed. |
| **Fastvægtenhed** | Den fastvægtenhed, som varen sælges i. Værdien hentes automatisk fra vareopsætningen. |
| (Andre dimensioner) | Yderligere produkt-, lager- og sporingsdimensioner kan vises som kolonner i gitteret. Vælg **Vis dimensioner** i handlingsruden for at vælge de ekstra dimensioner, der vises. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Fanen Generelt på siden Behovsprognose

Fanen **Generelt** viser yderligere oplysninger om den linje, der aktuelt er valgt under fanen **Oversigt**. Nogle af disse oplysninger gentages fra fanen **Oversigt**. I følgende tabel beskrives de felter, der er entydige for fanen **Generelt**.

| Felt | Betegnelse |
|---|---|
| Løbenummer i behovsprognose | Det entydige nummer på behovsprognoselinjen. Dette nummer genereres ved hjælp af den nummerserie, der er valgt til behovsbudgetter på siden **Varedisponeringsparametre**. |
| Varegruppe | Den varegruppe, som transaktionen er knyttet til. |
| Rapportér | Angiv denne indstilling til *Ja* for at medtage transaktionen i rapporter. |
| Bemærkninger | Indtast eventuelle kommentarer til budgetposten. |
| Aktive | Markér afkrydsningsfeltet for at medtage posteringen i budgetrapporter. Indstillingen af dette afkrydsningsfelt kan ikke ændres for rapporteringstransaktioner. |
| Medtag i likviditetsbudgetter | Markér afkrydsningsfeltet for at fordele budgettransaktionen til Finans. Indstillingen af dette afkrydsningsfelt kan ikke ændres for rapporteringstransaktioner. Du kan finde flere oplysninger under [Likviditetsbudget](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Momsgruppe | Den momsgruppe, der anvendes til at angive momsen for budgetposteringen. |
| Varemomsgruppe | Den varemomsgruppe, der anvendes til at angive momsen for budgetposteringen. |
| metode | <p>Vælg den metode, der skal bruges til fordeling af budgetposteringen:</p><ul><li>**Ingen** – Der sker ingen fordeling.</li><li>**Periode** – Budgettér det samme antal for hver periode. Hvis du vælger denne værdi, skal du angive et antal i feltet **Pr.** og en tidsenhed i feltet **Enhed**.</li><li>**Nøgle** – Alloker budgettet i henhold til den periodefordelingsnøgle, du angiver i feltet **Periodenøgle**. Du kan bruge denne metode, hvis du vil tage hensyn til sæsonudsving.</li><ul>|
| Pr. | <p>Angiv det antal tidsintervaller, som budgettet rækker ud i fremtiden. Feltet er kun tilgængeligt, hvis du vælger *Periode* i feltet **Metode**.</p><p>Du kan f.eks. vælge *Periode* i feltet **Metode**, angive *1* i feltet **Pr.** og vælge *Måneder* i feltet **Enhed**. Angiv en slutdato i feltet **Slut**, der rækker et år ud i fremtiden. Der oprettes én budgetlinje for hver måned i det kommende år baseret på den vare og det antal, der er angivet i hovedlinjen. |
| Enhed | Vælg enheden for tidsintervallet: *Dage*, *Måneder* eller *År*. Fordelingen svarer til det antal dage, måneder eller år, du angiver i feltet **Pr**.|
| Periodenøgle | Angiv den periodefordelingsnøgle, der bruges til fordeling af budgettet. Du kan finde flere oplysninger under [Datafordeling til budgetplanlægning](../../finance/budgeting/budget-planning-data-allocation.md). |
| Afslut | Angiv slutdatoen ved brug af felterne **Pr.** og **Enhed**. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Fanen Vare på siden Behovsprognose

Fanen **Vare** viser flere vareoplysninger om den linje, der aktuelt er valgt under fanen **Oversigt**. Nogle af disse oplysninger gentages fra fanen **Oversigt**. I følgende tabel beskrives de felter, der er entydige for fanen **Vare**.

| Felt | Betegnelse |
|---|---|
| Prisenhed | Det antal salgsenheder, som salgsprisen gælder for. Værdien hentes automatisk fra varetabellen, men du kan ændre den. |
| Salgsgebyrer | Faste gebyr på salgsprisen. Gebyrerne er uafhængige af antallet. |
| Kostpris | Omkostningen for den aktuelle budgettransaktion pr. lagerenhed. Værdien hentes fra varetabellen, men du kan ændre den. |
| Rabat % | Rabatten som en procentdel. |
| Rabatbeløb | Rabatten som et beløb pr. salgsenhed. |
| Bruttobeløb | Beløbet, hvis der ikke anvendes rabatter. |
| Lagerantal | Posteringsantallet i varens lagerenhed. |
| Brug specifik stykliste | Styklistenummeret på en bestemt stykliste. |
| Brug specifik rute | Rutenummeret på en bestemt underrute. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Fanen Projekt på siden Behovsprognose

Fanen **Projekt** viser flere projektoplysninger om den linje, der aktuelt er valgt under fanen **Oversigt**. Nogle af disse oplysninger gentages fra fanen **Oversigt**, **Generelt** eller **Vare**. I følgende tabel beskrives de felter, der er entydige for fanen **Projekt**.

| Felt | Betegnelse |
|---|---|
| Projektdato | Datoen for behovsprognosetransaktionen. |
| Projekt-id | Det id for projektet, der refereres til i den aktuelle transaktion. |
| Finansieringskilde | Den finansieringskilde, der er knyttet til behovsprognosen. |
| Aktivitetsnummer | Den aktivitet, der er knyttet til behovsprognosens transaktion. |
| Kategori | Omkostningskategorien for den aktuelle transaktion. |
| Linjeegenskab | Statussen, som posteringen er tilknyttet. |
| Posterings-id | System-id'et for behovsprognosens transaktion. |
| Kostbeløb | Beløbet for behovsprognosetransaktionen. |
| Enhedspris | Prisen pr. enhed. |
| Ændret af | Identifikationen af den arbejder, der sidst har ændret den valgte transaktion. |
| Fakturadato | Angiv den forventede fakturadato. |
| Elimineringsdato | Få vist eller rediger elimineringsdatoen. Når prognosen oprettes, angives elimineringsdatoen til samme dato som slutdatoen for projektet. Hvis projektet ikke har nogen slutdato, anvendes projektdatoen. Dette felt er kun gyldigt for fastprisprojekter og investeringsprojekter. |
| Kostbetalingsdato | Angiv den forventede dato for indkøbsbetalingen. |
| Salgsbetalingsdato | Angiv den forventede dato for salgsbetalingen. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Fanen Økonomiske dimensioner på siden Behovsprognose

Fanen **Økonomiske dimensioner** viser alle de økonomiske dimensionsværdier for den linje, der aktuelt er valgt under fanen **Oversigt**.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Fanen Lagerdimensioner på siden Behovsprognose

Fanen **Lagerdimensioner** viser alle de lagerdimensionsværdier for den linje, der aktuelt er valgt under fanen **Oversigt**.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Gitteret Fordeling på siden Behovsprognose

Hvis du bruger en varefordelingsnøgle, eller hvis du har angivet et varebudget for en eller flere fremtidige perioder, kan du fordele budgettet ved at vælge **Fordel budget** på værktøjslinjen under fanen **Oversigt**. Antallet fordeles derefter på den måde, der er angivet af linjerne i **Fordeling**-gitteret.

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Lagerbudget

Siderne med forsynings- og behovsbudgetlinjer har knappen **Lagerbudget**, som åbner en visning af den **Lagerbudget**-side, der er filtreret for den samme kombination af vare/model. Dette lagerbudget repræsenterer en saldo mellem udbud og efterspørgsel, der er angivet for samme vare. Det kan ikke redigeres. Lagerbudgettet hjælper lagerstyringsteamet med at gennemgå forventede ændringer af lagerbeholdningen af en vare i løbet af den kommende periode, der er udarbejdet budget for.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Handlingsruden på siden Lagerbudget

I følgende tabel beskrives de kommandoer, der er tilgængelige i handlingsruden på siden **Lagerbudget**.

| Handling | Betegnelse |
|---|---|
| Forsyningsprognose | Åbn en visning af siden **Forsyningsprognose**, der er filtreret for den samme kombination af vare/model/dato. |
| Behovsprognose | Åbn en visning af siden **Behovsprognose**, der er filtreret for den samme kombination af vare/model/dato. |
| Lager \> Vis dimensioner | Vælg de produkt-, lager- og sporingsdimensioner, der skal vises i gitteret **Oversigt**. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Gitteret på siden Lagerbudget

I følgende tabel beskrives felterne i gitteret på siden **Lagerbudget**.

| Felt | Betegnelse |
|---|---|
| **Model** | Den budgetmodel, som posteringen er knyttet til. |
| **Varenummer** | Identifikationen for varen. |
| **Budgetdato** | Datoen for budgetposten. |
| **Budgettype** | Kilden til posteringen (*Behovsprognose* eller *Forsyningsprognose*). |
| **Fastvægtantal** | Budgetantallet i fastvægtenheden. |
| **Mængde** | Budgetantallet i lagerenheden. |
| **Akkumuleret fastvægt** | Det akkumulerede budgetantal i fastvægtenheden, når der er akkumuleret flere budgetlinjer for samme vare. |
| **Understykliste** | Styklistenummeret på en bestemt understykliste. |
| **Underrute** | Rutenummeret på en bestemt underrute. |
| (Andre dimensioner) | Yderligere dimensioner kan vises som kolonner i gitteret. Vælg **Lager \> Vis dimensioner** i handlingsruden for at vælge de ekstra dimensioner, der vises. |

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Masseopdatere budgetposter

Du kan bruge denne procedure til at behandle eksisterende budgetposteringslinjer. Du kan kopiere, redigere og slette budgetposteringslinjer.

1. Vælg **Masseopdatering** på siden med forsynings- og behovsbudgetlinjer.
1. Vælg **Filter** i dialogboksen.
1. Vælg de kriterier, der identificerer de kildebudgetdata, du vil kopiere, ændre eller slette, under fanen **Område**. Disse data kan omfatte budgetmodel, varenummer og debitorkonto.
1. Vælg **OK** for at bekræfte valget.

    Når dataene er valgt, kan du bruge dialogboksen **Rediger budgetposter** til at definere, hvordan du vil kopiere, redigere eller slette dem.

    > [!NOTE]
    > Filtreringstrinnet er en forudsætning for, at du kan bruge funktionen **Masseredigering**. Hvis du springer det over, vælges og opdateres **alle** budgetlinjer. Derfor kan du utilsigtet få dublering eller fjernelse af posteringer.

1. I sektionen **Administration** skal du vælge, om du vil kopiere, opdatere eller slette de valgte budgetposter.
1. Brug sektionen **Ændringer i felt** til at ændre parametrene for budgettet. Markér afkrydsningsfeltet for en parameter, og vælg mellem de tilgængelige indstillinger. Markér f.eks. afkrydsningsfeltet **Model**, og vælg derefter et budgetmodelnummer. Eksisterende budgetlinjer kopieres til den valgte budgetmodel.
1. Brug sektionen **Ændring af periode** til at flytte budgettets start- og slutdatoer frem eller tilbage. Markér afkrydsningsfeltet, og brug felterne for antal og periode til at definere, hvor budgetdatoerne skal flyttes hen. Du kan angive et negativt antal, hvis du vil flytte startdatoen fremad (så den er tidligere).

    Hvis du f.eks. vil udskyde startdatoen for budgetposteringen med seks måneder, skal du markere afkrydsningsfeltet, angive *6* som antal og vælge *Måneder* som periode.

1. Brug sektionen **Ret felt** til at opdatere de faktiske budgetdata. Vælg det kriterium, du vil ændre, i feltet **Felt**. Angiv en multiplikationsfaktor i feltet **Faktor**, der skal anvendes på det valgte kriterium, eller indsæt en additions- eller subtraktionskonstant. Vælg f.eks. *Antal* som kriterium, og angiv faktoren *1,5* for at multiplicere varens antal med 1,5. Du kan også indsætte en konstant på *-25* for at reducere vareantallet med 25 enheder.
1. Brug sektionen **Økonomiske dimensioner** til at opdatere de økonomiske dimensioner for budgetlinjerne. Vælg de økonomiske dimensioner, du vil ændre, og angiv derefter en værdi, der skal gælde for de valgte dimensioner.
1. Vælg **OK** for at anvende ændringerne.

## <a name="use-forecasts-with-master-planning"></a>Brug prognoser med varedisponering

Når du har indtastet efterspørgselsprognosen og/eller forsyningsprognosen, kan du medtage prognoserne under behovsplanlægningen for at tage højde for den forventede efterspørgsel og/eller forsyning i behovsplanlægningen. Når prognoser medtages i behovsplanlægningen, beregnes der bruttobehov for materialer og kapacitet, og der genereres ordreforslag.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Oprette en behovsplan, der omfatter et lagerbudget

Hvis du vil konfigurere en behovsplan, så den omfatter et lagerbudget, skal du følge disse trin.

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en eksisterende plan, eller opret en ny plan.
1. I oversigtspanelet **Generelt** skal du indstille følgende felter:

    - **Prognosemodel** – Vælg den prognosemodel, der skal anvendes. Denne model tages i betragtning, når der genereres et forsyningsforslag for den aktuelle behovsplan.
    - **Medtag forsyningsprognose** – Angiv denne indstilling til *Ja* for at medtage forsyningsprognosen i den aktuelle behovsplan. Hvis du angiver den til *Nej*, medtages der ikke forsyningsprognosetransaktioner i behovsplanen.
    - **Medtag behovsprognose** – Angiv denne indstilling til *Ja* for at medtage behovsprognosen i den aktuelle behovsplan. Hvis du angiver den til *Nej*, medtages der ikke behovsprognosetransaktioner i behovsplanen.
    - **Metode, der bruges til at reducere prognosekrav** – Vælg den metode, der skal bruges til at reducere prognosekravet. Du kan finde flere oplysninger under [Prognosereduktionsnøgler](planning-optimization/demand-forecast.md#reduction-keys).

1. I oversigtspanelet **Tidshorisonter i dage** kan du angive følgende felter for at angive den periode, som prognosen er inkluderet under:

    - **Hovedplan** – Angiv denne indstilling til *Ja* for at tilsidesætte den hovedplanstidshorisont, der stammer fra de enkelte disponeringsgrupper. Angiv værdien til *Nej* for at bruge værdierne fra de enkelte disponeringsgrupper for den aktuelle behovsplan.
    - **Prognoseperiode** – Hvis du angiver indstillingen **Hovedplan** til *Ja*, skal du angive det antal dage (fra dags dato), som behovsprognosen skal gælde for.

    > [!IMPORTANT]
    > Indstillingen **Hovedplan** understøttes ikke med Planlægningsoptimering.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Køre en behovsplan, der omfatter et lagerbudget

Hvis du vil køre en behovsplan, der omfatter et lagerbudget, skal du følge disse trin.

1. Gå til **Varedisponering \> Arbejdsområder \> Varedisponering**.
1. Angiv eller vælg den behovsplan, du konfigurerede i foregående procedure, i feltet **Behovsplan**.
1. Vælg **Kør** i feltet **Varedisponering**.
1. Angiv indstillingen **Registrer procestiden** i dialogboksen **Varedisponering** til *Ja*.
1. Indtast et antal i feltet **Antal tråde**.
1. I oversigtspanelet **Medtagne poster** skal du vælge **Filtrer**.
1. Der vises en standarddialogboks med forespørgselseditoren. Under fanen **Område** skal du vælge den række, hvor feltet **Felt** er angivet til *Varenummer*.
1. Vælg det varenummer, der skal medtages i planen, i feltet **Afgrænsning**.
1. Vælg **OK**.

Åbn siden **Bruttobehov** for at få vist de beregnede behov. I handlingsruden på siden **Frigivne produkter** under fanen **Plan** i gruppen **Behov** kan du f.eks. vælge **Bruttobehov**.

Hvis du vil have vist de oprettede ordreforslag, skal du gå til **Varedisponering \> Fælles \> Ordreforslag** og vælge den relevante hovedplan.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over behovsprognoser](introduction-demand-forecasting.md)
- [Konfigurere behovsprognoser](demand-forecasting-setup.md)
- [Generere et statistisk budgetgrundlag](generate-statistical-baseline-forecast.md)
- [Foretage manuelle justeringer af prognosegrundlaget](manual-adjustments-baseline-forecast.md)
- [Varedisponering med behovsprognoser](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
