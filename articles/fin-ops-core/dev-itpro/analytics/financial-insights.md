---
title: Økonomisk analyse
description: Økonomisk analyse bruger Microsoft Power BI til at samle økonomiske nøgletal (KPI'er), diagrammer og regnskaber.
author: kweekley
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 21d7d045c812c54d6776394ad9a0b025b55df8e1
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109106"
---
# <a name="financial-analysis"></a>Økonomisk analyse

[!include [banner](../includes/banner.md)]

**Økonomisk analyse** bruger Microsoft Power BI til at samle økonomiske nøgletal (KPI'er), diagrammer og regnskaber. Power BI er integreret i programmet. Fokus for **økonomiske analyse** er en analytisk rapportering. Personer på tværs af en organisation kan få vist, undersøge, forstå og reagere. 

**Økonomiske analyse** kombinerer data fra finansmodulet og reskontroer til at give et mere komplet billede af en organisations økonomiske tilstand.

> [!NOTE]
> Dette dokument bruger følgende Power BI-terminologi:
> 
> - **Rapport** – en enkelt .pbix-fil, hvor alle visuelle elementer på alle faner gemmes.
> - **Side** – En fane i en enkelt .pbix-fil. Hver side kan indeholde et eller flere visuelle elementer.
> - **Visuelt element** – en enkelt datakilde, f.eks. et kort, KPI, diagram, grafik, matrix eller regnskab. En side med et regnskab som et visuelt element kan ikke have andre visuelle elementer på grund af størrelsen af de data, der rapporteres om.

Arbejdsområdet **Økonomisk analyse** fokuserer på, at du kan få vist og filtrere dataene om eksisterende rapporter. Du kan tilføje nye visuelle elementer til arbejdsområdet **Økonomisk analyse**. Arbejdsområdet **Økonomiske analyse** er tilgængeligt for det aktuelle firma og alle firmaer, hvor de kan se data for alle juridiske enheder, uanset hvilke juridiske enheder rollen har adgang til.

- [Tilføje eller redigere Power BI-visualiseringer på dashboardet](/powerapps/user/add-powerbi-dashboards)

## <a name="dynamics-365-finance-setup"></a>Opsætning af Dynamics 365 Finance
**Økonomi**

Kategorierne hovedkontotype og hovedkonto bruges til at udfylde relevante standardhovedkonti i regnskabet **Balance** og de forskellige regnskaber **Resultatopgørelse** i **Økonomisk analyse**.

På siden **Hovedkonti** skal du definere din hovedkonto, så en af følgende typer knyttes til den:

- Indtægter
- Expense
- Aktiver
- Passiver
- Egenkapital

Tildel ikke nogen anden hovedkontotype, f.eks. **Balance** eller **Drift**, til dine hovedkonti. Rapportering kan ikke bestemme typen af hovedkontoen, når der er tildelt andre typer af hovedkonto, fordi de ikke tilstrækkeligt detaljerede. Typen af hovedkonto skal bestemmes for at vise passiver og indtægter som positive beløb i finansielle rapporter.

For at kunne vises på regnskaberne og få at kunne inkluderes i forskellige andre visuelle elementer, f.eks. KPI'er, skal hver hovedkonto tildeles en hovedkontokategori. Hovedkontokategorierne er blevet forbedret, så de inkluderer en visningsrækkefølge. Visningsrækkefølgen bruges specifikt i regnskaber i **økonomisk analyse**. Når du redigerer eller tilføjer en ny hovedkontokategori, kan du ændre værdien **Visningsrækkefølge** for at definere den rækkefølge, som bruges til visning af hovedkontokategorierne i et regnskab. Hvis du er nødt til at ændre visningsrækkefølgen for mange hovedkontokategorier, kan du bruge Åbn i Excel-funktionen til hurtigt at redigere og udgive ændringerne tilbage til programmet.

## <a name="entity-store"></a>Enhedslager
Dataene til **Økonomisk analyse** trækkes fra enhedslageret (**Systemadministration** \> **Konfiguration** \> **Enhedslager**). Hvis du åbner arbejdsområdet **Regnskabsdirektørens oversigt** eller **Økonomisk analyse**, og følgende advarsel vises i de visuelle elementer, skal du opdatere enhederne.

![Advarsel.](./media/Cantdisplay.png)

Du skal opdatere følgende enheder for at se data i arbejdsområdet **Økonomisk analyse**:

- Transaktionsdata version 3 til økonomirapportering 
- Kredit V2
- LedgerCovLiquidityMeasurement
- Indkøbskube
- Salgskube

Du kan definere et tilbagevendende batchjob for regelmæssigt at opdatere dataene i enhederne. Da hver enhed genopbygges fuldstændig under en opdatering, skal du være omhyggelig med valg af tidspunkt og hyppighed af opdateringer til enheden. Den primære enhed, der bruges til regnskaber er enheden FinancialReportingTransactionData. Derfor kan du beslutte dig til at opdatere enheden oftere.

## <a name="security"></a>Sikkerhed
På nuværende tidspunkt kan dataene i integrerede Power BI-rapporter ikke begrænses til de juridiske enheder, som brugeren har adgang til. Derfor styres de integrerede Power BI-rapporter via opgaver i sikkerhedsopsætningen. De opgaver, der er defineret, giver adgang til data for enten alle juridiske enheder eller kun det aktive firma. Følgende tabel viser de opgaver, der findes og de roller, de er tildelt. Opgaverne kan fjernes eller tildeles til forskellige roller, baseret på din organisations krav.

| Programadgangsrettighed                                    | Roller | Betegnelse |
|-----------------------------------------|-------|------------|
| Vis økonomisk analyse i aktuelt firma | <ul><li>Bogholder</li><li>Regnskabschef</li><li>Regnskabsansvarlig</li><li>Revisor</li><li>Budgetchef</li><li>Administrerende direktør</li><li>Økonomidirektør</li><li>Finansinspektør</li></ul> | Denne pligt giver adgang til økonomisk analyse. Som standard bruges det aktive firma som et filter. Du kan ikke tilføje andre juridiske enheder. |
| Vis hele firmaets økonomisk analyse   | I Microsoft Dynamics 365 Finance, Enterprise Edition 7.3 er denne opgave ikke tildelt en rolle. I den næste udgave knyttes denne pligt til rollen Økonomidirektør. | Denne pligt giver adgang til menuelementet for arbejdsområdet Regnskabsdirektørens oversigt. Som standard bruges det aktive firma som et filter. Du kan dog tilføje alle juridiske enheder, uanset om brugeren har adgang til de andre juridiske enheder. |


## <a name="financial-reporting-vs-financial-analysis"></a>Økonomirapportering vs. Økonomisk analyse
Selvom **Økonomisk analyse** indeholder regnskaber, er det ikke en erstatning for Økonomirapportering i programmet. Standardregnskaberne i **Økonomisk analyse** har begrænset omfang og omfatter ikke alle former for regnskaber. Økonomirapportering er stadig det primære værktøj til at designe, oprette og generere lovpligtige regnskaber.

I følgende diagram til sammenligning får du hjælp til at skelne mellem de to indstillinger:


| Funktion                                                   | Financial Reporting                                               | Økonomisk analyse |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Redigere standardrapporter**                                 | Ja                                                               | Nej |
| **Oprette nye rapporter**                                   | Ja                                                               | Nej |
| **Udskrivning af rapporter**                                        | Ja                                                               | Nej |
| **Eksportér til Excel**                                      | Ja                                                               | Rådata for begrænsede eksporter til Excel, ikke en formateret rapport |
| **Understøtte rapporteringshierarki/organisationshierarki**   | Ja                                                               | Nej |
| **Rapportere reskontrodata**                             | Ja Begrænset til kreditor, debitor                              | Ja Kreditor, debitor, kreditor-/debitorgrupper, kreditor-/debitoradresser osv. |
| **Rapporteringsvaluta**                                   | Ja Regnskabsvaluta og omregning til rapporteringsvaluta       | Nej Kun regnskabsvaluta |
| **Sikkerhed**                                             | Ja Overholder Finans-sikkerhed i trædiagrammet | Begrænset Vis rapporter for alle firmaer (uanset sikkerhed for finans og drift) eller kun aktivt firma |
| **Understøtte forskellige kontoplaner og regnskabsår** | Ja                                                               | Nej |
| **Rapportere eksterne data**                              | Nej                                                                | Nej |
| **Understøtte konsolideringer**                               | Ja                                                               | Begrænset Kan rapportere om flere firmaer, men kun bruge regnskabsvaluta |

Følgende regnskaber er tilgængelige:

- Råbalance
- Balance
- Resultatopgørelse efter region
- Resultatopgørelse - faktisk vs. budget
- Resultatopgørelsen med afvigelser
- 12-måneders tendensresultatopgørelse
- Tre års tendens for udgifter
- Udgifter efter kreditor
- Salg pr. kunde

## <a name="edit-visuals"></a>Redigere visuelle elementer
I tidligere versioner af **økonomisk analyse** kan ingen af de visuelle elementer redigeres. I fremtidige versioner vil brugere, der har den nødvendige sikkerhed, kunne oprette nye visuelle elementer, kopiere eksisterende visuelle elementer og redigere visuelle elementer. Selvom de .pbix-filer, der indeholder rapporterne, er tilgængelige som ressourcer, anbefaler vi ikke, at du redigerer standardrapporterne. Der vil blive foretaget yderligere ændringer af datamodellen, standardrapporterne og de brugerdefinerede visuelle elementer til regnskab, der bruges til at oprette regnskabet. Hvis du derfor vil drage nytte af nye funktioner og ændringer til datamodellen i den næste version, vil du være nødt til at gentage alle de ændringer, du har foretaget i standardrapporterne via Microsoft Power BI Desktop.

## <a name="filtering"></a>Filtrering
Brugere kan filtrere rapporten ved hjælp af ruden **Filter** til venstre. Denne rude er den samme rude, der er tilgængelig via Power BI Desktop. Der findes forskellige niveauer af filtrering, hvoraf nogle muligvis ikke er tilgængelige, afhængigt af hvad du har valgt på en side (fane), eller om du bruger funktionerne til detaljeadgang:

- **Filtre på rapportniveau** – Disse filtre anvendes på alle visuelle elementer på alle sider (faner).
- **Filtre på sideniveau** – Disse filtre anvendes på alle visuelle elementer på den aktive fane. Disse filtre anvendes oven på filtrene på rapportniveau.
- **Filtre på visuelt niveau** – Disse filtre anvendes kun på det valgte visuelle element. Disse filtre anvendes oven på filtrene på sideniveau.
- **Detaljeadgangsfilter** – Dette filter filtrerer fra et visuelt "kilde"-element, som er tilknyttet det aktuelle visuelle element, når du foretager detaljeadgang fra det visuelle kildeelement til det aktuelle visuelle element.

![Filtreringsindstillinger.](./media/filter.png)

Vælg viskelædersymbolet ud for den for at fjerne en bestemt værdi. Fjern ikke et filter ved at vælge X. Hvis du vælger X, fjernes det felt, du filtrerer på, som en filtreringsindstilling. Hvis du ved et uheld fjerner et felt fra filteret, skal du lukke arbejdsområdet, og derefter åbne det igen. Standardindstillingerne for filter anvendes igen.

Når du åbner et arbejdsområde første gang, bruges den aktive juridiske enhed som standard som filteret på rapportniveau. Afhængigt af deres sikkerhed er brugere muligvis i stand til at tilføje andre juridiske enheder eller til at ændre den juridiske enhed, der er valgt i filteret.

Filteret **regnskabskalender** er nødvendigt, for at den rette kalender bruges til visuelle elementer. Som standard er filteret på rapportniveau angivet til den aktive juridiske enheds regnskabskalender. Hvis du ændrer filteret til en regnskabskalender, der har en anden start- eller slutdato, medtages startsaldi ikke. Derfor vil dine regnskaber af typen **Balance** ikke vise de korrekte saldi. Hvis du vælger en yderligere regnskabskalender i filteret, har du et ekstra sæt af kolonner. Hver ekstra sæt kolonner viser beløbene for en anden regnskabskalender.

Filteret **posteringslag** er også påkrævet. Som standard er filteret angivet til Aktuelt. Du kan vælge flere posteringslag i filteret for at få vist de akkumulerede beløb.

Der er også filtre tilgængelige for felterne **Dato** og **Regnskabsår**. Filtrene anvendes typisk på sideniveau. Som standard bruger filteret **Dato** en associeret dato, du kan ændre. Du kan også fjerne det associerede datofilter og bruge filteret **Regnskabsår** i stedet.

## <a name="currency"></a>Valuta

Alle visuelle elementer, der rapporterer på finansdata, viser beløb i regnskabsvalutaen. Når du filtrerer på den juridiske enhed, skal du derfor sørge for at medtage kun juridiske enheder, der har samme regnskabsvaluta. Ellers samler du data i forskellige valutaer.

Alle visuelle elementer, der rapporterer på data for reskontro, f.eks. **Likviditetsbudget** og **Top 10**, viser beløb i systemvalutaen. Systemvalutaen og systemvalutakurstypen defineres på siden **Systemparametre**.

Det visuelle element **Saldo pr. bankkonto** bruger beløb i bankkontoens valuta.

## <a name="dimensions"></a>Dimensioner

Standardregnskaberne medtager ikke økonomiske dimensioner, men er kun fokuseret på hovedkontoen. Understøttelse af økonomiske dimensioner vil være tilgængelig i fremtidige versioner, når rapporterne bliver redigerbare. Organisationer kan derefter filtrere på økonomiske dimensionsværdier.

Nogle regnskaber indeholder dimensioner, der er baseret på posteringer for reskontro. Formålet med de nye regnskaber er at gøre det muligt at filtrere efter dimensioner, der ikke er konfigureret som økonomiske dimensioner. Standardrapporten Udgifter pr. kreditor kan du f.eks. udvide ned ud over hovedkontoen, så du kan se saldiene opdelt efter kreditor. Kreditoren ikke er konfigureret som en økonomisk dimension. I stedet returnerer systemet til den oprindelige postering for reskontro for at finde kreditoren.

Følgende dimensioner bruges i standardrapporterne. Ingen af disse dimensioner er økonomiske dimensioner.

- Leverandør
- Leverandørgruppe
- Kunde
- Kundegruppe
- Land/område
- Område
- Bynavn

> [!IMPORTANT] 
> Hvis du opsummerer posteringer for flere leverandører eller kunder i et enkelt bilag ved hjælp af de økonomiske kladder, vil dataene være forkerte. Rapporteringsprocessen kan ikke fastslå, hvilken leverandør eller kunde er relateret til en bestemt finanskonto i en kladdepostering, da disse oplysninger ikke vedligeholdes overalt. Vi anbefaler derfor, at du ikke angiver flere leverandører, kunder, anlægsaktiver eller projekter i et enkelt bilag.

## <a name="drill-on-data"></a>Detailudledning på data

Forskellige niveauer af detailudledning er tilgængelig via Power BI. Hvert niveau har et andet navn og forskellige funktioner. Du kan også foretage detailudledning på rækker og kolonner. I dette afsnit beskrives de forskellige indstillinger ved hjælp af regnskabet **Råbalance** som et eksempel, og det vises, hvordan du kan foretage detailudledning på rækkerne. De samme funktioner findes til kolonner. Du behøver kun at ændre indstillingen **Detailudledning**.

I følgende illustration er regnskabet **Råbalance** skjult i det højeste niveau i rækkehierarkiet, hovedkontotypen.

![Råbalanceregnskab.](./media/trial-balance.png)

For at få vist næste niveau i hierarkiet, hovedkontokategorierne, kan du angive feltet **Detailudledning** til **Rækker** og derefter vælge knappen **Udvid** knap (den tredje knap efter feltet Detailudledning). Du kan nu se alle hovedkontokategorierne udvidet. I øjeblikket giver Power BI dig ikke mulighed for kun at udvide én række eller kolonne, men stadig se alle de andre rækker eller kolonner.

![Råbalance i detaljer på rækker.](./media/trial-balance2.png)

For at udvide til hovedkontiene for alle rækker, kan du igen bruge knappen **Udvid**. Men hvis du vil foretage detailudledning til hovedkontiene for kun én række, skal du først markere knappen **Detailudledning** (den enkelte nedadgående pil i højre side af vinduet), og derefter vælge rækken, der skal foretages detailudledning for. I følgende illustration vises resultatet, når rækken **Salg** er markeret, efter at knappen **Detailudledning** er valgt.

![Knappen til udvidelse af råbalance.](./media/trial-balance3.png)

Når du ruller ned på en enkelt række, kræves flere klik for at vende tilbage til den fulde råbalance. Knappen **Rul op** (den første knap efter **Detailudledning** på feltet) ruller kun op i forbindelse med kategorien **Salg**, som vist i følgende illustration.

![Knappen til oprulning af råbalance.](./media/trial-balance4.png)

Du kan fortsat bruge knappen **Rul op** for at vende tilbage til det højeste niveau af opsummering for rækkerne.

Power BI har også en knap, hvor du kan gå til næste niveau i hierarkiet (den anden knap efter feltet **Detailudledning**). Virkningen af denne knap adskiller sig fra resultatet af knappen **Udvid** (den tredje knap efter feltet **Detailudledning**), som bruges til at udvide hierarkiet. Når du udvider hierarkiet, bevares hierarkiet i rapporten. Som det for eksempel blev vist tidligere, hvis du udvider på hovedkontotypen, kan du stadig se hovedkontotypen på rapporten. Men når du går videre til næste niveau i hierarkiet, viser rapporten ikke længere det overordnede element i hierarkiet, som vist i følgende illustration.

![Knappen til tilbagerulning af råbalance.](./media/trial-balance5.png)

For at få vist posteringsoplysningerne bag de opsummerede saldi, kan du vælge nogle beløb, der skal rulle tilbage i Financial and Operations.

Tilbagerulningen fra regnskaberne fører dig til Sporing af regnskabskilde (ASE), ikke til bilagsposteringerne. ASE viser ikke blot regnskabsposterne i finansmodulet. I stedet vises detaljerne om posteringen for reskontroen. Derfor kan du få mange flere oplysninger om den oprindelige transaktion og kan bruge den til analyse. For eksempel kan du se, hvem leverandøren eller kunden var, hvad kunden købte eller leverandøren solgte og endog hvilket projekt, der var på transaktionen.

De følgende filtre fra regnskabet er sendt til ASE, så ASE viser de transaktioner, der er samlet:

Obligatoriske felter til filtrering:

- Juridisk enhed
- Regnskabskalender
- År
- Hovedkonto-id

Valgfrie felter til filtrering:

- Kvartal
- Måned
- Termin

Hvis du ikke udvider langt nok ned på en række, virker nedrulningen ikke. Hvis du f.eks. kun udvider ned til hovedkontokategorien, kan du ikke rulle ned i ASE på saldoen, fordi hovedkontoen er et obligatorisk felt til filtrering i ASE.

Hvis du udvider for langt ned på en række, sendes de ekstra filtre i regnskaber ikke til ASE. Du kan derfor se en forskel på tallene. Hvis du f.eks. udvider ned til landet eller området på rækkerne i resultatopgørelsen ved regnskab for område, medtages land/område ikke som et filter i ASE.

> [!NOTE]
> Du kan rulle længere nede i regnskabsrækkerne eller -kolonnerne, end ASE understøtter i øjeblikket til filtrering. I nogle situationer vil summen af detaljerede posteringer i ASE derfor ikke svare til den saldo, som du ruller tilbage til. Denne funktion vil fortsat blive udvidet fremover.

## <a name="hierarchies"></a>Hierarkier

Standardregnskaber bruger to hierarkier til at detailudlede og udvide på dataene. Der er ét hierarki for rækkerne og andet hierarki for kolonnerne. Begge hierarkier er foruddefineret i udformningen af regnskabet. I de fleste regnskaber er rækkehierarkiet **Hovedkontotype** \> **Hovedkontokategorier** \> **Hovedkonto**. Men nogle rapporter har flere felter, f.eks. Land/område. De yderligere noder i hierarkiet er baseret på data for reskontro for hver transaktion.

For kolonnerne fokuserer hierarkiet på de juridiske enheder og regnskabsperioderne. I de fleste regnskaber er kolonnehierarkiet **Juridisk enhed** \> **Regnskabskalender** \> **Regnskabsår** \> **Kvartal** \> **Periode**.

I øjeblikket understøtter regnskabet ikke organisationshierarkier, så du kan indsamle data.

## <a name="data-limitations"></a>Databegrænsninger
Visuelle elementer til regnskab har en begrænsning på antallet af rækker, der kan vises. I øjeblikket er grænsen angivet til 30.000. Hvis du overskrider denne grænse, får de visuelle elementer et advarselssymbol, for at fortælle dig om denne situation.

![Databegrænsninger.](./media/data-limit.png)

Hvis det maksimale antal overskrides, vil totaler, der vises på regnskabet, være forkerte, fordi ikke alle rækker blev indlæst i det visuelle element.

### <a name="empty-rows"></a>Tomme rækker
Power BI giver ikke mulighed for at vise og skjule tomme rækker. Hvis en række ikke har nogen data, vises rækken ikke i det visuelle element.


## <a name="additional-resources-for-power-bi"></a>Yderligere ressourcer for Power BI

Oplysningerne i følgende ressourcer er ikke påkrævet for at aktivere de integrerede rapporter til arbejdsområdet **Økonomisk analyse** i et produktionsmiljø. I stedet er de nyttige til udviklingsfelter, og hvis du vil integrere dine egne Power BI-rapporter.

- [Få adgang til analytiske arbejdsområder og rapporter i 1-box-miljøet](/archive/blogs/dynamicsaxbi/accessing-analytical-workspaces-on-1box-environment)

- [Tilføje analyser til arbejdsområder ved hjælp af Power BI Embedded](/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

